[Git 명령어]

* Fork

- 상대방의 remote repository(github..) 에서 프로젝트 전체를 복사하여 나의 remote repository로 통째로 옮기는 것을 말한다.

* clone

- fork 된 (예를들어, 다른사람의 프로젝트) 파일들은 지금 remote repository에 있는데 그걸 내 컴퓨터로 그대로 옮겨오는 것, 복사하는 것을 말한다.

git clone [repository 주소 (https, ssh 등)]

* branch

- 컴퓨터공학의 용어들은 나무의 구성요소들에서 유래된 경우가 많은데 root, chunk, 그리고 이야기할 branch가 있다.
- 파일들을 관리할 때 git의 branch없이 단순히 파일을 관리한다고 생각해보자. 
  

  파일1 => 파일2 => 파일3      => 파일4       => 파일5
                 => 파일3-고객 => 파일3-고객2    
  

  파일1 => 파일2 => 파일3 까지 왔는데 파일3에서 고객에게 배포해야하는 새로운 버전의 파일이 필요하다고 가정해보자.
  그럼 파일3에서 파일3-고객이라는 분기를 새로 만들어 파일들을 관리할 수 있다.
  
  이러다가 파일3-고객2와 파일5를 합쳐야 한다면? 합치는거 자체로 엄청 불편할 것이다.

  요럴 때를 위해 고안하여 나온 것이 branch다. 
  파일 관리말고도 test용 파일을 따로 만들어 관리한다는 등 여러 상황에서 직접 다양한 분기를 만들어 사용할 수 있다.
  이런 작업을 수월하게 해주는데 도와주는 명령어를 git branch, branch라 한다.

- git branch 관련 명령어

- git branch:
컴퓨터에 있는 모든 branch 확인

- git checkout [branch명]
해당 branch로 내 소속을 옮김. 사실 바라보는 걸 옮기는 거긴 한데,

등등

git branch : branch 확인 
[커밋 메세지 컨벤션]
나만 이해할 수 있는 메세지는 남들은 이해하지 못하고, 나중에는 나마저도 이해할 수 없는 메세지로 남는다.

커밋 메시지의 컨벤션을 지켜야 하는 이유는 다른 사람의 커밋 메시지를 빠르고 정확하게 이해하기 위해서이다. 이는 프로젝트의 효율성과 직접적으로 연결된다.

AngularJS Commit Message Conventions을 예로 들자면

<type>(<scope>): <subject> => 제목(간단 요약)
<BLANK LINE> => 빈칸
<body> => 내용
<BLANK LINE> => 빈칸
<footer> => 주요 변경 사항, 이슈 해결 사항

첫 줄엔 변경 내용을 한 줄로 요약한다. 
<type> : 
feat (feature) : 기능 추가/수정 등
fix (bug fix) : 버그 수정
docs (documentation) : 문서 수정
style (formatting, missing semi colons, …) : 스타일 변경 (형식, 세미콜론 누락 등)
refactor : 리팩토링
test (when adding missing tests) : 테스트
chore (maintain) : 빌드, 패키지 관련 (업데이트 등)

<subject : >
- 첫 글자를 소문자로 쓴다
- 마지막에 . 을 쓰지 않는다.
- 명령형으로 쓰고, 현재형으로 적는다. (change(O) → changed(X), changes(X))
- 변경 사항을 간단하게 한줄로 요약해서 적는다.

=> 파일 및 폴더 추가
docs : 자기 소개 파일 추가

[fork, pull request를 하고 느낀점]
지금까지 내가 진행한걸 정리하자면,

1. 진호님의 프로젝트는 fork해서 내 remote repository로 옮김.
2. 내 remote repository에 있는 진호님의 프로젝트 복사본을 내 컴퓨터로 복사함.
3. 내 컴퓨터에 있는 진호님의 프로젝트 복사본은 기본적으로 master라는 분기를 따르고 있었는데 내가 그 프로젝트에 새로운 분기는 besttomato 를 설정함.
4. besttomato 분기 안에서 새로운 폴더를 만들고 readme 파일을 만듦.
5. besttomato 분기에 속해 있는 파일과 폴더를 add와 commit을 통해 내 local repository에 옮김 

이때 commit 메세지는 docs : 자기 소개 파일 추가였음.

6. 그 다음 내 remote repository에 있는 프로젝트에 내 local repository에 있던 besttomato 분기에 속해 있는 폴더와 파일들을 push 함.
7. push하고 나서 진호님의 본래 프로젝트에 내 besttomato 분기에 있는 파일들을 pull request를 함. 이때 메세지는 위에 커밋 컨벤션의 형식을 따름.

느낀점 : 처음 해봐서 그런지 너무 복잡했다. 내 컴퓨터 갔다가 깃허브 갔다가 다시 옮겼다가 붙였다가 승인했다가, 정말 어지러웠다. 단지 2시간으로 git의 모든 걸 마스터하기에는 부족하다고 생각해서 나중에 추가공부로 생활코딩의 지옥에서 온 git을 봐서 조금 더 공부하고 싶다.