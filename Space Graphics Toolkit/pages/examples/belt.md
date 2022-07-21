# 소행성 벨트(Belt)

## Belt

뛰어난 성능으로 궤도를 도는 수천 개의 빌보드 소행성을 렌더링하는 방법을 보여줍니다. **SgtBeltSimple** 컴포넌트와 **Space Graphics Toolkit / Belt_Opaque** 셰이더를 사용하는 머티리얼을 사용하여 수행됩니다.

### Lighting

Belt 머티리얼의 Lighting 설정을 활성화하여 소행성에 조명을 추가하는 방법을 보여줍니다. 거기에 SgtBeltLightingTex 컴포넌트를 추가하여 원하는 대로 라이팅 그라디언트를 제어할 수 있습니다. 메인 씬 조명에 SgtLight 컴포넌트를 추가해야 함을 명심하십시오.

### Color

**SgtBeltSimple** 컴포넌트의 **AsteroidColors** 그라디언트를 사용하여 일부 소행성에 색조를 추가하는 방법을 보여줍니다.

## Additive

Belt 머티리얼을 **Space Graphics Toolkit / Belt_Additive** 셰이더로 변경하여 투명한 별을 렌더링할 수 있는 방법을 보여줍니다.

### Power RGB

Belt 머티리얼의 **POWER RGB** 설정을 활성화하여 색상이 추가된 별에 더 적합하게 만드는 방법을 보여줍니다.

## Custom

벨트의 소행성 데이터를 수동으로 수정할 수 있는 방법을 보여줍니다. **SgtBelt__** 컴포넌트를 찾아서 컨텍스트 메뉴(⋮ 버튼)를 열고 **Make Editable Copy** 옵션을 선택하여 수행됩니다. 그러면 **SgtBeltCustom** 컴포넌트가 부착된 새 게임 오브젝트가 생성되고 모든 절차적 소행성 데이터를 **Astroids** 목록에 복사하여 수동으로 수정할 수 있습니다. 코드에서 이 목록을 수정하는 경우 나중에 **DirtyMesh()** 메서드를 수동으로 호출해야 합니다.