# 대기(Atmosphere)

## Corona

볼류메트릭 코로나로 기본 별을 만드는 방법을 보여줍니다. **SgtAtmosphere** 컴포넌트를 별에 추가하고 **Space Graphics Toolkit/Atmosphere** 셰이더를 사용한 머티리얼을 **SourceMaterial**로 설정하면 됩니다. 그런 다음 **SgtAtmosphereDepthTex** 컴포넌트를 추가하여 원하는 대로 코로나에 색상을 지정할 수 있습니다.

## Atmosphere

대기 머티리얼의 **Lighting** 설정을 활성화하여 대기에 라이트를 추가하는 방법을 보여줍니다. 그 다음에 **SgtAtmosphereLightingTex** 컴포넌트를 추가하여 원하는 대로 색상을 제어할 수 있습니다. 메인 씬 라이트에 **SgtLight** 컴포넌트를 추가해야 함을 명심하십시오.

### Sunset

**SgtAtmosphereLightingTex** 컴포넌트의 **SunsetSharpnessR/G/B** 설정을 사용하여 행성의 일몰 및 일출 색상을 제어하는 방법을 보여줍니다.

### Scattering

**Atmosphere** 머티리얼의 **Scattering** 설정을 활성화하여 대기 산란을 추가하는 방법을 보여줍니다. 그런 다음 **SgtAtmosphereScatteringTex** 컴포넌트를 추가하여 원하는 대로 색상을 제어할 수 있습니다.

### Customize

UI 요소를 대기 설정에 연결하는 방법을 보여주므로 어떤 설정이 어떤 비주얼을 변경하는지 더 쉽게 확인할 수 있습니다.