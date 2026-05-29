# 함수 표현식
자바스크립트는 일반적인 함수 선언 말고도 함수를 만드는 방법이 있는데 바로 '함수 표현식'을 이용하는 방법이 있다.
<br>
함수 표현식이란 함수를 생성하고 변수에 값으로 저장하는 방법이다.

<br>
<hr>
<br>

#### 함수 선언과 함수 반환 코드 예제
```
function getArea(width, height){
    let area = width * height;
    return area;
}

let result = getArea(10, 20);
console.log(result);
```
<br><br>

#### 함수 표현식 코드 예제
```plantuml
let greeting = () => {
    console.log("hello");
};

greeting();
```
<br><br>
자바스크립트에서는 함수를 숫자나 문자열처럼 값으로 취급한다. 
그래서 변수에 함수를 저장할 수 있다. 
변수에 함수를 저장하면 변수 이름으로 호출할 수 있다. 
이렇게 함수를 변수의 값으로 저장해 생성하는 방법을 함수 표현식이라고 한다.

#### 다음은 선언한 함수를 변수에 저장해 사용하는 코드 예제
```plantuml
function greetFunc(){
    console.log("hello");
}

greetFunc();

let greeting = greetFunc;
greeting();
```
##### 한가지 주의할 점은 함수를 변수에 저장할 때에는 함수 호출과 달리 소괄호를 명시하지 않는다.

<br>
<hr>
<br>

## 함수 호출 시 "함수 선언"으로 만든 함수와 "함수표현식"의 차이
##### 💡함수 표현식으로 만든 함수는 함수 선언으로 만든 함수와는 달리 호이스팅 되지 않는다.

```plantuml
funcA();
funcB();    // ERROR

function funcA(){
    console.log("func A");
}

let funcB = function(){
    console.log("func B");
};
```
##### funcA는 함수 선언으로 만들었기 때문에 호이스팅 대상이다. 따라서 함수 선언 전에도 호출할 수 있었지만, funcB에 저장한 함수는 호이스팅 되지 않는다. 왜냐하면 함수 표현식을 사용하여 저장한 함수는 선언이 아닌 "값"으로 취급하기 때문에 호이스팅을 하지 못한다.
