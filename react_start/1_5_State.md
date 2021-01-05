# React state를 이용해 보자

## I. state 적용 (함수형)

상태를 바꾸거나 할 경우 사용한다

Onclick 같은 상황에 어떤 값을 변경하려고 하는 경우

function react를 이용하는 경우 useState를 import 해서 사용한다.

### 코드

```javascript
import './App.css';
import {Fragment, useState} from 'react';

function App() {
  const [count, setCount] = useState(0);

  return (
    <Fragment>
      <div>숫자는 {count}</div>
      <button onClick={() => setCount(count + 1)}>
        더하기
      </button>
      <button onClick={() => setCount(count - 1)}>
        빼기
      </button>
    </Fragment>
  );
}

export default App;
```

### 결과

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq12.PNG" alt="react" width="450"/><br><br>


## II. state 적용 (클래스형)

Component를 import 받은 후, 그것을 App에 extend 시킨다.

클래스를 정의하고 state라는 객체를 선언하고, 해당 state를 바꿀 때는 setState를 이용하여 바꾼다.

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq10.PNG" alt="react" width="450"/><br><br>