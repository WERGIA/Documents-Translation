# 시공간(Spacetime)

## Spacetime

기본 시공간 그리드를 렌더링하는 방법을 보여줍니다. 새 게임 오브젝트를 만들고 **SgtSpacetime** 컴포넌트를 붙여 사용합니다. 그 다음 **SgtSpacetimeMesh** 컴포넌트를 사용하여 **자식** 게임 오브젝트를 만들 수 있습니다. **SgtSpaceTimeMesh** 설정을 조정하여 생성된 그리드 메시의 크기와 해상도를 변경할 수 있습니다.

## Gaussian Well

기본 가우스 분포를 사용하여 시공간이 어떻게 변형될 수 있는지 보여줍니다. 새 게임 오브젝트와 **SgtSpacetimeWell** 컴포넌트를 만들고 **Distribution** 설정을 **Gaussian**으로 설정하여 수행합니다. 그런 다음 원하는 대로 **Radius**와 **Strength**를 조정할 수 있습니다.

### Orbit

현재 게임 오브젝트 위치와 함께 시공간 우물이 어떻게 아래에 있는 시공간 메시를 변형하는지 보여줍니다. 이 씬에서 **SgtRotate** 컴포넌트는 상위 게임 오브젝트에 사용되어 씬의 중심을 기준으로 회전합니다.

## Ripple Well

Ripple 분포를 사용하여 시공간이 어떻게 변형될 수 있는지 보여줍니다. **SgtSpacetimeWell** 컴포넌트와 새 게임 오브젝트를 만들고 해당 **Distribution** 설정을 **Ripple**로 설정하여 수행됩니다. 그런 다음 원하는 대로 **Radius**, **Strength** 및 **Frequency** 설정을 조정할 수 있습니다.

### Animation

Ripple을 애니메이션할 수 있는 방법을 보여줍니다. **SgtSpacetimeWell** 컴포넌트의 OffsetSpeed 설정을 사용하여 수행됩니다.

## Twist Well

Twist 분포를 사용하여 시공간이 어떻게 변형될 수 있는지 보여줍니다. **SgtSpacetimeWell** 컴포넌트와 새 게임 오브젝트를 만들고 해당 **Distribution** 설정을 **Twist**로 설정하여 수행됩니다. 그런 다음 원하는 대로 **Radius**, **Strength**, **Frequency**, **HoleSize** 및 **HolePower** 설정을 조정할 수 있습니다.

### Animation

Twist를 애니메이션할 수 있는 방법을 보여줍니다. **SgtSpacetimeWell** 컴포넌트의 OffsetSpeed 설정을 사용하여 수행됩니다.

## Pinch Well

시공간이 어떻게 시공간 우물을 향해 중력을 끌기 위해 변형될 수 있는지 보여줍니다. **SgtSpacetimeWell** 컴포넌트와 새 게임 오브젝트를 만들고 **Distribution** 설정을 **Pinch**로 설정하여 수행됩니다. 그런 다음 원하는 대로 **Radius** 및 **Strength** 설정을 조정할 수 있습니다.

## Styles

다양한 스타일의 시공간 그리드를 렌더링하는 방법을 보여줍니다. **Space Graphics Toolkit / Spacetime Additive** 셰이더로 새 머티리얼을 만들고 설정을 조정하여 수행됩니다. 각 설정이 무엇을 다루는지 알아보려면 **Spacetime** 기능에 대한 문서을 참조하십시오.