## Javascript 객체 및 객체 접근, map 함수, 객체 key, value 출력

---

 

자바스크립트의 객체는 {  …  } 중괄호를 사용해 객체를 생성한다. 

```jsx
let Obj = {
  name: "user",
  password: "asdf1234",
}
```

해당 객체 Obj에서 name, password 는 key 값이 된다. 그리고 “user”, “asdf1234”는 해당 키 값에 대한 value의 역할을 한다. 

### 명령어 접근법

```jsx
Obj.name // 'user'
```

### 이미 선언한 객체에 대한 key, value값 추가

```jsx
obj.email = "qwe@naver.com" // obj객체에 새로운 key, value 추가
obj.phone = 12345 // obj 객체에 새로운 값 추가
```

위와 같은 방법으로 객체의 프로퍼티를 추가 할 수 있다.

---

### 객체순회

### Object.keys()

- 해당 메소드는 어떤 객체가 가지고 있는 key들을 Array 형태로 리턴하는 메소드이다. 객체의 내장 메소드가 아닌 객체생성자인 Object가 직접 가지고 있는 메소드임.

```jsx
const obj = {
  name: 'kim',
  weight: 65,
  height: 180,
  sex: "man"
}

Object.keys(obj) // ['name', 'weight', 'height', 'sex'] 출력됨
```

- 반복문으로 해당 객체에 접근했을 때, 하나의 값이 아니라 해당 객체의 모든 key 값을 출력한다.

### Object.values()

- 해당 메소드는 어떤 객체가 가지고 있는 value의 값을 출력한다.

```jsx
const obj = {
  name: 'kim',
  weight: 65,
  height: 180,
  sex: "man"
}

Object.keys(obj) // ['kim', 'weight', 'height', 'sex'] 출력됨
```

- Object.key() 메소드와 같이 객체에 접근시, 하나의 값이 아니라 해당 객체의 모든 values를 출력한다.

### for-in

- for 문과 같은 종류의 문법이지만, 객체와 배열을 위해 특별히 존재하는 ES6에서 추가된 문법이다.

```jsx
const obj = {
  name: 'melon',
  weight: 4350,
  price: 16500,
  isFresh: true
}
for (let key in obj) {
  console.log(`${key} ${obj[key]}`)
  
}
아래 결과가 출력됨
/*
'name melon'
'weight 4350'
'price 16500'
'isFresh true'
*/
```

- 해당 반복문에서는 객체를 for-in문으로 사용하면 해당 인덱스에 변수들이 문자열로 할당받게 됨
