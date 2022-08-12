# 광원과 그림자(Lighting & Shadow)

## SgtLight

유니티에 내장된 광원 시스템은 모든 시나리오에 적합하지 않으므로 이 컴포넌트를 사용하여 이를 지원하는 특정 컴포넌트에 대한 맞춤형 광원 시스템으로 확장할 수 있습니다.

#### TreatAsPoint : bool

이 컴포넌트와 함께 붙어있는 **Light** 컴포넌트가 Directional이지만 포인트 라이트인 것처럼 보이게 하기 위해 카메라를 향해 지속적으로 회전하게 하려면 이 설정을 활성화해야 합니다.

#### UseLightIntensity : bool

이 설정을 활성화하면, SGT 컴포넌트는 관계된 **Light.intensity** 값에 **Brightness** 값을 곱하도록 만듭니다.

#### Brightness : float

SGT 컴포넌트에 표시되는 이 라이트의 밝기 값입니다.

> **NOTE** - **UseLightIntensity** 설정을 활성화하면, SGT 컴포넌트는 관계된 **Light.intensity** 값에 **Brightness** 값을 곱하도록 만듭니다.

## SgtShadow

이 기본 클래스는 셰도우 매트릭스와 셰도우 텍스처의 계산을 다룹니다.

## SgtShadowLayer

이 컴포넌트를 사용하면 SgtShadow__ 컴포넌트의 그림자를 씬의 불투명 렌더러에 추가할 수 있습니다.

#### Radius : float

이 그림자 리시버의 반지름입니다.

#### Renderers : List\<MeshRenderer>

그림자가 적용되기 원하는 렌더러들입니다.

## SgtShadowRing

이 컴포넌트를 사용하면 현재 게임 오브젝트에서 고리 그림자를 드리울 수 있습니다.

#### Texture : Texture

그림자의 텍스처입니다(왼쪽 = 안쪽, 오른쪽 = 바깥쪽).

#### RadiusMin : float

이 그림자가 드리울 고리의 안쪽 반지름입니다(고리가 설정되어 있다면 자동으로 설정됩니다).

#### RadiusMax : float

이 그림자가 드리울 고리의 바깥쪽 반지름입니다(고리가 설정되어 있다면 자동으로 설정됩니다).

## SgtShadowRingFilter

이 컴포넌트를 사용하면 일반 텍스처를 기반으로 흐릿한 SgtShadowRing.Texture를 생성할 수 있습니다.

#### Source : Texture2D

필터링될 소스 고리 텍스처입니다.

#### Format : TextureFormat

생성될 텍스처의 포맷입니다.

#### Iterations : int

블러 처리를 반복할 횟수입니다.

#### ShareRGB : bool

RGB 채널을 알파 채널로 덮어쓸 지를 결정합니다.

#### Invert : bool

알파 채널을 반전할 지를 결정합니다.

#### ExportTexture : void

이 메서드를 사용하면 생성된 텍스처를 에셋으로 추출할 수 있습니다.

텍스처 추출이 완료되면, 이 컴포넌트를 제거하고, **SgtShadowRing** 컴포넌트의 **Texture** 설정에 추출한 텍스처 에셋을 사용할 수 있습니다.