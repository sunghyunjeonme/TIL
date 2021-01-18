# Array 배열

> 드림코딩 강의로 선회하여 강의 노트를 정리

![rabbit_carrot](./images/rabbit_carrot.png)

🐰 : 토끼라는 '오브젝트'는 귀 두 개, 동물이라는 프로퍼티와 먹는다와 같은 메서드로 구성되어 있다.

🥕 : 당근이라는 '오브젝트'는 채소, 주황색, 비타민 C라는 프로퍼티로 구성되어 있으며 오브젝트는 당근처럼 프로퍼티만 존재하고, 메서드는 없을 수도 있다.

![rc_in_basket](./images/rc_in_basket.png)

위의 사진처럼 🐰와 🥕을 🧺 안에 정리해서 보다 효율적이고 체계적으로 관리할 수 있는데, 이렇게 비슷한 것들끼리 🧺 안에 묶어서 관리하는 것을 프로그래밍 언어에서는 `자료 구조 📚`라고 한다.

🐰와 🥕이 너무 많다면, 토끼와 당근을 🧺 안에 담아 놓을 수도 있다. 일상생활에서 비슷한 물건을 `한 곳🧺`에 담아 놓는 것처럼 프로그래밍 언어에서도 비슷한 것들끼리 묶어서 보관하는데 이를 `자료구조(data structure) 📚(`라고 부른다.

`자료구조(data structure) 📚`에는 어떤 방식으로 어떤 형식으로 데이터를 담느냐에 따라서 다양한 방법이 존재한다. (Array, Tuple, Linked list, Hash table 등)

자료구조를 충분히 이해하고, 그에 따라서 프로그래밍을 한다면 좋은 소프트웨어를 만들 수 있을 것이다.

## 1. 선언

```js
const arr1 = new Array();
const arr2 = [1, 2];
```

## 2. 접근

```js
const fruits = ["사과", "오렌지", "자두"];
alert(fruits[0]); // 사과
alert(fruits[1]); // 오렌지
alert(fruits[2]); // 자두
```

위와 같은 방법으로 요소를 수정할 수도 있다.

```js
fruits[2] = "배"; // 배열이 ["사과", "오렌지", "배"]로 바뀜
```

요소를 추가할 수도 있다.

```js
fruits[3] = "레몬"; // 배열이 ["사과", "오렌지", "배", "레몬"]으로 바뀜
```

`length`를 사용하면 배열에 담긴 요소의 개수를 알 수 있다.

```js
let fruits = ["사과", "오렌지", "자두"];

alert(fruits.length); // 3
```

**배열 요소의 자료형엔 제약이 없다.**

```js
// 요소에 여러 가지 자료형이 섞여 있습니다.
let arr = [
  "사과",
  { name: "이보라" },
  true,
  function () {
    alert("안녕하세요.");
  },
];

// 인덱스가 1인 요소(객체)의 name 프로퍼티를 출력합니다.
alert(arr[1].name); // 이보라

// 인덱스가 3인 요소(함수)를 실행합니다.
arr[3](); // 안녕하세요
```

### 배열 메서드

**pop**

배열 끝 요소를 제거하고, 제거한 요소를 반환한다.

```js
let fruits = ["사과", "오렌지", "배"];

alert(fruits.pop()); // 배열에서 "배"를 제거하고 제거된 요소를 얼럿창에 띄웁니다.
alert(fruits); // 사과,오렌지
```

**push**

배열 끝에 요소를 추가할 수 있다.

```js
let fruits = ["사과", "오렌지"];
fruits.push("배");
alert(fruits); // 사과, 오렌지, 배
```

**shift**

배열의 앞 요소를 제거하고, 제거한 요소를 반환한다.

```js
let fruits = ["사과", "오렌지", "배"];

alert(fruits.shift()); // 배열에서 "사과"를 제거하고 제거된 요소를 얼럿창에 띄웁니다.

alert(fruits); // 오렌지,배
```

**unshift**

배열의 앞에 요소를 추가한다.

```js
let fruits = ["오렌지", "배"];

fruits.unshift("사과");

alert(fruits); // 사과,오렌지,배
```

아래와 같이 요소 여러 개를 한 번에 더할 수도 있다.

```js
let fruits = ["사과"];

fruits.push("오렌지", "배");
fruits.unshift("파인애플", "레몬");

// ["파인애플", "레몬", "사과", "오렌지", "배"]
alert(fruits);
```