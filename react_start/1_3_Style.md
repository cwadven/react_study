# React style 및 css를 이용해보자

## I. 직접 JSX에 style 적용

style이라는 객체를 만들어서 CSS와 유사한 코드를 작성

CSS에 '-' 가 들어갈 부분에 '-'를 없애고 그 바로 다음 문자를 대문자로 작성하면 JSX에서 사용하는 Style<br>
(해당 형태를 카멜 형태라고 함)

> **( 예 )**

**`CSS`**
~~~
{
    background-color : 'black';
    padding : 10px;
}
~~~

**`JSX`**
~~~
{
    backgroundColor : 'black',
    padding : '10px'
}
~~~

### 코드

**`App.js`**

```javascript
import './App.css';
import {Fragment} from 'react';

function App() {
  let home = "우리집";
  let style = {
    backgroundColor: 'yellow',
    padding: '10px',
  }
  return (
    <Fragment>
      <div style={style}>
        분리시키자1{home}
      </div>
      <div>
        분리시키자2{home}
      </div>
    </Fragment>
  );
}

export default App;
```

### 결과

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq04.PNG" alt="react" width="300"/><br><br>


## II. CSS를 이용하여 Style 변경

1. 가장 위에 CSS를 외부에서 가져온다.

**`App.js`**

```javascript
import './App.css';
```

2. 원해는 태그에 해당 class CSS를 적용시키고 싶은 경우, className을 만들어서 App.css에 있는 클래스 중 하나를 직접 문자열로 대입한다.

### 코드

**`App.js`**

```javascript
import './App.css';
import {Fragment} from 'react';

function App() {
  let home = "우리집";
  let style = {
    backgroundColor: 'yellow',
    padding: '10px',
  }
  return (
    <Fragment>
      <div className="App" style={style}>
        분리시키자1{home}
      </div>
      <div>
        분리시키자2{home}
      </div>
    </Fragment>
  );
}

export default App;
```

### 결과

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq004.PNG" alt="react" width="450"/><br><br>