# react 개발환경 구축

_create-react-app을 사용하여 react 개발환경 구축_

react는 개발 프레임워크가 아닌 라이브러리이기 때문에 필요한 기술이나 기능을 설치하여 사용해야 한다. (webpack, babel 등) 하지만 create-react-app을 사용하여 환경을 구축하면 따로 설치할 필요없이 필요한 기능들을 바로 사용할 수 있다.

---

## node.js 설치

create-react-app을 사용하기에 앞서 node.js(node, npm, npx)가 설치되어 있어야 한다.
[node.js 설치하기](https://nodejs.org/en/)

- LTS는 안정적인 지원을, Current는 신기술 지원을 약속함.
- node.js를 설치하면 npm(node pakage manager)가 자동으로 설치되므로 따로 설치할 필요가 없다.

```
node -v
npm -v
npx -v
```

설치를 진행한 후 `-v` 명령어를 통해 설치여부 및 버전을 확인할 수 있다.

## create-react-app을 통한 react 폴더 생성

[react 문서 확인하기](https://ko.reactjs.org/docs/create-a-new-react-app.html#create-react-app)

```
npx create-react-app [folder name]
```

<details>
<summary>proxy환경에서 node.js설정</summary>

create-react-app을 실행했을 때 아래와 같은 오류가 확인되었다.

```
npm ERR! code ERR_SOCKET_TIMEOUT
npm ERR! network Socket timeout
npm ERR! network This is a problem related to network connectivity.
npm ERR! network In most cases you are behind a proxy or have bad network settings.
npm ERR! network
npm ERR! network If you are behind a proxy, please make sure that the
npm ERR! network 'proxy' config is set properly.  See: 'npm help config'

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/jeonga/.npm/_logs/2022-06-27T04_25_22_210Z-debug-0.log
```

해결방법은 두가지가 있음.

**첫번째 방법**

```
npm config set proxy http://:
npm config set https-proxy http://:
```

**두번째 방법**

```
npm config set proxy false
npm cache clean --force
```

</details>

## 실행

```
cd [folder name] // 해당 폴더로 이동
npm start // 로컬 환경에서 개발모드를 확인하기 위해 실행하는 명령어
```

npm start를 사용하면 브라우저를 통해 `http://localhost:3000/` 가 열리고 코드 수정 시 바로 화면으로 확인할 수 있다.

## 폴더 생성 후 필요없는 코드 삭제 및 수정

- css, logo.svg 삭제
- title, favicon, mata 코드 수정

## 라이브러리 설치

프로젝트에 필요한 라이브러리 설치

```
npm i [react-router-dom etc.]
```

- react-router-dom
- styled-components
