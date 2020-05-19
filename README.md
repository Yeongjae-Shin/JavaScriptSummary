# 자바스크립트 정리
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
    - forEach 구문 (명령형 반복문을 함수형으로 작성하기)
    **함수를 인자로 받음**
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
      1. for...in 구문의 본문은 객체의 각 프로퍼티에 대해 한번씩 실행된다.
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
        // name: 0; value: 10 name: 1; value: 11 name: 2; value: 12
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
객체는 키와 값으로 이루어져 있고, 그 사이는 콜론(:)으로 구분한다. 중괄호를 이용하여 객체를 생성하고 각 개체는 쉼표(,)로 구분
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
# reduce (꽤 어려움)
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