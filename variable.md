# 변수
- ### 변수란 프로그램을 실행하는 과정에서 변경될 수 있는 값을 저장하는 저장소.
- ### 또한 변수는 어떤 값을 이름으로 가리킬 때 사용하는 기능.
<br><hr>
# 자바스크립트의 변수 키워드
## var, let, const

## <span style="color:red">1.</span> 중복 선언 가능 여부
### <span style="color:red">var</span> 
- 중복해서 선언(+초기화)가 가능하다.
- 마지막에 할당된 값이 변수에 저장된다.
- **기존에 선언해둔 변수의 존재를 까먹고, 값을 재할당하게 되는 등의 실수가 발생하기 쉽다.**

### <span style="color:blue">let, const</span>
- 중복 선언 불가능
- 이미 선언한 변수를 다시 선언할 경우, 에러가 발생한다.
- var에 비해서 코드의 안정성을 높여줄 수 있는 방식.

## <span style="color:red">2.</span> 재할당 가능 여부
### <span style="color:red">var, let</span> 
- 값의 재할당이 가능한 변수다.
- 변수 선언 및 초기화 이후에 반복해서 다른 값을 재할당 할 수 있다.

### <span style="color:blue">const</span>
- 값의 재할당이 불가능한 상수다.
- const는 상수를 선언하는 키워드.
- 처음에 선언 및 초기화하고 나면 다른 값을 재할당 할 수 없다.

### **<span style="color:orange">var과 let과는 달리, const 선언에서는 반드시 값을 선언과 동시에 정의해야 한다.**</span> 
- 재할당이 필요없는 경우, const를 사용해 불필요한 변수의 재사용을 방지하고, 재할당이 필요한 경우 let을 사용하는 것이 좋음.

## <span style="color:red">3.</span> 변수 스코프 유효범위
- 스코프란 유효한 참조 범위를 말한다.<br>예를 들어, 함수 내부에서 선언된 변수는 함수 내부에서만 참조가 가능하다.
<br><br> 자바스크립트는 var로 선언한 변수의 스코프와 let, const로 선언한 변수의 스코프가 다르다.
<br><br> 
<span style="color:red">var </span>: 함수 레벨 스코프(function-level scope)<br>
var는 블록 스코프를 가지지 않는다. 따라서 if문, for문 같은 블록 내부에서 선언해도 해당 블록 밖에서 접근할 수 있다. 단, 함수 내부에서 선언된 경우에는 함수 스코프를 가진다.
<br><br><span style="color:blue">let, const : </span>블록 레벨 스코프(block-level scope)
<br>
let, const는 함수 내부는 물론, if문이나, for문 등의 코드 블럭{...} 에서 선언된 변수도 지역변수로 취급한다.
따라서 해당 블록 밖에서는 참조할 수 없다.

### 💡Tip
    정리하자면, var는 함수 내부에 선언된 변수만 지역 변수로 인정하는 함수 레벨 스코프이다.
    let, const는 모든 블록 내부에서 선언된 변수까지 지역변수로 인정하는 블록 레벨 스코프이다.

