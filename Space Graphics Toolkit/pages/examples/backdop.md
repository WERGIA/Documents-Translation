# 우주 배경(Backdrop)

## Backdrop

씬의 배경에서 구름을 렌더링하는 방법을 보여줍니다. 이것은 **Space Graphics Toolkit/Backdrop** 셰이더를 사용하는 머티리얼과 함께 **SgtBackdrop** 컴포넌트를 사용하여 수행됩니다. 이 구름은 어디를 보든 크기와 회전을 유지하므로 VR에서 멋지게 보입니다.

### PowerRGB

**Backdrop** 셰이더의 **Power RGB** 설정을 활성화하는 방법을 보여줍니다. 이 설정은 별 텍스처 외부의 색상만 변경하여 별을 렌더링하는데 적합합니다.

### ClampSizeMin

**SgtBackdrop** 컴포넌트의 **ClampSizeMin** 설정을 증가시켜 별이 너무 작아지는 것을 방지하는 방법을 보여줍니다. 별이 너무 작아지면 카메라가 회전하면서 깜빡거리기 시작합니다.

### Customize

UI 슬라이더로 별의 설정을 제어하는 방법을 보여줍니다.

### Pulse

시간이 지남에 따라 각별의 크기를 펄스로 만드는 backdrop 머티리얼의 **PULSE** 설정을 활성화하는 방법을 보여줍니다. **SgtBackdrop** 컴포넌트의 **StarPulseSpeedMin/Max** 설정을 사용하여 펄스 속도를 제어할 수 있습니다.