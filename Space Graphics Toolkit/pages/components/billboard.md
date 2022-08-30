# 빌보드(Billboard)

## SgtBillboard

이 컴포넌트는 현재 게임 오브젝트를 항상 카메라를 바라보도록 하는 빌보드로 바꿉니다.

이 기능은 **SpriteRenderer** 또는 **SgtFlare**(플레어 기능) 컴포넌트와 함께 사용할 수 있습니다.

#### RollWithCamera : bool

카메라가 롤링 회전을 한다면 이 빌보드도 함께 롤링 회전을 할지 결정합니다.

#### AvoidClipping : bool

빌보드가 극단적인 각도에서 잘려 보이지 않는 경우 이 설정을 활성화하면 됩니다.

## SgtFastBillboard

이 컴포넌트는 현재 게임 오브젝트를 렌더링 카메라 방향으로 회전시킵니다.

#### RollWithCamera : bool

카메라가 롤링 회전을 한다면 이 빌보드도 함께 롤링 회전을 할지 결정합니다.

#### AvoidClipping : bool

빌보드가 극단적인 각도에서 잘려 보이지 않는 경우 이 설정을 활성화하면 됩니다.

#### Instances : static LinkedList\<SgtFastBillboard>

이 컴포넌트의 모든 활성화된 인스턴스를 저장합니다.

## SgtFastBillboardManager

이것을 통해서 모든 SgtFastBillboard가 업데이드됩니다.

#### Instances : static LinkedList\<SgtFastBillboard>

이 컴포넌트의 모든 활성화된 인스턴스를 저장합니다.

