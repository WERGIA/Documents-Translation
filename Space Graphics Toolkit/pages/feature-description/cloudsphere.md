# 클라우드스피어(Cloudsphere)

**클라우드스피어(Cloudsphere)** 기능을 사용하면 행성에 구름 레이어를 추가할 수 있습니다.

**Features/Cloudsphere/Examples** 폴더의 데모 씬은 이 기능의 기본 구성을 단계별로 안내합니다.

## Cloudsphere Shader

**SgtCloudsphere** 컴포넌트는 **Space Graphics Toolkit/Cloudsphere** 셰이더를 사용하는 머티리얼을 사용하여 렌더링됩니다. 설정이 수행하는 작업은 다음과 같습니다:

### Depth Tex

광학(optical) 깊이 기울기에 대한 룩업 테이블입니다.

> **NOTE** - **SgtCloudsphereDepthTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### NEAR FADE

이 설정을 통해 카메라가 접근함에 따라 클라우드스피어가 페이드 아웃됩니다.

### Near Range Recip

이 설정을 통해 페이드가 시작될 월드 공간 거리의 역수를 설정할 수 있습니다.

> **NOTE** - **SgtCloudsphereNearTex** 컴포넌트를 사용하여 이 값을 계산할 수 있습니다.

### Near Tex

페이드 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtCloudsphereNearTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### DETAIL

이 설정을 통해 클라우드스피어 기본 텍스처의 디테일을 향상시킬 수 있습니다.

### Detail Strength

이 설정을 통해 디테일 텍스처가 기본 텍스처의 불투명도에 얼마나 영향을 미칠지 제어할 수 있습니다.

### Detail Tiling

디테일 텍스처는 클라우드스피어 주변에 여러 번 타일링됩니다.

### Detail Tex

디테일 텍스처입니다.

> **NOTE** -  이 텍스처는 알파 채널에 저장된 세부 정보화 함께 심리스로 처리되어야 합니다.

### LIGHTING

> **NOTE** - 이 기능을 사용하기 위해서는 메인 씬 라이트에 SgtLight 컴포넌트가 연결되어 있어야 합니다.

이 설정을 통해 클라우드스피어는 SGT 커스텀 라이팅 모델을 사용하여 빛과 그림자를 받을 수 있습니다.

### Ambient Color

이 설정을 통해 클라우드스피어에 다른 라이트가 비춰지지 않을 때 앰비언트 라이트 컬러를 설정할 수 있습니다.

### Lighting Tex

라이팅 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtCloudsphereLightingTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.