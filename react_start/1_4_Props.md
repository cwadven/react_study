# React props를 알아 보자

## I. props 사용

props는 자신이 받아온 this.의 키워드를 조회 할 수 있다.

**`MyName.js`** 이라는 새로운 컴포넌트를 만들어 보자 (class로 만들어 보았다)

```javascript
import React, { Component } from 'react';

class MyName extends Component {
  render() {
    return (
      <div>
        안녕하세요! 제 이름은 <b>{this.props.name}</b> 입니다.
      </div>
    );
  }
}

export default MyName;
```

이렇게 this.props.name을 통해서 **`App.js`**에 해당 컴포넌트를 작성하는데,

그 태그에 name="" 해서 넣으면 **`MyName.js`**에서 this.props.name으로 접근 가능하다.

**`App.js`**

```javascript
import React, { Component } from 'react';
import MyName from './MyName';

class App extends Component {
  render() {
    return (
      <MyName name="리액트" />
    );
  }
}

export default App;
```

- **결과**

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq13.PNG" alt="react" width="300"/><br><br>


## II. defaultProps 사용

아래 코드와 같이 만약 **`App.js`**에 있는 MyName 태그에 name을 넣지 않았을 경우 defaultProps에 있는 값이 들어간다!

1. 방법 1

```javascript
import React, { Component } from 'react';

class MyName extends Component {
  static defaultProps = {
    name: '기본이름'
  }
  render() {
    return (
      <div>
        안녕하세요! 제 이름은 <b>{this.props.name}</b> 입니다.
      </div>
    );
  }
}

export default MyName;
```

1. 방법 2
```javascript
import React, { Component } from 'react';

class MyName extends Component {
  render() {
    return (
      <div>
        안녕하세요! 제 이름은 <b>{this.props.name}</b> 입니다.
      </div>
    );
  }
}

MyName.defaultProps = {
  name: '기본이름'
};

export default MyName;
```

**추가**

- **함수형 컴포넌트**

```javascript
import React from 'react';

const MyName = ({ name }) => {
  return (
    <div>
      안녕하세요! 제 이름은 {name} 입니다.
    </div>
  );
};

export default MyName;
```