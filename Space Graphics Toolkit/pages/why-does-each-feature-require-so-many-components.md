# 각 기능에 많은 컴포넌트가 필요한 이유는 무엇입니까?

많은 SGT 기능은 컴포넌트 조합을 사용하여 렌더링됩니다. 예를 들어, **Atmosphere** 기능은 **SgtAtmosphere**, **SgtAtmosphereDepthTex**, **SgtAtmosphereLightingTex** 및 **SgtAtmosphereScatteringTex** 컴포넌트를 사용하여 렌더링됩니다.

이런 식으로 컴포넌트가 분리되는 주된 이유는 코드 구조를 개선하기 위한 것이지만 이 시스템을 이용하면 씬을 최적화할 수도 있습니다. 이러한 컴포넌트의 오른쪽 상단에 있는 컨텍스트 메뉴 버튼(⋮ 버튼)을 클릭하면 **Export Mesh**(메시 내보내기), **Export Texture**(텍스처 내보내기) 등의 옵션이 있음을 알 수 있습니다. 예를 들어, **SgtAtmosphereLightingTex** 컴포넌트의 컴포넌트의 컨텍스트 메뉴에는 **ExportMesh** 옵션이 있습니다. 이렇게 하면 생성된 대기의 **LightingTex** 텍스터를 에셋으로 저장할 수 있으므로 이제 이 컴포넌트를 제거하고 저장된 텍스처를 대기 머티리얼의 **LightingTex**로 끌어다 놓을 수 있습니다.

이렇게 하면 씬에 대기를 추가할 때마다 **SgtAtmosphereLightingTex** 컴포넌트가 더 이상 새 텍스처를 생성할 필요가 없기 때문에 씬의 성능을 향상시킬 수 있습니다. 물론 단점으로는 텍스처 설정을 더 이상 조정할 수 없기 때문에 게임에서 생성 설정을 제어할 수 있어야 하는 프로젝트에는 적합하지 않을 수 있습니다.