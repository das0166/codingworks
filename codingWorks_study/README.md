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
        기본 너비 값 : 컨텐츠의 너비 값 / 한 줄에 여러개 배치 / 크기 값을 가질 수 있음 / 상하좌우 마진 값 가질 수 있음 


