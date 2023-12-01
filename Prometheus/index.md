# Prometheus

prometheus는 메트릭을 수집하여 시각화, 경고, 기록하는 오픈소스 모니터링 툴이다.

초기에는 SoundCloud에 의해 빌드되었으나 현재는 Cloud Native Computing Foundation 산하 프로젝트로 들어가게 되었다.</br></br>


## 특징

## 아키텍쳐

## 기능
 - TSDB
   Prometheus는 모든 데이터를 시계열로 저장한다.
   
   
 - 강력한 쿼리
   시계열 데이터를 실시간으로 검색하고 집계할수있도록 PromQL이라는 기능적 쿼리 언어를 사용한다.

   
 - 시각화
   Grafana를 이용하여 Prometheus의 대시보드를 만들 수 있다.

   
 - 간단한 운영
   Prometheus는 Command-Line과 Config File만으로 설정할 수 있다.
   > Command-Line : 시스템 매개변수(스토리지 위치, 디스크와 메모리에 보관할 데이터 양 등)을 정의하는데 사용된다.</br>
   > Config File  : 스크래핑 작업과 인스턴스 및 파일 로드 규칙 등을 정의하는데 사용된다.

   
 - 스토리지
   기본적으로 로컬 저장소이 사용되지만 선택적으로 원격 저장소를 사용할 수도 있다.

   

 - 경고
 - 확장성

출처 : https://prometheus.io/
