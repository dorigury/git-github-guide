# git - github 설치 가이드 

## git 설치
- <https://git-scm.com/> 에서 설치 
- 설치과정에서 Git Bash 설치 (기본으로 설정)

### 설치후 버전 확인 
- git -v 

## SourceTree 설치
- <https://www.sourcetreeapp.com/> 에서 설치
- 건너뛰기 : Bitbucker Server, Bitbucker 설치하지 않음 (github 같은 원격저장소)
- 체크해제 : Mercurial 설치하지 않음 (git같은 프로그램)

## vscode 설치 
- <https://code.visualstudio.com/> 에서 설치

### 머티리얼 테마 설치
```
VS Code에서 파일 탐색기같은 방식으로 아이콘을 보이게 하려면
왼쪽의 확장 탭(블럭 모양 아이콘)에서 Material Icon Theme 테마를 검색하여 설치
```

## Git 최초 설정

### Git 전역으로 사용자 이름과 이메일 주소를 설정

- Git Bash, 또는 vscode 터미널에서
```
git config --global user.name "username"
git config --global user.name "username@gmail.com"
```

- 전역정보 확인
```
git config --global user.name
git config --global user.name
```

- 기본 브랜치명 변경
```
git config --global init.defaultBranch main 
```

## Git 프로젝트 설정
- 해당폴더에서 초기화 설정
```
git init 
```

- git으로 관리하지 않은 파일 등록
```
.gitignore 파일 생성해서 관리하지 않은 파일 등록
```

- 작업후 변경사항 확인 
```
git status
vscode u 표시는  untracked, m은 modified 의미 
```

- 작업후 변경사항 확인 
```
git status
vscode u 표시는  untracked, m은 modified 의미 
```

- 작업사항 등록하기 
```
git add . 
```

- 작업사항 저장하기 
``
git commit -m "first commit" 
```

## 원격저장소 사용하기

- github에 접속하기 
```
<https://github.com> 접속하고 가입하고 로그인하기 
```

- Personal access token 만들기
```
우측 상단의 프로필 - Settings
Developer Settings
Personal access tokens - Generate new token
repo 및 원하는 기능에 체크, 기간 설정 뒤 Generate token 
예를 들면 - repo기능과 무제한으로 설정
토큰 안전한 곳에 보관해 둘 것, 화면을 닫으면 다시 토큰값을 확인할 수 없음 
```

- 토큰 컴퓨터에 저장하기
```
Windows 자격 증명 관리자
Windows 자격 증명 선택
git:https://github.com 자격 정보 생성
사용자명과 토큰 붙여넣기
```

- GitHub에 새 Repository 생성
- 로컬에 원격저장소 추가 후 푸시 
```
git remote add origin https://github.com/dorigury/express_basic.git (원격저장소 주소)
git branch -M main
git push -u origin main
```

## git 원격저장소 명령 
- 원격 목록 보기
```
git remote 
자세히 보기 : git remote -v
```

- 원격 지우기 (연결만 없애는 것)
```
git remote remove https://github.com/dorigury/express_basic.git
```

## github에서 프로젝트 다운받기 
- 터미널이나 git bash에[서 대상폴더 이동후 ]
```
git clone https://github.com/dorigury/express_basic.git (원격저장소 주소)
```
