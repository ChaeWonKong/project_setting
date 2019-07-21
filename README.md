# Setting up Node Projects

## Git and .gitignore
.gitignore 파일 생성

```bash
$ curl "http://gitignore.io/api/git,node,macos,windows,visualstudiocode" > .gitignore

# Git Repository 생성
$ git init
```

## Node
먼저 nvm을 설치한 후, 현재 Node는 10.16.0이 LTS 버전이므로, 10.16.0 버전을 설치.

```bash
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
$ nvm install 10.16.0
```

node 10.16.0 버전을 사용하도록 .nvmrc 파일을 설정한 후 nvm use 명령을 통해 해당 nvm 설정을 적용.
```bash
$ echo "10.16.0" > .nvmrc
$ nvm use
```

## NPM
최근 npm이 기능이 많이 개선되어, 굳이 yarn을 사용할 필요가 없을 것으로 판단됨. 일관성을 위해 npm을 사용하면 좋을 것 같음.

프로젝트 생성
```bash
$ npm init
```
입력 필드가 계속 뜨는데, 엔터를 치면서 넘어가면 됨.
계속 엔터를 치다 보면 끝이 나고 해당 디렉토리에 package.json 파일이 생성된 것을 확인할 수 있음.

## VS Code

preference > settings에서 settings.json을 찾은 후, 다음 코드를 추가.

```json
"[javascript]": {
    "editor.formatOnSave": true
  }
```
파일을 저장할 때마다 자동으로 포멧이 맞춰짐.

## Express 설치
```bash
$ npm i express```