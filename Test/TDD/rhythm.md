## TDD 리듬
1. 재빨리 테스트를 하나 추가한다.
   1. 마음속에 있는 오퍼레이션이 코드에 어떤 식으로 나타나길 원하는지 생각해보라. 올바른 답을 얻기 위해 필요한 모든 요소를 포함시켜 원하는 인터페이스를 개발하라.
        - 오퍼레이션 : 보통 메서드와 비슷한 의미로 쓰이며 객체가 수행할 수 있는 연산을 의미. 언어가 다형성을 지원할 경우 오퍼레이션은 여러 메서드를 가질 수 있다.
2. 모든 테스트를 실행하고 새로 추가한 것이 실패하는지 확인한다.
3. 코드를 조금 바꾼다.
   1. 무엇보다 중요한 것은 빨리 초록 막대를 보는 것이다.
      - 가짜로 구현하기 : 상수를 반환하게 만들고 진짜 코드를 얻을 때까지 단계적으로 상수를 변수로 바꾸어 간다
      - 명백학 구현 사용하기 : 실제 구현을 입력한다
4. 모든 테스트를 실행하고 전부 성공하는지 확인한다.
5. 리팩토링을 통해 중복을 제거한다.
   1. 시스템이 작동하므로 직전에 저질렀던 중복을 제거하고 초록 막대로 되돌리자.

<br/>
---
<br/>

출처
- Test-Driven Development : By Example - 켄트 벡