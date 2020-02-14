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
## (Vue CLI로) Vue 프로젝트 생성하기
* https://kr.vuejs.org/v2/guide/installation.html#NPM
* node.js 다운로드(**Node version manager** 를 이용하여 다운받는 것을 ㅊㅊ)
    * OSX : https://github.com/nvm-sh/nvm
      * `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash`
    * windows : https://github.com/coreybutler/nvm-windows/releases
      * `nvm-setup.zip` 파일 추천

cf) npm(node package manager) ? Node.js에서 사용할 수 있는 모듈들을 패키지화하여 모아둔 저장소 역할과 패키지 설치 및 관리를 위한 CLI(Command line interface)를 제공 (java의 maven과 유사한 소프트웨어)
* https://cli.vuejs.org/


## 간단한 동작 확인
* https://www.vuemastery.com/courses/intro-to-vue-js/vue-instance/
  * Vue instance 를 Dom instance의 심장이라고 표현
  * 심장(Vue instance)에서의 변화가 reactive하게 Dom instnace에 반영됨
    * 특정 el(Dom element)에 연결된(pluged in) Vue instance를 생성
    * Vue instance의 데이터 값이 변경되면 Dom instnace에도 reative하게 반영됨