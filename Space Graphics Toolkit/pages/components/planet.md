# 행성(Planet)

## SgtPlanet

이 컴포넌트를 사용하면 높이맵으로 고도가 표현되고 동적인 워터 레벨을 가진 행성을 렌더할 수 있습니다.

#### Mesh : Mesh

행성을 렌더하는 데 사용되는 구형 메시입니다.

#### MeshCollider : MeshCollider

생성된 메시에 일치하는 콜라이더가 포함되도록 하려면 여기에서 지정할 수 있습니다.

#### Radius : float

로컬 스페이스에서 행성의 반지름입니다.

#### Material : Material

행성을 렌더하는 데 사용되는 머티리얼입니다. 가장 나은 결과물을 얻기 위해서는 SGT Planet 셰이더를 사용해야 합니다.

#### SharedMaterial : SgtSharedMaterial

이 터레인에 공유 머티리얼(예: 대기)을 적용하기를 원한다면, 여기서 지정할 수 있습니다.

#### WaterLevel : float

현재 수위입니다.

0 = 반지름

1 = 반지름 + 디스플레이스먼트

#### Displace : bool

행성 머티리얼의 높이맵을 이용해서 행성 메시를 바꿀지를 결정합니다.

#### Displacement : float

높이맵의 알파가 1일 때 행성 메시에 추가될 높이 변경의 최대 값입니다.

#### ClampWater : bool

이 설정을 활성화하면 수위가 상승하지 않고 지형이 축소됩니다.

#### Rebuild : void

이 메서드를 사용하면 행성 메시가 현재 설정에 따라 업데이트됩니다. 수정을 마친 후에 이것을 호출해야 합니다.