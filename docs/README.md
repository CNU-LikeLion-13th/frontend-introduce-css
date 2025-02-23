## 시멘틱 코드를 위한 첫걸음


- header : header는 일종의 '머리글', nav 태그를 담기위해 사용했다.

- nav : navigator 의 약자에서 따온 nav 태그. 이 태그는 주로 '메뉴'들을 담아주기 위해 nav로 메뉴 창을 만들었다.

- section : 말 그대로 섹션, 즉 구역을 나누는 태그. 나의 목표 세가지를 만들 때 구역을 나눠주었다. 

## CSS

>link rel="stylesheet" href="/style.css" <br> 내 스타일시트를 외부 파일로  link 했다.

- flexbox를 만들어 화면을 구성했다. 요소를 구역의 정 중앙에 배치 <br>
**display: flex;<br>align-content: center;<br>justify-content: center;** <br> 

- list 점 떼기 : **list-style: none;** 을 사용하면 ul의 점이 없어진다.

- 줄 간격 조절하기 : **line-height: ~%;** 를 사용해서 리스트들의 줄 간격을 조절했다.

- a 태그 색 없애기 : **text-decoration: none;** 을 사용해 하이퍼링크 표시를 지웠다. 

- 정렬하기 : <br>**왼쪽 정렬 -> margin-right: auto;** 오른쪽의 마진을 전부 채움<br>**오른쪽 정렬 -> margin-left: auto;** 왼쪽의 마진을 전부 채움 <br>**가운데 정렬 -> margin-right: auto; margin-left: auto;** 양쪽 마진을 전부 채움  **가운데 정렬 -> margin: 0 auto;** 위 아래 마진이 0인 가운데 정렬