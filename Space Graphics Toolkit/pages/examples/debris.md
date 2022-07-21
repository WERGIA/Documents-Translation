# 데브리(Debris)

## Debris Spawner

**SgtDebrisSpawner** 컴포넌트가 카메라 주위에 소행성 프리팹을 생성할 수 있는 방법을 보여줍니다. 이 소행성은 시간이 지남에 따라 무작위로 생성되므로 성능이 일정해야 하며 원하는대로 상호 작용할 수 있습니다. 소행성 위치는 지속되지 않는 점을 염두에 두십시오. 다시 비행하면 새로운 임의의 위치에 있게 됩니다.

### Shape

**SgtShapeSphere** 및 **SgtSphereGroup** 컴포넌트가 결합되어 별 주위에 구 모양을 만드는 방법을 보여줍니다. 그런 다음 shape 그룹은 **SgtDebrisSpawner.SpawnInside** 설정에서 설정되어 별 근터에서 소행성이 더 자주 생성되도록 합니다. 스폰 확률은 shape 그룹에 상대 적인 **SgtDebrisSpawner.Target** 위치를 기반으로 한다는 점에 유의하십시오. 이것은 파편이 충분히 작고 카메라가 그 안에 있는 경우 shape 외부에서 스폰될 수 있음을 의미합니다.

## Debris Grid

**SgtDebrisDebris** 컴포넌트를 사용하여 카메라 주위에 소행성을 절차적으로 생성하는 방법을 보여줍니다. **SgtDebrisSpawner** 컴포넌트와 달리 이 소행성은 영구적인 위치를 보여줍니다. 소행성이 생성된 후 이동하면 업데이트된 위치가 저장되지 않습니다.

### Shape

**SgtDebrisDebris** 컴포넌트의 **Spawn Inside** 설정을 사용하여 파편이 별 또는 Shape group에서 정의한 다른 모양 근처에서만 생성되도록 하는 방법을 보여줍니다.