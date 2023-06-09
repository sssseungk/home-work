# 과제 3: transition을 활용한 반응형 웹

## transition.html
- `<div class="menu_box">` : div 태그에 menu_box 클래스를 선언하여 겉의 회색 박스를 생성하였다.
- `<h2>관련 <span class="title">사이트</span></h2>` : h2 태그 안 span 태그에 title클래스를 선언하여 글자색을 다르게 적용하도록 하였다.
- `<ul class="category">` : 5개의 리스트를 가진 ul에 category 클래스를 선언하여 흰색 박스를 구성할 수 있도록 하였다.

<br>
<br>


---
## transition.css
- `@font-face` : 웹 폰트 사용
- `.menu_box{}` : menu_box에 배경색, 테두리, 너비 값을 주어 회색 박스를 생성한다. 
이때, 흰색박스에 마우스를 올렸을 때 회색 박스의 길이가 커지도록
하기 위해 height 값은 지정하지 않았다. 

- `.title{
  color: #ED552F;
}` : h2 태그의 '사이트'글자에 주황색을 적용하였다.
- `.category{}` : 흰 박스를 만들기 위해 배경색과 테두리 값을 정의하고 적절한 위치에 배치하였다. 그리고 창이 켜졌을 때 보이는 것과같이 짧게 만들기 위해 높이값을 30px 주었다.
</br>
</br>
```css
.category:hover{
  width: 165px;
  height: 120px;
  transition: all 400ms;
}
```
-> 흰 박스에 마우스를 올렸을 때 세로 길이가 120px까지 늘어날 수 있도록 하였다. 그리고 transition 속성을 통해 자연스럽게 늘어날 수 있도록 애니메이션을 추가하였다.

<br>

`.list1{
  display: none;
}` : 가장 상위에 있는 '제로베이스' 카테고리를 제외한 나머지는
display 속성값에 none을 주어 처음에 화면에 보이지 않도록 하였다.

`.category:hover .list1{
  display: block;
}`: 흰 박스에 마우스를 올렸을 때에는 숨겨진 리스트들이 보일 수 있도록 display 속성값에 block을 주었다.


---

## 과제 결과물
![이미지](./images/homework3.jpg "과제3 스크린샷")