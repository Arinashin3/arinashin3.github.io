Grafana Datasource
Azure 모니터링

Azure를 Grafana로 모니터링하기 위해 구축하기 시작했다.

가난한 나로써는 유료로 구축하기 어려워서
최대한 무료티어로 올리기위해 일단 무료티어 목록을 보았다..

윈도우랑 리눅스가 따로 적용되는건가..?
![image](https://github.com/Arinashin3/arinashin3.github.io/assets/109202506/9774eb02-218f-4c3c-a8a1-b860ddbdcfe9)

그리고 무료티어 사양..
CPU 1core / Memory 1GB..
리눅스라면 몰라도 이 사양으로 윈도우가 잘 돌아갈지부터가 의문이 든다..
![image](https://github.com/Arinashin3/arinashin3.github.io/assets/109202506/2bd5d316-ed2f-4d64-bbd9-15758206a29f)


일단 VM을 생성해준다.

생각보다 동작이 잘되어 놀랐다.
windows_exporter 먼저 설치부터 시작..

팅겼다..
왤까..? collector에 mssql을 포함해서 그런것인가..?

그래서 Grafana와 Azure를 연동을 하기로 한다.

## Azure 설정

1. Microsoft Entra 관리 센터로 이동한다.
- 아래 그림을 보면 알겠지만 Azure AD가 Microsoft Entra ID로 바뀌었기 때문에 Microsoft Entra 관리 센터로 이동해줘야한다.
![image](https://github.com/Arinashin3/arinashin3.github.io/assets/109202506/a42aaa62-364a-410a-9b80-069dc7ea4c72)

2. ID - 애플리케이션 - 앱 등록을 선택한다.
- 새 등록을 만들고 정보입력 후, 등록을 눌러주면 된다.
- Redirect URL은 선택사항이며 안넣어줘도 된다.
![image](https://github.com/Arinashin3/arinashin3.github.io/assets/109202506/91202a1f-436b-477c-b6aa-67946efc3b14)

// 3. Client Secret을 생성해준다.
// - 앱 생성이 완료되면, 우측의 클라이언트 자격증명 : "인증서 또는 비밀추가"를 선택한다.
// - 새 클라이언트 암호 - 클라이언트 암호를 클릭한다.
// - 클라이언트 암호는 6개월이 Default이며 만료되면 매번 갱신해주어야한다.(최대 2년까지 지정가능)
// ![image](https://github.com/Arinashin3/arinashin3.github.io/assets/109202506/8bb3710b-ac60-4bf5-8fed-4c76750d2db8)

// ![image](https://github.com/Arinashin3/arinashin3.github.io/assets/109202506/7d143f01-6ffe-4eed-ae63-023cc8fdf30c)

다음은 애플리케이션에 IAM을 할당해주어야한다.


참고자료
Azure 설정: https://learn.microsoft.com/en-us/entra/identity-platform/howto-create-service-principal-portal#get-tenant-and-app-id-values-for-signing-in
Grafana 설정: https://grafana.com/docs/grafana/latest/datasources/azure-monitor/
