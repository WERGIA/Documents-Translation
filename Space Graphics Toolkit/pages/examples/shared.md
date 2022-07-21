# 공유(Shared)

### Stars

기본 배경이 되는 별을 렌더링하는 방법을 보여줍니다. **SgtBackgroundMesh** 컴포넌트를 사용해서 수행되며, 이는 추가 셰이더로 텍스처링할 수 있는 빌보드 쿼드로 구성되는 구체를 생성합니다. 그런 다음 **CwFollow** 컴포넌트를 사용하여 카메라에 붙일 수 있으므로 항상 배경에 나타납니다.

### Clouds

**SgtBackgroundMesh** 컴포넌트가 구름 배경을 만들기 위해 구름 텍스처와 함께 더 큰 쿼드와 다른 머티리얼을 가질 수 있는 방법을 보여줍니다.

### Camera Controls

**SgtCameraMove** 및 **SgtCameraLook** 컴포넌트를 카메라에 추가하는 방법을 보여줍니다. 이를 통해 일반적인 자유-비행(freeflight) 카메라 스타일로 카메라를 이동하고 회전할 수 있습니다.

### Rigidbody Controls

**SgtCameraMove** 컴포넌트의 **Target** 설정을 사용하여 카메라 대신 소행성 **Rigidbody**를 제어하는 방법을 보여줍니다. 그러면 **TargetRotation** 설정을 사용하여 제어 입력을 기반으로 회전할 수 있습니다.

### Procedural Spin + Scale

여러 소행성을 추가하고 **SgtProcedualSpin** 및 **SgtProceduralScale** 컴포넌트를 사용하여 소행성에 다양성을 추가하는 방법을 보여줍니다. Rigidbodies를 사용하는 경우에는 **SgtProceduralTorque** 컴포넌트를 사용해야 합니다.

### Newtonian Gravity

**SgtGravitySource** 및 **SgtGravityReceiver** 컴포넌트를 결합하여 씬에 뉴턴 중력을 추가하는 방법을 보여줍니다. **SgtProceduralForce** 컴포넌트는 소행성이 궤도를 돌 수 있도록 초기 속도를 제공하는데 사용됩니다.

### Planet Gravity

**Procedural Spin** + **Scale** 및 **Newtonian Gravity** 데모 씬을 결합하는 방법을 보여줍니다.

### Simple Orbit

**SgtSimpleOrbit** 컴포넌트를 사용하여 게임 오브젝트가 서로 궤도를 돌도록 하는 방법을 보여줍니다.

### Shadow Layer

SGT 그림자가 씬의 일반 불투명 개체에 적용되는 방법을 보여줍니다. SgtShadowLayer 컴포넌트를 추가하여 수행됩니다.