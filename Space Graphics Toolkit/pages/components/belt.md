# 벨트(Belt)

## SgtBelt

이 기본 클래스는 소행성 벨트를 렌더링하는 기능이 포함되어 있습니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Belt** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Color : Color

벨트의 전반적인 색을 설정하는 데 사용됩니다.

#### Brightness : float

**Color.rgb**에 곱해지는 값입니다.

#### MainTex : Texture

벨트에 적용되는 텍스처를 설정하는 데 사용됩니다. 이 텍스처에 여러 소행성이 포함될 수 잇는 경우 **Atlas** 설정을 사용하여 해당 위치를 지정할 수 있습니다.

#### Atlas : SgtAtlas

이 머티리얼의 기본 텍스처가 아틀라스에 여러 텍스처를 포함하는 경우 여기에서 지정할 수 있습니다.

#### OrbitOffset : float

이 벨트가 애니메이션된 시간(초 단위)입니다.

#### OrbitSpeed : float

이 벨트의 애니메이션 속도입니다.

## SgtBeltAsteroid

SgtBelt__ 컴포넌트에 들어있는 소행성에 대한 모든 정보를 저장합니다.

#### Temp : static SgtBeltAsteroid

벨트가 생성될 때 사용되는 임시 인스턴스입니다.

#### Variant : int

소행성 텍스처의 좌표 인덱스입니다.

#### Color : Color

이 소행성의 색상 틴트입니다.

#### Radius : float

로컬 스페이스에서 이 소행성의 반지름입니다.

#### Height : float

로컬 스페이스에서 이 소행성의 궤도 높이입니다.

#### Angle : float

라디안 각으로 표현되는 이 소행성의 기본 롤 각도입니다.

#### Spin : float

이 소행성이 얼마나 빠르게 회전하는지에 대한 값입니다(라디안/초).

#### OrbitAngle : float

라디안으로 표현되는 이 소행성의 기본 공전 각도입니다.

#### OrbitSpeed : float

라디안으로 표현되는 이 소행성의 공전 속도입니다.

#### OrbitDistance : float

라디안으로 표현되는 이 소행성의 공전 거리입니다.

## SgtBeltCustom

이 컴포넌트를 사용하면 이 소행성 벨트에 있는 각 소행성의 정확한 위치/크기 등을 지정할 수 있습니다.

#### Occlusion : float

이 설정을 통해 라이트 플레어를 사용할 때 소행성이 얼마나 빛을 막을지 결정할 수 있습니다.

#### OuterRadius : float

이 설정을 통해 라이팅을 계산할 때 벨트의 외부 반지름을 지정할 수 있습니다.

#### Asteroids : List<SgtBeltAsteroid>

이 벨트의 커스텀 소행성들입니다.

> **NOTE** - 이것을 수정하면 **DirtyMesh** 메서드를 호출해야 합니다.

## SgtBeltLightingTex

이 컴포넌트를 통해 SgtBelt.LightingTex 필드를 생성할 수 있습니다.

#### FrontPower : float

들어오는 빛이 전방으로 얼마나 날카롭게 산란되는지 결정합니다.

#### BackPower : float

들어오는 빛이 후방으로 얼마나 날카롭게 산란되는지 결정합니다.

#### BackStrength : float

후방으로 산란되는 빛의 강도입니다.

#### BaseStrength : float

수직 산란광입니다.

#### ExportTexture : void

이 메서드를 통해 생성된 텍스처를 에셋으로 익스포트할 수 있습니다.

익스포트가 되면, 이 컴포넌트를 제거하고, 익스포트된 텍스처 에셋을 SgtBelt 컴포넌트의 LightingTex에 설정할 수 있습니다.

## SgtBeltModel

이 컴포넌트는 **SgtBelt** 컴포넌트를 렌더하는 데 사용됩니다.

> **NOET** - 이 컴포넌트는 자동으로 생성되고 관리됩니다.

## SgtBeltSimple

이 컴포넌트를 사용하면 간단한 지수 분포 방식으로 벨트를 생성할 수 있습니다.

#### Seed : int

이 설정을 사용해 절차적인 생성 과정에서 사용할 랜덤 시드를 설정할 수 있습니다.

#### Thickness : float

로컬 좌표계에서 벨트의 두께입니다.

#### ThicknessBias : float

이 값이 높을수록 더 작은 소행성이 생성됩니다.

#### InnerRadius : float

로컬 좌표계에서 벨트 내부 경계의 반지름입니다.

#### InnerSpeed : float

라디안 각으로 표현되는 벨트 내부 경계에서 공전 중인 소행성의 속도입니다.

#### OuterRadius : float

로컬 좌표계에서 벨트 외부 경계의 반지름입니다.

#### OuterSpeed : float

라디안 각으로 표현되는 벨트 외부 경계에서 공전 중인 소행성의 속도입니다.

#### RadiusBias : float

이 값이 높을수록고리의 내부 경계면 근처에서 소행성이 생성될 확률이 높아집니다.

#### SpeedSpread : float

각 소행성에 얼마나 많은 임의의 속도를 추가할 수 있는지 결정합니다.

#### AsteroidCount : int

벨트에 생성될 소행성의 양입니다.

#### AsteroidColors : Gradient

각 소행성은 이 그라디언트로터 랜덤한 색상을 가져옵니다.

#### AsteroidSpin : float

각 소행성의 최대 각속도입니다.

#### AsteroidRadiusMin : float

로컬 좌표계에서 소행성의 최소 반지름입니다.

#### AsteroidRadiusMax : float

로컬 좌표계에서 소행성의 최대 반지름입니다.

#### AsteroidRadiusBias : float

소행성을 생성할 때 크기가 작은 소행성이 생성될 확률입니다.(1 = 기본/선형)