# 번개(Lightning)

## SgtLightning

이 컴포넌트는 SgtLightningSpawner 컴포넌트로부터 스폰된 번개의 렌더링을 다룹니다.

#### LightningSpawner : SgtLightningSpawner

이것이 속한 번개 스포너입니다. 이것이 null이면 이 게임 오브젝트는 자동으로 파괴됩니다.

#### Age : float

이 번개가 활성화된 최대 시간(초)입니다.

#### Life : float

이 번개가 활성화될 수 있는 최대 시간(초)입니다.

## SgtLightningSpawner

이 컴포넌트를 사용하면 행성의 주변에 애니메이트된 번개 스프라이트를 생성할 수 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Lightning** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### DelayMin : float

번개 생성 사이의 최소 딜레이입니다.

#### DelayMax : float

번개 생성 사이의 최대 딜레이입니다.

#### LifeMin : float

생성된 각 번개의 최소 수명입니다.

#### LifeMax : float

생성된 각 번개의 최대 수명입니다.

#### Radius : float

로컬 좌표계에서 생성된 번개 메시의 반지름입니다.

#### Size : float

각도에서 번개의 크기입니다.

#### Detail : int

번개 메시의 행과 열의 양입니다.

#### Color : Gradient

번개가 생성될 때, 이 그라디언트에서 랜덤하게 색상을 고르게 됩니다.

#### Brightness : float

Lightning.Color.rgb 값에 이 값을 곱하여 전체 밝기를 빠르게 조정할 수 있습니다.

#### Sprites : List\<Sprite>

번개에 사용되는 무작위 스프라이트입니다.

