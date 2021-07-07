# Java 8

## 함수를 새로운 값의 형식으로 추가
멀티코어에서 병렬 프로그래밍을 활용할 수 있는 스트림과 연계될 수 있도록 함수를 만들었다.

<br/>

함수를 값처럼 취급한다고 했을 때 어떤 장점이 있는지?

자바 프로그램에서 조작할 수 있는 값은 int, double 등의 기본값이 있다. 그리고 객체(객체의 참조)의 값이 있다.

<br/>

왜 함수가 필요할까?

프로그래밍 언어의 핵심은 값을 바꾸는 것이다. 프로그래밍 언어에서 전달할 수 있는 값을 일급(first-class)값(또는 시민)이라고 부른다. 그리고 전달할 수 없는 구조체는 이급 시민이다. 자바의 기본형과 참조형 값은 일급 자바 시민이지만 메서드, 클래스 등은 이급 시민에 해당한다. 

<br/>

메서드와 클래스 그 자체로 값이 되는게 중요할까?

그렇다, 메서드를 일급 시민으로 만들면 프로그래밍에 유용하게 활용할 수 있다. 따라서 자바 8에는 메서드를 일급값으로 사용할 수 있는 기능을 추가했다. → 메서드 참조(method reference)

<br/>

### 메서드 참조(method reference)
`::` → '이 메서드를 값으로 사용하라'는 의미

<br/>

`예`

```java
File[] hiddenFiles = new File(".").listFiles(new FileFilter() {
    public boolean accept(File file) {
        return file.isHidden();
    }
});
```
자바 8 이전까지는 File의 isHidden 메서드를 전달하려면, 참조할 수 있는 FileFilter 객체로 isHidden 메서드 감싼 다음 전달해야 했다.

<br/>

```java
File[] hiddenFiles = new File(".").listFiles(File::isHidden);
```
자바 8에서는 메서드 참조 :: 문법을 이용해서 직접 isHidden 함수를 전달할 수 있다.