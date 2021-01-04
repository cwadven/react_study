# React 첫걸음 시작하기 App.js

## I. React 기본틀

~~~
src -> App.js
~~~

1. **return 규칙**

- return 안에 들어가는 값은 큰 `<div></div>` 안에 종속 되어야 한다!

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq1.PNG" alt="react" width="500"/><br><br>

- 만약 `<div></div><div></div>` 같은 형식을 이용하고 싶을 경우, 가장 바깥에 큰 `<div></div>`로 감싸야한다.

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq2.PNG" alt="react" width="500"/><br><br>

- 큰 `<div></div>`로 감싸기 싫을 경우 `<Fragment></Fragment>`라는 태그를 사용해야한다.
    - Fragment를 사용할 경우 위에 `import {Fragment} from 'react';`를 넣어줘야 한다!

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq3.PNG" alt="react" width="500"/><br><br>


2. **변수를 JSX에 넣어보자**

변수의 값을 이용하여 JSX에 값을 표현하고 싶을 경우!<br>
(js 코드를 JSX에 표현하고 싶을 경우!)

return 값 바로 위에 선언을 하고 JSX에 {}로 묶고 그 안에 해당 변수명을 넣는다.

- 코드

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq03.PNG" alt="react" width="500"/><br><br>

- 결과

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq003.PNG" alt="react" width="300"/><br><br>