# 오로라(Aurora)

## SgtAurora

이 컴포넌트로 행성 위의 오로라를 렌더링할 수 있습니다. 이 오로라는 셰이더를 설정하여 절차적으로 애니메이션되도록 할 수 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Aurora** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Color : Color

오로라의 전반적인 색상을 결정합니다.

#### Brightness : float

Color.rgb 값에 이 값을 곱합니다.

#### CameraOffset : float

오로라를 렌더링할 때 월드 스페이스에서 카메라 거리를 오프셋하여 렌더링 순서를 미세하게 제어합니다.

#### Seed : int

절차적으로 생성되는 동안에 사용될 랜덤 시드입니다.

#### RadiusMin : float

로컬 스페이스에서 오로라 메시의 내부 반지름입니다.

#### RadiusMax : float

로컬 스페이스에서 오로라 메시의 내부 반지름입니다.

#### PathCount : int

오로라 경로/리본의 양입니다.

#### PathDetail : int

각 패스 구축에 사용될 쿼드의 양입니다.

#### PathLengthMin : float

각 오로라 경로의 최소 길이입니다.

#### PathLengthMax : float

각 오로라 경로의 최대 길이입니다.

#### StartMin : float

극과 오로라 경로의 시작 지점 사이의 최소 거리입니다.

#### StartMax : float

극과 오로라 경로의 시작 지점 사이의 최대 거리입니다.

#### StartBias : float

오로라 경로가 극에 더 가깝게 시작될 확률입니다.

#### StartTop : float

오로라 경로가 북극 위에서 시작될 확률입니다.

#### PointDetail : int

길이에 따라 오로라 경로가 따라갈 웨이포인트의 양입니다.

#### PointSpiral : float

오로라 웨이포인트가 비틀릴 강도입니다.

#### PointJitter : float

오로라 웨이포인트가 랜덤으로 재배치되는 강도입니다.

#### TrailEdgeFade : float

오로라 경로의 시작점과 끝점에서 페이드되는 날카로움입니다.

#### TrailTile : float

기본 텍스처가 길이에 따라 타일링되는 횟수입니다.

#### TrailHeights : float

오로라 경로의 평탄한 정도입니다.

#### Colors : Gradient

오로라 경로의 상부 절반이 가질 수 있는 색상들입니다.

#### ColorsDetail : int

오로라 경로가 길이에 따라 가질 수 있는 색상 변화의 양입니다.

#### ColorsAlpha : float

오로라 경로 색상의 최소 불투명도 승수입니다.

#### ColorsAlphaBias : float

오로라 경로에서 바뀔 수 있는 알파의 양입니다.

#### AnimStrength : float

로컬 스페이스에서 오로라 경로가 바뀔 수 있는 위치의 강도입니다.

#### AnimStrengthDetail : int

오로라 경로가 길이에 따라 변경되는 애니메이션 강도의 양입니다.

#### AnimAngle : float

오로라 경로 섹션 사이의 최대 각도 단계입니다.

#### AnimAngleDetail : int

오로라 경로 길이에 따라 변경되는 애니메이션 각도의 양입니다.

## SgtAuroraMainTex

이 컴포넌트를 사용하면 SgtAurora.MainTex 필드를 생성할 수 있습니다.

#### NoiseStrength : float

노이즈 지점의 강도입니다.

#### NoisePoints : int

노이즈 지점의 양입니다.

#### NoiseSeed : int

이 텍스처를 생성할 때 사용될 랜덤 시드입니다.

#### TopEase : SgtEase.Type

상단과 하단 사이의 전환 스타일입니다.

#### TopSharpness : float

상단과 하단 사이의 전환 강도입니다.

#### MiddlePoint : float

상단과 하단을 구분하는 지점입니다.

#### MiddleColor : Color

바닥에서 시작하는 오로라의 기본 색상입니다.

#### MiddleEase : SgtEase.Type

오로라의 상단과 하단 사이의 전환 스타일입니다.

#### MiddleSharpness : float

상단과 하단 사이의 색상 전환의 강도입니다.

#### BottomEase : SgtEase.Type

하단과 중간 사이의 전환 스타일입니다.

#### BottomSharpness : float

하단과 중간 사이의 전환 강도입니다.

#### void ExportTexture()

이 메서드를 통해 에셋으로 생성된 텍스처를 익스포트할 수 있습니다.

익스포트가 완료되면, 이 컴포넌트를 제거하고 익스포트로 생성한 텍스터를 **SgtAurora** 컴포넌트의 **MainTex** 설정에 사용할 수 있습니다.

## SgtAuroraModel

이 컴포넌트는 **SgtAurora** 컴포넌트를 렌더하는 데 사용됩니다.

> **NOTE** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

## SgtAuroraNearTex

이 컴포넌트를 사용하면 **SgtAurora.NearTex** 필드를 생성할 수 있습니다.

#### Ease : SgtEase.Type

전환에 사용되는 ease 타입입니다.

#### Sharpness : float

전환의 날카로움입니다.

#### Offset : float

페이딩의 시작 지점입니다.

#### OverrideRange : float

이 컴포넌트가 오로라의 **NearRangeRecip** 설정을 덮어씌워서 제어하는 설정입니다.

-1 = 덮어씌우지 않음

#### void ExportTexture()

이 메서드를 통해 에셋으로 생성된 텍스처를 익스포트할 수 있습니다.

익스포트가 완료되면, 이 컴포넌트를 제거하고 익스포트로 생성한 텍스터를 **SgtAurora** 컴포넌트의 **NearTex** 설정에 사용할 수 있습니다.