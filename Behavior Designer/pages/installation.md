# 설치

비헤이비어 디자이너를 임포트한 후에 상단 메뉴바의 Tools에서 접근할 수 있습니다. 다운로드 페이지에 있는 런타임 소스 코드 패키지를 가져와서 런타임 소스 코드에 접근할 수 있습니다. **이 패키지를 추출하기 전에 비헤이비어 디자이너 폴더를 삭제했는지 확인하십시오. 그렇지 않으면 컴파일 오류가 발생합니다.**

UWP(Universal Windows Platform)용 비헤이비어 디자이너를 컴파일하려면 컴파일된 DLL 대신 런타임 소스 코드를 사용해야 합니다. 컴파일 설정을 변경할 필요는 없습니다. 비헤이비어 디자이너는 .NET Core가 활성화된 상테에서 컴파일할 수 있습니다.

UWP 앱을 실행하려고 하면 태스크를 찾을 수 없다는 오류가 표시될 수 있습니다. 이 문제를 해결하기 위해서는 `TaskUtility.GetTypesWithinAssembly`(TaskUtility.cs 안에 있는) 내의 다음 줄을 변경해야합니다:

```csharp
 loadedAssemblies = GetStorageFileAssemblies(typeName).Result;
```

변경 : 

```csharp
loadedAssemblies = new List();
loadedAssemblies.Add("Assembly-CSharp");
```

이렇게 하면 앱 안에서 Unity의 C# 어셈블리를 찾을 수 있게 됩니다.

IL2CPP를 사용하여 프로젝트를 빌드하는 경우에는 찾을 수 없는 기본 생성자와 관련된 `MissingMethodException`이 발생할 수 있습니다. 이 문제는 다음 방법 중 하나를 수행하여 해결할 수 있습니다.

- 런타임 소스 패키지 임포트
- [스트리핑 레벨을 '낮음'으로 변경](https://docs.unity3d.com/kr/2018.4/Manual/ManagedCodeStripping.html)
- link.xml 파일에 누락된 클래스 추가