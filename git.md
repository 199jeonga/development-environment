# 로컬 파일에 있는 파일 레파지토리와 연결하기

## create-react-app으로 생성한 폴더를 git repository와 연결하여 업로드

1. 깃허브에 레파지토리를 생성
2. 로컬에 프로젝트 생성

- (create-react-app을 통해 프로젝트 생성)

3. 프로젝트 폴더로 이동
4. cra로 생성한 프로젝트는 git이 이미 존재하므로 .git을 삭제

- `rm -r .git`
- `rm -rf .git`

5. git 환경 생성

- `git init`

6. 레파지토리를 remote로 등록

- `git remote add origin [레파지토리 주소]`

7. `git add .`
8. `git commit -m "커밋내용 입력"`
9. `git push --set-upstream origin main`

📍 git push 오류

```
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/199jeonga/wazzang.git'
```

위와 같은 오류가 확인 된다면!
파일 손상 우려 때문에 push를 멈췄다는 에러메세지이다.
현재 단계에서는 파일 손상을 걱정하지 않아도 되기 때문에 강제로 push를 진행해주면 됨!

```
git push origin +main
```
