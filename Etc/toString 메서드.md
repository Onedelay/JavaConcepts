## toString 메서드

`toString()` 메서드는 모두 클래스 인스턴스의 데이터를 문자열로 반환하는 메서드이다. 이 메서드를 클래스에서 정의하는 것은 개발자 간의 약속이라고 할 수 있다. 원래 `toString()`은 java.lang 패키지의 클래스에서 다음과 같이 정의된 메서드이다. 그리고 `클래스 이름@해시값`의 형태로 문자열을 반환한다.

> ★ Note : 해시값은 Java가(?) 인스턴스에 임의의 값을 부여한 것.

```java
public class Object {
    // 중략
    public String toString() {
        return getClass().getName() + "@" + Integer.toHexString(hashCode());
    }
    // 중략
}
```

 Java의 모든 클래스는 `Object` 클래스를 상속받는다. 이때 `toString()` 메서드를 재정의하면 '`Object` 클래스의 `toString()` 메서드를 오버라이드 했다' 라고 한다. 이때 자바의 메서드를 오버라이드할 때는 **클래스의 접근 제한을 바꿀 수 없다.**  항상 `public`으로 정의해야 한다. 그런데 클래스에서 `toString()`메서드를 오버라이드할 때는 클래스의 특성이나 인스턴스의 상태를 나타내는 적절한 문자열을 반환하는 것이 좋다. 