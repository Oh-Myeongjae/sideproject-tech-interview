- 함수 A, B가 있고, A 안에서 B를 호출했다고 가정했을때 호출한 함수는 A고, 호출된 함수는 B가 된다.

- #### 블럭/논블럭은 간단히 말해서 호출된 함수가 호출한 함수에게 제어권을 건네주는 유무의 차이라고 볼 수 있다.
  - Blocking : 함수 B는 내 할 일을 다 마칠 때까지 제어권을 가지고 있는다. A는 B가 다 마칠 때까지 기다려야 한다.
  - Non-blocking : 함수 B는 할 일을 마치지 않았어도 A에게 제어권을 바로 넘겨준다. A는 B를 기다리면서도 다른 일을 진행할 수 있다.

- #### 동기/비동기는 일을 수행 중인 동시성에 주목하면 된다.
  - Synchronous : 함수 A는 함수 B가 일을 하는 중에 기다리면서, 현재 상태가 어떤지 계속 체크한다.
  - Asynchronous : 함수 B의 수행 상태를 B 혼자 직접 신경쓰면서 처리한다. (Callback)

- #### 상황에 따라서 이 4가지는 조합적으로 사용될수 있다.
  - 블럭/동기
  - 블럭/비동기
  - 논블럭/동기
  - 논블럭/비동기

- # 참고자료
[http://homoefficio.github.io/2017/02/19/Blocking-NonBlocking-Synchronous-Asynchronous/](http://homoefficio.github.io/2017/02/19/Blocking-NonBlocking-Synchronous-Asynchronous/)
