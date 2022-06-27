# react 개발환경 구축

create-react-app을 사용하여 react 개발환경 구축

---

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

[react 문서 확인하기](https://ko.reactjs.org/docs/create-a-new-react-app.html#create-react-app)

```
npx create-react-app [folder name]
```

proxy환경에서 node.js설정
