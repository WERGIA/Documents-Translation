# 대기(Atmosphere)

**대기(Atmosphere)** 기능을 사용하면 오브젝트 주위에 볼류메트릭 안개를 추가할 수 있습니다. 이것은 항성 주위에 코로나를 만들거나 행성 주위에 라이팅을 사용해 행성 대기를 만들 수 있습니다.

**Feature/Atmosphere/Examples** 폴더의 데모 씬은 이 기능의 기본 구성을 단계별로 안내합니다.

## Atmosphere Shader

**SgtAtmosphere** 컴포넌트는 **Space Graphics Toolkit/Atmosphere** 셰이더를 쓰는 머티리얼을 사용하여 렌더링됩니다. 설정이 수행하는 작업은 다음과 같습니다:

### Inner Depth Tex

내부 메시(표면)에 적용된 **DepthTex**입니다.

> **NOTE** - **SgtAtmosphereDepthTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.
> 

### Outer Depth Tex

외부 메시(하늘)에 적용된 **DepthTex**입니다.

> **NOTE** - **SgtAtmosphereDepthTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.
> 

### LIGHTING

> **NOTE** - 이 기능을 사용하려면 메인 씬 조명에 **SgtLight** 컴포넌트가 연결되어 있어야 합니다.
> 

이 설정을 통해 SGT 커스텀 라이팅 모델을 사용하여 대기가 빛과 그림자를 받을 수 있습니다.

#### Ambient Color

이 설정을 통해 대기에 다른 라이트가 비치지 않을 때 앰비언트 라이트 색상으로 설정할 수 있습니다.

#### Lighting Tex

라이팅 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtAtmosphereLightingTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### LIGHTING SCATTERING

이 설정을 통해 대기 라이팅 계산에는 광원 주변에 후광(halo)/광선(glow)을 추가하는 대기 산란을 구현할 수 있습니다.

#### Scattering Terms

최대 3개의 서로 다른 대기 산란 레이어를 설정할 수 있습니다. 각 값을 사용하면 각 관원 주변의 후광(halo)/광선(glow) 크기를 제어할 수 있습니다. 값이 클수록 반경이 작아집니다.

> **NOTE** - 이 값은 0으로 설정할 수 없습니다.

> **NOTE** - 빛이 후방산란(back-scatter)되도록 하려면 적어도 하나의 값을 음으로 설정할 수 있습니다(예:-2.0).

#### Scattering Strengths

이 설정을 통해 위에서 설정한 4개의 산란 레이어 각각에 대한 강도(strength)/밝기(brightness)를 설정할 수 있습니다. 1으로 설정된 값을 0으로 바꾸면 해당 산란 레이어가 비활성화 됩니다.

#### Scattering Tex

라이팅 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtAtmosphereScatteringTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### LIGHTING SCATTERING HDR

이 설정을 통해 대기 산란 계산이 일반 0..1(0..255) 범위를 초과하여 HDR 렌더링에 적합하도록 만들 수 있습니다. 프로젝트에 HDR 카메라 렌더링을 사용하는 경우 이 옵션을 활성화해야 합니다.

> **NOTE** - 이 설정은 HDRP를 사용할 때 강제로 활성화됩니다.