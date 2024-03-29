#### DI는 의존성 주입의 약자로, 객체들 간의 의존성을 줄이기 위해 사용되는 스프링의 IOC 컨테이너의 구체적 구현 방식을 말한다.<br>

개발코드 부분에서 객체를 생성하는 것이 아니라, 데이터 주입만 담당하는 별도의 공간에서 객체를 생성하고, 데이터 간의 의존성을 주입해 개발코드에서 가져다 쓰면서 의존성을 줄인다.

두 객체 간의 결합도를 낮출수 있고 객체의 유연성을 높여 줍니다.

#### DI의 방법으로 크게 필드 주입, setter 주입, 생성자 주입 3가지가 있는데 이중 생성자 주입을 권장하고 있다.

- 생성자 주입의 장점
  - 객체의 불변성을 확보할 수 있다.
  - 테스트 코드의 작성이 용이해진다.
  - final 키워드를 사용할 수 있고, Lombok과의 결합을 통해 코드를 간결하게 작성할 수 있다.
  - 스프링에 침투적이지 않은 코드를 작성할 수 있다.
  - 순환 참조 에러를 애플리케이션 구동(객체의 생성) 시점에 파악하여 방지할 수 있다.
 
