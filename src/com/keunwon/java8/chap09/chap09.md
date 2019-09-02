# 디폴트 메소드

- 자바 8에서는 호환성을 유지하면서 API를 바꿀 수 있도록 새로운 기능인 디폴트 메소드를 제공한다.
```java
public interface Sized {
    int size();
    
    default boolean isEmpty() {  // 디폴트 메소드
        return size() == 0;
    }
}
```
- Sized 인터페이스를 구현하는 모든 클래스는 isEmpty의 구현도 상속받는다.

## 추상 클래스, 인터페이스 차이점
- 클래스는 하나의 추상 클래스만 상속받을 수 있지만 인터페이스는 여러 개 구현할 수 있다.
- 추상 클래스는 인스턴스 변수로 공통 상태를 가질 수 있다. 하지만 인터페이스는 인스턴스 변수를 가질 수 없다.

## 다른 클래스나 인터페이스로부터 같은 시그니처를 갖는 메소드를 상속받을 때 규칙
- 클래스가 항상 이긴다.
- 서브 인터페이스가 이긴다.
- 여러 인터페이스를 상속받는 클래스가 명시적으로 디폴드 메소드를 오버라이드하고 호출해야 한다.