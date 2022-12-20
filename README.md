# Front
## 1. HTML5
### 1_1. HTML개요
```html
<!DOCTYPE html>
<html lang="ko">
	<head>
		<meta charset="UTF-8">
    <meta name="generator" content="VScode"> 
    <meta name="author" content="yeseo"> 
    <meta name="keywords" content="글자,태그"> 
    <meta name="description" content="이 문서는 글자관련 태그들을 공부하는 문서입니다.">

		<title>글자관련태그</title> <!--title : 페이지의 제목을 나타내는 태그-->
	</head>
	
	<body>
	</body>
	
</html>
```
- \<!DOCTYPE html\> 
  - html문서 형식 선언 : html5형식이라는 걸 알려주기 위함
- \<html lang=”ko”\>
  - html문서의 시작, 끝을 표시해주는 태그
  - lang : 이 페이지가 어느 나라 언어로 되어있는 지 표시
- \<head\> 머리부
  - 해당 문서의 각종 정보와 제목, 설명 및 스크립트, 스타일 시트 내용 작성
  - \<meta\>, \<title\>, \<link\>, \<style\>, \<script\>
  - \<meta\>
     - 해당 html문서의 정보를 기술하는 태그
     [참고] 검색엔진에 전달
     - generator : 이 문서를 생성한 프로그램
     - author : 이 문서의 저자
  - \<title\>
     - 페이지의 제목을 나타내는 태그
- \<body\> 몸체부
  - 화면상에 출력해서 보여주고자 하는 모든 정보/내용들을 작성하는 부분
### 1_2. 글자 관련 태그
- h관련 태그 (h1~h6)
  - 한 줄 단위로 영역 차지 : br로 줄바꿈해주지 않아도 됨
  - 존재하지 않는 태그 사용시 : 일반글꼴로 취급
- 줄 바꿈 / 구분 줄
  - \<br\> : 문장의 줄 바꾸기(개행)
  - \<hr\> : 페이지에 가로로 밑줄을 만들어줌
- 문단을 나누는 태그 
  - p 태그
    - 줄바꿈하고자 한다면 별도의 태그 작성 \<br\>
    - 공백은 한 개의 공백만을 표시 => \&nbps; 기호문구 기술하여 여러개의 공백 입력
  - pre 태그
    - 시작태그부터 종료태그까지 입력된 내용을 그대로 표현
    - 줄바꿈, 여러개의 공백 바로 표현 가능
- 그 밖의 글자를 다루는 태그
  - 일반 글꼴 : 태그로 감사지 않은 텍스트
  - b 태그 : 글자를 굵게 표시하는 태그
  - strong 태그 : 글자를 굵게 표시하는 태그 + 스크린리더
  - u 태그 : 글자에 밑줄이 그어지는 태그
  - s 태그 : 글자에 취소선을 넣어주는 태그
  - em 태그 : 글자를 기울여서 표시하는 태그
  - i 태그 : 글자를 기울여서 표시하는 태그
  - mark 태그 : 형광펜 효과를 주는 태그
  - small 태그 : 글자를 작게 표시해주는 태그
  - sub 태그 : 기본글자에 아래첨자를 나타내는 태그
  - sup 태그 : 기본글자에 윗첨자를 나타내는 태그
  - abbr 태그 : 약어에 사용하며 태그 위에 마우스를 올려놓으면 툴팁 형태로 출력
    ```html
    <abbr title="Internet Of Things">IOT</abbr>란 각종 사물에 센서와 통신 기능을 내장해 인터넷을 연결하는 기술이다.
    ```
    
    ![제목 없음](https://user-images.githubusercontent.com/115604544/207537852-29425343-86ad-4eac-8f58-a635c5bbce66.png)

- 글자 관련 태그 응용 (중첩해서 사용 가능)
  ```html
  <b><em>굵게, 기울여서</em></b> 표현가능하고,
  <s><mark>취소선, 형광펜</mark></s>을 넣어 글자를 강조할 수 있음
  ```
  
  ![Untitled](https://user-images.githubusercontent.com/115604544/207537924-cbb86c80-8dab-455d-a453-619ca9b770e7.png)
### 1_3. 목록 관련 태그
- ul / li 태그 : 순서 없는 목록 태그
  - 불릿 (bullet) 기호 : 채워진원, 빈원, 네모, .. 변경 가능 => CSS 이용하여 수정
  - 중첩 사용 가능
- ol / li 태그 : 순서 있는 목록 태그
  - 기본적으로 1부터 시작하는 숫자값
  - type 속성값 : 1(default), A, a, i, I
  - start 속성:  시작값 변경
  - reversed 속성 : 역순으로 표기
- dl 태그 : 설명과 관련된 목록 태그 (주로 용어에 대해 정의할 때 사용)
  ```html
  <dl>
      <dt>* 이곳은 제목을 작성하는 곳</dt>
      <dd>- 여기에 해당 설명을 작성하는 곳</dd> 
      <dd>- 여러줄 작성 가능</dd>
  </dl>
  ```
  
  ![Untitled](https://user-images.githubusercontent.com/115604544/207538828-7b46b543-7965-4d63-93ea-fde77112e2c6.png)

  => dd 태그는 한 탭 들여써짐
### 1_4. 표 관련 태그
- 표
  - 웹 문서에서 자료를 정리할 때 자주 사용
  - 행과 열로 이루어져있고, 행과 열이 만나는 지점을 “셀”이라고 함
- table태그 : 기본적인 표를 생성해주는 태그
  - tr태그 : 표의 한 행을 나타내는 태그
  - th태그 : 표의 제목 셀을 나타내는 태그 ⇒ 글자 굵게, 가운데 정렬
  - td태그 : 표의 일반 셀을 나타내는 태그
- border 속성 : 표의 테두리 두께
- caption태그: 테이블 제목을 추가해주는 태그 (기본 위치 테이블 위 중앙)
- figure 관련 태그 (<figure></figure> / <figcaption></figcaption>)
  - 테이블의 설명 또는 이미지의 설명을 표현할 때 주로 사용
  - 작성하는 위치에 따라 위치 변경
- 표의 행과 열을 합치는 속성
  - 셀 (th, td) 태그의 속성을 이용하여 행 또는 열을 합칠 수 있음
  - colspan=”2” : 2개의 열 합치기 (가로로 두개의 셀 합치기)
  - rowspan=”2” : 2개의 행 햅치기 (세로로 두개의 셀 합치기)
- 테이블 내 구조 나누기 : thead / tbody / tfoot 태그
### 1_5. 이미지 관련 태그
```html
<img scr="삽입하고자하는 이미지의 경로" [alt=”이미지설명문구” width=”가로길이(px/%) height="세로길이(px/%)]">
```
- alt 속성

  ![Untitled](https://user-images.githubusercontent.com/115604544/207542390-c328274d-19bc-43ee-9f23-4f9e2bfb9cbf.png)

  - 사진의 경로가 잘못되었거나 이미지를 제대로 표현할 수 없는 경우 대체 텍스트의 용도
  - 시각장애인들을 위한 스크린리더 (화면낭독기)에서 이미지를 읽어주는 설명 문구
- width, height 속성
  - 이미지의 가로, 세로 길이 조정 가능
  - 고정길이 (px), 가변길이 (%)로 지정 => 단위 생략시 기본값 px
  - 고정길이 (px) : 화면 사이즈가 조정되어도 이미지의 크기 변동 없음
  - 가변길이 (%) : 화면 사이즈 또는 부모요소 사이즈에 따라 이미지의 크기도 같이 변동
### 1_6. 멀티미디어 관련 태그
- 오디오 관련 태그
  ```html
  <audio src=”” controls autoplay loop></audio>
  ```
  - src : 오디오 경로
  - controls : 재생도구 출력 여부
  - autoplay : 자동재생여부 지정 (크롬 x, IE o)
  - loop : 반복재생여부 지정
- 비디오 관련 태그
  ```html
  <video src="" controls autoplay loop width="" height="" poster="썸네일 이미지 경로"></video>
  ```
### 1_7. 입력 양식 및 폼 관련 태그
#### 1_7_1. 폼 관련 태그
```html
<form action=”” method=””></form>
```
- form태그 내에 submit 버튼 클릭시 해당 form안에 작성된 사용자가 입력한 값들을 서버로 넘기면서 요청하는 역할 수행
- action 속성 : 해당 form에 사용자가 입력한 값들을 전달하면서 요청할 서버의 경로 제시
- method 속성 : 요청 전송 방식을 지정하는 속성
  - get방식 (기본값)
      - 사용자가 입력한 값들이 요청시 url에 노출되는 방식
      - 전달값에 대한 크기 제한 있음
  - post방식
      - 사용자가 입력한 값들이 요청시 url에 노출되지 않는 방식
      - 크기 제한 없음
- 사용자가 입력한 값들은 항상 key=value 세트로 전달
  ```html
  <form action="search.do" method="post">
      검색어 : <input type="text" name="keyword">
      <input type="submit" value="검색">
  </form>
  ```
  => name 속성으로 key값 제시
- fieldset 태그 : 그룹을 묶는 태그   
  legend 태그 : 해당 그룹의 제목을 붙이는 태그
#### 1_7_2. 입력 양식 관련 태그
- input 태그 : 사용자에게 값을 입력받을 수 있는 텍스트상자 또는 체크박스 등을 만들 수 있음
  - text 관련 input태그 타입
    - type=”text”
      - 한 줄 짜리 텍스트를 입력할 수 있는 텍스트상자 (type 속성의 기본값)
      - \<label  for=”id이름”>\</label> : label을 클릭하는 것만으로 해당 id를 가진 입력 양식에 입력 가능
      - placeholder : 사용자 입력 전 입력 창 표시 글
      - maxlength : 사용자가 입력할 수 있는 글자수 제한
    - type=“password” : 사용자가 입력한 값이 노출이 안되도록 할 수 있는 텍스트 상자
    - type=”search” : 입력 후 x버튼 생김
    - type=”url” : url형식에 맞는지 (http://가 들어가있는지) 내부적으로 유효성 체크 (아니면 제출 불가)
    - type=”email” : email형식에 맞는지 내부적으로 유효성 체크
    - type=”tel” : 숫자키 입력창 뜸 (모바일에서만)
  - 숫자 관련 input태그 타입
    - type=”number”
      - 숫자값만 작성 가능한 텍스트 상자
      - 스핀박스가 표시됨 (스핀박스 : 위/아래 화살표 버튼)
      - step 속성 : 숫자 간격 지정
    - type=”range” : 슬라이드바를 통해 숫자 지정 가능 (눈금 설정 불가)
  - 날짜 및 시간 관련 input태그 타입
    - type=”date” : 연도, 월, 일 입력 받을 수 있는 텍스트 상자
    - type=”month” : 연도, 월까지만 입력 받을 수 있는 텍스트 상자
    - type = "week" : 연도, 해당 연도의 몇 번째 주인지 입력 받을 수 있는 텍스트 상자
    - type="time" : 오전|오후, 시, 분 입력 받을 수 있는 텍스트 상자
    - type="datetime-local" : 연도, 월, 일, 오전|오후, 시, 분 입력 받을 수 있는 텍스트 상자
  - 라디오버튼 및 체크박스 관련 input태그 타입
    - 라디오버튼 (type=”radio”)
      - 제시한 여러개의 값들 중 오로지 한 개만 선택해야할 때    
        (name속성값이 같은 것들끼리 하나의 그룹으로 지어짐 => 그룹내 한 가지만 선택 가능)
      - 제출 시 현재 선택된 (checked) 라디오버튼의 value값이 넘어감   
        (해당 라디오버튼 선택 시 어떤 값을 넘길 것인지 value값으로 명시)
      - checked 속: 처음에 선택될 값 지정
    - 체크박스 (type=”checkbox”)
      - 제시한 여러 개의 값들 중 여러 개 선택 가능
      - 제출 시 현재 checked된 체크박스의 key=value세트가 넘어감
      - checked 속성: 처음에 선택될 값 지정
  - 추가적인 input태그 타입
    - type=”color”
      - 색상을 선택할 수 있는 input
      - value 속성으로 초기 색상 지정 가능
    - type=”file”
      - 첨부하고자 하는 파일을 선택할 수 있는 input
      - multiple 속성 : 파일 다중 선택 가능 
    - type="hidden” : 특정값을 사용자에게 입력받지 않고, 화면에 노출시키지도 않고 넘기고자 하는 값이 있을 경우
    - input type="submit|reset|button”
    - button [type="submit|reset|button"]
      - type 생략시 기본값 submit
      - CSS를 이용하여 자유롭게 꾸밀 수 있음
- textarea 태그
  - 텍스트 상자이긴 하나 여러줄을 입력할 수 있음
  - style=”resize:none”으로 임의 크기 조정 불가하도록 할 수 있음
- select / option 태그
  - 사용자에게 직접 키보드로 값을 입력받지 않고 제시한 여러개의 옵션들 (목록) 중에 선택
  - 제출 시 현재 선택된 (selected) option 값이 넘어감
  - 각 option에 value 값을 명시하지 않았을 경우 content 영역값이 넘어감
  - value 값 명시했을 경우 value 값이 넘어감
  - select태그에 name속성 지정하여 key값 넘겨줌
  - selected : 기본으로 선택된 값
- datalist 태그
  - 사용자에게 직접 키보드로 값을 입력받을 수도 있고 목록에서 선택할 수도 있음
  - content 영역값 및 value 값 함께 표시 / 선택하면 value 값 나타남
### 1_8. 영역 관련 태그
- 블럭 요소
  - 한 줄 단위로 영역 차지
  - 줄 바꿈이 적용되어 이미 존재하는 태그의 다음 줄에 영역이 잡힘
  - p, pre, div, ...
- 인라인 요소
  - content영역 (내용물)에 해당하는 부분만 영역을 차지하는 요소
  - 줄 바꿈이 적용되지 않아 옆으로 영역이 잡힘
  - 다음 줄로 넘기려면 br태그 작성
  - b, mark, s, img, span, …
- div 태그와 spa n태그의 차이점 1 : 줄바꿈 적용
  - div 태그
    - 블럭요소로 한 줄 단위로 영역 차지 (이미 존재하는 요소 다음줄에 영역 잡힘)
    - style로 테두리, 가로, 세로 길이 지정 가능
  - span 태그 
    - 인라인요소로 content영역만 차지 (줄바꿈이 발생되지 않고 옆으로 배치)
    - 인라인요소에는 대부분 가로, 세로길이 지정 불가
- div 태그와 span 태그의 차이점2 : 영역지정방식
  - div 태그 : 전체 사각형 박스로 영역 지정
  - span 태그 : 각 문장 단위로 영역 지정
- iframe 태그
  - 웹 문서 안에 다른 웹 페이지를 추가하는 태그
  - 우클릭 - 소스코드 복사 - 붙여넣기하면 자동으로 iframe으로 만들어짐
## 2. CSS
### 2_1. CSS 개요
- CSS (Cascading Style Sheets) 란?
  - HTML로 작성된 웹 문서를 꾸미기 위한 기법
- 스타일 기술 방식
  ```css
  선택자{ 스타일속성:값; }
  ```
  - 내부 스타일 방식
    - 현재 문서에 적용시키고자 하는 스타일 정보들을 <head> 머리부 <style>태그 내에 기술
    - 해당 html문서 내에 스타일 정보를 같이 기술
  - 인라인 스타일 방식
    - 스타일을 부여하고자 하는 요소 내에 style 속성을 이용하여 직접 바로 기입하는 방법
  - 외부 스타일 방식
    - 스타일 정보만을 따로 기술하는 .css 외부문서를 만들고 link 태그를 이용하여 연결시켜주는 방식
    ```html
    <link href=”경로” rel=”관계” tyle=”유형”>
    ```
    ```html
    <head>
        <link href="resources/css/02.css" rel="stylesheet" type="text/css">
    </head>
    ```
### 2_2. 선택자
- 선택자 (Selector)란?
  - 특정 html요소를 선택하고자 할 때 사용하는 기능
  - 해당 요소를 선택해서 원하는 “스타일”과 “기능”을 적용시킬 수 있음
- 기본 선택자
  - 모든 (전체) 선택자 : *
    - 현재 문서상 모든 요소들을 다 선택하고자 할 때 사용

    ```css
    * {
        스타일속성:값;
        스타일속성:값;
    }
    ```
  - 태그 선택자 : 태그명
    - 현재 문서상 해당 태그들을 다 선택하고자 할 때 사용
    - 태그명 ,로 나열하여 한꺼번에 스타일 적용 가능

    ```css
    태그명 {
        스타일속성:값;
    }
    ```
  - 아이디 선택자 : #아이디명
    - 현재 문서상 특정 html요소  “딱 하나만”을 선택하고자 할 때 사용
    - 모든 태그에 아이디 부여 가능
    - 해당 요소에 id속성을 이용하여 고유 아이디 값 부여 (중복 불가)

    ```css
    #아이디명 {
        스타일속성:값;
    }
    ```
  - 클래스 선택자 : .클래스명
    - 해당 문서상 원하는 요소 “여러개”를 선택하고자 할 때 사용 (중복 가능)
    - 모든 태그에 클래스 부여 가능
    - class 속성에 “여러개”의 클래스명 나열 가능 (공백으로 연이어줌)

    ```html
    <ul>
        <li class="class1 class2">클래스선택자</li>
    </ul>
    ```
    ```css
    .클래스명 {
        스타일속성:값;
    }
    태그명.클래스명 {
        스타일속성:값;
    }
    ```
- 기타 선택자
  - 속성 선택자
    - 선택하고자하는 요소 내에 작성되어 있는 속성을 이용하여 선택
    - 선택자 뒤에 [] 이용하여 속성과 속성값을 제시하면서 선택
      - 선택자[속성=값]{} : “일치”하는 요소
      - 선택자[속성~=값]{} : 공백을 기준으로 한 단어가 “포함”되어 있는 요소
      - 선택자[속성|=값]{} : -을 기준으로 한 단어로 “시작”하는 요소
      - 선택자[속성^=값]{} : 제시한 값으로 “시작”하는 요소
      - 선택자[속성$=속성값]{} : 제시한 값으로 “끝”나는 요소
      - 선택자[속성*=속성값]{} : 제시한 키워드가 “포함”되어 있는 요소
  - 자손 선택자 / 후손 선택자
    - 많은 요소들이 중첩되면서 작성 가능
    - 자손 : 바로 하위인 요소들 / 후손 : 하위 요소들 전부
    
    ![화면 캡처 2022-12-16 173423](https://user-images.githubusercontent.com/115604544/208057393-864f8757-a3b7-42de-aba9-3a5fc35caa7d.png)

    - 자손 선택자 : >
      - a 요소의 “자손들” 중 b요소만 선택
      ```css
      a>b {
          스타일속성:값;
      }
      ```
    - 후손 선택자 :  (공백)
      - a요소의 “후손들” 중 b요소만 선택

      ```css
      a b{
          스타일속성:값;
      }
      ```
  - 동위 (같은 레벨) 선택자
    - 동위 관계에서 뒤에 위치한 특정 요소를 선택할 때 사용
    - a요소 바로 뒤에 있는 b요소 “하나만” 선택
      ```css
      a+b {
          스타일속성:값;
      }
      ```
    - a요소 뒤에 “모든” b요소 선택
      ```css
      a~b {
          스타일속성:값;
      }
      ```
  - 반응 선택자
    - 사용자의 움직임에 따라 선택되는 선택자
    - 해당 요소에만 적용되기 때문에 다른 요소에 적용하려면 자손/후손/동위 선택자 이용
    - 해당 요소가 클릭되는 순간 스타일 부여
      ```css
      선택자:active{
          스타일속성:값;
      }
      ```
    - 해당 요소에 마우스가 올라가는 순간 스타일 부여
      ```css
      선택자:hover{
          스타일속성:값;
      }
      ```
  - 상태 선택자
    - 요소의 상태에 따라 선택되는 선택자
    - 해당 요소에만 적용되기 때문에 다른 요소에 적용하려면 자손/후손/동위 선택자 이용
    - 체크된 (checked) 상태의 요소에 스타일 부여
      ```css
      선택자:checked{
          스타일속성:값;
      }
    - 초점 (focus)이 맞춰진 input 요소에 스타일 부여
      ```css
      선택자:focus{
          스타일속성:값;
      }
      ```
    - 활성화 (enabled) 되어 있는 요소에 스타일 부여
      ```css
      선택자:enabled{
          스타일속성:값;
      }
      ```
    - 비활성화 (disabled) 되어 있는 요소에 스타일 부여
      ```css
      선택자:disabled{
          스타일속성:값;
      }
      ```
- 선택자 우선순위
  - 기본적으로 css는 위에서부터 아래로 적용 (마지막에 작성된 스타일 반영)
  - 동일한 요소를 다양한 선택자로 스타일 부여했을 경우 작성순서에 상관 없이 우선순위에 따라 적용
  - 태그선택자 → 클래스선택자 → 아이디선택자 → 인라인스타일방식 → !important
  ```html
  <div id="id1" class="class1" style="background:purple">우선순위 테스트</div>
  ```
  ```css
  .class1{
      background:yellowgreen;
      color:white;
  }
  div{
      background:teal !important;
      color:red !important;
      width:200px;
      height:200px;
  }
  ```
### 2_3. 텍스트 스타일
- 글꼴 관련 스타일
	- font-family : 글꼴 지정
		```css
		선택자{ font-family:글꼴명1, 글꼴명2, ...;}
		```
		- 글꼴명 나열시 글꼴명1 적용 안되면 글꼴명2 적용… 다 안되면 브라우저 기본 글꼴 적용
		- 공백이 있는 글꼴명 반드시 (쌍)따옴표로 묶어야 함
	- font-size : 글꼴 크기 변경
		```css
		선택자{ font-size:크기(px|em|%) }
		```
		- px : 고정크기 / em : 가변크기 (배) / % : 가변크기
		- 가변크기 기준 : 상위 요소 글꼴 크기
	- font-weight : 글꼴 굵기 변경
		```css
		선택자 { font-weight:normal|bold|bolder|lighter|100~900(100단위); }
		```
		- bold : 굵은 글꼴 / bolder : 원래 굵기보다 더 굵게
		- 100 : lighter / 500 : normal / 900 : bolder
	- font-style : 텍스트 문구 기울임
		```css
		선택자{ font-style:normal|italic|oblique; }
		```
		- italic : 기울임 글꼴 / oblique : 원래 글자를 기울임
- 텍스트 관련 스타일
	- color : 텍스트의 색상을 지정
		```css
		선택자 {
			color: 색상명|16진수|rgb(x,x,x)|rgba(x,x,x,x)|hsl(x,x,x)|hsla(x,x,x,x);
		}
		```
		=> a : 투명도
		=> h:색상값(0~360), s:채도(%), l:명도(%)
	- text-decoration : 텍스트에 줄을 긋거나 기존의 줄을 없앨 때 사용
		```css
		선택자{
			text-decoration: none|underline|overline|line-through;
		}
		```
	- text-transform : 영문 텍스트의 대소문자 변환 시 사용
		```css
		선택자{
			text-transform : uppercase|lowercase|capitalize;
		}
		```
		- uppercase : 모든 영문자 다 대문자로
		- lowercase : 모든 영문자 다 소문자로
		- capitalize : 영문자를 단어별로 첫 글자만 대문자로
	- text-shadow : 텍스트에 그림자 효과를 줄 때 사용
		```css
		선택자{
			text-shadow : 가로거리(x) 세로거리(y) [번짐정도] [색상];
		}
		```
		=> 오른쪽(양수) / 왼쪽(음수) / 아래(양수) / 위(음수)
		=> 번짐정도 생략시 선명한 그림자 / 색상 생략시 글자색과 동일
		=> ,로 연이어서 여러개의 그림자 부여 가능
	- text-align : 텍스트 정렬할 때 사용
		```css
		선택자{
			text-align:left(기본값)|justify|right|center;
		}
		```
		=> justify : 양쪽 정렬
	- vertical-align : 세로를 기준으로 정렬할 때 사용
		```css
		선택자{
			vertical-align:middle|bottom|top;
		}
		```
		=> 인라인요소에서만 반영
	- text-height : 줄 간격 조정할 때 사용
		```css
		선택자{
			line-height:normal|px|em|%;
		}
		```
- 목록 관련 스타일
	- list-style-type : 불릿기호를 변경시켜줄 때 사용
	- list-style-image : 불릿기호로 이미지를 적용시키고자 할 때 사용
	- list-style-position : 불릿기호의 위치를 조정할 때 사용
		- 순서 없는 목록 (ul)
			```css
			선택자{
				list-style-type : disc(기본값)|circle|square|none;
				list-style-image : url("적용시키고자 하는 이미지의 경로");
				list-style-position : inside|outside(기본값);
			}
			```
		- 순서 있는 목록 (ol)
			```css
			선택자{
				list-style-type : decimal(기본값)|decimal-leading-zero;
				list-style-type : lower-alpha|upper-alpha;
				list-sytle-type : lower-roman|upper-roman;
			}
			```
### 2_4. 배경 스타일
- 배경 색
	- background-color : 배경색 지정하고자 할 때 사용
	- background-clip : 배경을 적용시키고자 하는 범위 지정할 떄 사용
		```css
		선택자{
			background-clip:border-box(기본값)|padding-box|content-box;
		}
		```
- 배경 이미지
	- background-image : 배경에 이미지 설정할 때 사용
			```css
			선택자{
				background-image:url('이미지 경로');
			}
			```
	- background-repeat : 배경 이미지 반복 출력 설정할 때 사용
		```css
		선택자{
			background-repeat:repeat|repeat-x|repeat-y|no-repeat;
		}
		```
		- repeat : 요소에 가득찰 때까지 가로 / 세로 반복 (기본값)
		- repeat-x / repeat-y : 넓이 / 높이만큼 반복
	- background-size : 배경 이미지 크기 조절할 때 사용
		```css
		선택자{
			background-size:auto|contain|cover|px px|% %;
		}
		```
		- auto : 원래 배경 이미지 크기만큼 표시
		- contain : 요소 안으로 이미지가 들어갈 수 있게 확대 / 축소
		- cover : 요소 범위를 이미지가 덮을 수 있게 확대 / 축소
	- background-position
		```css
		선택자{
			background-position:좌/우/가운데 위/아래/가운데|px px|% %;
		}
		```
	- background-attachment : 페이지가 위 아래로 움직여도 배경은 움직이지 않게 고정할 때 사용
		```css
		선택자{
		 	background-attachment:scroll|fixed;
		}
		```
		- scroll (기본값) : 배경 이미지가 움직이게 설정
		- fixed : 배경 이미지가 움직이지 않게 설정
- 변형 관련 스타일 : transform
	- 좌우로 움직이기
		```css
		선택자{
			transform:translateX(단위);
		}
		```
		=> 양수 : 오른쪽 / 음수 : 왼쪽
	- 상하로 움직이기
		```css
		선택자{
			transform:translateY(단위);
		}
		```
		=> 양수 : 아래 / 음수 : 위
	- 대각선으로 움직이기
		```css
		선택자{
			transform:translate(좌우, 위아래);
		}
		```
	- 가로로 확대 축소
		```css
		선택자{
			transform:scaleX(숫자);
		}
		```
		=> 배수 입력
		=> 음수 : 뒤집힘
	- 세로로 확대 축소
		```css
		선택자{
			transform:scaleY(숫자);
		}
		```
		=> 배수 입력
	- 전체 확대 축소
		```css
		선택자{
			transform:scale(가로, 세로);
		}
		```
	- 지정한 각도만큼 회전
		```css
		선택자{
			transform:rotate(각도);
		}
		```
		=> 단위 : deg
	- 지정한 각도만큼 가로로 뒤틀기
		```css
		선택자{
			transform:skewX(각도);
		}
		```
	- 지정한 각도만큼 세로로 뒤틀기
		```css
		선택자{
			transform:skewY(각도);
		}
		```
	- 지정한 각도만큼 전체 뒤틀기
		```css
		선택자{
			transform:skew(가로, 세로);
		}
		```
### 2_5. 레이아웃 스타일
- 여백 및 간격 관련 스타일
	![화면 캡처 2022-12-20 183758](https://user-images.githubusercontent.com/115604544/208634334-0bf8ca78-1bf5-433f-a78b-4a42f13bd877.png)

	- 요소 영역 == content (내용물) + padding (여백) + border (테두리)
	- padding : content 영역과 border 영역 사이의 거리 (여백)를 조절하는 스타일 속성
		```css
		선택자{
			padding : 숫자;
		}
		```
		=> 숫자 1개 제시 : 사방으로 여백 생김   
    숫자 2개 제시 : 위아래 좌우   
    숫자 4개 제시 : 위에서부터 시계방향   
	- margin : 타 요소들 간의 간격을 띄워주고자 할 때 사용
		```css
		선택자{
			margin : 숫자;
		}
		```
		=> 타 요소의 간격과 중첩됨   
		=> margin:auto; 화면의 가운데에 위치
- 테두리 관련 스타일
	```css
	선택자{
		* 테두리 스타일
		border[-위치]-style : none|dotted|dashed|solid|double|groove|ridge|inset|outset;

		* 테두리 두께
		border[-위치]-width : 테두리두께;

		* 테두리 색상
		border[-위치]-color : 테두리색상;

		* 한 번에 지정
		border[-위치] : 두께 스타일 색상;

		* 테두리 두께, 스타일, 색상을 한 큐에 지정
		border[-위치] : 두께 스타일 [색상(생략시 글자색과 동일)];

		* 테두리 모서리를 둥글게
		border[-상하위치-좌우위치]-radius : 숫자;

		* 박스에 그림자 효과
		box-shadow : 가로거리(x) 세로거리(y) 흐림정도 번짐정도 색상;
	}
	```
- 레이아웃 관련 스타일
	- width / height : 기본적으로 내용을 차지하는 content 영역의 가로, 세로 길이를 조절하는 속성
		- 고정크기 (px)
		- 가변크기 (%)
	- display : 화면 배치 방법
		```css
		선택자{
			display:inline|block|inline-block|none;
		}
		```
		- inline : block 요소를 inline 요소로 변경, width와 height 속성은 적용되지 않음
		- inline-block : inline 레벨이면서 content에는 block에 대한 속성 지정 (margin, height, width 설정 가능)
		- block : inline 요소를 block 요소로 변경
		- none : 화면에 표현되지도 않고 공간도 차지하지 않음
- 배치 관련 스타일
	- position
		- 상대위치 (relative)
		- 절대위치 (absolute)
			- 원하는 위치를 지정해 배치
			- 부모 / 조상 요소의 position 속성이 반드시 relative
			- 영역의 정 가운데에 배치
				```css
				선택자{
					margin:auto;
					position:absolute;
					top:0;
					bottom:0;
					left:0;
					right:0;
				}
				```
		- 고정위치 (fixed) : 지정한 위치에 고정 배치
- z-index
	![화면 캡처 2022-12-20 183842](https://user-images.githubusercontent.com/115604544/208634500-c8589313-b162-4e91-88d5-ee8198218d32.png)

	- 요소들을 순서대로 위로 쌓는 속성
	- 부모 / 조상 요소의 position 속성이 반드시 relative
	- 속성 값이 크면 가장 위에 있는 요소, 작으면 밑에 있는 요소
	- 요소들이 화면으로부터 띄워져 있기 때문에 이어서 다른 요소를 넣으려면 <br>로 줄바꿈해줘야함
- visibility : 특정 요소를 보이거나 보이지 않게 하는 스타일 속성
	- visability:hidden은 공간은 차지하고 있지만 화면에 보이지 않음
	- cf) display:none은 공간마저도 사라지게 함
- float : 페이지 내의 요소들을 화면으로부터 띄워서 왼쪽 또는 오른쪽으로 배치하는 속성
	```css
	선택자{
		float : right|left|none;
	}
	```
- clear : float 속성 초기화
	```css
	<br clear="both">
	```
## 3. JavaScript
### 3_1. JavaScript 개요
- 웹 3요소
	- HTML : 웹 문서의 큰 틀 (뼈대)
	- CSS : 스타일 (색상, 디자인, 간격, 배치 등)
	- JavaScript : 웹 문서상에 이벤트가 발생했을 때 실행해야하는 동적인 효과들을 처리
- 스크립트 언어란
	- 프로그램의 동작을 사용자의 요구에 맞게 수행되게끔 해주는 용도
	- 매우 빠르게 배우고 짧은 소스코드로 상호작용되도록 고안됨
- 자바스크립트
	- 웹 브라우저에서 많이 사용되는 "인터프리터 방식"의 스크립트 언어
	- 인터프리터 방식
		- 코드를 한줄씩 한줄씩 읽어가면서 바로 실행하는 방식
		- 실시간으로 텍스트 분석해서 실행됨 ⇒ 코드에 문법 오류가 있으면 그 코드가 실행되는 시점에서 알려줌
- 장단점
	- 장점
		- 컴파일 과정 없이 인터프리터로 코드를 한줄씩 읽어가면서 바로 실행되기 때문에 "수행속도가 빠름”
		- 코드 작성이 간단해서 초보자가 접하기 쉬움 (단순한 구조, 원칙)
			ex) 접근제한자의 개념 없음, 변수 선언시 자료형 정해둘 필요 없음
	- 단점
			- 웹에 특화된 기술임 => 내부에서 제공되는 기능이 다소 제한적
			- html소스코드에서 같이 작성하면 외부에 공개됨 => 보안의 취약점 발생
- 자바스크립트 사용법
	- inline (인라인) 방식
		- 태그 내에 간단 소스코드를 작성하여 실행되게 하는 방법
		```html
		<태그 on이벤트명="해당요소에 해당이벤트 발생시 실행시킬 소스코드">
		```
	- internal (내부) 방식
		- html문서 내에 script 태그를 작성하여 그 안에 소스코드를 작성하는 방법
		- script 태그는 head태그, body태그 어디서든 작성 가능
		```html
		<script>실행할 소스코드 작성</script>
		```
	- external (외부) 방식
		- 별도의 .js 파일로 소스코드를 작성하여 가져다가 실행되게 하는 방법
		```html
		<script src=“경로“ rel="javascript"></script>
		```
- 두 값이 동일한지 비교하는 연산자
	- == : 동등연산자(자료형과 무관하게 실제 값만 일치해도 true)
	- === : 일치연산자(값, 자료형 둘 다 일치해야 true)
### 3_2. 변수와 자료명
- 자바스크립트에서의 자료형
	- 자바스크립트에서는 변수 선언시 따로 자료형을 지정하지 않음
	- var, let, const를 이용해서 변수를 선언하고 아무 값이나 담을 수 있음
	- 특정 값 대입시 그때 그 값에 맞춰서 자료형이 지정됨
	- typeof() : 값의 자료형을 확인하는 연산자
- 자료형의 종류
	- string(문자열) : 홑따옴표 또는 쌍따옴표로 묶여 있는 리터럴
	- number(숫자)
	- boolean(논리값)
	- object(객체) : 배열, 요소, {}, …
		- 배열객체 : [값, 값, …]
		- 요소
			```jsx
			var divEl = document.getElementById(”id명”)
			```
		- {}
			```jsx
			var user = {
				name:"김말똥",
				age:30,
				id:"user01"
			};
			```
			=> key-value 세트로 저장
	- function(함수)
		- 익명 함수 : function() ⇒ 어딘가에 대입될 때 사용
			```jsx
			btn.onclick = function(){ 
				window.alert("버튼 클릭");
			};
			```
			=> 이벤트 발생시 실행할 함수(이벤트 핸들러)
		- 선언적 함수 : function 함수이름()
	- undefined(초기화가 안된 변수)
		```jsx
		var noVal;
		```
- var, let, const의 차이점
	- 변수 선언 방법
		- var
			- 중복 선언 가능
			- 재할당 가능
		- let
			- 중복 선언 불가능
			- 재할당 가능
		- const
			- 중복 선언 불가능
			- 재할당 불가능
			- 상수같은 개념
	- 스코프 (사용가능 범위)
		- var : function[al] scope == 변수가 선언된 “함수영역”내에서 다 사용 가능
			```jsx
			function diffScope(){
				if(true){
						var age = 20; // if 블럭안에서 선언된 변수
				}
				console.log(age);
			}
			```
			=> 변수가 속해 있는 function 안이라면 다 사용 가능
		- let, const : block scope == 변수가 선언된 "블럭{}"내에서만 사용 가능
			```jsx
			function diffScope(){
				if(true){
						let userId = "user01";
						const userPwd = "pass01";
				}
				console.log(userId); // 불가능
				console.log(userPwd); // 불가
			}
			```
- 변수 선언 위치에 따른 전역변수 / 지역변수
	- 전역변수
		- 특정 함수 밖에 선언된 변수
		- 어디서든 다 사용 가능
		- 선언 시 변수명에 var, let, const 붙이지 않으면 특정 함수 내에 있어도 전역변수로 간주
	- 지역변수
		- 지역변수명과 전역변수명이 중복될 경우 => 지역변수 우선시
		- 전역변수에 접근하고자 한다면 window. 또는 this.으로 접근
		- let, const는 window. 또는 this.이 적용되지 않으므로 전역변수명과 지역변수명을 다르게 써야함
### 3_3.데이터입출력
- 자바스크립트 내장 객체
	- window : 브라우저 창이 열릴 때마다 하나씩 만들어지는 객체   
						브라우저 창 안에 존재하는 모든 요소들의 최상위 객체
	- document : 웹 문서마다 하나씩 존재하는 객체
- 데이터 출력하는 구문
	- [window.]alert("브라우저의 알람창에 출력할 문구"); : 내용을 메시지 창에 출력
	- [window.]console.log("브라우저의 콘솔창에 출력할 문구"); : 개발자 도구 화면의 콘솔에 출력
	- document.write("화면상에 출력할 문구");
		- 기존에 화면에 있던 모든 요소들(head에 작성한 내용 포함)이 지워지고 입력한 문구가 나타남
		- 출력할 문구에 html태그가 있을 경우 해석돼서 시각적인 요소로 보여짐
	- 선택한요소.innerHTML|innerText = "요소에 출력할 문구";
		- 자바스크립트에서 특정 요소(element)안의 값(content)을 가지고 온다거나 변경하고자 할 때 innerHTML, innerText 속성에 접근
		```jsx
		console.dir(divEl);
		```
		=> console.dir : 요소객체의 디렉토리 구조(속성들에 대한 정보)를 볼 때
		- innerHTML : html 태그도 같이 보관   
		- innerText : 오로지 텍스트만 보관
- 데이터 입력받는 구문 (변수에 기록 가능)
	- 변수 = [window.]confirm("질문내용");
		- confirm 호출시 "질문내용"과 "확인"/"취소"버튼이 존재하는 브라우저의 알람창 발생
		- 확인 버튼 클릭시 true, 취소 버튼 클릭시 false를 반환
		- boolean값이 반환되기 때문에 if문에 활용 가능
	- 변수 = [window.]prompt("질문내용");
		- prompt호출시 "질문내용"과 입력할 수 있는 "텍스트 상자"와 "확인"/"취소"버튼이 존재하는 브라우저의 알람창 발생
		- 확인 버튼 클릭시 텍스트 상자에 입력되어있는 값을 문자열로 반환, 취소 버튼 클릭시 null을 반환
	- 변수 = 선택한요소.속성(id, className, innerHTML, innerText, ..);
	- 변수 = 선택한input요소.value;
### 3_4. 요소 가져오기 (접근하기)
- 아이디를 이용해서 요소 가져오기
	- document.getElementById(”아이디명”);
	- 선택된 요소객체 1개 반환
	- 선택한 요소의 속성값 가져온다거나 변경 가능
- 태그명을 이용해서 요소 가져오기
	- document.getElementsByTagName("태그명");
	- 선택된 요소객체들이 배열에 담겨서 반환
	- [요소객체, 요소객체, …]
	- 배열.length : 선택된 요소 갯
	- 배열의 인덱스까지 접근 (배열[인덱스])해서 요소객체에서 실행
- name속성값을 이용해서 요소 가져오기
	- document.getElementsByName("name속성값");
	- 선택된 요소들이 담겨있는 배열 반환
	- [요소객체, 요소객체, …]
- 클래스를 이용해서 요소 가져오기
	- document.getElementsByClassName("class속성값");
	- 선택된 요소들이 담겨있는 배열 반환
	- [요소객체, 요소객체, …]
- 선택자를 이용해서 요소 가져오기
	- 내가 원하는 요소 자유롭게 선택
	- document.querySelector("선택자"); : 선택된 요소객체 딱 하나만 반환
	- document.querySelectorAll("선택자") : 선택된 요소객체들이 담겨있는 배열 반환
### 3_5. 문자열과 숫자
- 문자열 관련 기본메소드
	- toUpperCase() : 대문자로
	- toLowerCase() : 소문자로
	- length : 문자열의 길이 (속성값임 ⇒ 메소드x)
	- charAt() : 찾는 위치의 문자 리턴
	- indexOf() : 앞에서부터 찾는 문자의 순번(위치) 리턴 / lastIndexOf() : 뒤에서부터 찾는 문자의 순번 리턴
		- indexOf(”찾는 문자”, 숫자) : 숫자 위치에서부터 탐색
		- 해당 문자가 존재하지 않을 경우 -1 반환
	- substring(시작인데스) / substring(시작, 끝) : 값을 일부분만 리턴 (끝 인덱스 이전까지)
	- split() : 토큰 문자로 분리한 문자열 배열 리턴
- 문자열 관련 html메소드
	- bold() : b태그
	- italics() : i태그
	- small() : small태그
	- sub() : sub태그
	- sup() : sup태그
	- link(”url”) : \<a href=”url”>
- 수학 (숫자) 관련 메소드
	- Math.abs() : 절대값 리턴
	- Math.random() : 임의의 난수발생 리턴(소수점)
	- Math.round() : 반올림처리 후 리턴, 위치 지정 불가
	- Math.floor() : 버림처리 후 리턴, 위치 지정 불가
	- Math.ceil() : 버림처리 후 리턴, 위치 지정 불가
- 문자열과 숫자간의 산술연산 / 형변환
	- 덧셈을 제외한 산술연산시 문자열이 숫자로 자동형변환 된 뒤에 산술연산됨. 단, 문자열에는 숫자만 존재해야함
	- 숫자와 문자를 덧셈 연산하게 되면 문자가 우선되어 숫자를 문자로 변환
	- 강제형변환 (문자열 => 숫자형) : input요소의 value 값은 무조건 string타입 (문자열)이므로 숫자 연산 시 강제 형변환 필
		- Number(문자열)
		- parseInt(문자열)  : 정수로 변환
		- parseFloat(문자열)
### 3_6. 배열
- 배열
	- 변수 선언시 별도의 자료형 지정 x
	- 모든 자료형(숫자, 문자열, 함수, boolean, undefined, 객체)을 하나의 배열 공간에 담을 수 있음
	- 크기 제약 없음
- for in문
	- 배열의 0번 인덱스부터 마지막 인덱스까지 순차적으로 모든 요소에 접근
	- for(let 변수 in 순차적으로접근할배열)
	```jsx
	for(let i in arr){ 
		area1.innerHTML += arr[i] + "<br>";
	}
	```
	=> i : 인덱스수가 순차적으로 담김
- 배열의 선언
	- 크기를 정하지 않은 배열 선언 : const 변수명 = new Array();
	- 크기를 정한 배열 선언 : const 변수명 = new Array(개수);
	- const 변수명 = [];
- 배열의 초기화
	- new 연산자 활용 : const 변수명 = new Array(값1, 값2, …);
	- [ ] 활용 : const 변수명 = [값1, 값2, …];
- 배열에 값 대입
	- 배열[인덱스수] = 값;
	- 인덱스 중간을 건너뛰고 값 대입 가능 : 건너뛴 인덱스는 empty
- 배열 관련 메소드
	- 배열.indexOf(찾고자하는요소)
		- 배열에서 해당 요소가 위치해있는 인덱스 반환
		- 해당 요소를 찾지 못하면 -1 반환
	- 배열.concat(배열, 배열, ...)
		- 배열에 여러개의 배열을 결합하고자 할 때 사용
		- 원본 배열에 영향을 끼치지 않는 메소드
	- 배열.reverse()
		- 배열에 담긴 값들을 역순으로 바꿔주는 메소드
		- 원본 배열에 영향을 끼치는 메소드
	- 배열.sort()
		- 배열 안에 담긴 값들을 정렬시켜주는 메소드 (오름차순)
		- 원본 배열에 영향을 끼치는 메소드
		- 내림차순 정렬 : 오름차순 정렬 후 역순으로 뒤집기
			```jsx
			배열.sort().reverse();
			```
		- 숫자의 경우 숫자 크기대로 정렬하는 것이 아니라 문자열로 바꿔서 정렬하기 때문에 제대로 안됨
			- sort메소드 내의 function에서 양수값 리턴시 두개의 순서가 바뀜
				- 오름차순 : 뒤의 값보다 앞의 값이 클 경우 순서 바꿔야함
						```jsx
						divEl.innerHTML += "오름차순 : " + arr2.sort(function(left, right){
																														return left - right;
																												})";
						```
				- 내림차순 : 앞의 값보다 뒤의 값이 클 경우 순서 바꿔야함
						```jsx
						divEl.innerHTML += "내림차순 : " + arr2.sort(function(left, right){
																														return right - left;
																												});
						```
	- 배열.push(추가할요소) / 배열.pop()
		- 배열.push(추가할요소) : 배열의 맨 뒤에 요소 추가시키고 배열의 크기 반환
		- 배열.pop() : 배열의 맨 뒤 요소 제거시키고 제거된 요소 반환
		- 원본배열에 영향을 끼치는 메소드
	- 배열.unshift(추가할요소) / 배열.shift()
		- 배열.unshift(추가할요소) : 배열의 맨 앞에 요소 추가 후 배열의 크기 반환
		- 배열.shift() : 배열의 맨 앞 요소 제거시키고 제거된 요소 반환
		- 원본 배열에 영향을 끼치는 메소드
	- 배열.slice(시작인덱스, 끝인덱스) / 배열.splice(시작인덱스, 제거수[, 추가할 값])
		- 배열.slice(시작인덱스, 끝인덱스) : 배열로부터 시작인덱스에서부터 끝인덱스까지 추출해주는 메소드
			- 원본 배열에 영향을 끼치지 않는 메소드
		- 배열.splice(시작인덱스, 제거수[, 추가할 값]) : 배열의 요소 추출해서 제거 및 추가
			- 원본 배열에 영향을 끼치는 메소드
	- 배열.toString() / 배열.join([구분자])
		- 배열의 각 인덱스에 담긴 값들을 하나의 "문자열"로 합쳐서 반환
		- 객체를 화면에 출력하면 내부적으로 객체.toString() 호출한 결과가 출력
		- 요소객체는 toString() 정의되어있지 않아 type반환
### 3_7. 함수
- 선언적 함수
	```jsx
	function 함수명([매개변수, 매개변수, ..]){
		해당 함수 호출시 실행할 소스코드;

		[return 결과값;]
	}
	```
- 익명 함수
	- 특정 변수나 속성에 대입되는 함수 제시시 주로 사용 (주로 이벤트 핸들러 작성시 사용)
	- 이벤트 핸들러 : 이벤트속성에 대입되는 function ex) 요소.onclick, window.onload (페이지 로딩 직후 실행)
	```jsx
	변수|속성 = function([매개변수, ..]){
		해당 함수 호출시 실행할 소스코드;

		[return 결과값;]
	};
	```
- 함수의 매개변수
	- 정의해둔 매개변수 갯수보다 더 많이 전달 가능 (오류 안남). 단, 초과된 전달값은 무시됨
	- 정의해둔 매개변수 갯수보다 더 적게 전달 가능 (오류안남) => undefined
	- 매개변수 제시시 자료형 지정x, 선언구문x => 변수명만
- 매개변수 관련 arguments배열
	- 함수 호출시 전달되는 값들은 내부적으로 arguments배열에 담김
	- arguments : 모든 함수마다 내부적으로 하나씩 존재하는 배열 객체
- 매개변수에 this관련 전달하기
	- this : 현재 (이벤트가 발생한) 요소객체
	- this.속성명 : 속성 전달 가능
- 함수의 리턴
	- 일반적인 값 리턴
		```jsx
		function ran(){
			return parseInt(Math.random() * 100 + 1);
		}
		```
	- 익명함수 리턴
		```html
		이름 : <input type="text" id="userName">
		<button onclick="test7()();">실행확인</button>
		```
		=> test7()자리로 익명함수 리턴되므로 () 한번 더 써야 실행됨
		```jsx
		function test7(){
			const inputEl = document.getElementById("userName");
			return function(){
				alert(inputEl.value);
			};
		}
		```
- 스스로 동작 함수
	- 호출 없이 바로 실행
	```jsx
	(function(){
		처리 로직
	})();
	```
### 3_8. 객체
- 객체 선언 및 사용
	```jsx
	변수 = {
		속성명:속성값,
		속성명:속성값,
		...
	};
	```
	- 중괄호{}를 사용해서 생성
	- 중괄호 안에 이 객체에 필요한 속성(property)들 정의
	- 속성명:속성값 의 형태로 정의 (키:밸류)
	- 속성값으로 모든 자료형의 값을 담을 수 있음
	- 자바스크립트에서의 배열 == 자바에서의 컬렉션(ArrayList)   
		자바스크립트에서의 객체 == 자바에서의 컬렉션(HashMap)
	- 속성명에 공백이나 특수문자가 포함될 경우
		- 반드시 문자열로 묶어야함
		- 접근 시 []을 이용한 방법만 가능
	- toString() 따로 정의하지 않으면 화면에 출력시 자료형 출력됨
- 객체의 속성에 접근하는 방법
	- 대괄호를 이용하는 방법 : 객체명["속성명"]
		- 유의할점 : 속성명 반드시 문자열 형태로 제시 (따옴표)
		- 속성명 오타 있을 시 undefined
	- .을 이용하는 방법 : 객체명.속성명
- 객체에서의 반복문
	- 객체가 가지고 있는 모든 속성들에 순차적으로 접근하고자 한다면 반복문 제시
	- for in문만 사용 가능
	- 접근 시 []을 이용한 방법만 가능
	```jsx
	for(let key in game){
		divEl.innerHTML += key + " : " + game[key] + "<br>";
	}
	```
	=> 반복문 돌 때마다 변수에 해당 객체의 순차적으로 접근되는 “속성명”이 차례대로 대입됨 (문자열 형태로)
- 객체의 메소드 속성
	- 객체의 속성 중 함수 자료형인 속성 == 메소드
	- 메소드 내에서 같은 객체 내의 속성에 접근하고자 한다면 this. 붙여야함
  - 객체명.메소드속성명();으로 호출
- in / with
	- in : 객체 내의 해당 속성이 있는지 확인해주는 연산자 (존재하면 true, 아니면 false)
		```jsx
		"속성명" in 객체명;
		```
	- with : 객체의 속성 접근시 객체명 제시하는걸 생략할 수 있음 (코드를 줄여주는 존재)
		```jsx
		with(객체명){
			속성명;
		}
		```
		=> 객체명. 제시할 필요 없음
- 객체의 속성 추가 및 제거
	- 객체에 속성 추가
		```jsx
		객체명.속성명 = "값";
		객체명.속성명 = function(){
				메소드 로직;
				[return 값;]
		};
		```
		=> 해당 속성명이 없으면 생성해주고 있으면 중복 불가하기 때문에 덮어씌워줌
	- 객체의 속성 제거
		```jsx
		delete(객체명.속성명);
		```
- 객체 배열
	- 다량의 데이터 관리
	```jsx
	function test1(){
		const student0 = {name:"김말똥", java:100, oracle:90, html:90, css:60};
		const student1 = {name:"홍길동", java:60, oracle:100, html:80, css:70};
		const student2 = {name:"강개순", java:70, oracle:80, html:100, css:50};
		const student3 = {name:"김개똥", java:100, oracle:60, html:80, css:50};

		const students = [];

		students.push(student0);
		students.push(student1);
		students.push(student2);
		students.push(student3);

		console.log(students);
		console.log(students[0]);
		console.log(students[0].name);

		for(let i in students){
			students[i].javascript = 100;
			students[i].getSum = function(){
				return this.java + this.oracle + this.html + this.css + this.javascript;
			};
			students[i].getAvg = function(){
				return this.getSum() / 5;
			}
		}

		const divEl = document.getElementById("area1");

		for(let i in students){
			divEl.innerHTML += "이름 : " + students[i].name  
											+ ", 총점 : " + students[i].getSum()
										  + ", 평균 : " + students[i].getAvg() + "<br>"; 
		}
	}
	```
- 생성자 함수
	- new 키워드를 이용해서 객체를 생성할 수 있는 함수 (함수명 제시시 첫글자를 대문자로)
	```jsx
	function Student(name, java, oracle, html, css, javascript){
		// 일반속성 정의
		this.name = name;
		this.java = java;
		this.oracle = oracle;
		this.html = html;
		this.css = css;
		this.javascript = javascript;

		// 메소드속성 정의
		this.getSum = function(){
			return this.java + this.oracle + this.html + this.css + this.javascript;
		}

		this.getAvg = function(){
			return this.getSum() / 5;
		}
	}
	```
	```jsx
	function test2(){
		const student0 = {name:"강개순", java:100, oracle:60, html:80, css:50, javascript:100};
		const student1 = new Student("홍길동", 100, 70, 60, 80, 90);
		const student2 = new Student("김말똥", 80, 90, 100, 50, 70);

		const students = [student0, student1, student2];

		console.log(students);

		for(let i in students){
			document.getElementById("area2").innerHTML += "이름 : " + students[i].name + "<br>";
		}
	}
	```
- Date 내장객체
	- 변수 = new Date(); : 현재 날짜 시간
	- 변수 = new Date(년, 월-1, 일);
	- 변수 = new Date(년, 월-1, 일, 시, 분, 초, ms)
		- ms (밀리세컨초) : 1s == 1000ms
	- 메소드
		- getFullYear() : 년도
		- getMonth() : 월 인덱스 (0 : 1월 ~ 11 : 12월)
		- getDate() : 일
		- getDay() : 요일 (0 : 일요일 ~ 6 : 토요일)
		- getHours() : 시간 (0 ~ 23시)
		- getMinutes() : 분 (0 ~ 59 분)
		- getSeconds() : 초
	- 날짜 - 날짜 ⇒ 두 날짜 사이의 밀리세컨초 반환
		- 1s == 1000ms   
			1m == 60s == 60*1000ms   
			1h == 60m == 60*60s == 60*60*1000ms   
			1d == 24h == 24*60m == 24*60*60s == 24*60*60*1000ms
		- 일로 환산 ⇒ (날짜 - 날짜) / (24*60*60*1000)
