# 거대 가스 행성(Jovian)

## SgtJovian

이 컴포넌트를 사용하면 목석과 같은 볼류메트릭 거대 가스 행성을 렌더할 수 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Jovian** 셰이더를 사용해야 합니다. 일반 머티리얼은 사용할 수 없습니다.

> **NOTE** - 빌드에서 이 머티리얼의 설정을 수정하는 경우, **SyncMaterial** 메서드를 수동으로 호출해야 합니다.

#### Color : Color

거대 가스 행성의 전반적인 색상을 결정합니다.

#### Brightness : float

**Color.rbg**에 곱해지는 값입니다.

#### MainTex : Texture

거대 가스 행성에 적용되는 텍스처입니다.

#### FlowTex : Texture

거대 가스 행성에 적용되는 플로우 텍스처입니다(가스 행성의 표면이 흐르는 것처럼 보이도록 만들어 줍니다).

> **NOTE** - 지정된 **SourceMaterial**이 **FLOW**를 활성화한 경우에만 사용됩니다.

#### CameraOffset : float

거대 가스 행성이 렌더링될 때 월드 스페이스에서의 카메라 거리를 오프셋하므로써, 렌더 순서를 미세조정할 수 있습니다.

#### Sky : float

반지름 내부로 카메라가 들어왔을 때, 대기의 두께를 제어할 수 있습니다.

#### Mesh : Mesh

거대 가스 행성이 렌더되는 데 사용되는 메시입니다. 이것은 구체여야 합니다.

#### MeshRadius : float

메시의 반지름입니다. 이 값이 잘못 설정되면 거대 가스 행성이 잘못 렌더될 수 있습니다.

#### Radius : float

로컬 스페이스에서 거대 가스 행성의 반지름입니다.

#### DistanceRadius : float

거리 계산을 사용할 때 로컬 스페이스에서 거대 가스 행성의 반지름을 설정할 수 있습니다. 거리 계산은 일반적으로 행성 표면에서 얼마나 멀리 떨어져 있는지 알려주지만 가스 행성은 고체가 아니므로 프로젝트에 따라 이것을 사용자 정의할 수 있습니다.

## SgtJovianDepthTex

거대 가스 행성을 위한 DepthTex를 생성하는 데 사용되는 컴포넌트입니다.

#### RimEase : SgtEase.Type

림 전환 스타일입니다.

#### RimPower : float

림 전환의 날카로움입니다.

#### RimColor : Color

림 컬러입니다.

#### AlphaDensity : float

대기의 밀도입니다.

#### AlphaFade : float

대기 상단에서의 밀도 페이딩 강도입니다.

#### ExportTexture : void

이 메서드를 통해 생성된 텍스처를 에셋 형태로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고, 추출한 텍스처를 **SgtJovian** 컴포넌트의 **DepthTex**에 사용할 수 있습니다.

## SgtJovianLightingTex

이 컴포넌트를 사용하여 거대 가스 행성 머티리얼에 사용할 LightingTex를 생성할 수 있습니다.

#### SunsetEase : SgtEase.Type

밤과 낮 사이의 전환 스타일입니다.

#### SunsetStart : float

일몰의 시작 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽).

#### SunsetEnd : float

일몰의 끝 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽).

#### SunsetSharpnessR

일몰 red 채널 전환의 날카로움입니다.

#### SunsetSharpnessG

일몰 green 채널 전환의 날카로움입니다.

#### SunsetSharpnessB

일몰 blue 채널 전환의 날카로움입니다.

#### ExportTexture : void

이 메서드를 통해 생성된 텍스처를 에셋 형태로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고, 추출한 텍스처를 **SgtJovian** 컴포넌트의 **LightingTex**에 사용할 수 있습니다.

## SgtJovianModel

이 컴포넌트는 **SgtJovian** 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

## SgtJovianScatteringTex

이 컴포넌트를 사용하면 거대 가스 행성 머티리얼의 ScatteringTex를 생성할 수 있습니다.

#### SunsetEase : SgtEase.Type

밤과 낮 사이의 전환 스타일입니다.

#### SunsetStart : float

일몰의 시작 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽).

#### SunsetEnd : float

일몰의 끝 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽).

#### SunsetSharpnessR

일몰 red 채널 전환의 날카로움입니다.

#### SunsetSharpnessG

일몰 green 채널 전환의 날카로움입니다.

#### SunsetSharpnessB

일몰 blue 채널 전환의 날카로움입니다.

#### ExportTexture : void

이 메서드를 통해 생성된 텍스처를 에셋 형태로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고, 추출한 텍스처를 **SgtJovian** 컴포넌트의 **ScatteringTex**에 사용할 수 있습니다.