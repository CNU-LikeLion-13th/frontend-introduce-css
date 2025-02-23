# 방학 과제 2차

**BEM 방법론**

:Block, Element, Modifier

*.header__navigation--navi-text {   color: red; }*

*header는 BLOCK, navigation은 ELEMENT, navi-text는 MODIFIER

*__와 —로 구분

⇒ ‘어떤 목적인가’에 따라 이름을 지음

⇒이름 연결할 때: -로 하이픈 하나만

**BLOCK**

: 재사용 가능한 기능적으로 독립적인 페이지 컴포넌트

**ELEMENT**

: 블럭을 구성하는 단위(의존적인 형태)
<form class="search-form">
<input class="search-form__input"/>
<button class="search-form__button">Search</button>
</form>

 `.search-form`은 블럭

 `.search-form__input`과 `.search-form__button`은 엘리먼트

**MODIFIER**

: 블럭이나 엘리먼트이 속성을 담당

**Flexbox**

-외부 엘리먼트에 display:flex; 스타일을 적용

→외부 엘리먼트=flex container, 내부 엘리먼트-flex item

-flex container와 flex item은 적용할 수 있는 속성이 다름

→flex container: flex-direction, justify-content, align-items

→flex item: flex, align-self, order

**justify-content**

: flex item을 main axis를 기준으로 어떻게 정렬할지 결정

-속성값: flex-end, center, space-between, spae-evenly, space-around etc.

-flex-start: 기본값

-flex-direction: row(좌측 정렬), column(상단 정렬)

**align-items**

: flex item을 cross axis를 기준으로 어떻게 정렬할지

-속성값: center, flex-start, flex-end, baseline etc.

ex) <nav>{ <a>} 스타일 적용

⇒ nav a{스타일 속성}

margin / padding

padding: top right bottom left;


**margin-left: auto;**

: 해당 요소의 왼쪽 여백(margin)을 "자동"으로 계산하여 가능한 모든 남은 공간을 채우도록 만드는 CSS 속성

예를 들어 좌측에 로고와 우측에 메뉴가 있을 때, 메뉴에 margin-left: auto;를 지정하면 로고와 메뉴 사이의 남은 공간을 모두 차지하여 메뉴를 오른쪽으로 밀어주는 역할

**CSS 선택자**

**id**

: class처럼 동시에 2개 이상을 사용하지 못하고 1개만 사용할 수 있다.(같은 요소라도 각기 다른 이름을 지정하여 따로 속성을 부여)
#아이디{ 속성1:속성값; 속성2:속성값; }

**type**

: 가장 간단한 선택자

**class**

: 같은 이름을 가진 태그들마다 CSS로 효과를 부여할 수 있는 것

`.클래스명{ 속성1:속성값; 속성2:속성값 }`

**flex-wrap**

-nowrap(기본값): 아이템들이 한 줄에 모두 배치, 넘치는 경우 컨테이너 너비 초과 O

-wrap: 아이템들이 컨테이너 너비를 넘으면 자동으로 다음 줄로 넘어감

-wrap-reverse: wrap과 동일하지만, 줄바꿈되는 방향이 반대로 이루어짐

**list-style-type:none;**

: ul이나 li에서 dot을 없애고 싶을 때