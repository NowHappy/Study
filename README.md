***
대상 : 초초초초초급자

들어가기에 앞서 Vue에 많은 편리한 기능이 있지만 모두 설명하지는 않음

현재 개발 환경에서 사용하고 있는 내용들만 간추림
(ex - vue ui 와 관련된 기능은 설명하지 않음)
***
# Vue.js 란 ? 
Vue.js is a progressive, incrementally-adoptable JavaScript framework for building UI on the web. http://vuejs.org
* Evan you가 구글에서 Angular 개발하다가 러닝 커브가 낮은 lite 한 javascript framework 를 만들어보자 해서 탄생
* 오픈 소스 Node module
* github URL : https://github.com/vuejs/vue

Home Link : https://kr.vuejs.org/index.html

Guide Link : https://kr.vuejs.org/v2/guide/

API Link : https://kr.vuejs.org/v2/api/#vm-data

* * *

현재 개발에서는 vue cli 를 통해 프로젝트를 생성하고 있음!
## 1. (Vue CLI로) Vue 프로젝트 생성하기
* https://kr.vuejs.org/v2/guide/installation.html#NPM

**Node version manager** 를 이용하여 다운받는 것을 ㅊㅊ
* node.js 다운로드
    * OSX : https://github.com/nvm-sh/nvm
    `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash`
    * windows : https://github.com/coreybutler/nvm-windows/releases

cf) npm(node package manager) ? Node.js에서 사용할 수 있는 모듈들을 패키지화하여 모아둔 저장소 역할과 패키지 설치 및 관리를 위한 CLI(Command line interface)를 제공 cf) java의 maven
* https://cli.vuejs.org/


## Intro
Vue instance 를 Dom instance의 심장이라고 표현. 
Dom instnace에 심장(Vue instance)이 연결(pluged in) 되어 있고 심장에서 변경된 데이터는 Dom에 reactive하게 반영됨

아주 간단한 예제 실습(특정 Dom instance와 연결된 Vue instance를 생성하고 데이터 변경에 reative 한 Dom instance 보기)
