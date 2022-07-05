### **JSX란?**

JSX는 JavaScript XML의 줄임말로 문자열도 아니고 HTML도 아니다.<br>
React에서 UI를 구성할 때 사용하는 문법으로 `JavaScript를 확장한 문법`이다.

JSX는 JavaScript가 확장된 문법이지만, 브라우저가 바로 실행할 수 있는 JavaScript 코드가 아니기 때문에 브라우저가 이해할 수 있는 코드로 변환을 해주어야 한다. 이때 이용하는 것이 `Babel`이다.<br>
Babel은 JSX를 브라우저가 이해할 수 있는 JavaScript로 컴파일 하고 그 후에 JavaScript를 브라우저가 읽고 화면에 렌더링할 수 있다.

JSX는 JavaScript의 공식적인 문법이라고할 수는 없고 JavaScript에서 HTML을 작성하듯이 비슷하게 작성할 수 있도록 해 주는것이 JSX의 가장 큰 장점이자 사용하는 이유이다.

> **JSX 문법의 특징 및 준수사항**

- 컴포넌트에 여러 요소가 있다면 반드시 부모 요소 하나가 감싸는 형태여야 한다.

```js
function App() {
  return (
    <h1>Hello</h1>
    <h2>World</h2>
  )
}
```

위 처럼 요소가 두 개이상 존재하므로 그것을 감싸는 요소가 있어야 한다.<br>
_위는 에러가 발생한다._

```js
function App() {
  return (
    <div>
      <h1>Hello</h1>
      <h2>World</h2>
    </div>
  );
}
```

이처럼 바깥을 div로 감싸는 이유는, 리액트가 사용하는 Virtual DOM 방식에서는 컴포넌트 변화를 감지할 때 효율적으로 비교하고자 `컴포넌트 내부는 하나의 DOM 트리 구조로 이루어져야 한다는 규칙`이 있기 때문이다.

> name의 값을 {name} 과 같이 넣어서 렌더링할 수 있다.

```js
import React from "react";

function App() {
  const name = "이름";

  return (
    <>
      <h1>{name}</h1>
      <h2>이름</h2>
    </>
  );
}

export default App;
```

> JSX내부의 JavaScript 표현식 내에서 if문을 사용할 수 없어서, 조건부 연산자(삼항 연산자)를 사용한다.

```js
function App() {
  const name = "이름";

  return <div>{name === "이름" ? <h1>Hello</h1> : <h2>World</h2>}</div>;
}
```
