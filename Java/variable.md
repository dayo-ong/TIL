# 변수

모든 참조형 변수의 크기 : 4byte

<br/>

### 선언위치에 따른 변수의 종류

```java
class Card {
    String kind;                // 멤버변수 - 인스턴스 변수
    int number;                 // 멤버변수 - 인스턴스 변수

    static int width = 100;     // 멤버변수 - 클래스 변수
    static int height = 250;    // 멤버변수 - 클래스 변수

    public int getScore() {
        int point = 5;          // 지역변수
        return number * point;
    }
}
```

**멤버 변수**

클래스 영역에 선언된 변수

**지역변수**

클래스 영역 이외의 영역에 선언된 변수(메서드, 생성자, 초기화 블럭 내부)

<br/>

**클래스 변수**

멤버변수 중 `static`이 붙어있는 변수
- 모든 인스턴스가 공유하는 변수
- 인스턴스를 생성하지 않고 바로 사용할 수 있다 → `클래스이름.클래스변수`
- 클래스가 메모리에 올라갈 때(loading) 생성되어 프로그램이 종료될 때 까지 유지
- `public`을 붙이면 프로그램 내 어디서나 접근할 수 있는 **전역변수** 성격을 갖는다

**인스턴스 변수**

멤버변수 중 `static`이 붙지 않은 변수
- 클래스의 인스턴스를 생성할 떄 만들어진다
- 인스턴스 마다 서로 다른 값을 가질 수 있다



  

<br/>

---

<br/>

출처
- Java의 정석 (남궁 성)