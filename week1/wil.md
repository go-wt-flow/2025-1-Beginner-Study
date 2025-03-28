## 개발 입문 스터디 1주차

#### 1. Git을 사용하는 이유
개발을 하다 보면 여러 개의 파일을 관리하고 코드의 변경 사항을 추적하는 것이 중요하다. 특히 여러 명이 협업하는 환경에서는 코드가 언제, 어떻게, 누구에 의해 수정되었는지 알 수 있어야 한다. 이를 위해 버전 관리를 돕고 협업을 지원하는 Git을 사용하는 것이다. 

#### 2. Git의 기본 개념
Git에는 다음 세 가지 영역이 있다.
* Working Directory: 실제 작업 중인 파일이 있는 공간
* Staging Area: 커밋 전 변경 사항을 임시 저장하는 공간
* Repository: .git 디렉토리, 모든 커밋 내역이 저장되는 공간

다음은 파일의 상태 4가지이다.
* Untracked: 파일이 처음 만들어진 상태, 아직 버전 관리 안됨
* Unmodified: 마지막 커밋 이후 수정된 적 없는 파일
* Modified: 마지막 커밋 후 수정이 일어난 파일
* Staged: 커밋을 할 때 버전으로 만들어질 파일

#### 3. Git의 기본 명령어
* 파일 추가 및 관리
    + git init: git 저장소 초기화
    + git add . : 모든 파일 한 번에 등록
    + git add <파일명> : 특정 파일만 등록
    + git rm --cached <file> : unstage로 되돌리기
* 커밋
    + git commit : 파일 수정 후 로컬 저장소에 등록
    + git commit -m "커밋 메세지"
* 커밋 메세지 작성 규칙
    + feat: 새로운 기능 추가
    + fix: 버그 수정
    + refactor: 코드 개선
    + chore: 코드 외 설정 수정
    + docs: 문서화
    + test: 테스트 코드 추가

#### 4. GitHub를 사용하는 이유
GitHub는 Git 저장소를 원격으로 관리할 수 있도록 도와주는 서비스로, 협업을 위해 필수적이다. 또한, 이슈 트래킹, 코드 리뷰, 프로젝트 업무 관리 등의 기능들도 이용할 수 있다.

#### 5. 실습
GitHub에 Remote Repository를 만들어 Local Repository와 연결했다. 그리고 자기소개를 적은 README.md 파일을 커밋하여 GitHub에 업로드했다. 이 과정을 통해 Git과 GitHub 활용 방법을 익힐 수 있었다.
