# 스타필드(Starfield)

**스타필드(Starfield)** 기능을 사용하면 많은 양의 별과 관련된 다양한 효과를 렌더링할 수 있습니다. 예를 들어, 타원 은하, 나선 은하, 심지어는 스타필드 워프 효과도 있습니다.

**Features/Starfield/Examples** 폴더의 데모 씬은 이 기능의 기본 구성을 단계별로 안내합니다.

## Starfield Shader

**SgtStarfield** 컴포넌트는 **Space Graphics Toolkit/Starfield** 셰이더를 사용하는 머티리얼을 사용하여 렌더링됩니다. 

### DstBlend

혼합 모드의 **DstBlend** 부분을 제어할 수 있습니다. 기본적으로 가산 혼합인 경우 **One**으로 설정됩니다. 그라니 이를 **OneMinusSrcColor**로 설정하면 블렌딩을 더 부드럽게 만들 수 있습니다.

> **NOTE** - **OneMinusSrcColor** 혼합은 HDR 카메라 렌더링이나 HDRP와 함께 사용할 수 없습니다.

### NEAR FADE

카메라가 접근함에 따라 스타필드가 페이드 아웃되게 합니다.

#### Near Range Recip

페이드가 시작될 월드 공간 거리의 역수를 설정할 수 있습니다.

#### Near Tex

페이드 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtStarfieldNearTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.

### FAR FADE

카메라가 너무 멀리 가면 스타필드가 페이드 아웃되게 압니다.

#### Far Radius

페이드가 시작될 월드 공간 거리를 설정할 수 있습니다.

#### Far Range Recip

페이드 영역의 월드 공간 두께의 역수를 설정할 수 있습니다.

#### Far Tex

페이드 그라디언트에 대한 룩업 테이블입니다.

> **NOTE** - **SgtStarfieldFarTex** 컴포넌트를 사용하여 런타임에 이를 생성하고 편집 중에 내보낼 수도 있습니다.