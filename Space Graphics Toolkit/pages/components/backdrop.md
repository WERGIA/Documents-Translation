# 우주배경(Backdrop)

## SgtBackdrop

이 컴포넌트를 통해 구체의 경계명에 절차적으로 배치된 쿼드를 생성할 수 있습니다.

이 쿼드들은 우주 먼지 구름이나 별의 텍스처를 사용할 수 있으며 렌더링 카메라를 따라 움직이는 우주 배경으로 사용됩니다.

이 우주 배경은 아주 빠르게 렌더되며, 스카이박스와 비교하여 메모리 요구 사항을 엄청나게 감소시킨 좋은 대체품으로써 제공됩니다.

#### SourceMaterial : Material

이 컴포넌트가 렌더하는데 사용할 머티리얼

> **NOTE** - 이 컴포넌트는 반드시 **Space Graphics Toolkit/Backdrop** 셰이더를 사용해야 합니다.일반 셰이더는 사용할 수 없습니다.

#### Color : Color

우주 배경의 전반적인 색상을 결정합니다.

#### Brightness : float

**Color.rgb** 값에 곱해지는 값입니다.

#### MainTex : Texture

이 설정을 통해 우주 배경에 적용되는 텍스처를 설정할 수 있습니다. 이 텍스처에 여러 개의 별이 포함될 수 있는 경우 **Atlas** 설정을 사용하여 별의 위치를 지정할 수 있습니다.

#### Atlas : SgtAtlas

이 머티리얼의 기본 텍스처가 아틀라스에서 여러 텍스처를 포함하는 경우 여기에서 지정할 수 있습니다.

#### ClampSizeMin : float

별의 크기가 더 이상 줄어들지 않고 희미해져야 하는 최소 크기입니다.

#### Seed : int

절차적 생성에서 사용되는 랜덤 시드입니다.

#### Radius : float

우주 배경의 반지름입니다.

#### Squash : float

별들이 얼마나 수평선에 가깝게 배치될 지를 결정합니다.

#### StarCount : int

우주 배경에 생성될 별의 갯수입니다.

#### StarColors : Gradient

각 별의 색상은 이 그라디언트 내에서 랜덤하게 결정됩니다.

#### StarRadiusMin : float

우주 배경의 별들의 최소 반지름입니다.

#### StarRadiusMax : float

우주 배경의 별들의 최대 반지름입니다.

#### StarRadiusBias : float

별의 크기를 설정할 때 큰 별보다 작은 별을 선택할 가능성입니다.(1 = 기본/선형)

#### StarPulseSpeedMin : float

별이 반짝이는 최소 속도입니다.

> **NOTE** - **SourceMaterial**에서 **PULSE** 설정을 활성화해야만 합니다.

#### StarPulseSpeedMax : float

별이 반짝이는 최대 속도입니다.

> **NOTE** - **SourceMaterial**에서 **PULSE** 설정을 활성화해야만 합니다.

## SgtBackdropModel

이 컴포넌트는 **SgtBackdrop** 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다. 

## SgtBackdropQuad

이 클래스는 SgtBackdrop에 의해 생성된 하나의 쿼드에 대한 데이터를 저장하며 일반적으로 절차적으로 생성됩니다.

#### Temp : static SgtBackdropQuad

우주 배경을 생성할 때 사용되는 임시 인스턴스입니다.

#### Variant : int

아틀라스 텍스처의 좌표 인덱스입니다.

#### Color : Color

이 쿼드의 컬러 틴트입니다.

#### Radius : float

로컬 스페이스에서 이 쿼드의 반지름입니다.

#### Angle : float

이 쿼드에 대한 각도(degree) 기반의 각입니다.

#### Position : Vector3

로컬 스페이스에서 이 쿼드의 위치입니다.

#### PulseSpeed : float

이 별이 얼마나 빠르게 깜빡이는가 입니다.

> **NOTE** - 이것은 머티리얼의 PULSE 설정이 활성화되어 있어야 합니다.

#### PulseOffset : float

펄스 위치가 이 값만큼 오프셋되어 모든 펄스가 동일하지 않게 만들어줍니다.

> **NOTE** - 이것은 머티리얼의 PULSE 설정이 활성화되어 있어야 합니다.