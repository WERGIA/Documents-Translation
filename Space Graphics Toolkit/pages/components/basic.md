# 기본(Basic)

## SgtShape

이것은 모든 볼류메트릭 셰입(shapes)를 위한 기본 클래스입니다. 이펙트가 표시되는 영역을 정의하는 데 사용될 수 있습니다.

#### float GetDensity(Vector3 worldPoint)

0..1 사이값을 반환합니다. 1인 경우 내부를 가득 채웁니다.

## SgtShapeBox

이 컴포넌트를 사용하면 다른 컴포넌트에서 볼륨에 국한된 작업을 수행하는 데 사용할 수 있는 상자 모양을 정의할 수 있습니다.

#### Extents : Vector3

박스의 최소/최대 크기입니다.

#### Ease : SgtEase.Type

최소 및 최대 밀도 사이에서의 전환 스타일입니다.

#### Sharpness : float

모양 내부에서 밀도의 증가가 얼마나 빠르게 이루어지는지를 결정합니다.

