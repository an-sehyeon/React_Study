# 컴포넌트란?
- 리액트 앱을 구성하는 최소 단위
- UI를 독립적이고 재사용 가능한 단위로 나눈 것

### 특징
1. MVC의 View를 독립적으로 구성하여 재사용 가능
2. 데이터를 입력받는 Props와 자체적으로 상태를 관리하는 state를 가짐.
3. 컴포넌트의 이름은 항상 대문자로 시작해야 함.

### 예시 코드
```
    function Header() {
        return <header>상단 메뉴</header>;
    }
    
    function ProductCard(){
        return <div>상품 카드</div>
    }
    
    function Footer(){
        return <footer>하단 영역</footer>
    }
```