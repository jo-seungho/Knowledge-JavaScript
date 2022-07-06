**저장소 복사**

> git clone [리포지토리 주소]

- 원격 리포지토리를 내 로컬에서 이용할 수 있도록 복사한다.

**저장소 생성**

> git init

- 선택한 폴더에 로컬 Git저장소를 설정한다.

**현재 상태 확인**

> git status

- 현재 작업 중인 파일의 상태를 확인한다.
- 내 로컬로 복사해 온 디렉토리의 commit 되기 전 까지의 상태를 표시
- 내 로컬의 staging area 목록 확인 가능

**현재 상태 추적**

> git add [원하는 파일명]

- Untracked files 를 Staging area 로 추가해서 Git 의 관리하에 둔다
- Staging area에 모든 파일을 한번에 추가하고 싶은 경우 파일명 대신 [ . ] 입력

**현재 상태 저장**

> git commit [-m "원하는 메세지 입력"]

- 수정 작업이 끝났을 때 변경 사항을 저장

**처음 clone 상태로 복귀**

> git restore [파일명]

- commit 혹은 staged 되지 않은 로컬 리포지토리의 변경 사항을 폐기

**커밋 내용 삭제**

> git reset [HEAD^]

- Local에서 commit 한 내용을 취소할 때
- HEAD^ 입력시 가장 최신의 commit을 취소한다

**작업 내용 받아오기**

> git pull [short name] [branch]

**업로드**

> git push [origin] [branch]

- Local에서 변경, commit된 사항을 Remote Repository에 업로드

**커밋 기록확인**

> git log

- 현재까지 commit 된 내역들을 터미널 창에서 확인 가능
