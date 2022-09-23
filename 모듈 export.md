> **require(), exports, module.exports**
> 

- require()는 함수이다.

```jsx
// require 함수
var require = function(src){                 //line 1
    var fileAsStr = readFile(src)            //line 2
    var module.exports = {}                  //line 3
    eval(fileAsStr)                          //line 4
    return module.exports                    //line 5
}
```

해당 내장함수를 사용하게 되면, module.exports를 리턴하게 된다.

```jsx
// app.js
const num1 = 500;
```

num1을 app.js 가 아닌 `foo.js에서 호출`했다.

```jsx
// foo.js
console.log(num1) // undifined 
```

당연스럽게 `undifined`가 발생한다.

- 해결을 위해서 `모듈을 호출`한다.

```jsx
// foo.js
const app = require('./app.js');
console.log(app.num1); // require로 모듈을 불러와도 undifined가 출력된다.
```

- 해당 과정에서 undifined가 출력되는 이유는 app.js에 exports 가 없기 때문임.

위에 `require함수`는 src를 인자로 받기 때문에

```jsx
const app = require('./app.js');
```

`app.js`파일을 인자로 가져오게 된다.

---

### 다른 방법으로 함수 내보내기

```jsx
const num1 = 1;

// 안내보낼 때
const getName = name => {
	return name;
}

// export 1
export const getName = name => {
	return name;
}

**// export 2**

const getName = name => {
	return name;
}
export {getName};

**// export 3 ES6 이전 문법**
const getName = name => {
	return name;
}

module.exports = {
	getName
}
```

require 함수 사용 말고도 `import` 를 통해 해당 함수모듈을 가져올 수 있다

```jsx
const app = require('./app.js');

import { getName } from './app.js';
```

### refs.

 [https://medium.com/@chullino/require-exports-module-exports-공식문서로-이해하기-1d024ec5aca3](https://medium.com/@chullino/require-exports-module-exports-%EA%B3%B5%EC%8B%9D%EB%AC%B8%EC%84%9C%EB%A1%9C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-1d024ec5aca3)
