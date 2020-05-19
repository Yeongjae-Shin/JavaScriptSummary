# 자바스크립트 정리
## 변수와 타입
- 변수는 상황에 따라 변할 수 있는 값
  - 변수 선언 👉 선언은 한번만 한다
  ```js
  let myName;
  ```
  - 값 할당
  ```js
  myName = 'Steve';
  ```
  - 최종 형태
  ```js
  let myName = 'Steve';
  ```
  
- 표현식(expression)에서 변수 활용 가능
  - 결과물도 변수로 담을 수 있다.
  ```js
  let pi = 3.14;
  let radius = 5;
  let areaOfCircle = pi * radius * radius;
  ```
- 변수에는 **공백**을 넣지 않는다. 제일 첫 글자 제외 항상 단어의 첫 글자는 대문자로 표현하여 구분
  - 이때 변수가 생긴 모양이 낙타의 등과 같다하여 `Camel Case`라고 부름. `python`은 `Snake Case`
  ```
  variable_example
  ```

- 변수는 동일한 변수를 대입할 수 있다.
  ```js
  let sum = 1;
  sum = sum + 2; // 한번 선언했던 변수를 다시 사용할 땐 let 키워드 사용 x
  sum = sum + 3;
  sum = sum + 4;
  
  // 10
  ```
- 변수의 타입
  - 숫자: `10`
  - 문자열: `'Hello'`
  - 불리언: `true/false`
  
- 여러개의 타입이 타입이 섞인 경우
  - 배열
  ```js
  let fruits = ['banana', 'apple', 'pineapple'];
  ```
  - 객체
  ```js
  let person = {
    name: 'Steve',
    age: 32.
    city: 'Seoul'
  };
  ```
  
## 조건문
  1. 조건문을 배우기 위해선 Boolean 타입에 대한 이해 필요
  2. 조건문은 조건을 판별하는 기준을 만드는 것
  3. 반드시 **비교연산자**가 필요함
  
- 비교연산자
  ```js
  3 > 5; // false
  9 < 10; // true
  'hello' === 'world' // false
  ```
  - 비교의 결과는 항상 Boolean이다.

- 비교연산자의 종류
  - `>` 초과
  - `<` 미만
  - `>=` 이상
  - `<=` 이하
  - `===` 같다
  - `!==` 다르다
  참고! `==`와 `!=` 엄격하게 비교 x 👉 사용 지양
  ```js
  1 === 1 // true
  1 === '1' // false
  1 == '1' // true
  ```

- 조건문
  - 조건문의 기본 형식
  ```js
  if (조건1) { // 여기서 조건에는 Boolean으로 결과가 나오는 표현식이 들어감
    // 조건1이 통과할 경우
  } else if (조건2) {
    // 조건1이 통과하지 않고 조건2가 통과할 경우
  } else { // 명령이 한 줄일 경우 else 생략 가능
    // 모든 조건이 통과하지 않는 경우
  }
  ```

- 두 가지 조건이 한번에 적용되는 경우
  - 논리연산자 `AND` 👉 둘 다 `true`일 경우
    ```js
    true && true // true
    true && false // false
    false && false // false
    ```
  - 논리연산자 `OR` 👉 둘 중 하나라도 `true`면 결과는 `true`
    ```js
    true || true // true
    true || false // true
    false || false // false
    ```
  - 논리연산자 `NOT` 👉 값을 반전시킴
    ```js
    !false // true
    !(3 > 2) // false
    !undefined // true
    !'Hello' // false
    // 모든 문자열은 truthy한 값 (빈 문자열 제외)
    ```

- 기억해야 할 6가지 falsy 값
  ```js
  1. if (false)
  2. if (null)
  3. if (undefined)
  4. if (0)
  5. if (NaN) // NaN: Not a Number
  6. if (' ')
  // 위 6가지는 if문에서 false로 변환됨
  ```

## 함수
  1. 함수는 컴퓨터에게 일을 시키기 위한 지시사항의 묶음
  2. 함수는 입력 👉 함수 👉 출력의 과정으로 이루어짐
  3. JavaScript에서의 함수 사용은 함수 이름과 입력을 이용
  ```js
  let length = getLength('안녕하세요');
  console.log(length); // 5
  ```

- 함수선언식
  ```js
  function myFunction (input) {
    // 컴퓨터에게 시킬 일
  }
  ```
  위 코드에서 `input`을 매개변수(parameter)라 부름. 이는 함수 실행시 입력에 따라 가변적이지만 let 등의 키워드를 쓰지 않고도 사용 가능

- 함수표현식
  ```js
  let myFunction = function (input) {
    // 컴퓨터에게 시킬 일
  }
  ```
