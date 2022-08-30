# 대기(Atmosphere)

## SgtAtmosphere

이 컴포넌트를 사용하면 볼류메트릭 대기를 렌더링할 수 있습니다. 대기는 표면(내부)과 하늘(외부)의 두 가지 머티리얼을 사용하여 렌더링됩니다.

대기의 외부 부분은 지정한 OuterMesh를 사용하여 이 컴포넌트에 의해 자동으로 생성됩니다.

대기의 외부 부분은 사용자가 제공하며(예: 일반 Sphere GameObject) 이 컴포넌트가 자동으로 추가하는 SgtSharedMaterial 컴포넌트에 지정됩니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더링하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Atmosphere** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Color : Color

대기의 전반적인 색상을 변경합니다.

#### Brightness : float

**Color.rgb** 값에 이 값이 곱해집니다.

#### InnerMeshRadius : float

SgtSharedMaterial에 설정된 메시의 반지름입니다.

#### OuterMesh : Mesh

대기를 렌더링하는 데 사용되는 메시를 설정할 수 있습니다. 이 메시는 구체여야 합니다.

#### OuterMeshRadius : float

OuterMesh의 반지름을 설정합니다. 이 값을 잘못 설정하면 대기가 이상하게 렌더링됩니다.

#### OuterSoftness : float

대기권 안팎에 있는 큰 물체가 있으면 날카로운 교차선이 생길 수 있습니다. 이 설정을 높이면 이 교차점을 부드럽게 처리할 수 있습니다.

#### Height : float

로컬 공간의 행성 표면으로부터 얼마나 높은 곳까지 대기가 표현될 지 설정할 수 있습니다.

#### InnerFog : float

표면 대기의 fog level을 조정할 수 있습니다.

#### OuterFog : float

하늘 대기의 fog level을 조정할 수 있습니다.

#### Sky : float

카메라가 대기에 들어갈 때 하늘이 최대 불투명도에 도달하는 속도를 제어할 수 있습니다.

1 = 불투명도가 최대에 도달하기 위해서는 지면까지 내려가야 합니다.

2 = 지표면까지 최소한 절반은 내려가야 합니다.

#### Middle : float

대기 밀도가 최대 지점에 도달하는 고도를 설정할 수 있습니다. 이 값을 낮게 설정할수록 표면에 접근할 때 수평선이 더 안개가 자욱하게 나타납니다.

#### CameraOffset : float

이 설정을 통해 대기를 렌더링할 때 월드 공간에서 카메라 거리를 오프셋하여 렌더링 순서를 미세하게 제어할 수 있습니다.

#### Night : bool

밤에 해당하는 대기 부분이 낮 쪽의 대기와 다른 하늘이 보이도록 할지를 설정합니다.

#### NightSky : float

밤 쪽의 ‘Sky’ 값입니다.

#### NightEase : SgtEase.Type

낮과 밤 사이의 스타일 전환입니다.

#### NightStart : float

낮/일몰 전환의 시작 지점입니다. (0 = 어두운 쪽, 1 = 밝은 쪽)

#### NightEnd : float

낮/일몰 전환의 끝 지점입니다. (0 = 어두운 쪽, 1 = 밝은 쪽)

#### NightPower : float

밤으로 전환되는 부분의 강도입니다.

## SgtAtmosphereDepthTex

이 컴포넌트를 통해 SgtAtmosphere.InnerDepthTex와 SgtAtmosphere.OuterDepthTex 필드를 생성할 수 있습니다.

#### HorizonColor : Color

수평선에 나타나는 색상을 설정할 수 있습니다.

#### InnerColor : Color

내부 텍스처의 기본 색상입니다.

#### InnerEase : SgtEase.Type

수평선과 표면 사이의 전환 스타일입니다.

#### InnercolorSharpness : float

내부 텍스처 전환의 강도입니다.

#### InnerAlphaSharpness : float

내부 텍스처 전환의 강도입니다.

#### OuterColor : Color

외부 텍스처의 기본 색상입니다.

#### OuterEase : SgtEase.Type

하늘과 수평선 사이의 전환 스타일입니다.

#### OuterColorSharpness : float

외부 텍스처 전환의 강도입니다.

#### OuterAlphaSharpness : float

외부 텍스처 전환의 강도입니다.

#### void ExportInnerTexture()

이 메서드로 에셋 텍스처를 만들어서 익스포트할 수 있습니다.

완료되면 이 컴포넌트를 제거하고 익스포트한 에셋을 사용하여 **SgtAtmosphere** 컴포넌트의 **InnerDepth** 설정으로 지정할 수 있습니다.

#### void ExportOuterTexture()

이 메서드로 에셋 텍스처를 만들어서 익스포트할 수 있습니다.

완료되면 이 컴포넌트를 제거하고 익스포트한 에셋을 사용하여 **SgtAtmosphere** 컴포넌트의 **OuterDepth** 설정으로 지정할 수 있습니다.

## SgtAtmosphereHeight

이 컴포넌트는 카메라 근접성을 기반으로 SgtAtmosphere.Height를 수정합니다.

#### DistanceMin : float

대기 중심과 로컬 공간에서의 카메라 위치 사이의 최소 거리

#### DistanceMax : float

대기 중심과 로컬 공간에서의 카메라 위치 사이의 최대 거리

#### HeightClose : float

DistanceMin 값 이하일 때 설정되는 SgtAtmosphere.Heigt 값입니다.

#### HeightFar : float

DistanceMax 값 이상일 때 설정되는 SgtAtmosphere.Height 값입니다.

## SgtAtmosphereLightingTex

이 컴포넌트는 SgtAtmosphere.LightingTex 필드를 생성합니다.

#### SunsetEase : SgtEase.Type

낮과 밤 사이의 전환 스타일입니다.

#### SunsetStart : float

낮/일몰 전환의 시작 지점입니다. (0 = 어두운 쪽, 1 = 밝은 쪽)

#### SunsetEnd : float

낮/일몰 전환의 끝 지점입니다. (0 = 어두운 쪽, 1 = 밝은 쪽)

#### SunsetSharpnessR : float

Sunset Red 채널 전환의 날카로움입니다.

#### SunsetSharpnessG : float

Sunset Green 채널 전환의 날카로움입니다.

#### SunsetSharpnessB : float

Sunset Blue 채널 전환의 날카로움입니다.

#### void ExportTexture()

이 메서드를 통해 텍스처를 에셋으로 만들고 익스포트할 수 있습니다.

에셋으로 익스포트 한 다음에는, 이 컴포넌트를 제거할 수 있고, **SgtAtmosphere** 컴포넌트의 **LightingTex** 설정에 익스포트한 에셋을 설정할 수 있습니다.

## SgtAtmosphereModel

이 컴포넌트는 **SgtAtmosphere** 컴포넌트를 렌더링하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

## SgtAtmosphereScatteringTex

이 컴포넌트를 통해 SgtAtmosphere.ScatteringTex 필드를 생성할 수 있습니다.

#### SunsetEase : SgtEase.Type

낮과 밤 사이의 전환 스타일입니다.

#### SunsetStart : float

낮/일몰 전환의 시작 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽).

#### SunsetEnd : float

일몰/밤 전환의 끝 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽).

#### SunsetSharpnessR : float

sunset red 채널 전환의 날카로움입니다.

#### SunsetSharpnessG : float

sunset green 채널 전환의 날카로움입니다.

#### SunsetSharpnessB : float

sunset blue 채널 전환의 날카로움입니다.

#### void ExportTexture()

이 메서드를 통해 에셋으로 생성된 텍스처를 익스포트할 수 있습니다.

익스포트가 완료되면, 이 컴포넌트를 제거하고 익스포트로 생성한 텍스터를 **SgtAtmosphere** 컴포넌트의 **ScatteringTex** 설정에 사용할 수 있습니다.