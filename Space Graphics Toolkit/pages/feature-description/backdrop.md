# 배경(Backdrop)

**배경(Backdrop)** 기능을 사용하면 배경 별, 구름 및 기타 시각 효과를 만들 수 있습니다. 이 시각 효과들은 항상 카메라를 향하고 따라오는 빌보드를 사용하여 작동합니다. 다음과 같은 이유로 배경에 매우 적합합니다:

1. 오버드로가 거의 없기 때문에 렌더링에 매우 효율적입니다(개별 빌보드 크기를 너무 많이 늘리지 않는 한).
2. 각 빌보드는 고유한 질감을 가질 수 있으므로 확대해도 스카이박스와 달리 디테일을 유지합니다.
3. 빌보드는 파티클 빌보드와 달리 정적이고 모든 각도에서 일관되게 보이기 때문에 VR에 사용하기 적합합니다.
4. 각 빌보드가 4개의 버텍스에 불과하기 때문에 메모리를 거의 소모하지 않습니다.

**Features/Backdrop/Examples** 폴더의 데모 씬은 이 기능의 기본 구성을 단계별로 안내합니다.

## Backdrop Shader

**SgtBackdrop** 컴포넌트는 **Space Graphics Toolkit/Backdrop** 셰이더를 쓰는 머티리얼을 사용하여 렌더링됩니다. 각 설정이 수행하는 작업은 다음과 같습니다.

### POWER RGB

일반적으로 각 배경 빌보드의 색상에 빌보드 텍스처를 곱하여 색상을 부여합니다. 그러나 이 설정을 사용하면 RGB 값이 대신 해당 색상의 거듭제곱으로 올라갑니다. 빌보드에 별 텍스처가 있는 경우 별의 가장자리만 색상이 지정되고 가운데는 흰색으로 유지됩니다. 이 방식은 별을 렌더링하는 데 적합합니다.

### Color Influence

이 설정을 통해 빌보드 텍스처에 컬러 틴트를 적용하는 정도를 제어할 수 있습니다.