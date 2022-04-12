# 로그인화면 구현하기

- ## 구현 화면

<div align="center">
<img src="images/결과.png" width="600">
</div>

- ## 사이트 주소

  https://yoojs1205.github.io/loginform_excercise/

- ## 사용한 기술 스택

  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white"/></a>&nbsp;
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/></a>&nbsp;

- ## 개발 이슈
  1. 로그인화면 중앙정렬<br><br>
     ```css
     .log-in {
       background-color: #ffffff;
       /* 중앙 정렬 */
       position: absolute;
       left: 50%;
       top: 50%;
       transform: translate(-50%, -50%);
       padding: 30px 25px;
       width: 400px;
       height: 200px;
       box-sizing: border-box;
     }
     ```
  2. 좌우 정렬
     - flexbox => 수업시간에 배운 float 사용 시도<br>
       flex를 사용하면 html의 코드가 늘어나는 단점이 생겨 간단하게 float를 사용하였다.
     ```css
     /* float에 생기는 문제를 해결하기 위해 부모에 해당 클래스 지정 */
     .clear-fix::after {
       content: "";
       display: block;
       clear: both;
     }
     /* float을 적용할 요소들 */
     .find {
       float: left;
     }
     .signup {
       float: right;
     }
     ```
  3. 이미지와 text의 높이 맞추기
     - 방법론
     1. display: inline-block + vertical-align에 고정 px 주기
     2. float + margin에 고정 px 주기 (채택)<br>
        => float 적용했을 때 높낮이가 잘 맞아서 margin을 주지는 않았다.
