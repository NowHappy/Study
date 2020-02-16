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

### cf) what is node js?
Node.js is a JavaScript runtime that is useful for both server and desktop applications.
Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficent.
-> A runtime environment for executing JavaScript code
ex) JRE(Java Runtime environment) = JVM + libraries + other files

https://github.com/nodejs/node/blob/master/BUILDING.md
Node.js relies on V8 and libuv. We adopt a subset of their supported platforms.

#### what is V8?
구글에서 만든 자바스크립트 엔진
what is Javascript engine?
자바스크립트 코드를 기계어로 번역해주는 소프트웨어
ex) microsoft Edge - chakra, firefox - spiderMonkey, chrome -V8

#### what is libuv?
https://github.com/libuv/libuv
이벤트 루프를 기반으로 논블로킹 비동기 I/O를 지원하는 다중 플랫폼 C 라이브러리

==> 한마디로 정리하면 javascript로 작성된 코드를 windows나 OSX, unix, Android 등 OS에서 실행시켜주는 소프트웨어

탄생 비화 : 2009년에 라이언 달(Ryan Dahl)이 자바스크립트를 브라우저 밖에서도 썼으면 좋겠다고 생각해서  C++ 프로그램에 V8 엔진을 넣어서 만든게  Node.exe

===> 노드는 JRE같은 건데 JVM 말고 V8엔진 자바 라이브러리 대신 libuv 가 있는거라고 생각하면 된다. 그리고 리뷰 라이브러리의 특징(이벤트 루프를 기반으로 논블로킹 비동기 I/O를 지원)을 가진다. 

#### Node에서 추천/비추천
이벤트 루프를 기반으로 논블로킹 비동기 I/O를 지원하기때문에 IO intensive 한 앱 개발엔 추천!(디스크나 네트워크 Access가 많은 앱 / 서버가 많지 않아도 반응성 유지에 좋음)
하지만 노드는 싱글 쓰레드 기반이기 때문에 쓰레드가 사용중이면 나머지 작업들은 기다려야 함. 그래서 비디오 인코딩이나 이미지 수정과 같은 CPU insentive 한 앱 (CPU가 처리해야하는 계산이 많고 file system이나 network 작업은 적은)에는 비추천!

### cf) npm(node package manager) ? 
* Node.js에서 사용할 수 있는 모듈들을 패키지화하여 모아둔 저장소 역할과 패키지 설치 및 관리를 위한 CLI(Command line interface)를 제공 (java의 maven과 유사한 소프트웨어)
* Node.js프로젝트의 2대 BDFL이었던 아이작 슐레터가 오픈소스 프로젝트로 시작(참조 : https://terms.naver.com/entry.nhn?docId=3580502&cid=59088&categoryId=59096)
* https://cli.vuejs.org/


## 간단한 동작 확인
* https://www.vuemastery.com/courses/intro-to-vue-js/vue-instance/
  * Vue instance 를 Dom instance의 심장이라고 표현
  * 심장(Vue instance)에서의 변화가 reactive하게 Dom instnace에 반영됨
    * 특정 el(Dom element)에 연결된(pluged in) Vue instance를 생성
    * Vue instance의 데이터 값이 변경되면 Dom instnace에도 reative하게 반영됨
