# 플레어(Flare)

## SgtFlare

이 컴포넌트를 사용하면 고해상도 메시 플레어를 생성할 수 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Flare** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Mesh : Mesh

플레어를 렌더하는 데 사용되는 메시를 설정할 수 있습니다.

#### FollowCameras : bool

플레어가 카메라에 자동으로 스냅될 지 결정합니다.

#### FollowDistanse : float

카메라로부터의 거리. 이 플레어는 월드 스페이스에 배치됩니다.

#### CameraOffset : float

플레어를 렌더링할 때 월드 스페이스에서 카메라 거리를 오프셋하여 렌더 순서를 미세하게 제어합니다.

## SgtFlareMainTex

이 컴포넌트를 사용하여 SgtFlare를 위한 텍스처와 머티리얼을 생성할 수 있습니다.

#### Color : Color

기본 색상에 곱해지는 색상 값입니다.

#### Ease : SgtEase.Type

색상 전환 스타일입니다.

#### SharpnessR : float

red 전환의 날카로움입니다.

#### SharpnessG : float

green 전환의 날카로움입니다.

#### Sharpness : float

blue 전환의 날카로움입니다.

#### ExportTexture : void

이 메서드를 사용하여 텍스처를 에셋으로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고 **SgtFlare** 컴포넌트의 **Material** 설정에 생성한 에셋을 넣어 사용할 수 있습니다.

## SgtFlareMesh

이 컴포넌트를 사용하여 SgtFlare.Mesh 필드를 생성할 수 있습니다.

#### Detail : int

플레어 메시를 생성할 때 사용될 포인트의 양입니다.

#### Radius : float

로컬 스페이스에서 플레어의 기본 반지름입니다.

#### Wave : bool

코사인 파형을 기반으로 플레어를 변형시킬지를 결졍합니다.

#### WaveStrength : float

로컬 스페이스에서 파형의 강도입니다.

#### WavePoint : int

파형 포인트의 양입니다.

#### WavePower : float

파형의 날카로움입니다.

#### WavePhase : float

파형의 각도 오프셋입니다.

#### Noise : bool

플레어를 노이즈 기반으로 변형시킬지를 결정합니다.

#### NoiseStrength : float

로컬 스페이스에서 노이즈의 강도입니다.

#### NoisePoint : int

노이즈 포인트의 양입니다.

#### NoisePhase : float

노이즈의 각도 오프셋입니다.

#### NoiseSeed : int

랜덤 노이즈에 사용될 랜덤 시드입니다.

#### ExportMesh : void

이 메서드를 사용하여 텍스처를 에셋으로 익스포트할 수 있습니다.

익스포트를 완료한 다음에는, 이 컴포넌트를 제거하고 **SgtFlare** 컴포넌트의 **Mesh** 설정에 생성한 에셋을 넣어 사용할 수 있습니다.

## SgtFlareModel

이 컴포넌트는 SgtFlare 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.