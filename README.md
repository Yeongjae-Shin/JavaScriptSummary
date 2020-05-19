# 자바스크립트 정리
# 목차
1. [변수와 타입](https://github.com/Yeongjae-Shin/JavaScriptSummary#%EB%B3%80%EC%88%98%EC%99%80-%ED%83%80%EC%9E%85)
2. [조건문](https://github.com/Yeongjae-Shin/JavaScriptSummary#%EC%A1%B0%EA%B1%B4%EB%AC%B8)
3. [함수](https://github.com/Yeongjae-Shin/JavaScriptSummary#%ED%95%A8%EC%88%98)
4. [배열](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B0%B0%EC%97%B4)
5. [반복문](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B0%98%EB%B3%B5%EB%AC%B8)
6. [배열의 반복](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B0%B0%EC%97%B4%EC%9D%98-%EB%B0%98%EB%B3%B5)
## 변수와 타입
- 변수는 상황에 따라 변할 수 있는 값
  - 변수 선언 ➡️ 선언은 한번만 한다
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
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
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
  참고! `==`와 `!=`는 엄격하게 비교 ❌ ➡️ 사용 지양
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
  - 논리연산자 `AND` ➡️ 둘 다 `true`일 경우
    ```js
    true && true // true
    true && false // false
    false && false // false
    ```
  - 논리연산자 `OR` ➡️ 둘 중 하나라도 `true`면 결과는 `true`
    ```js
    true || true // true
    true || false // true
    false || false // false
    ```
  - 논리연산자 `NOT` ➡️ 값을 반전시킴
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
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 함수
  1. 함수는 컴퓨터에게 일을 시키기 위한 지시사항의 묶음
  2. 함수는 입력 ➡️ 함수 ➡️ 출력의 과정으로 이루어짐
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
  ```js
  // ex) 집까지 가는데 걸리는 시간
  let timeToGoHome = function (speed, distance) {
    let time = distance / speed;
    console.log(time);
  }
  // speed와 distance를 매개변수로 둔 이유?
  // 사람마다 조건이 다르기 때문(가변적)
  timeToGoHome(20, 100); // 5
  ```
  - 함수 바깥으로 결과를 가져오려면?
  ```js
  console.log(time); // ReferenceError
  let myTime = timeToGoHome(20, 100);
  console.log(myTime); // undefined myTime의 값이 없기 때문
  ```
  - `return`을 사용하면 출력이 된다.
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 배열
1. 배열은 순서가 있는 값이다.
2. 순서와 값은 각각 `index`와 `element`로 부른다.
3. `index`는 0이 아닌 1부터 번호를 매긴다.
4. 배열의 예시
  ```js
  let myNumber = [73, 98, 86, 61, 96];
  // myNumber라는 배열의 1번째 element는 98이다.
  ```
- 배열의 값을 변경할 수도 있다.
  ```js
  myNumber[1] = 33;
  myNumber; // [73, 33, 86, 61, 96];
  ```
- 이차원으로 배열을 구성할 수도 있다.
  ```js
  let myNumber = [[13, 30], [73, 8], [44, 17]];
  myNumber[1] // [73, 8]
  myNumber[1][0] // 73
  ```
- 배열로 할 수 있는 것들
  - 배열의 길이 구하기
    ```js
    let myNumber = [73, 98, 86, 61];
    myNumber.length // 4
    ```
  - 요소 추가하기
    ```js
    let myNumber = [73, 98, 86, 61];
    myNumber.push(96) // [73, 98, 86, 61, 96]
    // push 메서드는 배열의 가장 마지막에 요소 추가
    ```
  - 요소 삭제하기
    ```js
    let myNumber = [73, 98, 86, 61];
    myNumber.pop(); // [73, 98, 86]
    // 가장 마지막 요소 삭제
    ```
  - 첫 번째 요소 삭제
    ```js
    let myNumber = [73, 98, 86, 61];
    myNumber.shift(); // [98, 86, 61]
    ```
  - 맨 앞에 요소 추가
  ```js
    let myNumber = [73, 98, 86, 61];
    myNumber.unshift(96) // [96, 73, 86, 61]
    ```
  - 배열인지 아닌지 판단
  ```js
    let myNumber = [73, 98, 86, 61];
    Array.isArray(myNumber) // true
    // Array.isArray 메서드는 항상 boolean값 리턴
    ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 반복문
  - 반복문이란?
  
    ➡️ 같거나 비슷한 코드를 여러 번 실행시켜야 할 경우에 쓰는 구문
  - 반복문의 종류
    - for 구문
      반복할 조건을 `초기화`, `조건식`, `증감문` 순으로 넣어준다
      
      이 때 시작 조건은 `i`로 설정하는것이 좋다. `index`에서 `i`를 따왔기 때문
      `i`, `j` ... 순으로 설정
      ```js
      let sum = 1;
      for (let i = 0; i <= 4; i++) {
        sum = sum + i;
      }
      ```
    - while 구문
      반복할 조건 중 `초기화`, `증감문`은 따로 적고 조건식만 괄호안에 넣는다.
      ```js
      // 조건이 true일 때만 반복, false시 중단
      let sum = 1;
      let i = 2;
      while (i <= 4) {
        sum = sum + i;
        i++;
      } // 10
      ```
      초기화와 증감문이 필요없을 때 `while`을 사용하면 좋음

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 배열의 반복
