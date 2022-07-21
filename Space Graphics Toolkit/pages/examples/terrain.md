# 지형(Terrain)

## Burst

## Terrain Planet

**SgtTerrainPlanet** 컴포넌트를 사용하여 카메라 거리에 기반한 동적 LOD로 행성 메시를 생성하는 방법을 보여줍니다. **SgtTerrainPlanetMaterial** 컴포넌트가 함께 추가되어 **Space Graphics Toolkit/Terrain Planet** 셰이더를 사용한 머티리얼로 메시를 렌더링합니다. 셰이더 설정에 대한 자세한 내용은 **Planet** 및 **Terrain** 기능 설명서를 참조하세요.

### Atmosphere

**SgtTerrainSharedMaterial** 컴포넌트를 사용하여 지형 위에 대기를 렌더링하는 방법을 보여줍니다.

### Heightmap

**SgtTerrainHeightmap** 컴포넌트를 사용하여 높이맵 텍스처를 사용하여 동적 행성 메시를 변형한느 방법을 보여줍니다. 이 텍스처는 정방형(원통형) 텍스처를 사용해야 합니다.

### Simplex

**SgtTerrainSimplex** 컴포넌트를 사용하여 지형에 절차적 높이를 추가하는 방법을 보여줍니다. 데모 씬에서 행성 표면으로 이동하여 이 기능이 동작하는 모습을 확인할 수 있습니다.

### Collider

카메라가 행성의 표면에 접근할 때 **SgtTerrainCollider** 컴포넌트를 사용하여 지형에 MeshCollider를 생성하는 방법을 보여줍니다. 생성된 콜라이더의 **디테일(Detail)**을 제어하여 각 MeshCollider에 제공되는 삼각형의 수를 변경할 수 있습니다. 또한 **해상도(Resolution)**를 제어하여 각 MeshCollider의 측면을 제어할 수 있습니다.

### Spawner

**SgtTerrainPrefabSpawner** 컴포넌트를 사용하여 카메라가 접근함에 따라 행성의 지형 표면에 프리팹을 절차적으로 생성하는 방법을 보여줍니다. 이 컴포넌트를 통해 생성되는 객체의 최대 양(**Limit**), 방향(**Rotate**), 무작위로 선택되는 프리팹(**Prefabs**)의 목록을 제어할 수 있습니다.

### Areas

**SgtTerrainPlanet.Areas** 설정을 사용하여 행성 표면의 다른 영역을 정의하는 방법을 보여줍니다. **SgtTerrainSimplex** 및 **SgtTerrainPrefabSpawner**와 같은 컴포넌트는 **Area** 설정을 사용하여 이 영역에 스스로를 잠글 수 있습니다. 이러한 영역은 입력 색상 텍스터(input color texture)를 사용하는 **SgtTerrainSplatmap** 에셋을 사용하여 정의되며 다른 색상을 이름으로 다른 영역과 연결할 수 있습니다. 예제 에셋을 복제하여 자신만의 에셋을 만들 수 있습니다.

### Feature

**SgtTerrainFeature** 컴포넌트가 커스텀 높이맵 텍스처를 사용하여 행성의 특정 영역을 변형시키는 데 어떻게 사용될 수 있는지 보여줍니다.

## Terrain Ocean

터레인 행성에 바다 레이어를 추가하는 방법을 보여줍니다. 새 게임 오브젝트에 **SgtTerrainOcean** 및 **SgtTerrainOceanMaterial** 컴포넌트를 추가하여 수행됩니다. 이것은 **Space Graphics Toolkit / Terrain Ocean** 셰이더를 사용하는 머티리얼로 렌더링 되어야 합니다(자세한 내용은 문서 참조). 바다는 카메라에 **SgtDepthTextureMode** 컴포넌트를 추가하여 활성화할 수 있는 깊이 텍스처를 렌더링해야 합니다.

### Atmosphere

**SgtTerrainSharedMaterial** 컴포넌트를 지형과 바다 게임 오브젝트 모두에 추가하여 그 위에 대기가 렌더링되도록 하는 방법을 보여준다.

### Depth Color

Ocean 머티리얼의 **DEPTH COLOR** 설정을 사용하여 해안선에 접근할 때 바다의 색상을 변경하는 방법을 보여줍니다.

### Detail

Ocean 머티리얼의 **BAKE DETAIL** 설정을 활성화하여 최대 3개의 세부 레이어를 바다에 추가할 수 있는 방법을 보여줍니다. 각 세부 수준의 타일링은 **SgtTerrainOcean** 컴포넌트의 **BakeDetailTilingA/B/C** 설정을 사용하여 조정할 수 있습니다. 각 디테일 레이어에는 **Fade Range** 설정도 있습니다. 이 설정은 다음 레이어에 접근할 때 이전 레이어를 숨기는데 사용할 수 있습니다.

### Animation

**SgtTerrainOceanMaterial** 컴포넌트의 **Animate** 설정을 활성화하는 방법을 보여줍니다. 이렇게 하면 시간 경과에 따라 바다의 디테일 텍스처가 움직이며 바다의 표면이 더 흥미롭게 보이게 됩니다. **Detail A/B/C** 설정을 사용하여 수정되는 세부 레이어를 제어할 수 있습니다.

### Waves

Ocean 머티리얼의 **WAVES** 설정을 사용하여 바다 해안선에 애니메이션 파도를 추가하는 방법을 보여줍니다. 웨이브 설정에 대한 자세한 내용은 **Terrain** 기능 설명서를 참조하세요.

### Shore

Planet 머티리얼의 **SHORE** 설정을 사용하여 지형의 해안선에 해변을 추가하는 방법을 보여줍니다. wave 설정에 대한 자세한 내용은 **Terrain** 기능 설명서를 참조하세요.