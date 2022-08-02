# 데브리(Debris)

## SgtDebris

이 컴포넌트는 단일 데브리 오브젝트를 다룹니다.

#### OnSpawn : event System.Action

데브리가 스폰될 때 호출됩니다(풀링이 활성화된 경우).

#### OnDespawn : event System.Action

데브리가 스폰 해제될 때 호출됩니다(풀링이 활성화된 경우).

#### Pool : bool

이 데브리를 풀링할 수 있는지를 의미합니다.

#### State : StateType

스케일링의 현재 상태입니다.

#### Prefab : SgtDebris

이것이 인스턴스화된 프리팹입니다.

#### Scale : Vector3

이것은 데브리가 생성될 때 자동으로 복사됩니다.

#### Cell : SgtLong3

이 데브리가 생성된 셀입니다.

## SgtDebrisGrid

이 컴포넌트를 사용하면 각 데브리 오브젝트가 사각형 그리드 안에 있어야 하는 대상 지점(예: 카메라) 주위에 데브리 프리팹을 생성할 수 있으므로 씬 전체에 파편을 고르게 분포시킬 수 있습니다.

#### Target : Transform

데브리가 트랜스폼 주변에 스폰됩니다.

#### SpawnInside : SgtShapeGroup

형태 내부에 데브리가 스폰됩니다.

#### ShowDistance : float

데브리가 생성되기 시작하는 대상으로부터의 거리입니다.

#### HideDistance : float

데브리가 숨겨지는 대상으로부터의 거리입니다.

#### CellCount : int

HideDistance 내에서 각 축의 그리드에 있는 셀 수를 설정할 수 있습니다.

#### CellNoise : float

각 셀의 중심에서 데브리가 생성될 수 있는 거리입니다. 데브리가 교차하는 것을 막으려면 이 값을 줄여야 합니다.

#### DebrisCountTarget : float

셀 크기 설정에 따라 예상되는 최대 데브리 양입니다.

#### ScaleMin : float

데브리에 곱해지는 최소 크기입니다.

#### ScaleMax : float

데브리에 곱해지는 최대 크기입니다.

#### ScaleBias : float

이 값이 0보다 크면 작은 파편이 스폰될 가능성이 높아집니다. 이 값이 0 미만이면 큰 파편이 생성될 가능성이 더 높아집니다.

#### RandomRotation : bool

데브리를 무작위로 회전시킬지 아니면 데브리를 스폰한 프리팹에서 받아와서 회전시킬지를 결정합니다.

#### Seed : int

절차적으로 생성되는 동안 사용될 랜덤 시드 값입니다.

#### Prefabs : List\<SgtDebris>

새로운 데브리를 생성할 때 이 프리팹 중에 랜덤으로 하나를 선택합니다.

## SgtDebrisSpawner

이 컴포넌트를 하용하면 시간이 지남에 따라 카메라 주변에 무작위로 데브리를 생성할 수 있습니다.

#### Target : Transform

이 트랜스폼이 반경 안에 있으면 데브리가 스폰되기 시작합니다.

#### SpawnInside : SgtShapeGroup

형태 내부에 데브리가 스폰됩니다.

#### ShowSpeed : float

데브리가 생성된 이후에 얼마나 빠르게 보이는지 입니다.

#### ShowDistance : float

데브리가 생성되기 시작하는 대상으로부터의 거리입니다.

#### HideDistance : float

데브리가 숨겨지는 대상으로부터의 거리입니다.

#### SpawnOnAwake : bool

시작시에 모든 데브리가 자동으로 생성되어야 하는지 입니다.

#### SpawnLimit : int

생성될 수 있는 데브리의 최대 양입니다.

#### SpawnRateMin : float

데브리 스폰 사이의 최소 시간(초)입니다.

#### SpawnRateMax : float

데브리 스폰 사이의 최대 시간(초)입니다.

#### SpawnScaleMin : float

데브리에 곱해지는 최소 크기입니다.

#### SpawnScaleMax : float

데브리에 곱해지는 최대 크기입니다.

#### Prefabs : List\<SgtDebris>

새로운 데브리를 생성할 때 이 프리팹 중에 랜덤으로 하나를 선택합니다.

