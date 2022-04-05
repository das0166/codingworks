# 코딩웍스
1. 폼요소
    ```html
    <form> : 폼 요소 만들기
    <label> : 폼 요소에 레이블 붙이기
    <fieldset> : 폼 요소 그룹으로 묶기
    <legend> : 보더라인 안에 소제목 넣기
    <input> : 입력 항목 만들기 
    <form>
        <fieldset>
            <legend>로그인 정보</legend>
            <label for="">아이디</label>:<input type="text">
        </fieldset>
    </form>
    
    <form>안에 checkbox, radio, select&option, textarea 등 다양한 것들을 사용할 수 있음.
    ```
2. CSS 선택자 - 적용 우선순위
    1. !important Style
    2. Inline Style
    3. ID Selector Style
    4. Class Selector Style
    5. Tag Selector Style
3. 레이아웃 스타일 - 인라인요소 vs 블록요소
    1. 인라인 요소
        ex) span, a, small, big, em, u, s, del, br, q, b, strong, mark, sub, sup, video, audio
        기본 너비 값 : 컨텐츠의 너비 값 / 한 줄에 여러 개 배치, 크기 값을 가질 수 없음, 상하 마진은 가질 수 없음
    2. 블록 요소
        ex) div, h1~h6, table, figure, figcaption, caption, header, nav, footer, section, article, aside, p, ul, ol, blockquote, li, td, form, fieldset, hr
        기본 너비 값 : 100% / 한 줄에 하나만 배치 / 너비 값,높이 값 가질 수 있음 / 상하좌우 마진 가질 수 있음
    3. 인라인 블록 요소
        ex) img, input 태그들, button, FontAwesome
        기본 너비 값 : 컨텐츠의 너비 값 / 한 줄에 여러개 배치 / 크기 값을 가질 수 있음 / 상하좌우 마진 값 가질 수 있음<br>
4. 인라인요소 vs 블록요소의 차이를 알아야하는 이유<br>
     ```html
    1.
    <ul class="sns">
        <li><a href=""><i class="fa-fa-facebook"></i>facebook</a></li>
        <li><a href=""><i class="fa-fa-twitter"></i>twitter</a></li>
        <li><a href=""><i class="fa-fa-linkedin"></i>linkedin</a></li>
        <li><a href=""><i class="fa-fa-google-plus"></i>google</a></li>
    </ul>
    2.
    <div class="sns">
        <a href=""><i class="fa-fa-facebook"></i>facebook</a>
        <a href=""><i class="fa-fa-twitter"></i>twitter</a>
        <a href=""><i class="fa-fa-linkedin"></i>linkedin</a>
        <a href=""><i class="fa-fa-google-plus"></i>google</a>
    </div>
    ```
    - 2번이 1번보다 html 구조가 훨씬 간결함(계층구조가 적음)
    - 1번의 경우 css에서 float:left; 속성을 줘야하지만 2번은 그렇지 않음
5. 레이아웃 스타일(display 속성 : inline, block, inline-block, none) : 레이아웃 요소를 배치 및 특성을 변경하는 정말 중요한 속성과 값<br>
    ex)image 태그는 기본 속성이 inline-block이기 때문에 가로 배치 됨. 그러므로 display:block을 주게 되면 세로 배치가 됨<br>
6. 애니메이션<br>
    1. animation-name : 이름이 지정되면 해당 이름과 일치하는 키 프레임이 사용됨<br>
    ex)animation-name:'<span style="color:red">애니메이션 이름</span>' @keyframes'<span style="color:red">애니메이션 이름</span>'
    2. animation-duration : 애니메이션이 지속되는 시간을 정의<br>
    ex) animation-duration:2s; = 애니메이션을 2초동안 실행
    3. animation-timing-function : 애니메이션의 속도 곡선을 지정하는 속성, 키프레임과 키프레임이 넘어가는 구간을 부드럽게 해주는 속성, 대표적으로 linear를 사용함<br>
    ex)linear, ease, ease-in, ease-out, ease-in-out
    4. animation-delay : 애니메이션을 시작하기 전에 기다려야하는 시간을 정의, 에니메이션은 첫번째 반복에서만 지연됨<br>
    ex)animation-delay : 0.5s; == animation-delay : 500ms;
    5. animation-iteration-count : 애니메이션이 재생될 횟수, 양의 정수와 infinite(무한 반복 재생)만 입력 가능<br>
    ex) animation-iteration-count:1; animation-iteration-count:infinite;
    6. animation-direction : 애니메이션이 재생되는 방향을 정하는 속성<br>
    normal, reverse, alternate, alternate-reverse 주로 alternate 사용
    7. animation-play-state : 애니메이션 일시중지 또는 실행<br>
    paused : 일시중지 / running : 실행(기본값)
    8. animation-fill-mode : 애니메이션이 동작하지 않고 있을 때, 애니메이션의 상태 설정<br>
    - none : 애니메이션 종료 후 시작할 때의 상태로 돌아옴(기본값)
    - forwards : 애니메이션 종료 후 끝난 상태 그대로 유지
    - backwards : 애니메이션 종료 후 시작할 때의 상태로 돌아옴
    - both : 종료 후 forwards, backwards 둘 다 적용하여 양방향으로 속성을 확장
    ```css
    .content{
        position:relative;
        animation-name : ani;
        animation-duration : 3s;
        animation-timing-function : linear;
        animation-delay : 1s;
        animation-iteration-count:infinite;
    }
    .content:hover{
        animation-play-state : paused;
    }
    @keyframes ani{
        from{left:0;}
        to{left:200px;}
    }
    ```
7. 애니메이션 키프레임
    - @keyframes를 타임라인 안의 하나의 스테이지(구간)
    - @keyframes 속성 구간별로 지정하기
        - 0%-100%; from(0%과 같음) 그리고 to(100%과 같음)
        - 각 구간에 css 적용
    ```css
    @keyframes 애니메이션 이름{
        0%{변경시킬 css 속성}
        100%{변경시킬 css 속성}
    }
    @keyframes 애니메이션 이름{
        from{변경시킬 css 속성}
        to{변경시킬 css 속성}
    }
    ```

