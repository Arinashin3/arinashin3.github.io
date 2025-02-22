# SVN 실습 - Local 환경

사용 Tools : TortoiseSVN-1.14.3

1. 파일 다운로드
   1.14.3버전으로 다운로드, 기본값으로 설치한다.
   Tools = TortoiseSVN-1.14.3.29387-x64-svn-1.14.2.msi


2. 폴더 작업
   E://svn//gusiya.com 경로 디렉터리를 생성한다.
   생성한 폴더에서 우클릭 후, TortoiseSVN > Create repository here > OK
   SVN Checkout > Checkout Directory: E:\svn\gusiya.com  > OK


3. 다음 사항 확인
   (확인이 안될 경우, 재부팅)
   gusiya.com 폴더 아이콘 초록색 체크
   At Revision:0


4. 저장소에 데이터 넣기
   Revision 상태 확인하기
   TortoiseSVN > Refo-Browser

바탕화면에 폴더 생성, 이미지파일 5개 넣기
TortoiseSVN > Import

Revision 상태 재확인하기
TortoiseSVN > Refo-Browser


5. 저장소 내용 불러오기
   폴더생성
   E:\svn\gusiya.com.1
   gusiya.com.1우클릭, SVN Checkout > OK
   폴더에 들어가면 저장된 내용이 들어간것을 볼수있음


6. 저장소 갱신(Update), 저장소에 등록(Commit)
   gusiya.com.1 폴더에 이미지 2개를 추가한다.
   폴더에 들어간후 우클릭, SVN Commit > 새로 넣은 파일 2개 체크 > OK
