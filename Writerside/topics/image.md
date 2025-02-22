# Image

Container Image는 애플리케이션 실행에 필요한 프로그램 + 라이브러리 + 운영체제/네트워크 설정 값등을 하나의 객체로 만든 것이다.  
주로 사용되는 OS는 Alpine Linux, Ubuntu, Olacle Linux가 있다.  
그 외에도 Google에서 만든 distroless image가 있다.

distroless 이미지는 애플리케이션 실행에 필요한 프로그램(Go, Python, Java)와 라이브러리 만으로 구성이 되어있으며,  
운영체제가 없기 때문에 이미지 용량이 작고, 쉘이 없기 때문에 보안적으로도 뛰어나다는 장점이 있다.  
패키지 관리자가 없기 때문에 컨테이너 내에 추가적인 소프트웨어를 설치할 수 없다.  
또한, AWS에서는 모든 컨테이너에 쉘이 있다고 생각하기 때문에 distroless 이미지를 배포하면 Health Check를 실패가능성이 있다고한다...

