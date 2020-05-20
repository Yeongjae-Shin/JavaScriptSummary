# 목차
1. [변수와 타입](https://github.com/Yeongjae-Shin/JavaScriptSummary#%EB%B3%80%EC%88%98%EC%99%80-%ED%83%80%EC%9E%85)
2. [조건문](https://github.com/Yeongjae-Shin/JavaScriptSummary#%EC%A1%B0%EA%B1%B4%EB%AC%B8)
3. [함수](https://github.com/Yeongjae-Shin/JavaScriptSummary#%ED%95%A8%EC%88%98)
4. [배열](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B0%B0%EC%97%B4)
5. [반복문](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B0%98%EB%B3%B5%EB%AC%B8)
6. [배열의 반복](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B0%B0%EC%97%B4%EC%9D%98-%EB%B0%98%EB%B3%B5)
7. [객체](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EA%B0%9D%EC%B2%B4)
8. [배열의 메서드](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EA%B0%9D%EC%B2%B4)
9. [reduce](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#reduce-%EA%BD%A4-%EC%96%B4%EB%A0%A4%EC%9B%80)
10. [Scope](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#Scope)
11. [변수](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B3%80%EC%88%98)
12. [Closure](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#closure-%EB%A7%A4%EC%9A%B0-%EC%96%B4%EB%A0%A4%EC%9B%80)
13. [객체지향 프로그래밍](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5-javascript)
14. [매개변수](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%A7%A4%EA%B0%9C%EB%B3%80%EC%88%98)
15. [비동기 호출](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%B9%84%EB%8F%99%EA%B8%B0-%ED%98%B8%EC%B6%9C)
16. [타이머 API](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%ED%83%80%EC%9D%B4%EB%A8%B8-api)
17. [서버 요청하기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EC%84%9C%EB%B2%84-%EC%9A%94%EC%B2%AD%ED%95%98%EA%B8%B0)
18. [this](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#this)
19. [Prototype](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#prototype)
20. [함수 메서드](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%ED%95%A8%EC%88%98-%EB%A9%94%EC%84%9C%EB%93%9C)
21. [재귀함수](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EC%9E%AC%EA%B7%80%ED%95%A8%EC%88%98)
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
    areaOfCircle // camel case
    variable_example // snake case
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
  
- 여러개의 타입이 섞인 경우
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
    - forEach 구문 (명령형 반복문을 함수형으로 작성하기)
      - **함수를 인자로 받음**
        ```js
        let users = [
          { name: 'Tim', age: 40 },
          { name: 'Satya', age: 30 },
          { name: 'Sundar', age: 50 }
        ];
        // 이름을 출력하기 위해 for문 사용
        for (let i = 0; i < users.length; i++) {
          console.log('Name: ' + users[i].name);
        } // Name: Tim Name: Satya Name: Sundar
        // 이것을 간단하게 함수 정의와 forEach로 구현 가능
        function printName (user) {
          console.log('Name: ' + user.name);
        }
        user.forEach(printName); // Name: Tim Name: Satya Name: Sundar
        ```
    - for...in 구문 (객체의 프로퍼티를 순환할 때)
      - 기본 형태
        ```js
        for (let 변수 in 객체) {
          // 구문
        }
        ```
      1. `for...in` 구문의 본문은 객체의 각 프로퍼티에 대해 한번씩 실행된다.
      2. 각 반복에 앞서 객체 프로퍼티 중 하나의 이름이 변수에 문자열 타입으로 할당된다.
      - 객체를 받고 이차원 배열로 변환하는 함수
        ```js
        function convertObjectToList (obj) {
          let result = []; // 이차원 배열로 변환해야 하니 빈 배열 생성
          for (let key in obj) { // 주어진 객체에서 각 key 탐색
            result.push([key, obj[key]]) // 빈 배열에 [key, value] 형태로 push
          }
          return result;
        }
        // 예시
        let obj = [10, 11, 12];
        for (let key in obj) {
          console.log('name: ' + key + '; value: ' + obj[key]);
        }
        // name: 0; value: 10
        // name: 1; value: 11
        // name: 2; value: 12
        ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 배열의 반복
  - 반복문을 이용해 배열의 요소를 출력해보기
    ```js
    let myNum = [73, 98, 86, 61];
    for (let i = 0; i < myNum.length; i++) {
      console.log(myNum[i]);
    }
    ```
  - 배열의 요소의 합 구하기
    ```js
    let myNum = [10, 20, 30, 40];
    let sum = 0;
    for (let i = 0; i < myNum.length; i++) {
      sum = sum + myNum[i];
    } // 80
    ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 객체
객체는 키와 값으로 이루어져 있고, 그 사이는 콜론`:`으로 구분한다. 중괄호를 이용하여 객체를 생성하고 각 개체는 쉼표`,`로 구분
  - 객체의 값을 사용하는 방법
    - Dot notation
      ```js
      let user = {
        name: 'Steve',
        city: 'Seoul'
      };
      user.name // 'Steve'
      user.city // 'Seoul'
      ```
    - Bracket notation ➡️ 키 값이 동적일 때 반드시 사용
      ```js
      let user = {
        name: 'Steve',
        city: 'Seoul'
      };
      user['name'] // 'Steve'
      user['city'] // 'Seoul'
      user[name] // undefined
      ```
      이 때, 브라켓 안에는 따옴표가 반드시 있어야 함. 만약, 따옴표 없이 쓰고 싶을 땐 변수로 지정해야함.
      ```js
      let noQuote = 'city'
      user[noQuote] // 'Seoul'
      ```
    - dot/bracket notation을 이용해 값을 추가 가능
      ```js
      user.isMale = true;
      user.tags = ['JavaScript', 'TIL'];
      user['category'] = '코딩';

      user;
      // {name: "Steve", city: "Seoul", isMale: true, tags: ['JavaScript', 'TIL'], category: "코딩"}
      ```
    - delete를 이용해 삭제도 가능
      ```js
      delete user.name;
      // name: 'Steve' 가 없어짐
      ```
    - in을 이용해 해당 키가 객체에 존재하는지 확인 가능
      ```js
      'name' in user; // true
      'email' in user; // false
      ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 배열의 메서드
### 1. 원본이 변하지 않는 새로운 배열 만들기 (slice)
1. 원본 배열은 수정되지 않는다. (immutability)
2. arr이라는 배열에 slice를 이용해 newArr을 생성하면 arr의 뒤에 새로운 element가 추가된 형태
  ```js
  let arr = [1, 2, 3];
  let newArr = arr.slice();
  newArr; // [1, 2, 3]

  newArr.push(4); // [1, 2, 3, 4]
  arr; // [1, 2, 3]
  ```
3. 시작점과 끝나는 점을 설정하여 잘라내기
  ```js
  let arr = [1, 2, 3, 4];
  arr.slice(0, 2) // [1, 2]
  arr.slice(1, 4) // [2, 3, 4]
  // 끝나는 점을 따로 설정하지 않으면 항상 배열의 끝까지 자름
  // 따라서
  arr.slice(1, 4) === arr.slice(1)
  ```
### 2. 특정 인덱스의 요소 제거 (splice)
  ```js
  let arr = [1, 2 ,3];
  arr.splice(1[시작점], 1[삭제할 개수]) // [1, 3]
  ```
### 3. 배열의 형태 바꾸기 (map)
  **기존 배열과 length는 같지만 모양이 다른 경우**
  - 추출할 수 있는 함수
    - users라는 배열의 객채에서 name의 값만 추출하기
      ```js
      let users = [
        { name: 'Tim', age: 40 },
        { name: 'Satya', age: 30 },
        { name: 'Sundar', age: 50 }
      ];

      function getName (user) {
        return user.name;
      }
      getName({ name: 'Tim', age: 40 }) // 이것을 3번 반복해야함
      // 따라서
      users.map(getName) // ['Tim', 'Satya', 'Sundar']
      ```
### 4. 조건에 따라 걸러내기 (filter)
  **immutable하기 때문에 새로운 배열 return**
  - 객체에서 나이가 40 이상인 사람 걸러내기
    ```js
    let users = [
      { name: 'Tim', age: 40 },
      { name: 'Satya', age: 30 },
      { name: 'Sundar', age: 50 }
    ];

    let searchResults = [];
    for (let i = 0; i < users.length; i++) {
      if (users[i].age > 40) {
        searchResults.push(users[i])
      }
    }
    searchResults; // { name: 'Sundar', age: 50 }
    // filter를 이용하면
    function moreThan40 (user) {
      return user.age > 40
    }
    users.filter(moreThan40) // [{ name: 'Sundar', age: 50 }]
    ```
  - 이름에 S가 들어간 사람을 찾을 때
    ```js
    function includeS (user) {
      return user.name.indesOf('S') !== -1;
    }
    users.filter(includeS) // [{ name: 'Satya', age: 30 }, { name: 'Sundar', age: 50 }]
    ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## reduce (꽤 어려움)
- reduce의 작동 원리: 배열 축소

  array.reduce(reducer, [initalValue])
  - 전달 인자: 리듀서, 초기값

  ➡️ 리듀서 함수는 리턴값이 필요하며, 다음번 리듀서 호출 시 첫 번째 파라미터로 전달됨
  - 리턴 값: 리듀서가 마지막으로 리턴하는 값
  - 리듀서의 형태
    ```js
    function reducer (accumulator, value, index, array) {
      // accumulator에 값을 누적시킴
      return accumulator; // 새롭게 누적된 값
    }
    ```
    |리듀서의 구성요소|설명|
    |:------:|:---:|
    |누적값|배열의 요소를 하나하나 줄여가면서 생기는 중간 과정(결과)|
    |현재값|리듀서가 배열을 지나갈 때 만나는 배열의 요소|
    |초기값|배열의 요소를 줄이기 전, 누적값의 초기 상태|
  - reduce 활용 예제
    ```js
    [0, 1, 2, 3, 4].reduce(function (accumulator, value, index, array) {
      return accumulator + value;
    });
    ```
    |callback|accumulator|value|index|array|return|
    |:------:|:---:|:---:|:---:|:---:|:---:|
    |1번째 호출|0|1|1|[0, 1, 2, 3, 4]|1|
    |2번째 호출|1|2|2|[0, 1, 2, 3, 4]|3|
    |3번째 호출|3|3|3|[0, 1, 2, 3, 4]|6|
    |4번째 호출|6|4|4|[0, 1, 2, 3, 4]|10|

- 배열에서 문자열로 변형
  ```js
  let users = [
    { name: 'Tim', age: 40 },
    { name: 'Satya', age: 30 },
    { name: 'Sundar', age: 50 }
  ];

  let resultStr = '';
  for (let i = 0; i < users.length; i++) {
    resultStr = resultStr + users[i].name + ', ';
    return resultStr
  } // 'Tim, Satya, Sundar'

  // reduce 활용
  function joinName (resultStr, user) {
    resultStr = resultStr + user.name + ', ';
    return resultStr;
  }

  users.reduce(joinName, '');
  // 'Tim, Satya, Sundar'
  ```
- 배열에서 객체로 변형 (reduce로 주소록 객체 만들어보기)
  ```js
  let users = [
    { name: 'Tim', age: 40 },
    { name: 'Satya', age: 30 },
    { name: 'Sundar', age: 50 }
  ];

  // 1. 이름의 첫 번째 글자로 색인(key)을 만든다.
  // 2. 만약 key가 없으면, 해당 배열을 만들고 사람 추가
  // 3. 만약 key가 있으면, 해당 배열에 사람 추가

  function makeAddressBook (addressBook, user) {
    // 1. 이름의 첫 번째 글자로 색인(key)을 만든다.
    let firstLetter = user.name[0];
    // addressBook의 형태는 객체
    if (firstLetter in addressBook) {
      // 3. 만약 key가 있으면, 해당 배열에 사람 추가
      addressBook[firstLetter].push(user);
    } else {
      // 2. 만약 key가 없으면, 해당 배열을 만들고 사람 추가
      addressBook[firstLetter] = [];
      addressBook[firstLetter].push(user);
    }
    return addressBook;
  }

  // return 값
  {
    T: [{ name: 'Tim', age: 40 }],
    S: [{ name: 'Satya', age: 30 },
        { name: 'Sundar', age: 50 }]
  }
  ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## Scope
**코드의 작동 범위를 설정하는 것**
- Local Scope 안쪽에서 선언된 변수는 밖에서 사용할 수 없다.
  ```js
  let greeting = 'Hello';
  function greetSomeone () {
    let firstName = 'Josh';
    return greeting + ' ' + firstName;
  }

  greetSomeone(); // 'Hello Josh'
  firstName; // Reference Error
  ```
- Scope의 정의
  1. 변수는 어떠한 환경 내에서만 사용이 가능하고, 프로그래밍 언어는 각각의 변수 접근 규칙을 가지고 있다.
  2. 변수와 그 값이 어디부터 어디까지 유효한지 판단하는 범위이다.
  3. JavaScript는 기본적으로 함수가 선언되는(lexical) 동시에 자신만의 scope를 가진다.
- Local Scope vs Global Scope
  1. Local Scope에서 Global Scope의 변수/함수에 접근 가능
  2. Local Scope에서 정의된 변수/함수는 Global Scope에서 사용 불가
- Scope는 중첩이 가능

  ex) 함수 안의 함수
- Global Scope는 최상단의 scope로 전역 변수는 어디서든 접근 가능
- 지역변수는 함수 내에서 전역변수보다 더 높은 우선순위를 가짐
- Function Scope vs Block Scope
  - Block: 중괄호로 시작하고 끝나는 단위
    ```js
    if (true) {
      console.log('I am in the block!');
    }

    for (let i = 0; i < 10; i++) {
      console.log(i);
    }

    { console.log('it works!') }
    ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 변수
- var vs let
  - 변수를 정의하는 또다른 키워드 var
    - JavaScript는 기본적으로 **함수 단위**로 자신만의 scope를 가진다.

      ➡️ var (old way👎)
    - 그러나 Block 단위로 scope를 구분 했을 때 예측하기 쉬운 코드를 작성할 수 있다.

      ➡️ let
- const
  - **값이 변하지 않는** 변수, 즉 상수를 정의할 때 사용하는 키워드
    - let과 동일하게 Block Scope를 따른다.
    - 값을 재정의 하려고 하면 TypeError 출력
- 변수 선언 키워드
  ||let|const|var|
  |:------:|:---:|:---:|:---:|
  |유효 범위|Block Scope|Block Scope|Function Scope|
  |값 재정의|가능|불가능|가능|
  |재선언|불가능|불가능|**불**가능|

  ➡️ var의 재선언은 가능했으나 불가능으로 바뀜
- 전역변수와 window 객체
  - 전역 범위를 대표하는 객체 window
  - Global Scope에서 선언된 함수, 그리고 var 키워드를 이용해 선언된 변수는 window 객체와 연결
  - 콘솔창에 window를 입력하면 window 객체가 출력됨
    ```js
    var myName = 'Paul';
    console.log(window.myName); // 'Paul'

    function foo () {
      console.log('bar');
    }
    console.log(foo === window.foo); // true
    ```
  - 전역 범위에 너무 많은 변수를 선언하지 않도록 주의!

    ➡️ 전역 영역은 최상위 scope이기 때문에 어디서 어떻게 이용될지 모름
- 선언 없이 초기화된 전역 변수

  🔥**절대로 선언 키워드(var, let, const)없이 변수를 초기화하지 말 것**🔥
  ```js
  function showAge () {
    age = 90;
    console.log(age);
    // age는 전역 변수로 취급되어 age === window.age가 됨
  }

  showAge(); // 90
  console.log(age); // 90
  ```
  - 이런 실수를 방지하고 싶을 경우 **Strict Mode** 사용
    ```js
    'use strict';
    function showAge () {
      age = 90; // 여기서 에러 발생
        ...
    }
    ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## Closure (매우 어려움)
- 외부 함수의 변수에 접근할 수 있는 함수
  ```js
  function outerFn () {
    let outerVar = 'outer';
    console.log(outerVar);

    function innerFn () {
      let innerVar = 'inner';
      console.log(innerVar);
      console.log(globalVar);
    }
    return innerFn;
  }

  let globalVar = 'global';
  let innerFn = outerFn();
  innerFn();
  // outer
  // inner
  // global
  ```
  **여기서 클로저 함수는 `innerFn()`. 클로저 함수 안에서는 지역변수(innerVar), 외부 함수의 변수(outerVar), 전역변수(globalVar) 모두 접근 가능**
- 유용한 클로저 예제
  - 커링: 함수 하나가 n개의 인자를 받는 대신, n개의 함수를 만들어 각각 인자를 받게 하는 법
    ```js
    function adder(x) {
      return function (y) {
        return x + y;
      }
    }
    adder(2)(3); // 5

    let add100 = adder(100);
    add100(2); // 102
    add100(10); // 110

    let add5 = adder(5);
    add5(2); // 7
    ```
- 외부 함수의 변수가 저장되어 마치 템플릿 함수와 같이 사용 가능
  ```js
  function htmlMaker (tag) {
    let startTag = '<' + tag + '>';
    let endTag = '</' + tag + '>';
    return function (content) {
      return startTag + content + endTag;
    }
  }

  let divMaker = htmlMaker('div');
  divMaker('Hello'); // <div>Hello</div>
  divMaker('World'); // <div>World</div>

  let h1Maker = htmlMaker('h1');
  h1Maker('This is Headline'); // <h1>This is Headline</h1>
  ```
- 클로저 모듈 패턴

  ➡️ 변수를 스코프 안쪽에 가두어 함수 밖으로 노출시키지 않는 방법
  ```js
  function makeCounter () {
    let privateCounter = 0;
    return {
      increment: function () {
        privateCounter++;
      },
      decrement: function () {
        privateCounter--;
      },
      getValue: function () {
        return privateCounter;
      }
    }
  }

  let counter1 = makeCounter();
  counter1.increment();
  counter1.increment();
  counter1.getValue(); // 2

  let counter2 = makeCounter();
  counter2.increment();
  counter2.decrement();
  counter2.increment();
  counter2.getValue(); // 1
  ```
**임의로 privateCounter의 값을 변경할 수 없음**

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)

## 객체지향 JavaScript
- 객체 지향 프로그래밍?

  ➡️ 하나의 모델이 되는 청사진(class)을 만들고, 그 청사진을 바탕으로 한 객체(instance)를 만드는 프로그래밍 패턴
  ```js
  function Car (color) { // class
    let avante = new Car('blue'); // instance
    let mini = new Car('cyan'); // instance
    let beetles = new Car('red'); // instance
  }
  ```
  **class를 만들 때 함수의 이름은 대문자로 시작**
- class라는 키워드를 이용하여 정의할 수도 있음 (ES6)
  ```js
  class Car () {
    constructor(brand, name, color) {
      // instance가 만들어질 때 실행되는 코드
    }
  }
  ```
- 함수로도 정의 가능 (ES5)
  ```js
  function Car (brand, name, color) {
    // instance가 만들어질 때 실행되는 코드
  }
  ```
- new 키워드로 class의 instance를 만들 수 있다
  ```js
  let avante = new Car ('hyundai', 'avante', 'black');
  let mini = new Car ('bmw', 'mini', 'white');
  // 각 instance는 Car라는 class의 고유한 속성과 메서드를 갖는다.
  ```
- 속성과 메서드
  - class에 속성과 메서드를 정의하고 instance에서 이용함

    |속성|메서드|
    |:---:|:---:|
    |brand|refuel()|
    |name|setSpeed()|
    |color|drive()|

  ➡️ 이와 같이 OOP는 현실 세계를 기반으로 프로그래밍 모델을 만들 때 유용함
- class: 속성의 정의
  - ES5
    ```js
    function Car (brand, name, color) {
      this.brand = brand;
      this.name = name;
      this.color = color;
    }
    ```
  - ES6
    ```JS
    class Car () {
      constructor (brand, name, color) {
        this.brand = brand;
        this.name = name;
        this.color = color;
      }
    }
    ```
- class: 메서드의 정의
  - ES5
    ```js
    function Car (brand, name, color) {
      // 생략
      Car.prototype.refuel = function () {
        // 연료 공급 구현 코드
      }
      Car.prototype.drive = function () {
        // 운전 구현 코드
      }
    }
    ```
  - ES6
    ```js
    class Car () {
      constructor (brand, name, color) {
        // 생략
        refuel () {
          // 연료 공급 구현 코드
        }
        drive () {
          // 운전 구현 코드
        }
      }
    }
    ```
- instance에서의 사용
  ```js
  let avante = new Car ('hyundai', 'avante', 'black');
  avante.color; // black
  Car.prototype.drive = function () {
    console.log(this.name + '가 운전을 시작합니다.');
  }
  avante.drive(); // avante가 운전을 시작합니다.
  ```
- prototype? constructor? this?
  - prototype: 모델의 청사진을 만들 때 쓰는 원형 객체(original form)
  - constructor: instance가 초기화 될 때 실행하는 **생성자** 함수
  - this: 함수가 실행될 때, 해당 scope마다 생성되는 고유한 **실행 context(execution context)**.

    `new` 키워드로 instance를 생성했을 때 해당 instance가 this의 값이 됨
- 요약
  ```js
  function Car (brand, name, color) { // Car는 class
    this.brand = brand; // 여기서 this값은 avante
    this.name = name;
    this.color = color;
  }
  // 위 함수를 constructor(생성자) 함수라 함

  Car.prototype.drive = function () { // Car.prototype 까지를 prototype 객체라 함. 저기에 속성이나 메서드 정의 가능
    console.log(this.name + '가 운전을 시작합니다.');
  }

  let avante = new Car ('hyundai', 'avante', 'black');
  avante.color; // black
  avante.drive(); // avante가 운전을 시작합니다
  ```
- 실전 예제 - 배열
  ```js
  let arr = [1, 2, 3]
  let arr = new Array (1, 2, 3)
  // 위 두 코드는 완전히 같은 코드임
  ```

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 매개변수
  - 만약 전달인자(arguments)의 길이가 유동적이라면?
    ```js
    Math.max(3, 5, 8, 10); // 10
    Math.max(3, 5, 8, 10, 20); // 20
    Math.min(3, 5, 8, 10, 100, 1000); // 3
    ```
    - `Rest parameter`를 이용하여 `Math.max`와 같은 기능을 하는 함수 만들어 보기 (ES6)
      ```js
      function getMaxNum (...nums) { // rest parameter는 배열의 형태로 전달됨
        return nums.reduce (function (acc, cur) {
          if (acc > cur) {
            return acc;
          } else {
            return cur;
          }
        });
      }

      getMaxNum (3, 5, 8, 10); // 10
      ```
    - `arguments`라는 키워드도 이용 가능 (ES5)
      ```js
      function getMaxNum () {
        ...
        console.log(arguments); // { 0: 3, 1: 5, 2: 8, 3: 10 }
        ...
      }

      getMaxNum (3, 5, 8, 10); // 10
      ```
      arguments 객체는 배열의 형태지만 배열은 아님. 이를 **유사배열**이라함.
      ```js
      arguments[0]; // 3
      arguments[1]; // 5
      arguments[2]; // 8
      arguments[3]; // 10

      arguments.forEach // undefined
      ```
      **배열이 아니기 때문에 배열의 메서드 사용 불가**
- 매개변수에 기본값을 넣어주고 싶은 경우? (ES6)
  - Default Parameter를 할당해 줄 수 있음. 문자열/숫자/객체 등 어떤 타입이던 가능
    ```js
    function getRoute (destination, departure = 'ICN') {
      return '출발지: ' + departure + ',' + '도착지: ' + destination;
    }

    getRoute('PEK'); // '출발지: ICN, 도착지: PEK'
    ```
    ```js
    function getRoute (departure = 'ICN', destination) {
      return '출발지: ' + departure + ',' + '도착지: ' + destination;
    }

    getRoute(undefined, 'PEK'); // '출발지: ICN, 도착지: PEK'
    ```
    **중간에 기본 매개변수가 들어가는 경우, undefined로 넘겨줬을 때 기본값으로 처리함**
    
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 비동기 호출
- callback
  1. 다른 함수(A)의 전달인자(argument)로 넘겨주는 함수(B)
  2. parameter를 넘겨받는 함수(A)는 callback 함수(B)를 필요에 따라 즉시실행 or 나중에 실행 가능
  ```js
  function B () {
    console.log('called at the back');
  }

  function A () {
    callback(); // callback === B
  }
  A(B); // called at the back
  ```
- callback in action: 반복 실행 함수(iterator)
  ```js
  [1, 2, 3].map(function(element, index) {
    return element * element;
  });
  // [1, 4, 9]
  ```
- callback in action: 이벤트에 따른 함수(event handler)
  ```js
  document.querySelctor('#btn').addEventListener('click', function(e) {
    console.log('button clicked');
  });
  ```
🔥**헷갈리지 말 것**🔥
  ```js
  function handleClick () {
    console.log('button clicked');
  }

  document.querySelector('#btn').onclick = handleClick; // ⭕️
  document.querySelector('#btn').onclick = function() { // ⭕️
    handleClick();
  }
  document.querySelector('#btn').onclick = handleClick.bind(); // ⭕️
  document.querySelector('#btn').onclick = handleClick(); // ❌
  ```
  ❗️마지막이 틀린 이유는 **함수 실행을 연결하는 것이 아니라 함수 자체를 연결해야하기 때문**
- blocking vs non-blocking
  |전화|문자|
  |:---:|:---:|
  |하던 일을 멈추고 받아야함(blocking)|확인 후 나중에 답장 가능(non-blocking)|
  |요청에 대한 결과가 동시에 일어남(synchronous)|요청에 대한 결과가 동시에 발생 ❌(Asynchronous)|
- 커피 주문으로 알아보는 동기 vs 비동기
  - 만약 커피 주문이 동기적으로 작동한다면?
    1. 손님1이 아메리카노를 주문한다.
    2. 접수 받은 직원이 아메리카노를 내린다.
    3. 직원이 손님1에게 아메리카노를 전달한다.
    4. 손님2가 카페라떼를 주문한다. ➡️ 손님2는 손님1이 아메리카노를 받기 전까지 주문도 못하고 기다림
    5. 접수 받은 직원이 카페라떼를 만든다.
    6. 직원이 손님2에게 카페라떼를 전달한다.

  - 비동기적이라면?
    1. 손님1이 아메리카노를 주문한다.

      a-1. 접수 받은 직원이 아메리카노를 내린다.
      
      a-2. 아메리카노가 완성(이벤트)되면 직원이 손님1을 부른다. ➡️ callback
      
      a-3. 아메리카노를 손님1에게 전달한다.
      
    2. 손님2가 카페라떼를 주문한다.
    
      b-1. 접수 받은 직원이 카페라떼를 만든다.
      
      b-2. 카페라떼가 완성되면 직원이 손님2를 부른다. ➡️ callback
      
      b-3. 카페라떼를 손님2에게 전달한다.

    **a-1 ~ b-3이 비동기 영역임**
- 비동기적으로 커피 주문 해보기
  ```js
  function waitAsync (callback, ms) {
    setTimeout(callback, ms);
  }
  
  function drink (person, coffee) {
    console.log(person + '님 주문하신 ' + coffee + ' 나왔습니다');
  }

  let customers = [{
    name: 'Steve',
    request: '카페라떼'
  }, {
    name: 'John',
    request: '아메리카노'
  }];

  function orderCoffeeAsync (menu, callback) {
    console.log(menu + '가 접수되었습니다');
    waitAsync(function () {
      callback(menu);
    }, 2000);
  }

  customers.forEach(function(customer) {
    orderCoffeeAsync(customer.request, function(coffee) {
      drink(customer.name, coffee);
    });
  });

  // 카페라떼가 접수되었습니다
  // 아메리카노가 접수되었습니다
  // 2초 후
  // Steve님 주문하신 카페라떼 나왔습니다
  // John님 주문하신 아메리카노 나왔습니다
  ```
- 비동기 함수 전달 패턴 1: callback 패턴
  ```js
  let request = 'caffe latte';
  orderCoffeeAsync(request, function(response) {
    // response -> 주문한 커피 결과
    drink(response);
  });
  ```
- 비동기 함수 전달 패턴 2: 이벤트 등록 패턴
  ```js
  let request = 'caffe latte';
  orderCoffeeAsync(request).onready = function(response) {
    // response -> 주문한 커피 결과
    drink(response);
  }
  ```
- 비동기의 주요 사례
  - DOM Element의 이벤트 핸들러
    - 마우스, 키보드 입력(click, keydown 등)
    - 페이지 로딩(DOMContetLoaded 등)
  - 타이머
    - 타이머 API(setTimeout 등)
    - 애니메이션 API(requestAnimationFrame)
  - 서버에 자원 요청 응답
    - fetch API
    - AJAX(XHR)
- 브라우저의 비동기 함수 작동 원리를 알려면?
  - [Event Loop MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/EventLoop) 찾아보기

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 타이머 API
- setTimeout(callback, ms)
  - 일정 시간 후 함수 실행
  - arguments: 실행할 callback 함수, callback 함수 실행 전 기다려야 할 시간(밀리초)
  - return value: 임의의 타이머 ID
    ```js
    setTimeout(function () {
      console.log('1초 후 실행');
    }, 1000);
    ```
- setInterval(callback, ms)
  - 일정 시간의 간격을 가지고 함수를 반복적으로 실행
  - arguments: 실행할 callback 함수, 반복적으로 함수를 실행시키기 위한 시간 간격(밀리초)
  - return value: 임의의 타이머 ID
    ```js
    setInterval(function () {
      console.log('1초마다 실행');
    }, 1000);
    ```
- clearInterval(timer ID)
  - 반복 실행중인 타이머를 종료
  - arguments: 타이머 ID
  - return value: 없음
    ```js
    var timer = setInterval(function () {
      console.log('1초마다 실행');
    }, 1000);
    
    clearInterval(timer);
    ```
    ❗️setTimeout에 대응하는 clearTimeout도 있음
- 다음은 어떻게 나올까요?
  ```js
  console.log(1);
  setTimeout(function () {
    console.log(2);
  }, 1000);
  console.log(3);
  // 1, 3 ...1초 후... 2

  console.log(1);
  setTimeout(function () {
    console.log(2);
  }, 1000);
  setTimeout(function () {
    console.log(3);
  }, 0);
  console.log(4);
  // 이건 어떻게 나올까요?
  ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 서버 요청하기
- 서버와 클라이언트
  - 요청하는 주체: 클라이언트
  - 요청에 따른 응답을 주는 서버

  (이미지)
- 서버에게 요청하기
  - 일반적으로 서버에게 HTTP(URL) 요청 후, 응답을 처리
  - 응답은 다양한 형태로 받을 수 있음(JSON, HTML, Plain text 등)

  (이미지)
- HTTP 요청은 fetch API로
  ```js
  fetch('http://서버주소/weather?q=Seoul')
    .then(function (resp) {
      // 응답 형식에 따라 resp.text()가 될 수도 있다.
      return resp.json();
    })
    .then(function (json) {
      console.log(json); // {"temperature": 27}
    });
  ```
- API 사용 시 유의할 점
  - API는 공짜가 아니다

    ➡️ 서비스 제공자로부터 권한을 받아야 함
  - 그러므로 **API Key는 암호처럼** 취급되어야 함
- 서버에 기록 하려면?
  - HTTP 요청을 `GET`이 아닌 `POST`를 이용
  - 내용(payload)와 함께 전달
  - 예시
    - 게시판에 새로운 글을 쓰고자 할 때
    - 아이디와 비밀번호로 로그인을 하고자 할 때
- 게시판에 새로운 글을 쓰고자 할 때
  - 방법: `POST` 메서드
  - 주소: /posts
  - 내용

  (이미지)
  보통 새로운 글의 ID를 반환
  ```js
  let newPost = {
    "userID": 1,
    "title": "새 글을 써봤습니다",
    "body": "안녕하세요"
  }

  fetch('http://서버주소/posts', {
    method: 'POST'.
    body: JSON.stringify(newPost)
  }).then(function (resp) {
    return resp.json();
  }).then(function (json) {
    console.log(json); // { id: 123 }
  });
  ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## this
- Execution context(실행 콘텍스트)
  - 어떤 함수가 호출되면 실행 콘텍스트가 만들어진다.
    - call stack에 push ➡️ 불려진 순서대로 담긴다
    - 함수를 벗어나면 call stack에서 pop
  - function scope별로 생성
  - 여기에 담긴 것
    - scope 내 변수 및 함수(local, global)
    - 전달인자(arguments)
    - 호출된 근원(caller)
    - this
- `this` Keyword
  - 모든 함수 scope내에서 자동으로 설정되는 특수한 식별자
  - execution context의 구성 요소 중 하나로, 함수가 실행되는 동안 이용할 수 있다.

🔥**this의 4가지 패턴**🔥
  1. Global & Function Invocation
    ```js
    var name = 'Global Variable';
    console.log(this.name); // Global Variable

    function foo () {
      console.log(this.name);
    }
    foo(); // Global Variable

    function outer () {
      function inner () {
        console.log(this.name); // Global Variable
      }
      inner();
    }
    outer();

    function outer2 () {
      var closure = function () {
        console.log(this.name); // Global Variable
      }
      return closure;
    }
    outer2()();
    ```
  2. Method 호출: 부모 Object
    ```js
    var counter = {
      val: 0,
      increment: function () {
        this.val += 1;
      }
    };

    counter.increment();
    console.log(counter.val); // 1
    counter['increment']();
    console.log(counter.val); // 2

    var obj = {
      fn: function (a, b) {
        return this;
      }
    };
    var obj2 = {
      method: obj.fn
    };

    console.log(obj2.method() === obj2); // true
    console.log(obj.fn() === obj;) // true
    // obj2.method()가 실행되는 시점의 부모 = obj 따라서 true
    // obj.fn이 실행되는 시점의 부모 = obj 따라서 true
    ```
  3. Construction Mode(new 연산자로 생성된 function 영역의 this): 새로 생성된 객체
    ```js
    function F (v) {
      this.val = v;
    }
    // create new instance of F
    var f = new F('WooHoo!');

    console.log(f.val); // WooHoo!
    console.log(val); // Reference Error
    ```
  4. `.call` or `.apply` 호출: call, apply의 첫 번째 인자로 명시된 객체
    ```js
    function identify () {
      return this.name.toUpperCase();
    }

    function speak () {
      var greeting = "Hello, I'm " + identify.call(this);
      console.log(greeting);
    }

    var me = { name: "Kyle" };
    var you = { name: "Reader" };

    identify.call(me); // KYLE
    identify.call(you); // READER
    speak.call(me); // Hello, I'm KYLE
    speak.call(you); // Hello, I'm READER

    var add = function (x, y) {
      this.val = x + y;
    }
    var obj = {
      val: 0
    };

    add.apply(obj, [2, 8]); // 배열로 넘겨준다
    console.log(obj.val); // 10
    add.call(obj, 2, 8);
    console.log(obj.val); // 10

    let arr = [23, 1, 10, 4, 9, 35]
    Math.max.apply(null, arr) // 35
    ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## Prototype
- `Array.something();`과 `Array.prototype.something()`의 차이점?
  - `Array.something()`은 Array 클래스에서만 작동
  - `Array.prototype.something()`은 Array 인스턴스에서만 작동
    ```js
    let arr = [1, 2, 3, 4] // arr은 Array의 인스턴스
    // 위 아래는 같음
    let arr = new Array (1, 2, 3, 4)
    ```
- `prototype`이란?
  - 인스턴스가 생성(instantiation)될 때 원형(original form). 즉 prototype의 모양대로 인스턴스가 생성
  - 인스턴스의 메서드는 `Object.prototype.something()`으로 표현 prototype === 원형
- class란?
  - JavaScript는 prototype 기반 언어
  - prototype을 기반으로 객체 지향 프로그래밍(OOP)를 흉내냄
  - 문법적 편의로 class란 keyword를 도입(ES6)
- `prototype` 이해하기
  ```js
  function Car (model, brand) {
    this.model = model;
    this.brand = brand;
  }
  let spark = new Car ('spark', 'chevrolet');
  let avante = new Car ('avante', 'hyundai');

  Car.prototype.ride = function () {
    console.log('Vroooom! ' + this.model)
  };
  spark.ride(); // Vroooom! spark
  avante.ride(); // Vroooom! avante
  ```
  - JavaScript에서 기본적으로 제공되는 객체에 사용자 정의 메서드를 직접 추가할 수 있음(비추천)
  - 메서드 확장은 다른 코드와 충돌을 일으킬 수 있음
    ```js
    Number.prototype.invert = function () {
      return -(this);
    }
    let num = 5;
    num.invert(); // -5
    ```
    ```js
    Array.prototype.pluck = function (propertyName) {
      return this.map(function (el) {
        return el[propertyName];
      });
    }

    let arr = [
      { first: 'Yeongjae', last: "Shin" },
      { first: 'Gildong', last: 'Hong' }
    ];
    arr.plunk('first'); // ['Yeongjae', 'Gildong']
    ```
- `class` 키워드
  - class 키워드는 ES6에서 추가됨
    ```js
    class Car {
      constructor (model, brand) {
        this.model = model;
        this.brand = brand;
      }
      ride() {
        console.log('Vroooom! ' + this.model)
      };
    }

    let spark = new Car ('spark', 'chevrolet')
    spark.ride(); // Vroooom! spark
    ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 함수 메서드
- 함수를 실행하는 다양한 방법
  - function(method) 호출
  - new 키워드를 이용한 추출
  - 함수 메서드 `.call`, `.apply`, `.bind` 이용
- call, apply 복습
  ```js
  function add (x, y) {
    this.val = x + y;
    console.log(this.val);
  }

  let obj = { val: 0 };

  add.apply(obj, [2, 8]); // 10
  add.call(obj, 2, 8); // 10
  ```
- bind
  - call/apply와는 다르게 함수를 바로 실행시키지 않고, this값이 바인딩된 함수를 리턴
    ```js
    function add (x, y) {
      this.val = x + y;
      console.log(this.val);
    }

    let obj = { val: 0 };
    let boundFn = add.bind(obj, 2, 8); // call과 인자 순서 같음. boundFn은 함수가 됨
    boundFn(); // 10, add는 여기서 실행됨
    // 일반적인 function(method) 호출처럼 보이지만 이미 this 값이 바인딩 되어있음.
    ```
- apply case
  ```js
  let arr = [7, 35, 2, 8, 21]
  ```
  - 이 배열 중 가장 작은 값을 `Math.min`을 이용해 얻어내려면?
    ```js
    let minimum = Math.min.apply(null, arr);
    // this값이 의미가 없으므로, null로 넘겨도 됨. (Math는 constructor가 아니라 실행 context가 없음)
    console.log(minimum);
    ```
- call/apply case
  - call 또는 apply를 이용해 주체가 되는 인스턴스와 메서드의 순서를 바꿀 수 있음
    ```js
    function moreThanFive (element) {
      return element.length > 5;
    }

    let arr = ['abc', 'abcdef']
    arr.filter(moreThanFive); // ['abcdef'] -> 인스턴스(arr)가 먼저 등장하고 메서드(filter)가 뒤에 등장

    Array.prototype.filter.call(arr, moreThanFive); // ['abcdef']
    // 메서드(filter)가 먼저 등장하고 인스턴스(arr)가 나중에 등장
    // filter라는 Array 내장 메서드 사용
    // arr -> 다른 this(인스턴스) 지정
    ```
- call case
  - 배열 메서드를 유사 배열(array like object)에 적용시키고자 할 때 사용
    ```js
    // selected라는 이름의 class가 담긴 element를 filter 메서드를 이용해 찾고자 할 경우
    let list = document.querySelectorAll('li');
    list; // Nodelist(11) [li, li, li, li.selected, li ... ]
    list.filter(function (elementLi) {
      return elementLi.classList.contains('selected');
    }); // TypeError 발생
    // why? list.filter는 정의되지 않음(undefined) 그래서 실행되지도 않음(list는 유사배열이기 때문)
    ```
  - 메서드를 먼저 가술하고, 그 뒤에 인스턴스(this 인자)를 넘겨줌으로 해결
    ```js
    Array.prototype.filter.call(list, function (elementLi) {
      return elementLi.classList.contains('selected');
    }); // [li.selected]
    // Array.prototype.filter -> 프로토타입(원형, original form)으로부터 메서드 가져옴
    // list -> 유사 배열을 this에 넣어줌
    // function (elementLi) { ~ } -> filter의 첫 번째 인자인 콜백함수를 두 번째 인자로 넘김
    ```
- bind case: 특정 함수가 this 값을 바꿔버리는 경우
  ```js
  function Box (w, h) {
    this.width = w;
    this.heigth = h;

    this.getArea = function () {
      return this.width * this.height;
    }
    this.printArea = function () {
      console.log(this.getArea()); // 이 때 this는 b, 즉 Box라는 클래스의 인스턴스 b임. 실행하는 시점의 this
    }
  }

  let b = new Box (100, 50);
  b.printArea(); // 5000

  setTimeout(b.printArea, 2000); ❌ // 2초 후 b.printArea를 실행
  // TypeError 발생 -> this에 getArea라는 함수가 없는 것으로 보임. 그럼 this는? window 객체가됨
  setTimeout(b.printArea.bind(b), 2000); ⭕️
  ```
  >MDN에 의하면 setTimeout의 경우, 인자로 넘기는 함수의 this값은 기본적으로 window 객체가 바인딩됨.
  따라서, setTimeout에는 함수를 인자로 넘겨야 하며(**함수 실행을 넘기는게 아님**) this값이 window로 들어가지 않도록 명시적으로 this 값을 인스턴스 b로 지정해야함.
- bind case: 커링
  - 커링: **인자 여러개를 받는 함수**를 **인자 하나를 받는 함수**로 바꾸는 방법
    ```js
    function template (name, money) {
      return '<h1>' + name + '</h1><span>' + money + '</span>';
    }

    let tempSteve = template.bind(null, 'Steve'); // tempSteve함수의 name 파라미터에는 'Steve'라는 값이 이미 바인딩 되어있음.
    tempSteve(100); // <h1>Steve</h1><span>100</span>

    let tempJohnny = template.bind(null, 'Johnny'); // template이라는 함수에는 this 값을 사용하지 않으므로, 다른 특별한 값을 넣어줄 필요가 없음.
    tempJohnny(500); // <h1>Steve</h1><span>500</span>
    tempJohnny(1000); // <h1>Steve</h1><span>1000</span>
    ```
⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)
## 재귀함수
- 어떤 함수가 자기 자신을 호출하는 함수
  ```js
  // 팩토리얼 구하는 함수
  function fac (n) {
    if (n === 1) {
      return 1;
    }
    return n * fac(n - 1);
  }

  fac(5); // 120
  ```
- `fac(5)`는 5 * fac(4) ➡️ 4 * fac(3) ➡️ 3 * fac(2) ➡️ 2 * fac(1) ➡️ 1 순으로 진행
- 결국 5 * 4 * 3 * 2 * 1이 되어 120이 나옴

🎉🎉🎉**수고하셨습니다**🎉🎉🎉

⬆️ [목차로 가기](https://github.com/Yeongjae-Shin/JavaScriptSummary/blob/master/README.md#%EB%AA%A9%EC%B0%A8)