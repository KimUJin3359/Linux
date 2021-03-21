# Linux

### 운영체제
- Windows : PC시장 지배
- 리눅스 : 서버, 임베디드 OS 시장 지배
- Android : 리눅스로 만들어진 Mobile OS
- MacOS : 유닉스로 만들어진 Apple OS

### 리눅스란
- OS가 아닌 커널
  - OS 자체가 아닌, OS의 핵심 소스코드 역할인 커널
  - OS = App + Shell + Kernel
- 리눅스에 App, Shell을 추가하여 만든 하나의 운영체제를 리눅스 배포판이라 함

#### 우분투란
- 리눅스 배포판 중 가장 널리 쓰이는 배포판

#### 리눅스의 활용
- 서버
  - 2020년 기준 Unix + Linux가 서버의 70% 차지
  - W3Techs.com 자료에는 Linux가 Unix 계열이기에 Unix로 표기
    - Unix : C 언어 제작자가 만든 OS, 이 계열에 대표적으로 iOS, macOS, Linux 등이 있음
    - Linux : Unix 계열 운영체제로, 리누즈토발즈가 Unix를 토대로 만든 OS
- 모바일 OS
  - iOS : Unix 계열
  - Android : Linux 계열
- 임베디드 OS
  - 임베디드 운영체제는 Non-OS, RTOS, Linux 등이 사용
  - 고성능 임베디드 장치에는 Linux가 자주 쓰임
  - 임베디드 회사의 Linux 사용 이유
    - 구글링 시 레퍼런스가 많이 존재
    - 개발자를 구하기 쉬움
    - 무료이면서 역사로 검증된 안정성 보유
  - Linux를 사용하지 않는 이유
    - Linux를 동작하는 HW를 구성하는데 임베디드 제품 단가가 올라감

### 패키지 관리 시스템
- 예시
  - iOS의 앱스토어
  - Android의 플레이스토어
- 역할
  - 프로그램 설치
  - 다운로드
  - 실행
  - 제거
- 리눅스의 패키지 관리 시스템
  - 빌드 완료된 바이너리 패키지라면 그대로 실행
  - 소스코드 패키지라면 빌드 후 사용
- 우분투 패키지 관리 시스템
  - APT
    - 바이너리 형태로 배포
    - 소스코드 형태로 배포
  - Gnome Software
    - 바이너리 형태로 배포

### 리눅스 파일시스템
- 파일시스템이란
  - 파일을 관리하는 방법
- 리눅스에서 폴더 = Directory
- 우분투 GUI에서는 폴더라고 부름

| Windows | Linux |
| --- | --- |
| Program Files | /bin |
| Windows\System | /sbin |
| 사용자 | Home |

- 링크 파일 : 윈도우의 바로가기

### 리눅스 쉘 프로그래밍

| GUI(Graphic UI) | CLI(Command Line Interface) |
| --- | --- |
| 그래픽 기반 | 글자 기반|

- CLI의 장점
  - GUI OS는 버전 업그레이드 시 UI가 바뀌나, CLI 명령어는 거의 비슷
  - 편리한 CLI 패키지 설치도구
- 단축키
  - 복사 : Ctrl + Insert
  - 붙여넣기 : Shift + Insert
  - 터미널 화면 멈추기 : Ctrl + S
  - 터미널 화면 재생 : Ctrl + Q
- 명령어
  - ls : 디렉토리 명령보기
    - a옵션 : all, 숨김파일까지 출력
    - l옵션 : list, 리스트 형태로 상세 표시
  - pwd : 현재 디렉토리 확인
  - clear : 화면 지우기
  - cd : 디렉토리 이동하기
  - touch : 새로운 빈 파일을 생성 / 이미 존재하는 파일이라면, 변경된 시간을 업데이트
  - rm : 파일을 삭제
    - r옵션 : 디렉토리 내부 파일까지 모두 삭제
  - mkdir : 디렉토리 생성
    - p옵션 : 디렉토리 하위메뉴까지 모두 한꺼번에 생성
  - rmdir : 디렉토리 삭제
  - mv : 파일 이동
  - cp : 파일 복사
    - r옵션 : 디렉토리 복사 
  - apt install : 패키지 설치
  - apt list : 전체 패키지 목록 확인
    - --installed옵션 : 설치된 패키지 확인
  - apt show "패키지이름" : 패키지 정보 확인
  - apt purge : 패키지 삭제
  - apt remove : 설정 파일은 남겨두고, 파일을 삭제

| apt | apt-cache | apt-get |
| --- | --- | --- |
| apt-cache와 apt-get의 기능을 합친 멍령어 | 패키지 검색, 상세정보 확인 | 패키지 설치, 삭제 |

### VI editor

| vi | vim |
| --- | --- |
| 40년 전 만들어진 editor | vi 업그레이드 버전 |
| 키보드 방향키가 없어 h, j, k, l을 방향키 대용으로 사용 | 방향키 사용 |
| 기본 설치 | apt install vim을 이용한 설치 필요 |

- :w : 저장
- :q : 종료

#### visual 모드
- v를 눌러 visual 모드 진입 가능
- y : 복사
- p : 붙여넣기
- u : 실행취소
- ctrl + r : 다시 실행

#### command 모드
- G : 맨 아랫줄로 이동
- gg : 맨 윗줄로 이동
- dd : 한 줄 삭제
- /찾을단어 : 검색
  - n : 다음 검색
  - shift n : 이전 검색
- %s /찾을단어/바꿀단어/g
  - 찾을 단어를 전체 

#### Edit 모드
- i를 눌러 모드 진입 가능

### Shell
- 사용자와 커널 사이의 인터페이스
  - 컴퓨터를 키면 OS가 부팅된 후 실행됨
  - 사용자는 Shell을 통해서 커널에 명령
  - Shell을 통해서 명령에 대한 결과 확인
-  인터페이스
  - 사용자가 쉽게 동작 및 사용하는데 도움을 주는 시스템

#### 정의
- Shell은 프로그램
  - 운영체제 내부에 접근하기 위한 프로그램
  - 커널을 감싼다는 의미에서 껍데기라는 용어를 사용
