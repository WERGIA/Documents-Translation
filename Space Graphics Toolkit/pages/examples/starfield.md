# 스타필드(Starfield)

## Box

Box 분포를 사용하여 절차적으로 생성된 스타필드를 렌더링하는 방법을 보여줍니다. **Space Graphics Toolkit / Starfield** 셰이더를 사용하는 머티리얼과 함께 **SgtStarfield** 컴포넌트를 사용하여 수행됩니다.

### Offset

**SgtStarfieldBox** 컴포넌트의 **Offset** 프로퍼티를 사용하여 스타필드 분포를 변경하는 방법을 보여줍니다.

### Colors

**StarColors** 설정을 사용하여 각 별을 사용할 때 무작위로 선택되는 색상의 범위를 정의하는 방법을 보여줍니다.

### Clouds

**StarRadiusMin/Max**, **MainTex** 및 **OverrideBrightness** 설정을 조정하여 별 대신 구름을 만드는 방법을 보여줍니다.

### Soft

Starfield 머티리얼의 **DstBlend** 설정이 **OneMinusSrcColor**로 설정될 수 있는 방법을 보여줍니다. 이 설정은 많은 별/구름이 겹칠 때 Starfield가 렌더링되는 방식을 변경하여 더 부드럽게 보이게 합니다. 이 기술을 HDRP나 HDR 렌더링에서 작동하지 않을 수 있습니다.

### PowerRGB

Starfield 머티리얼의 **POWER RGB** 설정을 사용하여 별의 가장자리에만 색상을 지정하고 중심을 흰색으로 유지하는 방법을 보여줍니다. 이렇게 하면 색상이 바뀌더라도 별처럼 보입니다.

### ClampSizeMin

**SgtStarfieldBox** 컴포넌트의 **ClampSizeMin** 설정을 사용하여 스크린의 특정한 최소 크기 아래로 떨어질 때 별을 스케일링하는 대신 페이드 아웃시키는 방법을 보여줍니다. 이렇게 하면 계단 현상이 줄어들고 시각적 품질이 향상됩니다.

### Layering

여러 스타필드를 다른 설정과 결합하여 더 흥미로운 모습을 제공하는 방법을 보여줍니다.

## Elliptical

**SgtStarFieldElliptical** 컴포넌트를 사용하여 절차적으로 타원 형태의 은하 또는 구 형태의 스타필드를 생성하고 렌더링하는 방법을 보여줍니다.

### Symmetry

**Symmetry** 설정을 사용하여 별 분토를 디스크로 평평하게 만드는 방법을 보여줍니다.

### Offset

**Offset** 설정을 사용하여 별을 중앙에서 멀리 밀어내는 방법을 보여줍니다.

### Bias

별이 중심에서 더 가깝거나 멀리 나타날 확률을 변경하기 위해 **Bias** 설정을 사용하는 방법을 보여줍니다.

### Layering

여러 스타필드를 다른 설정과 결합하여 더 흥미로운 모습을 제공하는 방법을 보여줍니다.

## Spiral

**SgtStarfieldSpiral** 컴포넌트를 사용하여 절차적으로 나선 은하 형태의 스타필드를 생성하고 렌더링하는 방법을 보여줍니다.

### Rotation

**SgtRotate** 컴포넌트를 사용하여 나선 은하를 자동으로 회전 시키는 방법을 보여줍니다.

### ArmCount

**ArmCount** 설정을 사용하여 나선형 팔의 갯수를 변경하는 방법을 보여줍니다.

### Twist

**Twist** 설정을 사용하여 나선형 팔의 비틀림 비율을 변경하는 방법을 보여줍니다.

### ThicknessInner

**ThicknessInner** 설정을 사용하여 중앙의 나선형 팔 두께를 변경하는 방법을 보여줍니다.

### ThicknessOuter

**ThicknessOuter** 설정을 사용하여 중심에서 멀어지는 나선형 팔 두께를 변경하는 방법을 보여줍니다.

### Layering

여러 스타필드를 다른 설정과 결합하여 더 흥미로운 모습을 제공하는 방법을 보여줍니다.

## Nebula

SgtStarfieldNebula 컴포넌트를 사용하여 지정한 사용자 정의 SourceTex 형태의 스타필드를 절차적으로 생성하고 렌더링하는 방법을 보여줍니다. 여기에 사용하는 텍스처는 Read/Write 설정을 Enable로 해줘야 합니다.

### HeightSource

**HeightSource** 설정을 사용하여 별이 로컬 XZ 평면에서 오프셋이 되는 방식을 변경하는 방법을 보여줍니다.

### ScaleSource

**ScaleSource** 설정을 사용하여 기본 색상을 기반으로 별의 크기를 조정하는 방법을 보여줍니다.

### Jitter

**Jitter** 설정을 사용하여 밝은 별 무리가 스타필드의 밝기를 날려버리는 것을 방지하는 방법을 보여줍니다. 이 설정은 스타필드의 전체 모양이 선명도를 잃는 원인이 됩니다.

### HorizontalBrightness

**HorizontalBrightness** 설정을 사용하여 측면에서 볼 때 스타필드에 조명이 비추는 방식을 제어하는 방법을 보여줍니다. 이렇게 하면 은하와 같은 평평한 스타필드를 만들 때 밝기가 날아가는 것을 방지할 수 있습니다.

### Layering

여러 스타필드를 다른 설정과 결합하여 더 흥미로운 모습을 제공하는 방법을 보여줍니다.

### Infinite

**SgtStarfieldInfinite** 컴포넌트를 사용하여 카메라 주위에 무한하게 반복되는 별을 만드는 방법을 보여줍니다.

### Far

**Far** 설정과 **SgtStarfieldInfiniteFarTex** 컴포넌트를 사용하여 **FarRadius** 및 **FarThickness** 설정을 기반으로 별을 페이드 아웃하는 방법을 보여줍니다. 한 방향으로 무한하게 이동할 때 해당 방향에서 갑자기 별이 나타나거나 이동 방향의 반대 방향에서 별이 갑자기 사라지는 현상을 숨기기 위해 사용됩니다.

### Warp

**Stretch** 설정을 사용하여 **SgtCamera** 컴포넌트가 있는 카메라의 속도에 따라 별을 늘어지게 만드는 방법을 보여줍니다. 움직이지 않을 때는 stretch가 0이 되므로 별이 사라집니다. 이를 방지하기 위해 이 데모 씬에는 동일한 설정의 확장되지 않은 스타필드도 있으므로 움직이지 않을 때에도 별을 볼 수 있습니다.

### Dust

설정을 변경하여 무한 반복되는 우주 먼지를 만드는 방법을 보여줍니다.

### Dust Near

**Near** 설정과 **SgtStarfieldNear** 컴포넌트를 사용하여 **NearRadius** 및 **NearThickness** 설정을 기반으로 별을 페이드 아웃하는 방법을 보여줍니다. 별이 너무 가까워져 카메라에 끼일 때 별을 부드럽게 흐리도록 만들기 위해 사용됩니다.

### Floating Camera

**SgtStarfieldInfinite**가 플로팅 오리진 시스템의 **SgtFloatingCamera** 컴포넌트와 어떻게 자동으로 작동하는지 보여줍니다. 자세한 내용은 **Universe** 기능을 참조하세요.

## Dome

**SgtStarfieldDome** 컴포넌트를 사용하여 돔 모양의 스타필드를 절차적으로 생성하고 렌더링하는 방법을 보여줍니다.

### Bias

Bias 설정을 사용하여 수평선 근처에 더 많거나 적은 별을 배치하는 방법을 보여줍니다.

## Custom

스타필드의 star 데이터를 수동으로 수정할 수 잇는 방법을 보여줍니다. **SgtStarfield__** 컴포넌트를 찾고 컨텍스트 메뉴(⋮ 버튼)를 열고 **Make Editable Copy** 옵션을 선택하여 수행됩니다. 그러면 **SgtStarfieldCustom** 컴포넌트가 부착된 새 게임 오브젝트가 생성되고 모든 절차적 별 데이터를 별 목록에 복사하여 수동으로 수정할 수 있게 됩니다. 코드에서 이 목록을 수정하는 경우 나중에 **DirtyMesh()** 메서드를 수동으로 호출해야 합니다.

## Pluse

**Starfield** 머티리얼의 **PULSE** 설정을 활성화하여 시간이 지남에 따라 각 별의 크기를 변화하게 만드는 방법을 보여줍니다. **SgtStarfield__** 컴포넌트의 **StarPulseSpeedMin/Max** 설정을 사용하여 펄스 속도를 제어할 수 있습니다.