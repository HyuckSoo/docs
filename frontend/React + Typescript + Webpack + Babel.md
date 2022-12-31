# 1. Basic React + Typescript + Webpack5

### Structure Looks like

````
project
   - build // 정적인 폴더 리액트 파일 -> 번들 (webpack) -> 트랜스퍼 (babel) 해서 만들 페이지
   - src // 리액트 소스 파일들 넣을 폴더
      | App.tsx
      | index.tsx
      | index.html
   - .babelrc / babel 설정 파일
   - .package.json / package 관리 파일
   - .tsconfig.json / typescript 설정 파일
````
### 초기설정
````
mkdir <projectName>
cd <projectName>
npm init --y // create package.json
yarn add react react-dom
yarn add -D typescript @types/react @types/react-dom
tsc --init // create tsconfig.json
yarn add -D @babel/core @babel/preset-env @babel/preset-react @babel/preset-typescript
yarn add -D webpack webpack-cli webpack-dev-server html-webpack-plugin
yarn add -D babel-loader
````
---
# Babel 이란?

자바스크립트 컴파일러

왜 인터프리터 언어에 컴파일러가 필요하지? 라는 의문이 들 수 있다.

정확히 바벨은 javascript 로 결과물을 만들어주는 컴파일러이다. 혹은 소스 투 소스 컴파일러 (transpiler) 라고도 부른다.

그렇다면, Babel 은 왜! 필요한가. 현재 프론트엔드의 시장 및 발전은 너무 빠르다. 심지어 최신 브라우저 조차도 지원하지 못하는 문법과 여러 기술들이 난무한다. (es5, es6, ESNext!!!! ESNext and Legacy...)

이러한 새로운 ESNext 의 문법을 기존 브라우저에 사용하기 위해서 Babel 은 필수적이다.

> 결론, Babel 은 javascript 의 새로운 문법을 지원하는 혹은 안하는 브라우저 간의 호환을 돕기 위한 트랜스파일러이다.