# 거대 가스 행성(Jovian)

## Jovian

볼류메트릭 거대 가스 행성을 렌더링하는 방법을 보여줍니다. **Space Graphics Toolkit / Jovian** 셰이더를 사용하는 머티리얼과 **SgtJovian** 컴포넌트를 함께 사용하여 수행됩니다. 거기에 **SgtJovianDepthTex** 컴포넌트를 추가하여 원하는 대로 가장자리의 그라이언트를 제어할 수 있습니다.

### Rim

**SgtJovian.Rim__** 설정을 사용하여 거대 가스 행성의 외부 가장자리 색상을 제어하는 방법을 보여줍니다.

### Lighting

Jovian 머티리얼의 **Lighting** 설정을 활성화하여 거대 가스 행성에 라이팅을 추가하는 방법을 보여줍니다. **SetJovianLightingTex** 컴포넌트를 추가하여 원하는 대로 라이팅 그라디언트를 제어할 수 있습니다. 메인 씬 라이트에 **SgtLight** 컴포넌트를 추가해야 함을 명심하십시오.

### Sunset

**SgtJovianLightingTex.SunsetSharpnessR/G/B** 설정을 사용하여 일몰 색상을 제어하는 방법을 보여줍니다.

### Scattering

Jovian 머티리얼의 **Scattering** 설정을 활성화하여 거대 가스 행성에 대기 산란 효과를 추가하는 방법을 보여줍니다. **SgtJovianScatteringTex** 컴포넌트를 추가하여 원하는 대로 라이팅 그라디언트를 제어할 수 있습니다. 이 기능을 사용하기 위해서는 메인 씬 조명에 **SgtLight** 컴포넌트를 추가해야 합니다.

### Flow

Jovian 머티리얼의 FLOW 설정을 활성화하여 거대 가스 행성의 표면에 애니메이션 움직임을 추가하는 방법을 보여줍니다. 이 텍스터의 픽섹은 알베도가 흐를 방향을 정의합니다. 여기서 RGB 128,128,0 = 움직임 없음, 255,128,0 = 오른쪽으로, 0,128,0 = 왼쪽으로 흐릅니다.