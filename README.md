## 설치 할 항목
 - Node.js : 리액트 프로젝트를 준비하기 위해 필요한 webpack, babel 등의 도구들을 실행하는데에 사용됩니다.
 - Yarn : 자바스크립트 패키지를 관리하기 위해서 사용됩니다. Node.js 를 설치하면 npm 이 설치되어서 npm 으로 해도 되긴 하지만, yarn을 사용하면 훨씬 빠릅니다.
 - Code Editor (VS Code, Atom, ...) : 코드 에디터는 여러분이 좋아하는걸 사용하시면 됩니다. 저는 VS Code 를 사용하여 강의를 진행하겠습니다. 

## Windows 
### Node.js 
https://nodejs.org/ko/ 에 들어가서 좌측 LTS 버전을 설치하면 됩니다
### Yarn
https://yarnpkg.com/en/docs/install#windows-tab 에 들어가서 인스톨러를 사용하여 설치하세요.
### Git Bash
일반 CMD 대신에 Bash 시뮬레이터를 사용하는것이 정신 건강에 좋습니다.
https://git-scm.com/download/win 에 들어가서 본인의 운영체제 (32 / 64) 에 맞는 인스톨러를 사용하여 설치하세요.
### VS Code
https://code.visualstudio.com/ 에 들어가서 설치하세요

## macOS
### nvm 설치
nvm 은 노드 버전 관리 매니저입니다. 이 도구를 통해 설치하는것이 편합니다.
```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash
```
그 다음, `source ~/.bash_profile` 명령어를 사용하거나 터미널을 재시작하여 새 .bash_profile 을 적용하세요.

`nvm --version` 을 실행해서 제대로 설치됐는지 확인하세요.

만약에 nvm 이 실행되지 않을 경우, vim 으로 `.bash_profile` 파일을 열어서 다음 라인들을 추가해주세요

```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
```

그 다음 터미널을 다시 열거나 `source ~/.bash_profile` 을 하시면 됩니다.

이 명령어를 실행하면 최신 LTS 버전이 설치됩니다.
```
nvm install --lts
nvm list
nvm alias default [현재버전]
# 예: nvm alis default v6.10.1
```

### Yarn 설치
brew 를 사용하여 yarn 을 설치합니다. 만약에 Homebrew 가 설치되어있지 않다면 다음 명령어를 통해 설치하세요.
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

yarn 을 설치합니다
```
brew update
brew install yarn
```

### VS Code
https://code.visualstudio.com/ 을 통하여 설치하면 됩니다.

## Linux
리눅스는 워낙 버전이 많아서.. 가장 흔히 사용되는 우분투를 예를들어서 진행하겠습니다.

### nvm 설치
nvm 은 노드 버전 관리 매니저입니다. 이 도구를 통해 설치하는것이 편합니다.
```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash
```
그 다음, `source ~/.bash_profile` 명령어를 사용하거나 터미널을 재시작하여 새 .bash_profile 을 적용하세요.

`nvm --version` 을 실행해서 제대로 설치됐는지 확인하세요.

만약에 nvm 이 실행되지 않을 경우, vim 으로 `.bash_profile` 파일을 열어서 다음 라인들을 추가해주세요

```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
```

그 다음 터미널을 다시 열거나 `source ~/.bash_profile` 을 하시면 됩니다.

이 명령어를 실행하면 최신 LTS 버전이 설치됩니다.
```
nvm install --lts
nvm list
nvm alias default [현재버전]
# 예: nvm alis default v6.10.3
```

### Yarn 설치
```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```
다른 리눅스 distro 는 https://yarnpkg.com/en/docs/install#linux-tab 를 참고하세요.

### VS Code 설치
이 페이지를 참고하세요: https://code.visualstudio.com/docs/setup/linux
