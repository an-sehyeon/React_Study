# React_Study

# React란?
- 사용자 인터페이스를 만들기 위한 JavaScript 라이브러리
- 빠르고 동적인 웹 어플리케이션 개발에 적합
- 컴포넌트 기반 : UI를 독립적이고 재사용 가능한 조각으로 나눔
- SPA(Single Page Application) 지원 : 화면 전체 새로고침 없이 필요한 부분만 업데이트
- JSX 문법 : HTML과 JavaScript를 함께 작성할 수 있어 직관적
- 실제 DOM보다 빠른 렌더링 성능

### JSX란?
- JSX는 JavaScript 안에서 HTML처럼 화면 구조를 작성할 수 있게 해주는 문법
    ```
    function App(){
        return (
            <div>
                <h1>상품 목록</h1>
                <p>오늘의 추천 상품.</p>
            </div>
        );
    }
    ```

- 특징
    1. 공식적인 JavaScript 문법은 아니며, 바벨에 의해 React.createElement()형태의 일반 JavaScript 코드로 변환됨.
    2. HTML과 매우 유사하여 가독성이 높고 작성하기 쉬움.
    3. {} 중괄호를 사용하여 JavaScript 표현식을 넣을 수 있음


### SPA(Single Page Application) 방식
- 최초 1회 전체 페이지 로드 -> 이후엔 필요한 데이터만 요청
- Ajax를 통한 데이터 바인딩 -> 전체 새로 고침 없이 콘텐츠 갱신
- JavaScript 기반 화면 렌더링 -> 빠르고 유연한 UI 구성

### DOM(Document of Object Model)
- HTML 문서의 요소를 제어하기 위해 문서의 각 항목을 계층으로 표현하여 
생성, 변형, 삭제할 수 있도록 돕는 인터페이스

### Virtual DOM이란?
- 실제 DOM의 복사본
- DOM 변경을 미리 시뮬레이션하여 성능 최적화
- 변경 사항을 비교 후 필요한 부분만 실제 DOM에 반영
- 빠르고 효율적인 렌더링

## [ React App의 구성요소 ]
#### [public 폴더]
    - 앱의 정적 파일(HTML, 이미지 등) 저장
    - index.html : 리액트 앱이 삽입될 html 틀
    - favicon.ico : 브라우저 탭 아이콘 등

#### [src 폴더]
    - 실제 코딩이 이루어지는 공간(핵심 로직)
    - 컴포넌트, css, JavaScript 모듈 등 포함
    - App.js, index.js 등 리액트 앱의 시작점