<Week 1>
<인터넷의 구조>
1. URI (Uniform Resource Identifier)
인터넷에 있는 자원을 나타내는 주소, 일종의 꼬리표다. URI는 꼬리표의 상위 개념이다. 참고로 인터넷에 있는 자원은 웹 리소스, 디렉토리, 등등 컴퓨터의 모든 것을 포함한다. 큰 하위범주로 URL과 URN을 가지고 있다.

2. URL (Uniform Resource Location)
네트워크 상에서 자원이 어디 있는지를 알려주기 위한 규약이다. 자원을 나타내는 꼬리표인데 어떻게 이 자원을 가져올지 이 자원이 위치를 나타내는 꼬리표이다. (대강 느낌은 어느 프로토콜을 따르고 무슨 IP에 위치해 있는가?) URL은 단순히 웹 사이트 주소 뿐만 아니라 컴퓨터 네트워크상의 모두를 나타낼 수 있다. 흔히 웹 사이트 주소로 알고 있지만, 웹 사이트 주소뿐만 아니라 컴퓨터 네트워크상의 자원을 모두 나타낼 수 있다.

기본적인 골격은 이렇다.
scheme://<user>:<password>@<host>:<port>/<url-path>
지정된 scheme에 따라 표현방법이 다를 수 있다.

흔히 사용하는 HTTP URL의 scheme은 다음과 같다.
http://<host>:<port>/<path>?<searchpart>

1. 제일 앞 자원에 접근할 방법을 정의해둔 프로토콜의 이름을 적는다.
흔히 알고 있는 http, gopher, telnet, ftp, usenet 등등
2. 프로토콜 이름 다음에는 프로토콜 이름을 구분하는 구분자인 :을 적는다. :)
3. 만약 IP혹은 Domain name 정보가 필요한 프로토콜이라면 :다음에 //을 적는다.

    예1) http://www.somehost.com/a.gif
    예2) mailto:somebody@mail.somehost.com (IP정보가 필요없는 프로토콜)

 3. URN (Uniform Resource Name)   
그 자원이 위치해 있는 공간 대신에 이름으로 자원을 찾는 방법이다. URL의 꼬리표가 '이런 통신규약을 사용하니 이런 방법으로 가져올건데 서울 사는 naver 소속에 위치함' 이거라면 urn은 'naver a통로에 있는 전형진' 이런식으로 직접 찾는 느낌이다. 어떻게 자원을 가져올지 방법은 나타나 있지 않고 경로와 자원 자체를 특정하는 느낌이다.

<서버와 클라이언트>

기계의 구조와 원리에 대해 알고 있어야 기계를 잘 다룰 수 있듯이
개발자도 컴퓨터의 각 분야의 원리를 알고 있어야 효과적으로 개발할 수 있다.
# 1주차 - (1)
# 서버와 클라이언트
### 게임 속의 서버와 클라이언트
자.. 인터넷 주소에 대해 알기 전에 우선은 우리가 어떻게 인터넷에서 홈페
이지에 접속하는지 그 과정을 알 필요가 있다.

흔히 우리는 **스타크래프트**를 할 때 렉이 걸리면, 
> 게임이 겁나 느리네, 서버 좀 바꾸자;

라고 한다. 흔히 서버는 서비스를 제공하는 컴퓨터, 클라이언트는 서비스를 받는 컴퓨터이다. 위의 대화에서는 내 컴퓨터가 클라이언트, 블리자드가 서버가 된다.

![](https://velog.velcdn.com/images/besttomato/post/db9d7335-0b09-47dc-b20e-ab4411c579b6/image.png)

서버나 클라이언트는 고정된 칭호가 아니고 역할의 의미이다. 예를 들어 내가 편의점을 운영했을 때 나는 편의점에서는 '사장님'이지만 편의점 앞 국밥집을 가면 나는 '손님'이 된다. 마찬가지로 이 컴퓨터가 지금은 서버 역할을 하지만 나중에 클라이언트 역할을 할 수 있다. 


<Week 2>
<git의 명령어>

기본적으로 깃과 깃허브는 4가지의 영역을 가지고 있다.
깃의 명령어들을 잘 이해하기 위해서는 각각의 영역들이 무슨 역할을 하는지 알 필요가 있다.

- Working Directory
: 우리가 코딩하는 공간으로 visual studio, visual studio code 등의 프로그램이 포함된다.

- Staging Area
: Local Repository에 commit하기 전까지의 파일들을 모아두는 장소다.
A라는 기술을 만들기 위해서는 a1, a2, a3의 코드들이 필요하다고 해보자.
각각의 코드들은 분량이 너무 많아 한번에 코드를 만들기가 어렵다. 따라서 commit하기 전 파일들을 모아두는 공간과 이를 합쳐주는 공간이 필요한데 그게
staging area이다.

staging area는 합쳐주기뿐만 아니라 원하는 파일만 커밋, 수정할 수 있다.
한 파일에 변경사항 A, B가 있다고 해보자. 내가 실질적인 Git 저장소인 local repository에 변경사항 A, B를 동시에 커밋을 했다. 근데 변경사항 A에 오류가 생겼다는 것을 인지해서 수정하려고 한다. 문제는 local repository에 변경사항 A, B를 동시에 올리는 바람에 A, B 둘다 되돌려서 오류해결을 해야한다.

이런 불편함을 막기 위해 staging area이라는 공간이 생겼다. staging area에서 변경사항 A따로, B따로 올릴 수 있다면 나중에 A에 오류가 생겨도 A만 불러오면 되니까 전보다 편해진거다. 원하는 파일만 커밋할 수 있도록 해주는 것도 staging area의 존재 이유다.

git이 로봇을 만드는 공간이라고 치면,
working directory에서는 자원을 캐서 각각의 부분을 만드는 곳이고,
staging area는 각 부분을 결합하거나 수정하는 작업대이다.

- Local Repository
staging area가 작업대였다면, local repository는 전시회에 출간하기 전 작품들을 모아두는 창고의 성격을 가지고 있다. 여기서 우리는 remote repository로 push 할 수 있는데 push는 전시회에 전시한다는 의미로 생각하면 된다.

- Remote Repository
전시회장이다. github가 관리하는 공식 repository 저장소다!
local은 내 컴퓨터에 있는 저장소인데 remote repository에 push를 하면 다른 사람들이 내 파일을 볼 수 있게 된다.

=========================================================================

1. add
 
git add 명령어는 내가 변경한 파일들을 staging area에 모아두고 싶을 때, 다시 말하면 working directory에서 staging area로 파일들을 보내고 싶을 때 사용한다. git add는 staging area에만 파일을 올릴뿐 Git 저장소에 실질적인 영향을 미치지는 않는다. 

2. commit

git commit 명령어는 staging area에 있는 파일들을 local repository에 옮기고 싶을 때 사용한다. staging area에서 파일들을 수정하고 묶는 작업이 끝났다면 local repository에 옮기고 옮긴 파일들은 remote repository로, 깃허브에 올릴 수 있게 된다.

git add로 수많은 변경사항들을 저장한 다음, commit으로 이름을 붙이고 한번에 repository로 보낼 수 있다. 
add가 변경사항을 하나씩 저장한다면 commit은 묶음으로 한번에 처리하기 위한 느낌이다.

3. push

git push <저장소명> <브랜치명> 이렇게 사용한다. local repository에 있는 파일들을 remote repository로 보낼 때 사용한다. 내 컴퓨터에 있는 파일들을 깃허브로 보낼 때 이 명령어를 사용한다. 전시회 창고에서 진짜 전시회장으로 가는 거다!

4. fetch 와 pull

local repository = 로컬 저장소 = 내 컴퓨터
remote repository = 원격 저장소 = 깃허브

git fetch 원격저장소 이름

fetch는 원격저장소에 있는 변경사항들을 로컬저장소에 가져오기 전에 변경내용을 확인하고 싶은 경우에 사용하는 명령어다. 내가 예전에 깃허브에 A파일을 올렸는데 누가 A파일을 수정했나 내역만 확인할 때 사용한다. 변경한 내용은 가져오지 않고 변경한 내역들만 확인하고 싶을 때 사용한다.

git pull

pull은 원격저장소에 있는 내용들을 로컬저장소로 가져와 합치고 싶을 때 사용한다. 변경한 내용까지 다 가져온다는 의미이다.


git <=> react 
https://github.com/BestTomaTo/react-app.git

리액트를 실행하면 이게 정확히 어떻게 연결되는지 모르겠다. 리액트를 python처럼 코드를 입력하면 그 파일들이 깃으로 가는건지 역할을 잘 모르겠다.