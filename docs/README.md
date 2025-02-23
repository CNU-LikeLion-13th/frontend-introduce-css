# 1주차 과제 코드 개선
1주차 과제 코드 리뷰를 바탕으로 코드를 개선해보았다.

![시멘틱 태그](https://seo.tbwakorea.com/wp-content/uploads/2023/09/%EC%8B%9C%EB%A7%A8%ED%8B%B1-%ED%83%9C%EA%B7%B8_html.png)

## 기본 시멘틱 태그 틀
* `<header>` : 머리말
* `<nav>` : 다른 웹 페이지로 연결하거나, 현재 웹 페이지의 콘텐츠 내부로 연결되는 탐색을 위한 링크가 있는 영역
* `<aside>` : 옆에 위치하는 콘텐츠
* `<main>` : 메인 콘텐츠
  * `<article>` : 독립적인 콘텐츠
  * `<figure>` : 주변 콘텐츠의 이해나 흐름과 관련된 이미지, 그림, 도표, 사진, 코드 목록 또는 기타 관련 콘텐츠
    * `<figcaption>` 태그를 사용해서 이 콘텐츠를 참조할 수 있는 설명을 추가
  * `<p>` : 문단을 나타내는 태그
  * `<section>` : 일반적인 섹션
* `<footer>` : 바닥글 (저자 정보, 저작권 등)

## 기타
* `<ul>` : unordered list (순서가 상관 없는 리스트)
* `<ol>` : ordered list (순서가 상관 있는 리스트)
* `<li>` : `<ul>`, `<ol>` 안의 구성요소로 사용된다.

---
코드 리뷰를 보고 코드를 수정하며 시멘틱 태그의 사용법에 더욱 익숙해질 수 있었다. 화면을 어떻게 분할할지 생각하여 디자인, 태그를 사용해야겠다.

# 2주차 과제 진행
## sr-only
.sr-only 클래스를 사용하여 화면에는 보이지 않지만 스크린 리더로는 인식할 수 있는 컨텐츠를 생성할 수 있음

디테일한 설명 부분에서 sr-only 클래스를 사용할 수 있을 것 같다.

## BEM 방법론
### B : 블록(Block)
독립적이고 재사용 가능하며 논리적으로 독립된 개체
> e.g. header, button, nav-menu
### E : 요소(Element)
블록의 일부로, 독립적인 의미가 없고 블록과 의미적으로 연결되어 있음
> e.g. nav-menu__item nav-menu__logo
### M : 수식어(Modifier)
블록이나 요소의 플래그. 모양이나 동작을 변경하는 데 사용
> e.g. nav-menu__item--active

B__E--M 형식으로 언더바, 하이픈 2개씩으로 연결하여 사용
## CSS 네이밍 규칙
* 소문자, 숫자 조합으로 사용
* 조합은 -(하이픈) 으로 연결하여 사용
* 정수는 한자리 보다 01, 02 같이 사용을 권장

## CSS display
> 박스 모델을 정의하고 어떻게 배치될지를 설정
```
  display: block          /* 블록 레벨 요소 (전체 너비 차지) */
  display: inline         /* 인라인 요소 (내용만큼의 너비 차지) */
  display: inline-block   /* 인라인처럼 배치되지만, 너비와 높이를 설정 가능 */
  display: flex           /* 플렉스 컨테이너 (플렉스 아이템 배치) */
  display: grid           /* 그리드 컨테이너 (그리드 아이템 배치) */
  display: none           /* 요소를 보이지 않게 함 (공간 차지하지 않음) */
  display: table          /* 테이블 레이아웃으로 표시 */
```
`display: flex` 를 가장 많이 사용했다. CSS Flex에 대해 추가적인 공부가 필요할 것 같다.

## CSS text-align
> 텍스트의 정렬 기준
```
  text-align: start         /* 왼쪽 정렬 (글 방향이 좌 -> 우 일 경우) */
  text-align: end           /* 오른쪽 정렬 (글 방향이 좌 -> 우 일 경우) */
  text-align: left          /* 왼쪽 정렬 */
  text-align: right         /* 오른쪽 정렬 */
  text-align: center        /* 가운데 정렬 */
  text-align: justify       /* 양쪽 정렬 */
  text-align: justify-all   /* 양쪽 정렬 (마지막 줄에도 적용) */
  text-align: match-parent  /* 부모의 방향에 따라 정렬 */
```

## CSS align-items
> Vertical 정렬을 할 때 사용
```
  align-items: stretch(default) /* container 전체에 맞춤 */
  align-items: center           /* container의 가운데 정렬 */
  align-items: start            /* container의 위쪽 정렬 */
  align-items: end              /* container의 아래쪽 정렬 */
```

## CSS justify-content
> 메인 축(Horizontal) 정렬을 할 때 사용

```
  justify-content: center;      /* 항목들을 축의 중심 부분에 정렬 */
  justify-content: start;       /* 항목들을 축의 시작 부분에 정렬 */
  justify-content: end;         /* 항목들을 축의 끝 부분에 정렬 */
  justify-content: flex-start;  /* 플렉스 항목들을 축의 시작 부분에 정렬 */
  justify-content: flex-end;    /* 플렉스 항목들을 축의 끝 부분에 정렬 */
  justify-content: left;        /* 항목들을 축의 왼쪽 부분에 정렬 */
  justify-content: right;       /* 항목들을 축의 오른쪽 부분에 정렬 */
```