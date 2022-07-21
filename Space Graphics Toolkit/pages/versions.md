# 버전

## 4.0.8

- 고리의 어두운 부분이 투명해지는 경우가 발생하던 문제를 수정했습니다.
- URP의 TerrainPlanet 셰이더 컴파일 문제가 수정되었습니다.
- **Displace**가 비활성화된 SgtPlanet의 시작 시 퍼포먼스가 개선되었습니다.

## 4.0.7

- **EveryWhere**로 설정된 터레인 영역이 작동하지 않는 문제를 수정했습니다.
- 목성형 행성의 어두운 부분이 투명해지는 경우가 발생하던 문제를 수정했습니다.
- **Starfield** 셰이더에 **Align To** 설정을 추가했습니다.
- **StarfieldInfinite** 셰이더에 **Align To** 설정을 추가했습니다.
- **Terrain** 기능에 **SgtTerrainClamp** 컴포넌트를 추가했습니다.
- 터레인 높이 모디파이어 컴포넌트가 컴포넌트 순서대로 실행됩니다.
- 목성형 행성들은 더 이상 자기 자신에게 그림자를 드리우지 않습니다.

## 4.0.6

- **SgtFlareMainTex** 컴포넌트의 **Color** 설정이 무시되는 문제가 수정되었습니다.
- URP/HDRP에서 **SgtStarfield__** 컴포넌트의 stretch 기능이 동작하지 않는 문제가 수정되었습니다.
- 플로팅 오리진 시스템을 사용할 때, **SgtDebrisGrid**를 수정했습니다.

## 4.0.5

- **SgtTerrainAreas**에서 사용하는 텍스처가 non-readable로 설정되어 있을 때 인스펙터에서 경고를 표시하도록 수정했습니다.
- 시각적 메시와 일치하도록 **SgtTerrainCollider**의 버텍스 정렬 및 분포를 수정했습니다.
- **SgtTerrainPrefabSpawner** 컴포넌트의 **Area**가 어긋나고 있는 문제를 수정했습니다.

## 4.0.4

- **Terrain Planet** 셰이더의 모든 세팅을 활성화 했을 때, 마젠타 색으로 표시되는 에러를 수정했습니다.
- 목성형 행성의 깊이 정렬을 개선하기 위해 **SgtRing.SortDistance** 설정을 추가했습니다.
- 목성형 행성에게 그림자가 나타나지 않던 문제를 수정했습니다.

## 4.0.3

- **SgtRing**의 깊이 정렬을 개선했습니다.
- 목성형 행성에 대한 **SgtOcclusionScaler**를 수정했습니다.
- 대기에 대한 **SgtOcclusionScaler**를 수정했습니다.

## 4.0.2

- **Universe/Floating Massive** 데모 씬을 수정했습니다.
- **SgtTerrainFeature.Scale** 설정을 수정했습니다.
- **SgtJovianScatteringTex.Mie** 설정을 제거했습니다.
- **SgtJovianScatteringTex.Rayleigh** 설정을 제거했습니다.
- **Jovian** 셰이더에 **Scattering** **Terms** 설정을 추가했습니다.
- **Jovian** 셰이더에 **Scattering Strengths** 설정을 추가했습니다.
- **Ring** 셰이더에서 **Scattering** **Mie** 설정을 제거했습니다.
- **Ring** 셰이더에서 **Scattering Strength** 설정을 제거했습니다.
- **Ring** 셰이더에 **Scattering** **Terms** 설정을 추가했습니다.
- **Ring** 셰이더에 **Scattering Strengths** 설정을 추가했습니다.
- **Planet** 셰이더에 **DETAIL / Fade Bound** 설정을 추가했습니다.
- **Terrain Planet** 셰이더에 **BAKE DETAIL / Fade Bound** 설정을 추가했습니다.

## 4.0.1

- HDRP에서 planet emission을 수정했습니다.
- **Starfield** 기능에 **Pulse** 데모 씬을 수정했습니다.
- **Starfield** 셰이더에 **PulseMin** 설정을 추가했습니다.
- **Starfield** 셰이더에 **PulseMax** 설정을 추가했습니다.
- **Starfield** 컴포넌트에 **StarPulseSpeedMin** 설정을 추가했습니다.
- **Starfield** 컴포넌트에 **StarPulseSpeedMax** 설정을 추가했습니다.
- **Backdrop** 기능에 **Pulse** 데모 씬을 추가했습니다.
- **Backdrop** 셰이더에 **PulseMin** 설정을 추가했습니다.
- **Backdrop** 셰이더에 **PulseMax** 설정을 추가했습니다.
- **Backdrop** 컴포넌트에 **StarPulseSpeedMin** 설정을 추가했습니다.
- **Backdrop** 컴포넌트에 **StarPulseSpeedMax** 설정을 추가했습니다.

## 4.0.0

> **NOTE** - 이것은 규모 업데이트입니다. 업데이트하려면 먼저 프로젝트를 백업하고 루트 SpaceGraphicsToolkit 폴더를 삭제한 다음 새 버전을 설치해야 합니다.

- 폴더 구조를 Plugins/CW/SpaceGraphicsToolkit 경로 안에 있도록 변경했습니다.
- 각 기능의 예제 폴더 구조가 /Examples 안에 있도록 변경되었습니다.
- 각 기능 코어의 폴더 구조가 /Required 안에 있도록 변경되었습니다.
- 중첩 인스펙터를 구현하는 타사의 에셋을 지원하도록 인스펙터 코드를 업데이트했습니다.
- 이전 장치를 지원하기 위해 **SgtJovian** 셰이더 변경을 되돌렸습니다.
- 더 큰 행성을 지원하도록 **SgtTerrainCollider**를 업데이트했습니다.
- 더 작고 빠른 빌드를 위해 외부 셰이더/머티리얼을 사용하도록 모든 기능을 업데이트했습니다.
- 대부분의 컴포넌트 머티리얼 설정을 외부 셰이더/머티리얼로 이동했습니다.
- 모든 머티리얼 설정에 **Unity Fog / Disable** 설정을 추가했습니다.
- **Accretion** 기능을 **Ring** 기능으로 병합했습니다.
- **SgtRingMesh** 컴포넌트를 제거했습니다.
- 모든 텍스처 생성 컴포넌트에서 **Width/Height** 및 **Format** 설정을 제거했습니다.
- **SgtFlareMaterial** 컴포넌트의 이름이 **SgtFlareMainTex**로 변경되었습니다.
- 극단적인 거리에서 깜빡임 문제를 줄이기 위해 **SgtOcclusionScaler.MaxRaycastDistance**를 추가했습니다.
- 더 큰 유연성을 위해 **BakedBackdrop** 메시를 **SgtBackgroundMesh** 컴포넌트로 대체했습니다.
- **SgtLens** 컴포넌트의 기본 실행 순서를 100으로 변경하여 대부분의 컴포넌트가 업데이트를 마친 후에 렌더링합니다.
- HDRP에서 Terrain Ocean의 투명도를 수정했습니다.
- HDRP에서 **SgtLens** 렝더링이 대부분 수정되었습니다.

## 3.9.13

- **SgtOcclusionScaler**가 더 먼 광원에서 작동하지 않는 문제를 수정했습니다.

## 3.9.12

- 구 버전의 SGT에서 업데이트할 때 발생하는 셰이더 에러를 수정했습니다.

## 3.9.11

- **Resolution** 값이 홀수인 **SgtTerrainCollider**를 수정했습니다.
- **Resolution** 값이 홀수인 **SgtTerrainPrefabSpawner**를 수정했습니다.
- URP에서 가능한 셰이더 오류를 수정했습니다.
- **SgtBelt__** 인스펙터가 나타나지 않던 문제를 수정했습니다.

## 3.9.10

- **Max Sphere Shadows = 0** 설정이 Lit 컴포넌트에서 작동하지 않는 문제를 수정했습니다.
- **Max Sphere Shadows > 2** 설정이 Lit 컴포넌트에서 작동하지 않는 문제를 수정했습니다.
- **SgtTerrainFeature** 빌드 오류를 수정했습니다.
- 새로운 InputSystem 패키지에서 우주선 컨트롤이 작동하지 않는 문제를 수정했습니다.
- Linear color space에서 대기 색상을 수정했습니다.

## 3.9.9

- 모든 데모 씬의 SgtBackdrop 컴포넌트의 RenderQueue 설정을 수정했습니다.
- 유니티 2021.2에서 트랜스폼 기즈모가 나타나지 않는 문제를 수정했습니다.
- 특정 키보드 레이아웃의 데모 씬 오류를 수정했습니다.
- **SgtStarfield__** 컴포넌트에서 **RenderQueue** 설정을 제거했습니다.
- **SgtBelt__** 컴포넌트에 **RenderQueue** 설정을 제거했습니다.
- 먼 은하 등을 렌더링하기 위한 **SgtFloatingMassive** 컴포넌트를 추가했습니다.
- **Universe** 기능에 **Floating Massive** 데모 씬을 추가했습니다.
- **Terrain** 기능에 **Terrain Planet / Feature** 데모 씬을 추가했습니다.

## 3.9.8

- HDRP에서 우주선 모션 블러 이슈를 수정했습니다.
- HDRP에서 거대한 행성의 스페큘러 하이라이트 각도를 수정했습니다.
- HDRP의 대규모 씬에서 배경 블러 이슈를 수정했습니다.
- **SgtBackdrop** 컴포넌트에서 **BlendMode** 설정을 제거했습니다.
- **SgtStarfield** 컴포넌트에서 **BlendMode** 설정을 제거했습니다.

## 3.9.7

- **SgtStarfield** 및 기타 컴포넌트가 씬 그림자를 차단한느 문제를 수정했습니다.
- **Starfield / Custorm** 데모 씬을 추가했습니다.
- **Starfield / Belt** 데모 씬을 추가했습니다.

## 3.9.6

- **SgtCorona**를 인스펙터에서 볼 때 발생하던 문제를 수정했습니다.

## 3.9.5

- **Terrain Planet** 셰이더에 **SHORE** 설정을 추가했습니다.
- **Terrain Ocean** 셰이더에 **SHORE** 설정을 추가했습니다.
- **Terrain** **Ocean** 셰이더에 **WAVES** 설정을 추가했습니다.
- **SolarSystemPack/Explore** 데모 씬에 달을 추가했습니다.
- **Terrain/Waves** 데모 씬을 추가했습니다.
- **Terrain/Shore** 데모 씬을 추가했습니다.
- 일부 시나리오에서 **SgtAtmosphere**가 깜빡거리는 문제를 수정했습니다.
- **SgtAtmosphere.InnerOffset** 설정을 제거했습니다.
- **SgtCorona.InnerOffset** 설정을 제거했습니다.

## 3.9.4

- starfield의 pulse가 작동하지 않는 문제를 수정했습니다.
- SgtTerrainPlanet의 플로팅 포인트의 정확도를 개선했습니다.
- 개선된 ocean mesh 렌더링을 위한 **SgtTerrainOcean** 컴포넌트를 추가했습니다.
- **Terrain Ocean** 셰이더의 depth coloring을 재작성했습니다.
- **Terrain** **Ocean** 셰이더에 **TRANSPARENCY / Mode** 설정을 추가했습니다.
- **Terrain Ocean** 셰이더에 **TRANSPARENCY / Fresnel** 설정을 추가했습니다.
- **Terrain** **Ocean** 셰이더에 **TRANSPARENCY / Depth Scale** 설정을 추가했습니다.
- **Terrain Ocean** 셰이더에 **REFRACTION / Enabled** 설정을 추가했습니다.
- **Terrain Ocean** 셰이더에 **WAVES** 설정을 추가했습니다.

## 3.9.3

- 메시 노멀 심 문제를 일으키는 **SgtPlanet**을 수정했습니다.
- 배경 색의 과포화를 일으키는 **SgtCloudsphere**를 수정했습니다.
- **SgtCloudsphere**의 적도 부근 타일링을 수정했습니다.
- **SgtJovian**의 그림자가 나타나지 않는 문제를 수정했습니다.
- **Cloudsphere** 기능에 두 개의 클라우드스피어 디테일 텍스처를 추가했습니다.

## 3.9.2

- **SgtLight**의 GC Alloc을 수정했습니다.
- URP에서의 **SgtLight** 포인트 라이트 감쇠를 수정했습니다.
- HDRP에서의 **SgtLight** 포인트 라이트 감쇠를 수정했습니다.

## 3.9.1

- **SgtFloatingCamera.GetPosition**의 구현을 수정했습니다.
- 더 적은 샘플러를 사용하도록 **Planet** 셰이더의 디테일 텍스처 구현을 재작성했습니다.
- 더 적은 샘플러를 사용하도록 **Terrain Planet** 셰이더의 디테일 텍스처 구현을 재작성했습니다.
- 새로운 셰이더 설정을 사용하도록 **Solar System Pack**을 업데이트했습니다.

> **NOTE** - 행성의 디테일 텍스처 설정을 재생성해야 합니다.

## 3.9.0

> **NOTE** - 이것은 대규모 업데이트입니다. 인스톨하기 이전에 프로젝트 파일을 백업해두십시오.

- **SgtTerrainCollider**가 간격을 유발할 수 있는 시나리오를 수정했습니다.
- **SgtTerrainPrefabSpawner**가 간격을 유발할 수 있는 시나리오를 수정했습니다.
- **SgtStarfieldInfinite**.Pulse 설정을 수정했습니다.
- 더 나은 HDRP 호환성을 위해 **Accretion** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Atmosphere** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Aurora** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Backdrop** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Belt** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Billboard** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Cloudsphere** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Corona** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Flare** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Jovian** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Lightning** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Prominence** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Ring** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Spacetime** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Star** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Starfield** 셰이더를 다시 작성했습니다.
- 더 나은 HDRP 호환성을 위해 **Thruster** 셰이더를 다시 작성했습니다.
- **Basic Pack / Continuum** 데모 씬을 추가했습니다.
- **SgtCameraPivot** 컴포넌트를 추가했습니다.
- **HDR** 렌더링을 위한 **SgtAtmosphere.ScatteringHdr** 설정을 추가했습니다.
- **SgtAtmosphere.InnerOffset** 설정을 추가했습니다.
- **SgtAtmosphere.AmbientBrightness** 설정을 추가했습니다.
- **SgtAtmosphere.MaxLights** 설정을 추가했습니다.
- **SgtAtmosphere.MaxSphereShadows** 설정을 추가했습니다.
- **SgtBelt__.AmbientBrightness** 설정을 추가했습니다.
- **SgtBelt__.MaxLights** 설정을 추가했습니다.
- **SgtBelt__.MaxSphereShadows** 설정을 추가했습니다.
- **SgtCloudSphere.AmbientBrightness** 설정을 추가했습니다.
- **SgtCloudSphere.MaxLights** 설정을 추가했습니다.
- **SgtCloudSphere.MaxSphereShadows** 설정을 추가했습니다.
- **SgtCorona.InnerOffset** 설정을 추가했습니다.
- **SgtJovian.AmbientBrightness** 설정을 추가했습니다.
- **SgtJovian.MaxLights** 설정을 추가했습니다.
- **SgtJovian.MaxSphereShadows** 설정을 추가했습니다.
- **SgtRing.AmbientBrightness** 설정을 추가했습니다.
- **SgtRing.MaxLights** 설정을 추가했습니다.
- **SgtRing.MaxSphereShadows** 설정을 추가했습니다.
- **SgtSpacetime.MaxGaussianWells** 설정을 추가했습니다.
- **SgtSpacetime.MaxRippleWells** 설정을 추가했습니다.
- **SgtSpacetime.MaxTwistWells** 설정을 추가했습니다.
- **SgtSpacetime.MaxPinchWells** 설정을 추가했습니다.
- **SgtSpacetimeWells.Distribution = Pinch** 설정을 추가했습니다.
- **SgtSpacetimeWells.Opacity** 설정을 추가했습니다.
- **SgtSpacetimeWells.Combine** 설정을 추가했습니다.
- **Spacetime / Pinch Well** 데모 씬을 추가했습니다.
- **Spacetime / Styles** 데모 씬을 추가했습니다.
- 터치 컨트롤이 마우스 컨트롤의 반대가 되도록 허용했습니다.
- 선형 색상 스페이스를 위한 모든 데모 씬을 업데이트했습니다.
- 모든 셰이더가 로컬 키워드를 사용하도록 업데이트했습니다.

## 3.8.6

- **SGT / Planet** 셰이더에 **SHARED / Detail Albedo** 설정을 추가했습니다.
- **SGT / Planet** 셰이더에 **DETAIL / Albedo R/G/B/A** 설정을 추가했습니다.
- **SGT / Terrain Planet** 셰이더에 **SHARED / Detail Albedo** 설정을 추가했습니다.
- **SGT / Terrain Planet** 셰이더에 **DETAIL / Albedo R/G/B/A** 설정을 추가했습니다.
- **SgtCameraLook**의 터치 컨트롤을 수정했습니다.
- **SgtThrusterControls**의 입력 민감도를 수정했습니다.
- 모든 예제 씬의 터치 컨트롤을 수정했습니다.

## 3.8.5

- 카메라가 있는 **SgtStarfieldNebula**의 롤을 수정했습니다.
- 애니메이션에서 수정되었을 때 모든 컴포넌트가 자동으로 업데이트되도록 만들었습니다.
- 사소한 데모 씬의 문제를 다수 수정했습니다.
- 일관성을 개선하기 위해 사소한 코드를 다수 수정했습니다.

## 3.8.4

- **SGT / Terrain Planet** 셰이더를 추가했습니다.
- **SGT / Terrain Ocean** 셰이더를 추가했습니다.
- **SGT / Planet** 셰이더에 두 번째 디테일 레이어를 추가했습니다.
- **SGT / Planet** 셰이더에 최대 4개의 옵션 디테일 채널을 추가했습니다.
- **SgtCameraMove** 컴포넌트에 사시 마우스 휠 지원을 추가했습니다.
- **Terrain** 기능에 새로운 튜토리얼 씬을 추가했습니다.
- 새로운 InputSystem 패키지를 사용할 때 일부 신에서 발생하는 에러를 수정했습니다.
- **SgtTerrainPlanet**과 관련된 컴포넌트에서 발생하는 메모리 누수 문제를 수정했습니다.
- **Planet Surfing** 데모 신에서 우주선 컨트롤을 수정했습니다.
- **SGT / Plane**t 셰이더의 디테일 설정을 단순화했습니다.
- **SgtTerrainPlanetMaterial** 컴포넌트에서 물 설정을 제거했습니다.

## 3.8.3

- 구 버전으로부터 업데이트 시의 호환성을 개선했습니다.

## 3.8.2

- HDRP에서는 SgtStarfieldInfinite의 렌더 문제를 수정했습니다.
- SRP에서 재 임포트 할 때 발생하는 분홍색 머티리얼을 수정했습니다.
- 모든 데모 씬의 하이어라키 구조를 단순화 했습니다.

## 3.8.1

- 문서의 미디어 팩 링크를 수정했습니다.
- 코드에서 SgtBeltSimple의 프로퍼티 에디팅을 수정했습니다.
- 빌드 에러를 수정했습니다.

## 3.8.0

> **NOTE** - 이 버전은 대규모 업데이트입니다. 에셋을 업데이트하기 이전에 프로젝트를 백업해두십시오.

- 메인 빌드을 유니티 2019.4.12f1로 옮겼습니다.
- 변수 **SgtJovian.Occlusion** 설정 출력이 수정되었습니다.
- **SgtFloaringOrbit.Offset** 설정을 추가했습니다.
- **SgtFloatingFollow** 컴포넌트의 회전 핸들링을 수정했습니다.
- **Singularity**기능에 **SgtBlackHole** 컴포넌트를 추가했ㅅ습니다.
- **SgtSingularity** 컴포넌트를 제거했습니다.
- **SGT** **Planet** 셰이더를 **Planet** 셰이더로 교체했습니다.
- **Planet** 셰이더에 **Has** **Lights** 설정을 추가했습니다.
- **Planet** 셰이더에 **Has Water** 설정을 추가했습니다.
- **Planet** 셰이더에 모든 렌더링 파이프라인을 위한 야간 불빛을 추가했습니다.
- **SgtAtmosphere** 컴포넌트를 비활성화 했을 때 발생하는 **SgtPlanet**의 버그를 수정했습니다.
- **PIPELINE** 도구를 제거했습니다(이제 머티리얼 교체가 자동으로 수행됩니다).
- HDRP에서의 대기 깜빡임을 수정했습니다.
- **SgtLight**에 렌더러 특정 강도 설정을 추가했습니다.
- HDRP 설정을 자동으로 수정하기 위해 씬에 **SgtManager** 컴포넌트를 추가했씁니다.
- **SgtLight.Intensity**의 이름을 **IntensityinSgt**로 변경했습니다.
- **Star** 기능을 위한 데모 씬을 개선했습니다.
- **SGT** **Star** 셰이더에 **Flow** 설정을 추가했습니다.
- **SGT Star** 셰이더에 **Sunspots** 설정을 추가했습니다.
- **SgtCorona** 인스펙터의 값이 업데이트되지 않는 문제를 수정했습니다.
- 새로운 **InputSystem** 패키지에 대한 지원을 추가했습니다.
- **SgtCameraMove** 컴포넌트를 재작성했습니다.
- **SgtCameraLook** 컴포넌트를 재작성했습니다.
- **SgtDragSource** 컴포넌트를 추가했습니다.
- **SgtDargReceiver** 컴포넌트를 추가했습니다.

## 3.7.11

- **Starfield** 기능에 **SgtStarfieldDome** 컴포넌트를 추가했습니다.
- **Starfield** 기능에 **Dome** 데모 씬을 추가했습니다.
- **Starfield** 기능에 **Dome / Bias** 데모 씬을 추가했습니다.
- 빌드에서 프리팹을 사용할 때 플레어가 분홍색으로 표시되던 문제를 수정했습니다.

## 3.7.10

- **SgtRing.Occlusion** 설정을 추가했습니다.
- SRP를 사용할 때 **SGT Planet** 셰이더에서 발생하는 기본 워터 레벨 문제를 수정했습니다.
- 단일 패스 인스턴스 VR 렌더링을 사용할 때의 **Singularity** 기능을 수정했습니다.

## 3.7.9

- **SgtBeltCustom.Occlusion** 설정을 추가했습니다.
- **SgtBeltSimple.Layout** 설정에서 그림자가 생기지 않는 문제를 수정했습니다.
- **SgtStarfieldCustom.Layout** 설정에서 그림자가 생기지 않는 문제를 수정했습니다.
- **SgtBeltCustom**의 인스펙터를 수정했습니다.

## 3.7.8

- 별의 숫자를 변경했을 때 발생하는 **SgtStarfieldCustom**의 에러를 수정했습니다.
- 운석의 숫자를 변경했을 때 발생하는 **SgtBeltCustom**의 에러를 수정했습니다.
- **Lightning** 기능의 문서와 튜토리얼 씬을 개선했습니다.
- Lightning 텍스처를 더 추가했습니다.

## 3.7.7

- 텍스처 생성 컴포넌트들로부터 발생하는 WebGL 오류를 수정했습니다.
- 텍스터 생성 컴포넌트들에서 인스펙터 값이 업데이트되지 않는 문제를 수정했습니다.
- 플로팅 오리진 시스템 컴포넌트에서 발생하는 잠재적인 재귀 루프 문제를 수정했습니다.
- 프리팹 모드에서 씬 오브젝트가 나타나는 문제를 수정했습니다.
- 숨김 상태의 씬 오브젝트가 나타나는 문제를 수정했습니다.
- **SgtJovian.CameraOffset** 설정을 추가했습니다.
- **SgtTerrainPlanetMaterial.ClampHeights** 설정을 추가했습니다.
- **SgtTerrainPlanet** LOD 스무딩을 추가했습니다.
- 오로라를 포함하는 **Jovian** 데모씬을 추가했습니다.
- **Earth Sized Plane**t 씬에 광원을 추가했습니다.
- **Obsidian Planet** 씬에 광원을 추가했습니다.

## 3.7.6

- **Obsidian Planet** 데모 씬을 추가했습니다.
- **SgtTerrainSimplex.Ridged** 설정을 추가했습니다.
- **SgtTerrainSimplex.Seed** 설정을 추가했습니다.
- **SgtPlanet.Channel** 설정을 추가했습니다.
- **SgtTerrainPlanetMaterial.WaterLevel** 설정을 추가했습니다.
- **SgtTerrainPlanetMaterial.HeightmapBias** 설정을 추가했습니다.
- **SgtStarfieldInfinite**에 스트래치 기능을 수정했습니다.
- 일부 기본 팩 데모 씬의 머티리얼을 수정했습니다.
- **SgtOcclusion** 코드를 Shader 폴더로 이동했습니다.

## 3.7.5

- **SgtLight.Intensity** 설정을 추가했습니다.
- **SgtTerrainPrefabSpawner.Threshold** 설정을 추가했습니다.
- **SgtTerrainPrefabSpawner.SharedMaterial** 설정을 추가했습니다.
- SRP 호환성을 위해 데모 씬 배경 RenderQueue와 스케일을 업데이트했습니다.
- SRP 호환성 문서를 개선했습니다.
- 단일 패스 스테레오VR 렌더링을 수정했습니다.
- **Spacetime**을 사용하기 쉽게 재작성했습니다.

## 3.7.4

> **NOTE** - 대규모 업데이트입니다. 프로젝트를 백업하고 구 버전 SGT 폴더를 삭제한 후 새 버전을 다시 설치하십시오.

- 메인 빌드를 유니티 2018.4.13f1로 이동했습니다.
- **Terrain** 기능을 추가했습니다.
- **Universe** 기능에 **SgtFloatingParticleSystem** 컴포넌트를 추가했습니다.
- **SgtStaticPlanet**의 이름을 **SgtPlanet**으로 변경했습니다.
- **SgtDepthScale**의 이름을 **SgtOcclusionScaler**로 변경했습니다.
- **SgtDepth**의 이름을 **SgtOcclusion**으로 변경했습니다.
- **SgtDepthCamera** 컴포넌트를 제거했습니다.
- **SgtDepthRaycast** 컴포넌트를 제거했습니다.
- 대기 내부 셰이더에서 Mie scattering을 제거했습니다.
- 메인 컴포넌트들을 위한 커스텀 오클루전 계산을 구현했습니다.
- 모든 컴포넌트에서 자동 생성되는 자식 컴포넌트들을 제거했습니다.
- 다중 카메라 렌더링 코드를 개선했습니다.
- 코드 전체를 리팩토링했습니다.

## 3.7.3

- 대기와 구름구체가 레이어링된 **SgtStaticPlanet**의 경계를 수정했습니다.
- **SgtDynamicPlanet**을 다시 **Planet** 기능으로 옮겼습니다.

## 3.7.2

- 문서를 업데이트했습니다.
- asmdef를 추가했습니다.
- **Universe/Nested Orbits** 데모 씬을 추가했습니다.
- **SgtDynamicPlanet**을 다시 **Terrain** 기능으로 옮겼습니다.
- **SgtStaticPlanet** 극선 UV 생성을 수정했습니다.
- 자동 의존 패키지 설치를 제거했습니다(문서를 확인하십시오).

## 3.7.1

- 유니티 **2018.4**를 사용할 때 발생하는 SRP 버그를 수정했습니다.
- 불필요한 패키지 의존성을 제거했습니다.
- **Shared/Camera Controls** 데모 씬을 추가했습니다.
- **Shared/Rigidbody Controls** 데모 씬을 추가했습니다.
- **Basic Pack/Planet Surfing** 데모 씬을 개선했습니다.
- **Basic Pack/Terrestrial Planet** 데모 씬을 개선했습니다.
- **Basic Pack/Terrastrial Planet + Ring** 데모 씬을 개선했습니다.
- **SgtFloatingSpeedometer.Updatein** 설정을 추가했습니다.

## 3.7.0

- 메인 빌드를 유니티 **2018.4.0f1**로 이동했습니다.
- 새로운 **Planet** 데모 씬을 추가했습니다.
- 새로운 **Universe** 데모 씬을 추가했습니다.
- **Earth Sized Planet** 데모 씬을 추가했습니다.
- **SgtFloatingWarpPin.FloatingCamera** 설정을 추가했습니다.
- **SgtFloatingWarpPin.WorldCamera** 설정을 추가했습니다.
- **SgtFloatingSpawner.Range** 설정을 추가했습니다.
- **SgtFloatingCamera**는 더 이상 카메라와 연결할 필요가 없습니다.
- **SgtFloatingCamera**의 스냅 시도가 사전 렌더링에서 LateUpdate로 이동되었습니다.
- **Terrain** 기능이 **Planet** 폴더로 이동되었습니다.
- **SgtMeshDisplacer**가 **SgtPlanet**으로 통합되었습니다.
- **SgtPlanetMeshConverter**가 **SgtPlanet**으로 통합되었습니다.
- **SgtPlanet**의 이름이 **SgtStaticPlanet**으로 변경되었습니다.
- **SgtTerrain**을 더 빠르게 작동하고 더 큰 스케일의 행성을 다룰 수 있도록 재작성했습니다.
- **SgtTerrain**의 이름이 **SgtDynamicPlanet**으로 변경되었습니다.
- 이동 속도를 수정하기 위해 **SgtCameraMove.MouseSensitivity**를 변경했습니다.
- **SgtFloatingPoint**가 **SgtFloatingCamera**로 통합되었습니다.
- **SgtFloatingPoint**가 **SgtFloatingObject**로 통합되었습니다.
- **SgtFloatingSpawnable**이 **SgtFloatingObject**로 통합되었습니다.
- **SgtFloatingLod** 컴포넌트를 제거했습니다.
- **SgtFloatingOrigin** 컴포넌트를 제거했습니다.
- **SgtFloatingCamera.Scale** 설정을 제거했습니다.
- 더 큰 행성에 대한 **SgtFloatingCamera**의 스냅 동작을 개선했습니다.
- **SgtFloatingFollow** 컴포넌트를 추가했습니다.
- **_MainTex**에 대한 **SgtJovian** 에러를 수정했습니다.

## 3.6.9

- **SgtStarfieldElliptical.StarRadiusBias**의 기본 값이 0이 되던 문제를 수정했습니다.
- **Billboard5** 텍스처의 해상도를 개선했습니다.
- **Billboard6** 텍스처의 해상도를 개선했습니다.
- **SgtInputManager**를 컴포넌트에서 일반 클래스로 변경했습니다.
- 모든 데모 씬을 업데이트했습니다.
- **Basic Pack/Elliptical Galaxy** 데모 씬을 추가했습니다.
- **Basic Pack/Spiral Galaxy** 데모 씬을 추가했습니다.
- **Basic Pack/Nebula** 데모 씬을 추가했습니다.
- **Starfield/Box** 데모 씬을 추가했습니다.
- **Starfield/Box Offset** 데모 씬을 추가했습니다.
- **Starfield/Box Color** 데모 씬을 추가했습니다.
- **Starfield/Box Clouds** 데모 씬을 추가했습니다.
- **Starfield/Box BlendMode** 데모 씬을 추가했습니다.
- **Starfield/Box PowerRGB** 데모 씬을 추가했습니다.
- **Starfield/Box ClampSize** 데모 씬을 추가했습니다.
- **Starfield/Box Layering** 데모 씬을 추가했습니다.
- **Starfield/Elliptical** 데모 씬을 추가했습니다.
- **Starfield/Elliptical Symmetry** 데모 씬을 추가했습니다.
- **Starfield/Elliptical Offset** 데모 씬을 추가했습니다.
- **Starfield/Elliptical Bias** 데모 씬을 추가했습니다.
- **Starfield/Elliptiacl Layering** 데모 씬을 추가했습니다.
- **Starfield/Spiral** 데모 씬을 추가했습니다.
- **Starfield/Spiral Rotation** 데모 씬을 추가했습니다.
- **Starfield/Sprial Arm Cound** 데모 씬을 추가했습니다.
- **Starfield/Spiral Twist** 데모 씬을 추가했습니다.
- **Starfield/Spiral Thickness Inner** 데모 씬을 추가했습니다.
- **Starfield/Spiral Thickness Outer** 데모 씬을 추가했습니다.
- **Starfield/Spiral Layering** 데모 씬을 추가했습니다.
- **Starfield/Nebula** 데모 씬을 추가했습니다.
- **Starfield/Nebula Height Source** 데모 씬을 추가했습니다.
- **Starfield/Nebula Scale Source** 데모 씬을 추가했습니다.
- **Starfield/Nebula Jitter** 데모 씬을 추가했습니다.
- **Starfield/Nebula HorizontalBrightness** 데모 씬을 추가했습니다.
- **Starfield/Nebula Layering** 데모 씬을 추가했습니다.
- **Starfield/Infinite** 데모 씬을 추가했습니다.
- **Starfield/Infinite Far** 데모 씬을 추가했습니다.
- **Starfield/Infinite Warp** 데모 씬을 추가했습니다.
- **Starfield/Infinite Dust** 데모 씬을 추가했습니다.
- **Starfield/Infinite Dust Near** 데모 씬을 추가했습니다.
- **Starfield/Infinite Floating Camera** 데모 씬을 추가했습니다.
- **Starfield/Infinite Floating Origin** 데모 씬을 추가했습니다.

## 3.6.8

- Accretion Disk 빌보드의 플레어 렌더링을 수정했습니다.
- SRP에서 발생하는 SgtShadowLayer 플리커링을 수정했습니다.
- SgtDebrisGrid 스폰 코드를 수정했습니다.
- SgtStarfieldElliptical.Bias 기본 값을 수정했습니다.
- VR 호환성을 위해 데모 씬의 빌보드 Roll To Camera를 활성화했습니다.
- SRP 호환성을 위해 Additive Overlay 셰이더 렌더 큐를 변경했습니다.
- 더 나은 제어 및 SRP 호환성을 위해 SgtAtmosphere.AmbientColor 설정을 추가했습니다.
- 더 나은 제어 및 SRP 호환성을 위해 SgtBelt.AmbientColor 설정을 추가했습니다.
- 더 나은 제어 및 SRP 호환성을 위해 SgtCloudsphere.AmbientColor 설정을 추가했습니다.
- 더 나은 제어 및 SRP 호환성을 위해 SgtJovian.AmbientColor 설정을 추가했습니다.
- 더 나은 제어 및 SRP 호환성을 위해 SgtRing.AmbientColor 설정을 추가했습니다.
- 루트 SGT 폴더에 Rendering Pipeline Switcher 도구를 추가했습니다.
- SgtSingularity에 단일 패스 VR 지원을 추가했습니다.
- SgtSingularity에 SRP 호환성을 추가했습니다.
- SgtStarfield.ClampSize 기능을 추가했습니다.
- Basic Pack에 VR Star 데모 씬을 추가했습니다.
- Basic Pack에 Water Level 데모 씬을 추가했습니다.

## 3.6.7

- SgtFloatingOrbit은 위치 변경이 발생하지 않는 경우 더 이상 이를 알리지 않습니다.
- 카메라 정보에 의존하는 컴포넌트에 대한 SRP 지원을 개선했습니다.
- Planet Pack 1 의존성을 수정했습니다.

## 3.6.6

- 문서를 업데이트했습니다.
- SgtSimpleOrbit을 추가했습니다.
- SgtThrusterControls를 추가했습니다.

## 3.6.5

- 문서를 업데이트했습니다.
- Debirs 데모 씬과 문서를 개선했습니다.

## 3.6.4

- Planet 셰이더에 야간 조명 지원을 추가했습니다.
- Debris 기능을 위한 새로운 데모 씬을 추가했습니다.
- Solor System Pack 링크를 업데이트했습니다.

## 3.6.3

- 그림자 캐스팅 계산을 수정했습니다.
- 컴포넌트 일관성을 개선했습니다.
- 문서를 새로 디자인했습니다.

## 3.6.2

- Solar System Pack을 더 현실적으로 업데이트했습니다.
- SgtStarfieldInfinite에 자동 플로팅 오리진 지원을 추가했습니다.
- 플로팅 오리진 지원을 위한 SgtCamera.UseOrigin 설정을 추가했습니다.
- 빠른 속도의 이동에서 개선된 워프 효과를 위해 SgtStarfield.StretchLimit를 추가했습니다.