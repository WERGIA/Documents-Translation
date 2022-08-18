# 고리(Ring)

## SgtRing

이 컴포넌트를 사용하면 고리를 렌더할 수 있습니다(예: 행성의 고리, 강착원반).

이 고리는 행성 주변에 배치될 때, 개선된 깊이 정렬 동작으로 절반으로 나누어집니다.

#### SourceMaterial : Material

이 컴포넌트를 렌더하는 데 사용되는 머티리얼입니다.

> **NOTE** - 이 머티리얼은 **Space Graphics Toolkit/Ring** 셰이더를 사용해야 합니다. 일반 셰이더는 사용할 수 없습니다.

#### Color : Color

고리의 전반적인 색입니다.

#### Brightness : float

**Color.rgb** 값에 곱해지는 값입니다.

#### MainTex : Texture

고리에 적용되는 텍스처입니다.

#### RadiusInner : float

로컬 스페이스에서 고리의 내부 경계의 반지름입니다.

#### RadiusOuter : float

로컬 스페이스에서 고리의 외부 경계의 반지름입니다.

#### Split : bool

이 고리를 행성에 대해 개선된 깊이 정렬을 통해서 두 부분으로 나눌지를 결정합니다.

#### SortDistance : float

로컬 스페이스에서 고리가 그려질 정렬 순서 지점을 설정할 수 있습니다.

이것은 투명한 가스 행성 주변에 있는 고리에 개선된 깊이 정렬을 사용할 때 쓸 수 있습니다. 이 값은 **RadiusOuter** 값과 비슷해야 하며 행성의 크기에 따라 더 커질 수도 있습니다.

