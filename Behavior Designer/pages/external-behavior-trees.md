# 외부 비헤이비어 트리(External Behavior Trees)

경우에 따라 여러 오브젝트에서 실행하려는 비헤이비어 트리가 있을 수 있습니다. 예를 들어 방을 순찰하는 비헤이비어 트리가 있을 수 있습니다. 각 유닛에게 별도의 비헤이비어 트리를 만드는 대신 외부 비헤이비어 트리를 사용할 수 있습니다. 외부 비헤이비어 트리는 `Behavior Tree Reference` 태스크를 사용하여 참조됩니다. 원본 비헤이비어 트리가 실행되기 시작하면 외부 비헤이비어 트리 내의 모든 태스크를 로드하고 마치 자신의 것처럼 작동합니다. 부모 트리의 이름과 타입이 같은 외부 트리 내의 모든 공유 변수(SharedVariable)는 자동으로 재정의됩니다. 예를 들어, 부모 트리에 값이 7인 "MyInt"라는 `SharedInt`가 있고, 값이 0인 "MyInt"라는 `SharedInt`가 외부 트리에 있는 경우, 트리가 실행될 때 외부 트리에 있는 "MyInt"는 7의 값을 가지게 됩니다.

## 비헤이비어 트리 참조

`Behavior Tree Reference` 태스크를 사용하면 현재 비헤이비어 트리 내에서 다른 비헤이비어 트리를 실행할 수 있습니다. 트리를 외부 비헤이비어 트리로 저장하여 이 비헤이비어 트리를 생성할 수 있습니다. 이 방법을 사용하는 방법 중에 하나가 공격을 위한 일련의 태스크를 수행하는 유닛이 있는 겨우입니다. 유닛이 비헤이비어 트리 내의 다른 지점에서 공격하기를 원할 수 있으며 그 공격이 항상 동일하기를 원할 수 있습니다. 이럴 때는 동일한 공격 태스크를 복사하여 붙여넣는 대신 외부 비헤이비어를 사용하면 태스크가 항상 동일하게 보장됩니다. 이 예제는 [샘플 페이지](https://opsive.com/downloads/?pid=803)에 있는 RTS 샘플 프로젝트에 나와있습니다.

`GetExternalBehavior` 메서드를 사용하면 이를 재정의할 수 있으므로 런타임에 결정되는 외부 비헤이비어 트리 배열을 제공할 수 있습니다.

Behavior Tree Reference 태스크를 사용하면 참조 태스크당 변수를 지정할 수 있습니다. 대부분의 경우 변수가 상위 트리에서 외부 트리로 자동 전송되기 때문에 이것은 필요하지 않습니다. 그러나 동일한 트리에 여러 Behavior Tree Reference 태스크가 모두 동일한 외부 트리를 가리키는 경우 트리 별로 다른 변수 값을 지정할 수 있기를 원할 수 있습니다. 이 상황에서 Behavior Tree Reference 태스크에서 변수 값을 지정할 수 있으며 해당 변수 값은 외부 트리로 전송됩니다.

## 풀링

다수의 외부 트리 사이에서 전환이 발생하는 경우에 더 나은 성능을 위해서 외부 비헤이비어 트리를 풀링할 수 있습니다. 외부 비헤이비어 트리가 인스턴스화 되면 `Init` 메서드를 호출하여 외부 비헤이비어 트리를 역직렬화(Deserialize)해야 합니다. 풀링된 외부 비헤이비어 트리는 풀링되지 않은 외부 비헤이비어 트리와 마찬가지로 비헤이비어 트리 컴포넌트에 할당될 수 있습니다. 아래는 그 예시입니다:

```csharp
using UnityEngine;
using BehaviorDesigner.Runtime;

public class ExternalPoolExample : MonoBehaviour 
{
    public BehaviorTree behaviorTree;
    public ExternalBehavior externalBehaviorTree;
    private ExternalBehavior[] externalPool;
    private int index;

    public void Awake()
    {
        // 재사용할 5개의 외부 비헤이비어 트리를 인스턴스화 합니다.
        // Init 메서드는 외부 비헤이비어 트리를 역직렬화합니다.
        externalPool = new ExternalBehavior[5];
        for (int i = 0; i < externalPool.Length; ++i) 
        {
            externalPool[i] = Object.Instantiate(externalBehaviorTree);
            externalPool[i].Init();
        }
    }

    public void OnGUI()
    {
        // 단순화된 풀 내에서 다음 외부 비헤이비어 트리를 할당합니다.
        if (GUILayout.Button("Assign")) 
        {
            behaviorTree.DisableBehavior();
            behaviorTree.ExternalBehavior = externalPool[index];
            behaviorTree.EnableBehavior();
            index = (index + 1) % externalPool.Length;
        }
    }
}
```