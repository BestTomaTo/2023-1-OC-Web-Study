git branch와 push, fork 복기
fast-forward, 3 ways 전략 복기하기

과제 리뷰
1. 본인 핸들명의 fork
2. 본인 핸들명 디렉토리
3. 브랜치 만들고 다시 push해서 pull request 신청

['HTML'의 등장]

1. 하이퍼텍스트, HTML 
논문 주석을 쉽게 만들 수 없을까? => 하이퍼링크 비스무리를 만듦.
하이퍼텍스트를 이용하여 이 문서, 저 문서 연결하다 보니 연결망이 거미줄 비슷하네? => WEB이 탄생함

2. HTML의 두 축 Tag, Attribute
HTML은 홈페이지의 뼈대다. 이 뼈대는 Tag와 Attribute라는 두개의 큰 축으로 만들 수 있다.

2-1. html의 기본구조
아무리 길더라도 html은 다음의 네가지 태그를 이용하여 문서의 시작과 끝을 알린다.

<!doctype> : 문서 유형을 지정하는 선언문.
<html> ~ </html> : html 문서의 시작과 끝을 나타냄.
<head> ~ </head> 
    : HEAD는 이 웹사이트에 대한 정보를 컴퓨터(브라우져)에게 주는 거다.
    실제로 화면에 보이는 부분은 아니다. 마치 홈페이지의 정보를 담고 있는 
    꼬리표라 보면 될 것 같다.

    <META> 정보에 대한 정보 : 메타 인지에 대한 어원을 찾아 보면 쉽다.

    <meta name='keywords' content='키워드를 입력합니다.'>
    
<body> ~ </body> : 실제로 웹 브라우져에 나타낼 내용을 담는다.
    <h1> 헤드가 아니라 하이라이트다. 검색엔진에게 정보를 주곤 한다.
    검색엔진은 큰 제목 밑에 부연설명할 거리들을 이 하이라이트에서 뽑아온다.

[html 만들어보기]

1. <html>, <head>, <body>

<h1> : 하이라이트 태그, html 문서상에서 어느 부분이 중요한지 표시하는 역할
<ul> : unordered list, list 즉, 자료 구조긴 한데 순서 표시 없이 단순 나열 할때 사용
    <u = underline> : 밑줄 태그 / <strong> : 강조 태그 / <span style = background> 형광팬 칠할 때 사용 / <i = italic> : 글자 기울기

2. table에 대해 알아보기

1. <table>	테이블을 만든다.
2. <tr>	테이블의 행(가로 한줄)을 만든다
3. <td>	테이블의 열을 만든다.
4. <th>	테이블(표)의 헤드 부분(자동으로 가운데 정렬,  굵게 적용)
5. <caption>	테이블 이름 표시
6. <thead>	테이블의 헤더 영역 지정
7. <hbody>	테이블의 바디 영역 지정

ex) : 2x2표
<table>
    <thead>
    </thead>

    <tbody>
        <tr>
            <td></td>
            <td></td>
        </tr>

        <tr>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>

3. 입력박스는 <input>



