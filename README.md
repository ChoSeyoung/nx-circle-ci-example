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

## CircleCI 프로젝트 설정
CircleCI 웹사이트에 접속하여 로그인합니다.

로그인 후, GitHub 또는 다른 VCS 계정을 CircleCI와 연결합니다.

연결된 계정에서 원하는 리포지토리를 선택합니다.

선택한 리포지토리에서 Set Up Project를 클릭하여 CircleCI 프로젝트 설정을 시작합니다.

이미 리포지토리의 루트에 .circleci/config.yml 파일이 있는 경우, 

CircleCI는 이를 자동으로 감지하고 파이프라인을 실행합니다.

## 빌드 실행
설정된 브랜치로 코드를 푸시하면, CircleCI가 자동으로 첫 빌드를 실행합니다.

CircleCI 대시보드에서 빌드 상태를 확인할 수 있습니다. 

빌드가 성공적으로 완료되었는지, 실패했는지 확인할 수 있으며, 만약 실패했다면 로그를 통해 문제를 파악할 수 있습니다.
