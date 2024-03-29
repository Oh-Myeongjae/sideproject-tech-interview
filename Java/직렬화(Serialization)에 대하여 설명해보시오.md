 ## 직렬화(Serialization)란?

- 자바 직렬화란 자바 시스템 내부에서 사용되는 객체 또는 데이터를 외부의 자바 시스템에서도 사용할 수 있도록 바이트(byte) 형태로 데이터 변환하는 기술과
바이트로 변환된 데이터를 다시 객체로 변환하는 기술(역직렬화)을 아울러서 이야기합니다.
- 시스템적으로 이야기하자면 JVM(Java Virtual Machine 이하 JVM)의 메모리에 상주(힙 또는 스택)되어 있는 객체 데이터를 바이트 형태로 변환하는 기술과
직렬화된 바이트 형태의 데이터를 객체로 변환해서 JVM으로 상주시키는 형태를 같이 이야기합니다.

### 직렬화는 왜 하는것일까요??
- 시스템의 고유 특성과 상관없는 대부분의 시스템에서의 데이터 교환 시 많이 사용됩니다.

### 자바 직렬화의 방법은?
- 자바 직렬화를 하기위한 조건으로 type이 primitive type(기본형 타입)이거나 java.io.Serializable 인터페이스를 상속 받아야 합니다.
- 직렬화는 방법은 java.io.ObjectOutputStream 객체를 이용합니다.

### 자바 직렬화의 장점
- 자바 직렬화는 자바 시스템에서 개발에 최적화되어 있습니다.
- 복잡한 데이터 구조의 클래스의 객체라도 직렬화 기본 조건만 지키면 큰 작업 없이 바로 직렬화를 가능합니다. 물론 역직렬화도 마찬가지입니다.
- 당연하게 보이는 장점 중에 하나지만 데이터 타입이 자동으로 맞춰지기 때문에 관련 부분을 큰 신경을 쓰지 않아도 됩니다.

## 참고자료(우아한형제들)
- ### 직렬화정의와 장점<br>[https://techblog.woowahan.com/2550/]
- ### 직렬화시 고려해야될 <br>[https://techblog.woowahan.com/2551/]
