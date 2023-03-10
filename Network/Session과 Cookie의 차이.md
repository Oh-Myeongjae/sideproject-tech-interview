### 쿠키와 세션을 사용하는 이유

HTTP프로토콜의 특징이자 약점을 보완하기 위해서 사용한다.

HTTP 프로토콜의 특징

1. Connectionless 프로토콜(비연결 지향)

- 클라이언트가 서버에 요청(Request)을 했을 때, 그 요청에 맞는 응답(Response)을 보낸 후 연결을 끊는 처리방식이다.

2. Sataeless 프로토콜

- 커넥션을 끊는 순간 클라이언트와 서버의 통신이 끝나며 상태 정보는 유지하지 않는 특성이 있다.

> 서버와 클라이언트가 통신을 할 때 통신이 연속적으로 이어지지 않고 한 번 통신이 되면 끊어진다.

## 쿠키(Cookie)
- HTTP의 일종으로 사용자가 어떠한 웹 사이트를 방문한 경우, 그 사이트가 사용하고 있는 서버에서 **사용자의 컴퓨터가 저장하는 작은 기록 파일 정보**이다.
- HTTP에서 클라이언트의 상태 정보를 클라이언트의 PC에 저장하였다가 **필요시 정보를 참조하거나 재사용할 수 있다.**

#### 사용 예시
1. 방문 사이트에서 로그인 시, "아이디와 비밀번호를 저장하시겠습니까?"
2. 팝업창을 통해 "오늘 이 창을 다시 보지 않기" 체크

## 세션(Session)
- 일정 시간 동안 같은 사용자(브라우저)로부터 들어오는 일련의 요구를 하나의 상태로 보고, 그 상태를 유지시키는 기술이다.
- **방문자가 웹 서버에 접속해 있는 상태를 하나의 단위로 보고 그것을 세션이라고 한다.**

#### 사용 예시
- 화면을 이동해도 로그인이 풀리지 않고 로그아웃하기 전까지 유지

## 쿠키와 세션의 차이
1. **사용자의 정보가 저장되는 위치가 다르다.**
   - 쿠키는 서버의 자원을 전혀 사용하지 않는다.
   - 세션은 서버의 자원을 사용한다. 
2. **보안**
   - 쿠키는 클라이언트 로컬에 저장되기 때문에 변질되거나 request에서 스니핑 당할 우려가 있어서 보안에 취약하다.
   - 세션은 쿠키를 이용해서 session-id만 저장하고 그것으로 구분하여 서버에서 처리하기 때문에 비교적 보안성이 높다.
3. **라이프 사이클**
   - 쿠키도 만료기간이 있지만 파일로 저장되기 때문에 브라우저를 종료해도 정보가 유지될 수 있다. 또한 만료기간을 따로 지정해 쿠키를 삭제할 때까지 유지할 수도 있다.
   - 세션도 만료기간을 정할 수 있지만, 브라우저가 종료되면 만료기간에 상관없이 삭제된다
4. **속도**
   - 쿠키는 쿠키에 정보가 있기 때문에 서버에 요청 시 속도가 빠르다
   - 세션은 정보가 서버에 있기 때문에 처리가 요구되어 비교적 느린 속도를 낸다.
