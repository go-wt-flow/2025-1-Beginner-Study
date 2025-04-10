## 개발 입문 스터디 3주차

#### 1. commit 관련
- git log
    + commit 기록을 최신순으로 확인
    + git commit --oneline: 각 커밋 한줄 요약

- commit id
    + commit 식별자 (SHA-1 해시 기반 40자리 16진수)

- HEAD
    + 현재 작업 중인 브랜치의 가장 최신 commit
    + 브랜치 변경시, 변경한 브랜치의 가장 최신 commit을 가르킴
    + 새로운 commit이 생기면 HEAD도 변경

- git status
    + untracked/modified/staged 로 분류하여 확인 가능

#### Commit 되돌리기
- amend
    + reset 없이 최신 커밋 내용 수정하기
    + 아예 새로운 커밋으로 대체된 것이라 commit ID 변경
    + vim으로 진입해 commit 메시지 수정
    + git commit --amend -m "commit message": vim 진입 없이 commit message 수정하기
    + git commit --amend --no-edit: commit message 수정 없이 commit 수정
    + 주의) 다른 사람이 작업 기반으로 삼은 commit amend 금지!

- reset
    + commit 제거
    + format: git reset '--option' "<commit id>"

- reset --soft
    + commit은 사라지고 변경 사항은 Staging Area로
- reset  --mixed
    + commit은 사라지고 변경 사항은 Working Directory로
    + default option
- reset --hard
    + commit과 변경 사항 모두 제거하고 이전 커밋으로 돌아감

- revert
    + commit을 제거하지 않고 되돌림
    + 되돌리기 위한 새로운 commit 생성
    + --edit: 편집기 진입 (default)
    + revert --no-edit: 편집기 진입 없이 바로 revert
    + revert --no-commit: 바로 커밋되지 않고 revert 내용을 Staging Area에 올림

- reset vs revert
    + reset은 commit을 제거하므로 위험!
    + commit 공유하는 다른 브랜치에도 영향
    + commit 삭제보다 commit 생성하여 되돌리는 revert가 더 안전
    + 협업 시 revert 사용 권장