# 목성형 행성(Jovian)

**목성형 행성(Jovian)** 기능을 사용하면 볼류메트릭 거대 가스 행성을 만들 수 있습니다.

**Features/Jovian/Examples** 폴더의 데모 씬은 이 기능의 기본 구성을 단계별로 안내합니다.

## Jovian Shader

**SgtJovian** 컴포넌트는 **Space Graphics Toolkit/Jovian** 셰이더를 사용하는 머티리얼을 사용하여 렌더링됩니다. 각 설정이 수행하는 작업은 다음과 같습니다:

### Depth Tex

광학(optical) 깊이 기울기에 대한 룩업 테이블입니다.

> **NOTE** - **SgtJovianDepthTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### Noise Tex (A)

이 텍스처를 이용해 Flow 텍스처가 오프셋됩니다.

> **NOTE** - SGT와 함께 제공되는 **Noise3D_Alpha** 텍스처를 여기에서 사용할 수 있습니다.

### LIGHTING

> **NOTE** - 이 기능을 사용하기 위해서는 메인 씬 라이트에 **SgtLight** 컴포넌트가 연결되어 있어야 합니다.

이 설정을 통해 목성형 행성은 SGT 커스텀 라이팅 모델을 사용하여 빛과 그림자를 받을 수 있습니다.

### Ambient Color

이 설정을 통해 목성형 행성에 다른 라이팅이 비치지 않을 때 앰비언트 라이트 색상을 설정할 수 있습니다.

### Lighting Tex

라이팅 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtJovianLightingTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### LIGHTING SCATTERING

이 설정을 통해 대기 라이팅 계산에 광원 주변에 halo/glow를 추가하는 대기 산란이 포함될 수 있습니다.

### Scattering Terms

최대 4개의 서로 다른 대기 산란 레이어를 설정할 수 있습니다. 각 값을 사용하면 각 광원 주변의 halo/glow 크기를 제어할 수 있습니다. 값이 클수록 반경이 작아집니다.

> **NOTE** - 이 값은 0으로 설정할 수 없습니다.

> **NOTE** - 빛이 후방-산란(back-scatter)되도록 하려면 적어도 하나의 값을 음수로 설정할 수 있습니다(예:-2.0).

### Scattering Strengths

이 설정을 통해 설정한 4개의 산란 레이어 각각에 대한 강도/밝기를 설정할 수 있습니다. 1을 0으로 설정하면 해당 산란 레이어가 비활성화됩니다.

### Scattering Tex

산란(scattering) 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtJovianScatteringTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### FLOW

이 설정을 통해 플로우 맵을 사용하여 목성 텍스처가 왜곡되도록 만들 수 있습니다.

### Flow Speed

플로우 맵이 움직이는 속도를 결정합니다.

### Flow Strength

플로우 맵은 이 값만큼 UV를 왜곡할 수 있습니다.

### Flow Noise Tiling

이 설정을 통해 플로우 맵 타이밍을 오프셋하여 불규칙하게 보이게 하는 데 사용되는 노이즈의 빈도를 설정할 수 있습니다.