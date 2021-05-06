### 프레임워크 vs 라이브러리

프레임워크 : 개발자가 작성한 코드를 제어하고, 실행

ex) JUnit

- 개발자는 JUnit 룰에 맞춰 테스트 코드를 작성하면 → JUnit이 자신의 라이프 사이클에 맞춰 개발자가 작성한 코드를 호출, 실행 → 제어권을 넘김

라이브러리 : 개발자가 작성한 코드가 직접 제어

ex) JSON parser

- 개발자가 직접 라이브러리를 포함시키고, 직접 호출

<br/>

### 톰캣이 사용자의 요청을 처리하는 방법
톰캣으로 사용자의 요청이 들어오면 그 요청은 우선 톰캣의 큐에 들어간다. 큐에 들어온 요청은 작업을 쉬고 있는 톰캣의 쓰레드가 있을 때 그 쓰레드가 받아서 처리한다.

큐의 기본 사이즈는 100이고, 요청을 처리하는 쓰레드는 기본 200개이다. 쓰레드가 처리하는 양보다 들어오는 요청이 더 많아지면 그때부터 들어오는 요청은 큐에 대기하게 된다. 대기 중인 요청은 당연히 응답 시간도 길어진다. 

큐에 요청이 계속 쌓이다가 큐가 꽉찾을 때 새로운 요청이 들어오면 그 요청부터는 실패하기 시작한다. 또한, 큐에 들어온 요청이 처리되는데 30초를 넘게되면 타임아웃 처리가 된다.

톰캣의 큐 사이즈, 쓰레드 풀, 타임아웃은 모두 변경이 가능하다.

<br/>

---

출처
- [클래스101 강의 - 현직 대기업 개발자 푸와 함께하는 진짜 백엔드 시스템 실무!](https://class101.net/products/T6HT0bUDKIH1V5i3Ji2M)