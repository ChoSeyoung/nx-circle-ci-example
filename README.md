# Nx Mono Project Example with Circle-Ci

<a alt="Nx logo" href="https://nx.dev" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/nrwl/nx/master/images/nx-logo.png" width="45"></a>

## 전체 서버 실행 방법
```shell
npx nx run-many --target=serve --all
```

## 독립 서버 실행 방법
```shell
# ex-user 서버를 실행하고 싶은 경우
npx nx serve ex-user
# ex-item 서버를 실행하고 싶은 경우
npx nx serve ex-item
# ex-shared 서버를 실행하고 싶은 경우
npx nx serve ex-shared
```

## 서버 추가 방법
```shell
npx nx generate @nrwl/nest:application ex-shared --directory=apps
```
위 명령어 실행 후 ${추가된서버}/src/main.ts 에 기본포트를 변경해야합니다.

## Circle CI 빌드
```shell
npx nx affected --target=build --parallel
```
