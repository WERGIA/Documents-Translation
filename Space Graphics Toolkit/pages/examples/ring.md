# 고리(Ring)

## Accretion Disk

강착 원반을 렌더링하는 방법을 보여줍니다. 이것은 **SgtRing** 컴포넌트와 **Space Graphics Toolkit / Ring** 셰이더를 사용하는 머티리얼을 함께 사용하여 수행됩니다.

### Animated Noise

기본 강착 원반 텍스처를 향상시키기 위한 방법으로 Ring 머티리얼의 **Detail** 설정을 **Color**로 설정하여 detail texture를 레이어링 할 수 있는 방법을 보여줍니다.

## Planetary Ring

다른 링 텍스처를 사용하여 행성 고리를 표현하는 방법을 보여줍니다.

### Lighting

Ring 머티리얼의 **LIGHTING** 설정을 활성화하여 링에 조명과 그림자를 추가하는 방법을 보여줍니다. 조명을 추가한 이후에 **SgtRingLightingTex** 컴포넌트를 추가하여 원하는 대로 라이팅 그라디언트를 제어할 수 있습니다. 메인 씬 조명에 **SgtLight** 컴포넌트를 추가해야 함을 명심하십시오.

### Scattering

Ring 머티리얼의 **LIGHTING SCATTERING** 설정을 활성화하여 고리를 통한 빛 산란 효과를 추가하는 방법을 보여줍니다.

### Planet Shadow

**SgtShadowSphere** 컴포넌트를 행성에 추가하여 고리에 자동으로 그림자를 드리우는 방법을 보여줍니다.

### Ring Shadow

Ring 게임 오브젝트에 **SgtShadowRing** 컴포넌트를 추가하는 방법을 보여줍니다. 그러면 행성 고리가 SGT 그림자 시스템을 사용하여 씬에 그림자를 드리울 수 있습니다. 이를 위해서는 SGT 그림자 시스템과 호환되도록 **SgtShadowLayer** 컴포넌트를 행성에 추가해야 합니다.

### Detail

Ring 머티리얼의 **DETAIL** 설정을 **Alpha**로 설정하여 링을 가까이서 더 흥미롭게 만드는 디테일 텍스처를 추가할 수 있는 방법을 보여줍니다.

### Near Fade

Ring 머티리얼의 **NEAR FADE** 설정을 활성화하는 방법을 보여줍니다. **NEAR FADE**를 활성화하면 카메라가 접근함에 따라 행성 고리가 페이드 아웃됩니다. **SgtRingNearTex** 컴포넌트를 추가하여 페이드 아웃 전환을 제어할 수 있습니다.

### Customize

실행 중에 고리의 크기를 제어할 수 있도록 하는 **SgtRing.RadiusInner** + **RadiusOuter** 설정을 제어하는 방법을 보여줍니다.