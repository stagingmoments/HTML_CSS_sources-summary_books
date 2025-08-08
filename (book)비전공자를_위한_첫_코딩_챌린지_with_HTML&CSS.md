핵심요약
1 클라이언트/서버 구조에서 클라이언트는 요청하고 서버는 응답합니다. HTTP 통신 규약을 이용한다. 이 통신 규약으로 실어 나르는 대상인 문서는 하이퍼텍스트 양식으로 되어 있고, 하이퍼텍스트는 HTML이라는 마크업 언어를 사용해 작성한다. 
2 브라우저는 하이퍼텍스트를 해석해 보여주는 대표적인 클라이언트입니다.
3 HTML은 하이퍼텍스트를 표현하는 마크업 언어로, 웹 페이지에 데이터를 구조적으로 기술하는 데 사용합니다. 
4 하이퍼텍스트는 정해진 순서 없이 참조를 통해 다른 문서에 접근할 수 있는 텍스트입니다. 
5 웹 페이지는 웹에 있는 HTML로 작성된 문서입니다. 
6 웹사이트는 URL 기반으로 인터넷에서 서비스되는 웹 페이지 집합입니다.
7 WWW는 World Wide Web의 약자입니다. 웹이라고 부릅니다. 

HTML 기본구조
<!DOCTYPE html>  : HTML5를 사용한다고 알려준다.
head 태그 : head 태그는 표시되지 않는다. 대신 페이지 정보(메타 데이터)를 제공한다.
title 태그: HTML 문서제목을 표현합니다. 예제에서는  my first page로 지정되어 있습니다. 따라서 웹 페이지 상단에 타이틀이 생성됩니다.
meta 태그 : 메타 데이터를 알려주는 태그입니다. 
<meta name=“description” content=“”> : 검색엔진에서 검색된 사이트명 바로 밑에 있는 설명 글이라고 생각하면 된다. 
<meta name=“viewport” content=“width=device-width, initial-scale=1”> : 요소를 볼 수 있는 화면이다. 브라우저가 사용자에게 스크롤 기능을 제공해 가능한 것이다.  

Vs code 에서 단축키 ctrl+/로 주석을 처리할 수 있습니다. 

HTML정보를 MDN, W3School에서 찾아 보세요. 스택오버플로(stackoverflow.com)를 사용하자. 

CH4. 태그로 웹 페이지 만들기
4.1 태그 이해하기 - 태그 표시하는 방법은 두 가지.
<태그명> 요소 </태그명> 
<태그명 요소 > : img, input, link

4.2 대표적인 태그 알아보기
h : 제목 태그, 별도의 줄바꿈 없이 자동으로 줄이 바뀜, 숫자가 커질수록 글자 크기가 작아짐(소제목으로 갈수록 덜 강조함)
html 한페이지에서 h1태그는 한 번만 사용하기
h 태그는제모을 나타내는 코드이므로 문단 처음에 배치하기
검색 엔진에 사용되는 태그이므로 검색어를 고려하기
h1~6 순서대로 사용하기 (권장 사항)

br, p, div, span
break, 줄바꿈, 한 문단에서 줄을 바꿈, 줄바꿈이 1번 일어남
paragraph, 문단, 문단을 나눔, 줄바꿈이 2번 일어남
division, 영역 나눔, 페이지 안에서 영역을 나눔, 줄바꿈이 1번 일어남
br이랑 미묘하게 같으면서도 다른것이 <br />은 자체로만 쓰이고 태그가 나오면 거기서 바로 줄을 바꾸게 되지만, <div> 영역 </div> 는시작과 끝에 대한 태그가 같이 세트로 움직이며 영역안에 있는 부분을 기준으로 앞과 뒤 모두 한줄씩 띄워주는 기능을 한다. 
span, 범위, 줄바꿈을 하지 않은 채 글꼴, 색상, 여백 등을 조절, 줄바꿈이 일어나지 않음

link
<link rel = “속성“ href = “파일 경로”>
예시: <link rel=“stylesheet” href=“style.css”>
stylesheet 즉 CSS 속성을 가진 파일과 연결(관계)한다는 의미입니다.
href=“style.css”는 style.css 파일을 링크합니다. 즉, 현재 파일에서 외부에 있는 자원인 style.css 파일을 스타일시트 관계로 연결시켜 사용한다는 뜻입니다. 

a 태그: href 속성을사용해 링크로 이동할 수 있습니다. 
<a href=“https://google.com”>visit google</a>
visit google 글자를 누르면 구글페이지로 이동된다. 

img
<img src=“경로“ alt=“설명” width=“폭“ height=”높이“>
src:source  이미지 경로
alt: alternative(대체하다)의 약자, 이미지 설명하는 문구
width: 이미지 가로 크기, height: 이미지 세로 크기
*html파일과 같은 폴더에 ~~.img파일이 있어야 제대로 실행된다.
 
form
<form action="myform.html">
    <label for="fname">First name:</label> 
    <input type="text" id="fname">
    <label for="lname">Last name:</label>
    <input type="text" id="lname">
    <input type="submit">
  </form>

<form> form 요소 태그 </form>

form태그: 제출 버튼을 눌렀을 때 입력값을 처리할 대상을 지정해준다. 위의 코드에서는 form 태그의action 속성을 이용해 myform.html로 이동하라고 지정했다. 
input태그: 사용자가 데이터를 입력하는 영역을 결정한다. 대표 속성은 다음과 같다.
type: input 태그의 속성을 결정한다.  값으로는 text(텍스트 입력), checkbox(체크박스), password(패스워드), date(날짜) 등이 올 수 있다. 
Id: input의 이름을 지정해주는 역할을 한다. 

label 태그: input 태그에 라벨지를 붙여준다고 생각하면 된다. label 을 사용하면 시각장애인이 폼을 음성으로 들을 수 있다. 
for: label이 설명하는 input등의 id를 지정한다. 

button 
button 태그는 클릭할 버튼을 만들 때 사용한다. 버튼 태그 안에는 텍스트나 이미지 같은 요소를 삽입할 수 있다. 
<button type=“속성값“>설명</button>
type: 버튼 종류를 지정한다. button, submit, reset등을 지정할 수 있다. 
설명: 버튼에 노출되는 문구이다.

ol, ui, li
목록을 표시하는 리스트 태그로는 ol, ul 태그가 있다. ol태그는 ordered list의약자입니다. 즉 순서가 있는 리스트를 뜻한다. ul 태그는 unordered list의 약자이다. 즉 순서가 없는 리스트를 뜻한다. 

## Ch5. Html 특징 정복하기
SEO를 위해서 메타태그가 작성이 필수적이다. 웹 크롤러 혹은 봇이 이 정보들을 수집하기 때문이다.

에멧 단축키: vscode 를 실행하고 느낌표 !를 치고 잠시 기다리면 다음 사지노가 같은 선택지가 생깁니다. 이 중에 첫번재를 선택하고 enter를누르면 HTML기본 구조가 자동 완성된다. 

HTML 태그에는 시맨틱 태그와 비시맨틱 태그로 구분할 수 있다. 
시맨틱 태그: 검색 봇이 읽을 수 있는 문서 구조를 작성하는 데 사용한다. 
Hh1, p, form, label 등 지금까지  배운 대부분 태그가 여기 해당한다. HTML5 에서는 header, nav, aside, section, article, footer 등 레이아웃과 관련된 태그들이 새로 추가되었다. 

비시맨틱 태그: 요소에 대하여 어떤 설명도 하지 않는 태그이다. div, span 등이 있다. 

챕터 7부터 시작해도 될 듯. 오늘 안에 마무리 하는 것 목표로 해보자.
## Ch.7 CSS가 뭐지?
1 Html 자체에서 style 태그를 통해서 일괄적으로 스타일을 지정해주는 방법이 있고, 
2 .css 파일에서 원하는 스타일을 입력한 다음 <head> </head>에서 
링크를 통하여 스타일시트 관계로 연결해서 사용하는 두 가지 방법이 있는데 길고 체계적인 css 스타일을 적용하려면 후자를 택해야 한다. 
