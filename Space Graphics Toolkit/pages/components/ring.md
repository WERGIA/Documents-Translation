# 고리(Ring)

## SgtRing

이 컴포넌트를 사용하면 고리를 렌더할 수 있습니다(예: 행성의 고리, 강착원반).

이 고리는 행성 주변에 배치될 때, 개선된 깊이 정렬 동작으로 절반으로 나누어집니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Ring** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Color : Color

고리의 전반적인 색입니다.

#### Brightness : float

**Color.rgb** 값에 곱해지는 값입니다.

#### MainTex : Texture

고리에 적용되는 텍스처입니다.

#### RadiusInner : float

로컬 스페이스에서 고리의 내부 경계의 반지름입니다.

#### RadiusOuter : float

로컬 스페이스에서 고리의 외부 경계의 반지름입니다.

#### Split : bool

이 고리를 행성에 대해 개선된 깊이 정렬을 통해서 두 부분으로 나눌지를 결정합니다.

#### SortDistance : float

로컬 스페이스에서 고리가 그려질 정렬 순서 지점을 설정할 수 있습니다.

이것은 투명한 가스 행성 주변에 있는 고리에 개선된 깊이 정렬을 사용할 때 쓸 수 있습니다. 이 값은 **RadiusOuter** 값과 비슷해야 하며 행성의 크기에 따라 더 커질 수도 있습니다.

## SgtRingLightingTex

이 컴포넌트를 사용하면 **SgtRing.LightingTex** 필드를 생성할 수 있습니다.

#### FrontPower : float

들어오는 빛 산란의 전방이 얼마나 날카로운 지를 결정합니다.

#### BackPower : float

들어오는 빛 산란의 후방이 얼마나 날카로운 지를 결정합니다.

#### BackStrength : float

후방 산란된 빛의 세기입니다.

#### BaseStrength : float

수직 산란된 빛의 세기입니다.

#### void ExportTexture()

이 메서드를 통해 생성된 텍스처를 에셋 형태로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고, 추출한 텍스처를 **SgtRing** 컴포넌트의 **LightingTex**에 사용할 수 있습니다.

## SgtRingMainTexFilter

이 컴포넌트를 사용하면 고리의 단순 RGB 텍스처를 기반으로한 **SgtRing.MainTex** 필드를 생성할 수 있습니다.

#### Source : Texture2D

필터링될 소스 링 텍스처입니다.

#### Format : TextureFormat

생성된 텍스처의 포맷입니다.

#### Power : float

빛/어둠 전환의 날카로움입니다.

#### Exposure : float

밝기를 제어할 수 있습니다.

#### void ExportTexture()

이 메서드를 통해 생성된 텍스처를 에셋 형태로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고, 추출한 텍스처를 **SgtRing** 컴포넌트의 **MainTex**에 사용할 수 있습니다.

## SgtRingModel

이 컴포넌트는 **SgtRing** 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

## SgtRingNearTex

이 컴포넌트를 사용하면 **SgtRing** 컴포넌트의 머티리얼을 위한 NearTex를 생성할 수 있습니다.

#### Ease : SgtEase.Type

전환에 사용되는 ease 유형입니다.

#### Sharpness : float

전환의 날카로움입니다.

#### Offset : float

페이딩의 시작 지점입니다.

#### OverrideRange : float

이 컴포넌트가 고리의 **NearRangeRecip** 설정도 제어해야 하는지를 결정합니다.

#### void ExportTexture()

이 메서드를 통해 생성된 텍스처를 에셋 형태로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고, 추출한 텍스처를 **SgtRing** 컴포넌트의 **NearTex**에 사용할 수 있습니다.

