# 행성(Planet)

## Planet

**SgtPlanet** 컴포넌트를 **SGT / Planet** 셰이더와 함께 사용하여 기본 행성을 렌더링하는 방법을 보여줍니다. **Albedo(RGB) Smoothness(A)** 텍스처, **Normal** 텍스처와 같은 머티리얼 설정을 조정하여 행성의 기본 모양을 조정할 수 있습니다.

### Displace

Planet 컴포넌트의 **Diplace** 설정이 행성 머티리얼에 설정된 높이맵을 기반으로 행성 높이를 변경하는 방법을 보여줍니다.

### Detail

행성에 심리스 디테일 텍스처를 추가하는 방법을 보여줍니다. 이것은 Planet 셰이더의 **SHARED / Detail R** 및 **SHARED / Normal Enabled** 설정을 활성화하여 수행됩니다. 그런 다음 모든 디테일 레벨에서 사용할 심리스 일반 텍스처인 **SHARED / Normal R** 텍스처를 설정할 수 있습니다. 그런 다음 **DETAIL / Enabled** 설정을 활성화하면 행성에 한 레벨의 디테일이 적용됩니다. 특정 영역에만 디테일이 나타나도록 하려면 **SHARED / Detail Mask(RGBA)** 텍스처를 설정할 수 있습니다. **Detail R/G/B**를 활성화하여 행성에 더 많은 타입의 디테일을 추가할 수도 있습니다.

#### Secondary

Planet 셰이더의 두번째 **DETAIL / Enable** 및 관련 설정을 사용하여 행성의 디테일을 더욱 향상시키는 방법을 보여줍니다. 이것은 행성에 더 가까이 확대하거나 접근하여 비행하는 경우에 유용합니다.

### Water

Planet 셰이더의 **Water** 설정을 활성화하는 방법을 보여주고 Planet 컴포넌트의 **Water Level**(수위) 설정을 조정할 수 있도록 합니다.

#### Clamp

Planet 컴포넌트의 **Clamp Water** 설정을 활성화할 수 있는 방법을 보여줍니다. 이렇게 하면 물이 **Radius** 값에 유지되고 최대 높이가 **Displacement** 값에 있게 되어 씬을 더 쉽게 설정할 수 있습니다.

#### Gradient

**P3dPlanetWaterGradient** 컴포넌트를 Planet 컴포넌트와 함께 추가하는 방법을 보여줍니다. 이를 통해 수심에 따라 물의 색상을 변경할 수 있습니다.

#### Texture

**P3dPlanetWaterTexture** 컴포넌트가 Planet 컴포넌트와 함께 어떻게 추가될 수 있는지를 보여줍니다. 이를 통해 물에 대한 노멀 맵을 선택할 수 있으며 이것은 애니메이션화된 행성의 물에 적용됩니다.

#### Coast

Planet 셰이더의 **Coast Sharpness** 설정을 사용하여 육지와 바다 사이의 전환을 조정하는 방법을 보여줍니다.

#### Emission

Planet 셰이더의 **Emission** 설정을 사용하여 물을 빛나게 하여 용암처럼 보이게 하는 방법을 보여줍니다.

### Atmosphere

Planet 컴포넌트의 **Shared Material** 설정이 행성 GameObject에 추가된 대기로 설정되는 방법을 보여줍니다. 대기의 **Inner Mesh Radius** 설정은 행성의 **Radius** 설정과 일치해야 합니다.

### Collider

Planet 컴포넌트의 **Mesh Collider** 설정을 사용하여 시각적 메시와 일치하는 Collider를 생성하는 방법을 보여줍니다. 메시가 고해상도인 경우 속도가 느릴 수 있습니다. 이 문제를 해결하기 위해서 Collider로 더 낮은 해상도의 ‘보이지 않는(invisible)’ 행성을 만들 수 있습니다.