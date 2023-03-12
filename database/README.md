# ORM에 대해 설명해주세요.

**orm이란?**

Object Relational Mapping의 약자로 OOP의 객체와 RDB에 쓰이는 데이터인 테이블을 자동으로 매핑하는 것을 말합니다. 원래는 객체와 테이블은 서로 호환되지 않기에 이를 해결하고자 ORM을 사용합니다. ORM은 따로 SQL문을 짤 필요없이 객체를 통해 간접적으로 데이터베이스를 조작할 수 있습니다.

**장점**

- **객체지향** → 클래스의 메서드를 통해 데이터베이스를 조작 가능하여 오로지 객체 모델에만 집중 가능하고 SQL문과 같이 쓰는 선언문, 할당, 종료같은 부수적인 코드가 줄어들며 객체 모델 코드에 집중하기 때문에 가독성이 높아지고 생산성도 함께 높아집니다.
- **재사용, 유지보수, 리팩토링 용이**
- **DBMS 종속성 하락 (종류 : mysql, oracle 등)** → 객체에만 집중할 수 있기 때문에 DBMS를 교체하는 큰 작업에도 리스크가 적고 드는 시간도 줄어듭니다.

**단점**

**ORM이 만능은 아니다.**

- n + 1의 문제, 순환참조(무한 루프) 등의 문제가 생길 수 있기 때문에 설계를 신경써서 해야합니다.
- 대형 SQL문은 속도를 위해 별도 튜닝이 필요하기 때문에 결국은 SQL문을 써야합니다.

**객체 - 관계 간의 불일치**

- 세분성 → 경우에 따라 데이터베이스에 있는 테이블 수보다 더 많은 클래스를 가진 모델이 생길 수 있음.
- 상속성 → RDBMS에는 상속 개념 없음
- 일치 → Java는 객체 식별과 객체 동일성 모두 정의 / RDBMS는 기본키(primary key) 이용하여 동일성 정의
- 연관성 → 객체지향 언어 : 객체 참조하여 연관 / RDBMS : 외래키(foreign key) 사용하여 연관
- 탐색 → Java는 그래프형태로 하나의 연결에서 다른 연결로 이동하여 탐색 / RDBMS는 SQL문을 최소화하고 JOIN을 통해 여러 엔티티를 로드하고 원하는 대상 엔티티 선택하는 방식

**ORM 프레임워크 종류** → JPA/Hibernate(java), Sequelize(Node.js), Django ORM(python)