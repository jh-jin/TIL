
# 서블릿 컨테이너

## 웹 애플리케이션 서버의 역할
* 웹 애플리케이션 서버는 클라이언트와 서버 간의 소켓 통신에 필요한 TCP/IP 연결 관리와 HTTP 프로토콜 해석 등의 네트워크 기반 작업을 추상화해 일종의 실행 환경을 제공합니다.
* 이런 실핸 환경에서 웹 프로그램을 작성하는 프로그래머는 웹 애플리케이션 서버에서 제공하는 요청, 응답이라는 개념 위에서 구현을 시작합니다.
* 따라서 웹 프로그래머는 TCP/IP 연결을 직접 생성하고 HTTP 프로토콜을 해석하는 과정을 생략해 웹을 쉽게 구현할 수 있습니다.

## 서블릿 컨테이너
* 엄밀하게 말해 웹 애플리케이션 서버는 Java EE 명세를 만족시키는 Java 구현체를 의미하지만, 웹 프로그래밍을 위한 미들웨어라는 개념이 일반화되면서 자바 이외의 프로그래밍 언어로 작성한 서버도 비슷한 역할을 하면 웹 애플리케이션 서버라고 부릅니다.
* 스프링 처럼 여려 경량 프레임워크가 인기를 얻고 널리사용 되고 있습니다. 경량 프레임워크도 Java EE 정의 중 웹 애플리케이션 기술 위에서 동작하는 것이 일반적이며, **이런 웹 애플리케이션 기술에 대한 구현체가 바로 서블릿 컨테이너 입니다.**
* 서블릿 컨테이너는 웹 애플리케이션 서버중에서 HTTP 요청을 받아 차리하는 기초 역할을 맡고 있습니다.
* 대부분의 웹 프레임워크가 제공하는 기능은 서블릿 컨테이너 위에서 동작하는 서블릿, 필터, 이벤트 리스너 등을 적절히 조합해 구현한 것입니다. 따라서 웹 프레임워크로 작성한 웹 애플리케이션은 결국 서블릿 컨테이너 위에서 동작합니다.
* 서블릿 컨테이너의 주요 목표는 서블릿을 동작시킨 데 있습니다. 