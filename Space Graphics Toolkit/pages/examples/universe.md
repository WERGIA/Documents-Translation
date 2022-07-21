# 우주(Universe)

## Camera

**SgtCameraMove** 및 **SgtCameraLook** 컴포넌트로 기본 씬을 만드는 방법을 보여줍니다. 이것은 작은 씬에서는 잘 작동하지만 카메라가 너무 멀리 이동하면 렌더링, 물리 등 뿐만 아니라 움직임이 중단되기 시작합니다.

## Floating Camera

**SgtFloatingCamera** 컴포넌트를 카메라에 추가하여 너무 멀리 이동할 때 위치가 다시 0, 0, 0으로 다시 스냅되도록하는 방법을 보여줍니다.누적 카메라 위치는 여전히 이 컴포넌트에 저장되므로 매우 멀리(예:광년 단위로 떨어져도) 정확한 위치를 가질 수 있습니다.

## Floating Object

**SgtFloatingObject** 컴포넌트를 소행성에 추가하여 카메라 위치가 스냅될 때마다 위치가 업데이트되도록 하는 방법을 보여줍니다. 이것이 플로팅 오리진 시스템의 전부로 이제 씬에서 이 시스템이 동작하게 됩니다. 오브젝트를 매우 먼 위치에 정확하게 배치하려면 **LocalX/Y/Z** 값을 조정하는 것이 좋습니다. 이 값은 **Transform.position**보다 더 높은 정밀도를 제공하고 카메라 위치가 스냅될 때 변경되지 않습니다.

## Floating Speedometer

**SgtFloatingSpeedometer** 컴포넌트가 **SgtFloatingCamera** 또는 **SgtFloatingObject** 컴포넌트의 속도를 추적하고 UI **Text** 요소에 속도를 표시하는 방법을 보여줍니다.

## Floating Orbit

**SgtFloatingOrbit** 컴포넌트를 소행성에 추가하는 방법을 보여줍니다. **ParentPoint** 설정은 별 주위를 도는 데 사용됩니다.

## Floating Orbit Visual

**SgtFloatingOrbitVisual** 컴포넌트를 사용하여 궤도의 시각적 고리를 그리는 방법을 보여줍니다. **SgtFloatingOrbit.Visual** 필드에서도 이 컴포넌트를 설정해야 합니다.

## Floating Spawner(Sphere)

**SgtFloatingSpawnerSphere** 컴포넌트를 **SgtFloatingObject** 컴포넌트와 함께 추가할 수 있는 방법을 보여줍니다. **SgtFloatingCamera**가 지정된 범위(**Range**) 내에 들어오면 Sphere 분포를 사용하여 지정한 프리팹을 생성합니다.

## Floating Spawner(Ring)

**SgtFloatingObject** 컴포넌트와 함께 **SgtFloatingSpawnerRing** 컴포넌트를 추가하는 방법을 보여줍니다. **SgtFloatingCamera**가 지정된 범위(**Range**) 내에 들어오면 Ring 분포를 사용하여 지정한 프리팹을 생성합니다.

## Floating Spawner(Orbit)

**SgtFloatingObject** 컴포넌트와 함께 **SgtFloatingSpawnerOrbit** 컴포넌트를 추가하는 방법을 보여줍니다. **SgtFloatingCamera**가 지정된 범위(**Range**) 내에 들어오면 궤도에서 지정한 프리팹을 생성합니다.

## Floating Root

**SgtFloatingRoot** 컴포넌트를 씬에 추가하는 방법을 보여줍니다. 생성된 모든 프리팹은 구조 개선을 위해 이 게임 오브젝트 아래에 배치됩니다.

## Floating Warp

화면에서 오브젝트를 탭하면 해당 오브젝트로 워프하는 방법을 보여줍니다. 탭핑은 **Canvas/Pin** 게임 오브젝트의 **SgtWarpPin** 컴포넌트에 의해 처리되며, **SgtFloatingTarget** 컴포넌트가 연결된 모든 게임 오브젝트를 선택합니다. 그 다음 워프는 **SgtWarpSmoothstep** 컴포넌트에 처리됩니다.

## Floating Scaler

**SgtFloatingScaler** 컴포넌트(오른쪽)을 사용하여 멀리 있는 오브젝트가 축소되는 속도를 줄이는 방법을 보여줍니다. 고정 축적(왼쪽)을 사용하는 방식은 빛을 발생시키지 않는 단단한 오브젝트에는 적합하지만 빛나는 별의 경우에는 너무 작아서 볼 수 없게 됩니다.

## Star Cluster

**SgtFloatingSpawnerSphere** 컴포넌트를 사용하여 워프할 수 있는 별을 생성하는 방법을 보여줍니다. 이 씬에는 100개의 별이 모두 반경 2광년 내에 생성되고 워프 거리가 100AU인 현실적인 거리를 사용합니다.

## Nested Spawner

**SgtFloatingSpawner__** 컴포넌트가 중첩될 수 있는 방법을 보여주며, 충분히 가까워지면 별이 행성을 생성하도록 합니다.

## Nested Orbits

**SgtFloatingSpawner__** 컴포넌트가 중첩될 수 있는 방법을 보여주며, 충분히 가까워지면 별이 행성을 생성하도록 합니다.

## Third Person

플로팅 오리진 시스템을 사용하여 3인칭 카메라 시스템을 만드는 방법을 보여줍니다. 카메라 상위 궤도 점에 SgtFloatingCamera 컴포넌트를 배치하여 수행됩니다. 워프는 카메라가 아닌 소행성 SgtFloatingObject에서 수행되며 카메라 피벗 포인트는 SgtFloatingFollower 컴포넌트를 사용하여 로켓 우주선을 따르도록 만들어집니다.

## Floating Massive

우주에서 거대하고 멀리 있는 물체(예:은하계)를 시뮬레이션 하는 방법을 보여줍니다. 유니티에서는 은하계 단위의 크기나 거리가 정상적으로 렌더링 될 수 없기 때문에 SgtFloatingObject를 사용할 수 없습니다. 이 문제를 해결하려면 SgtFloatingObject 대신에 **SgtFloatingMassive** 컴포넌트를 사용해야 합니다. 이 컴포넌트는 오브젝트의 크기를 조정하고 위치를 지정하여 개체가 엄청 멀리 있고 거대한 것처럼 보이도록 만들어주지만 실제로는 렌더링 문제를 방지하기 위해 가까이 가져옵니다. 이 컴포넌트는 SgtFloatingObject처럼 동작하지만 **Tranform** 컴포넌트를 가져오며, 수동으로 이동시킬 수 없습니다(예:Rigidbody 없음).