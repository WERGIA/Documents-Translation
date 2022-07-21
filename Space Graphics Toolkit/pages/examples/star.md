# 항성(Star)

## Star Shader

절차적으로 애니메이션된 항성을 만드는 방법을 보여줍니다. 구체 오브젝트의 머티리얼에 사용되는 SGT / Star 셰이더를 사용하여 수행됩니다.

### Flow

셰이더의 **Flow** 설정을 사용하여 항성의 표면이 다른 방향으로 흐르도록 하는 방법을 보여줍니다. 알파 채널에 흐름의 양을 저장하는 flow **텍스처**를 설정하여 수행됩니다. 이 텍스처는 정방형(원통형) 투영을 사용해야 합니다.

### Sunspots

셰이더의 Sunspots 설정을 사용하여 표면에 어둡고 밝은 점을 추가하는 방법을 보여줍니다. 밝기 변화를 저장하는 흑점 텍스처를 설정하여 수행됩니다. 여기서 회색(128)은 변화가 없고 흰색(255)는 더 밝으며 검정색(0)은 더 어둡습니다. 이 텍스처는 정방형(원통형) 투영을 사용해야 합니다.

### Rim

셰이더의 Rim Color 및 Rim Power 설정을 사용하여 별의 가장자리가 나타나는 방식을 제어하는 방법을 보여줍니다.