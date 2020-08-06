# Node.js & NPM

## Node.js
Node.js는 브라우저 밖에서도 자바스크립트를 실행할 수있는 환경을 의미

## NPM(Node Package Manager)
NPM은 명령어로 JS(javascript) library를 설치하고 관리할 수 있는 패키지 매니저입니다
전 세계 JS 개발자들이 JS library를 공개된 저장소에 올려놓고 간편하게 NPM 명령어로 다운로드 받을수 있습니다


###  Why use NPM ?
NPM이 만들어진 역사는 모듈 패키징이 엉망으로 완성되는것을 보고 패키지를 잘 관리하기 위해서 만들었다 NPM을 사용하면 쉽게 버전관리를 할수 있으며 번거로운 작성과정을 생략하고 간편하게 명령어로 library를 다운로드 받을수 있습니다 이것으로 인해 우리는 모듈 패키징을 좀더 쉽고 간편하게 할수있어서 사용합니다

### NPM local install & NPM global install
- local install  
  해당 프로젝트에 생성  

  <strong>option</strong>  
```
// 앱에 로직에 관련된,앱을 동작 시킬때 필요한 프로그램,화면 로직에 집적전인 연관(배포용 라이브러리)
//npm install library --save-prod,
//npm i library (축약)

dependencies : {
  "react" : "version",
  "vue" : "version",
  "angular" : "...",
  "jquery" : "..." ,
  .......
}

//개발을 할때 도움을 주는, 개발용 라이브러리, 개발보조(개발용 라이브러리)
//npm install library --save-dev,
//npm i library -D (축약)

devDependencies : {
  "webpack" : "...",
  "sass": "...",
  "js-compression; : "...",
  ......
}
```

- global install  
해당 프로젝트에서 사용하는게 아닌 시스템 레벨에서 사용할 라이브러리를 설치할떄 사용된다  
```
npm install library --global
npm i libary -g
```
