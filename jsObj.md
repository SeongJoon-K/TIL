### for-of (key의 value 반복)

- 반복가능한 객체 Array에 주로 씀 (Array, Map, Set, String…)

```jsx
const arr = ["하나", "둘", "셋"];

for(const num of number) {
    console.log(num);
}
```

### for-in (key 반복)

- Object 객체 반복시 사용

```jsx
const obj = {
  lion: "사자",
  tiger: "호랑이",
  rabbit: "토끼",
};

for (let property in obj) {
  console.log(`${property} : ${obj[property]}`);
}
```

### forEach 멈출수 없음

- Array에서만 사용이 가능함
- return 값이 존재하지 않음
- 원본 데이터에 영향을 주지 않는다.
- 해당 배열에 있는 인자에 대해서 함수 적용

```jsx
const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element));

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

### map

- Array에서만 사용이 가능함
- return 값이 존재함
- 해당 배열에 변화를 주고자 한다면 map을 사용해야함.

### Object.entries

- 객체에서 사용이 가능하다
- key, value 쌍이 배열행태로 출력이 된다.

```jsx
const obj = {
  lion: "사자",
  tiger: "호랑이",
  rabbit: "토끼",
};

console.log(Object.entries(obj));

// 출력됨 [ [ 'lion', '사자' ], [ 'tiger', '호랑이' ], [ 'rabbit', '토끼' ] ]
```

### Object.keys

- 객체에서 key 값을 모두 가져옴

```jsx
const obj = {
  lion: "사자",
  tiger: "호랑이",
  rabbit: "토끼",
};

console.log(Object.keys(obj));
// 출력값 [ 'lion', 'tiger', 'rabbit' ]
```

### Object.values

- 객체에서 value 값을 모두 가져옴

```jsx
const obj = {
  lion: "사자",
  tiger: "호랑이",
  rabbit: "토끼",
};

console.log(Object.values(obj));
// 출력값 [ '사자', '호랑이', '토끼' ]
```

### 

**.push()** : 배열의 맨 끝에 값을 추가한다.

**.unshift()** : 배열의 맨 앞에 값을 추가한다.