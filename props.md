# Props란?
- props는 properties의 줄임말.
- 부모 컴포넌트가 자식 컴포넌트에게 전달하는 데이터(속성)
- 상위 컴포넌트가 하위 컴포넌트에 값을 전달하기 때문에 단방향 데이터 흐름을 가짐.
- 부모 컴포넌트는 수정 가능하지만, 자식 컴포넌트는 읽기만 가능.

### props를 쓰는 이유
- 같은 컴포넌트를 여러 데이터로 재사용하기 위함.

### 📌 Props 사용 : 단방향 데이터 흐름
##### props를 사용하려면 두 단계가 필요.
1) 상위 컴포넌트에서 Props를 지정.
2) 하위 컴포넌트에서 받은 Props값을 렌더링
* 이때 상위 컴포넌트에서 하위 컴포넌트로 프로퍼티가 전달되는데 이것이 "단방향 데이터 흐름"
  <br><br>
#### 1) 상위 컴포넌트에서 Props 지정해서 넘기기
- App 컴포넌트에서 MyComponent에 props 값을 지정.
- ### App.js
```plantuml
import React from "react";
import MyComponent from "./MyComponent";

function App(){
    return(
        <MyComponent propValue="React Study!!">Hello React</MyComponent>
    );
}
export default App;
```
<br><br>

#### 2) 하위 컴포넌트에서 받아 Props 렌더링
- MyComponent 컴포넌트에서 상위 컴포넌트로 부터 받은 props 데이터를 뷰에 렌더링.
- {ㅔprops.propValue} : 상위 컴포넌트에서 props값을 propsValue로 전달했기 때문에 {props.propValue}로 나타냄.
- {props.children} : 리택트 컴포넌트 태그 사이에 내용을 보여주는 props 속성.
- ### MyComponent.js
```plantuml
import React from "react";
function MyComponent(props){
    return(
        <div>
            {props.propValue},{props.children}
        </div>
    );
}
```

### 결과
```plantuml
React Study!!, Hello React
```


### 📌 Props 타입
- props의 자료형은 JavaScript의 자료형을 모두 사용 가능.
#### 문자열 타입 프로퍼티
- 프로퍼티 타입이 문자열인 경우, 프로퍼티 값을 표현할 때는 큰 따옴표("")를 사용
```<MyComponent name = "React Study"/>```
<br><br>

#### 문자열 이외 타입 프로퍼티
- 문자열 타입 이외의 프로퍼티 값은 중과로({})를 사용.
```plantuml
<MyComponent
    boolProp={true}     // boolean
    arrProp={['a','b','c']}     // 배열
    objProp={{name : '세바리', title : 'React Study'}}   // 객체
    funcProp={()=> {alert('알림창');}}     // 함수
/>
```
