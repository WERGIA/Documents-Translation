# 클라우드스피어(Cloudsphere)

## SgtCloudsphere

이 컴포넌트를 사용하면 클라우드 큐브맵을 사용하여 행성주위에 구체를 렌더링할 수 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더링하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Cloudsphere** 셰이더를 사용해야 합니다. 일반 셰이더를 사용할 수 없습니다.

#### Color : Color

클라우드스피어의 전반적인 색을 설정합니다.

#### Brightness : float

**Color.rgb**에 곱해지는 값입니다.

#### MainTex : Cubemap

클라우드 스피어에 적용되는 큐브맵 텍스처를 설정합니다.

#### Radius : float

로컬 스페이스에서의 클라우드스피어의 반지름입니다.

#### CameraOffset : float

클라우드스피어를 렌더링할 때 월드 스페이스에서 카메라 거리를 오프셋하여 렌더링 순서를 미세하게 제어할 수 있습니다.

#### Softness : float

솔리드 지오메트리와 교차하는 경우 별이 희미해지게 하는지를 설정합니다.

#### Mesh : Mesh

클라우드스피어를 렌더링하는 데 사용되는 메시를 설정할 수 있습니다. 이것은 구체여야 합니다.

#### MeshRadius : float

메시의 반지름을 설정합니다. 이 값이 잘못 설정되면 클라우드스피어가 잘못 렌더링됩니다.

## SgtCloudsphereDepthTex

이 컴포넌트를 사용해서 클라우드스피어 머티리얼을 위한 **DepthTex** 설정을 생성할 수 있습니다.

#### RimEase : SgtEase.Type

림 전환 스타일입니다.

#### RimColor : Color

림 색상입니다.

#### RimPower : float

림 전환의 날카로움입니다.

##### AlphaDensity : float

대기의 밀도입니다.

#### AlphaFade : float

상단 대기에서 밀도가 페이딩되는 강도입니다.

#### void ExportTexture()

이 메서드를 사용하여 텍스처를 에셋으로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고 **SgtCloudsphere** 컴포넌트의 **DepthTex** 설정에 생성한 에셋을 넣어 사용할 수 있습니다.

## SgtCloudsphereLightingTex

이 컴포넌트를 이용해서 클라우드스피어 머티리얼을 위한 **LightingTex** 설정을 생성할 수 있습니다.

#### SunsetEase : SgtEase.Type

낮과 밤 사이의 전환 스타일입니다.

#### SunsetStart : float

일몰의 시작 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽)

#### SunsetEnd : float

일몰의 끝 지점입니다(0 = 어두운 쪽, 1 = 밝은 쪽)

#### SunsetSharpnessR : float

일몰 red 채널 전환의 날카로움입니다.

#### SunsetSharpnessG : float

일몰 green 채널 전환의 날카로움입니다.

#### SunsetSharpnessB : float

일몰 blue 채널 전환의 날카로움입니다.

#### void ExportTexture()

이 메서드를 사용하여 텍스처를 에셋으로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고 **SgtCloudsphere** 컴포넌트의 **LightingTex** 설정에 생성한 에셋을 넣어 사용할 수 있습니다.

## SgtCloudsphereModel

이 컴포넌트는 SgtCloudsphere 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

## SgtCloudsphereNearTex

이 컴포넌트를 이용해서 클라우드스피어 머티리얼을 위한 NearTex를 생성할 수 있습니다.

#### Ease : SgtEase.Type

전환에 사용되는 여유 유형입니다.

#### Sharpness : float

전환의 날카로움입니다.

#### Offset : float

페이디의 시작 지점입니다.

#### OverrideRange : float

이 컴포넌트가 스타필드의 **NearRangeRecip** 설정도 제어해야 하는지를 결정합니다.

-1 = 오버라이드 하지 않음

#### void ExportTexture()

이 메서드를 사용하여 텍스처를 에셋으로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고 **SgtCloudsphere** 컴포넌트의 **NearTex** 설정에 생성한 에셋을 넣어 사용할 수 있습니다.

