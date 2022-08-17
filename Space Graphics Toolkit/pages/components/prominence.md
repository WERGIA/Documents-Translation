# 돌출부(Prominence)

## SgtProminence

이 컴포넌트를 사용하면 항성 주위에 무작위로 회전된 일련의 디스크를 렌더링하여  볼류메트릭하고 디테일하게 보이는 코로나를 연출할 수 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Prominence** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Color : Color

돌출부의 전반적인 색상을 결정합니다.

#### Brightness : float

**Color.rgb** 값에 곱해지는 값입니다.

#### MainTex : Texture

돌출부에 적용되는 텍스처입니다.

#### CameraOffset : float

돌출부를 렌더링 할 때 월드 스페이스에서의 카메라 거리를 오프셋하여 렌더 순서를 미세조정할 수 있습니다.

#### Seed : int

절차적 생성 중에 사용할 랜덤 시드입니다.

#### PlaneCount : int

돌출부 평면의 수입니다.

#### PlaneDetail : int

각 평면에 사용될 쿼드의 수입니다.

#### RadiusMin : float

로컬 좌표계에서 돌출부 평면의 내부 반지름입니다.

#### RadiusMax : float

로컬 좌표계에서 돌출부 평면의 외부 반지름입니다.

## SgtProminenceModel

이 컴포넌트는 **SgtProminence** 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

