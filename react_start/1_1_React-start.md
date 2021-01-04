# React 기초 사용 및 빌드 방법

## I. React 초기 구축 환경 설정

1. **Node.js 설치** --> [Node.js 설치 링크](https://nodejs.org/ko/download/ "Node.js 설치 링크")
2. **yarn 설치** --> [yarn 설치 링크](https://classic.yarnpkg.com/en/docs/install#windows-stable "yarn 설치 링크")
3. **코드 에디터 설치** --> [VSCode 설치](https://code.visualstudio.com/ "VSCode 설치")

VSCode Extense(확장)에서 설치

- auto close tag
- auto rename tag
- path intellisense

4. **터미널에서 prettier 설치**
~~~
$ yarn add prettier --save-dev --save-exact
$ yarn add eslint-plugin-prettier eslint-config-prettier --save-dev
~~~

위의 터미널로 설치 완료 후

VSCode Extense(확장)에서 추가 설치

- ESlint
- Prettier

5. **Ctrl + , 를 눌러 오른쪽 종이 모양 클릭**

<img src="https://github.com/cwadven/react_study/blob/master/assets/seq0.PNG" alt="drawing" width="500"/><br><br>

settings.json 에 아래 코드 추가

~~~
"editor.formatOnSave": false,
// Enable per-language
"[javascript]": {
    "editor.formatOnSave": true
},
"editor.codeActionsOnSave": {
    // For ESLint
    "source.fixAll.eslint": true
}
~~~

6. **create-react-app 이라는 것 다운로드**
~~~
$yarn global add create-react-app
~~~

## II. React 프로젝트 시작

1. **리엑트 프로젝트 생성**

create-react-app으로 react를 생성하는 경우, react가 기본으로 필요한 라이브러리들을 자동으로 다운로드 해준다.

~~~
$create-react-app 프로젝트이름
~~~

2. **리엑트 프로젝트 실행**

~~~
$cd 프로젝트이름
$yarn start
~~~

3. **완료 못한 prettier, eslint 연결하기**

프로젝트 안에 .eslinrc.json 파일을 생성 후, 아래 코드 작성 후 저장

~~~
{
    "plugins": ["prettier"],
    "extends": ["eslint:recommended", "plugin:prettier/recommended"],
    "rules": {
      "prettier/prettier": "error"
    }
}
~~~

프로젝트 안에 .prettierrc.json 파일을 생성 후, 아래 코드 작성 후 저장

~~~
{
    "trailingComma": "es5", // 여러개 콤마 중 마지막에 콤마를 할 것인지
    "tabWidth": 4, // 들여쓰기 
    "semi": true, // 붙부분에 ; 붙여주는지
    "singleQuote": true // "" 이런거를 작은 따옴표로 혹은 큰 따옴표
}
~~~