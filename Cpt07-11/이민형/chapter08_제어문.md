## 8장 제어문

### 8.1 블록문

- 0개 이상의 문을 중괄호로 묶은 것
- 코드 블록, 블록

_자바스크립트는 블록문을 하나의 실행 단위로 취급한다._

_블록문은 언제나 문의 종료를 의미하는 자체 종결성을 갖기 때문에 블록문의 끝에는 세미콜론을 붙이지 않는다._

<hr>

### 8.2 조건문

- if ... else
- switch

#### \_\_8.2.1 if ... else 문

```javascript
if (조건식1) {
  // 조건식1이 참일 때 실행
} else if (조건식2) {
  // 조건식2가 참일 때 실행
} else {
  // 조건식이 거짓일 때 실행
}
```

- 대부분의 if ... else 문은 삼항 연산자로 바꿔쓸 수 있다.

#### \_\_8.2.2 switch 문

```javascript
switch (표현식) {
    case 표현식1:
        // 표현식과 표현식1이 일치할 때 실행
        break;
    case 표현식2:
        // 표현식과 표현식2이 일치할 때 실행
        break;
    ...
    default:
        // 표현식과 일치하는 case문이 없을 때 실행
}
```

- 폴스루(fall through): 표현식과 일치하는 case문으로 실행 흐름이 이동하여 문을 실행한 후 switch문을 탈춣지 않고 switch문이 끝날 때까지 모든 case문과 default문을 실행했을 때 발생

<hr>

### 8.3 반복문

- 조건식이 거짓일 때까지 반복
  > 반복문 대체 가능
  >
  > - forEach: 배열 순회
  > - for ... in: 객체 프로퍼티 열거
  > - for ... of: 이터러블 순회(ES6 도입)

#### \_\_8.3.1 for 문

```
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// 결과
0
1
2
3
4
```

#### \_\_8.3.2 while 문

- 반복 횟수가 불명확할 때 주로 사용

#### \_\_8.3.3 do ... while 문

- 코드 블록을 먼저 실행하고 조건식 평가

<hr>

### 8.4 break 문

- 코드 블록 탈출

  - 레이블문, 반복문, switch 문의 코드 블록을 탈출

- 레이블문: 식별자가 붙은 문 -프로그램의 실행 순서를 제어하는 데 사용

```javascript
foo: console.log("foo");
```

switch 문의 case 문과 default 문도 레이블 문

🚨레이블 문을 사용하면 프로그램의 흐름이 복잡해져 가독성이 나빠지고 오류를 발생시킬 가능성이 높아 일반적으로 권장하지 않는다.

<hr>

### 8.5 continue 문

- 코드 블록 실행을 현 지점에서 중단하고 반복문의 증감식으로 실행 흐름을 이동시킴
