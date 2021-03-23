# Linux

## 목차
- [운영체제](https://github.com/KimUJin3359/Linux#%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C)
- [리눅스란](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4%EB%9E%80)
- [패키지 관리 시스템](https://github.com/KimUJin3359/Linux#%ED%8C%A8%ED%82%A4%EC%A7%80-%EA%B4%80%EB%A6%AC-%EC%8B%9C%EC%8A%A4%ED%85%9C)
- [리눅스 파일시스템](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4-%ED%8C%8C%EC%9D%BC%EC%8B%9C%EC%8A%A4%ED%85%9C)
- [리눅스 쉘 프로그래밍](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4-%EC%89%98-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)
- [쉘이란](https://github.com/KimUJin3359/Linux#shell)
- [사용자 계정](https://github.com/KimUJin3359/Linux#%EC%82%AC%EC%9A%A9%EC%9E%90-%EA%B3%84%EC%A0%95)
- [사용자 그룹](https://github.com/KimUJin3359/Linux#%EC%82%AC%EC%9A%A9%EC%9E%90-%EA%B7%B8%EB%A3%B9)
- [파일과 소유권](https://github.com/KimUJin3359/Linux#%ED%8C%8C%EC%9D%BC%EA%B3%BC-%EC%86%8C%EC%9C%A0%EA%B6%8C)
- [파일 권한 이해하기](https://github.com/KimUJin3359/Linux#%ED%8C%8C%EC%9D%BC-%EA%B6%8C%ED%95%9C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)
- [리눅스 배포방법](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4-%EB%B0%B0%ED%8F%AC%EB%B0%A9%EB%B2%95)
- [VI Editor](https://github.com/KimUJin3359/Linux#vi-editor)

---

### 운영체제
- Windows : PC시장 지배
- 리눅스 : 서버, 임베디드 OS 시장 지배
- Android : 리눅스로 만들어진 Mobile OS
- MacOS : 유닉스로 만들어진 Apple OS

---

### 리눅스란
- OS가 아닌 **커널**
  - OS 자체가 아닌, OS의 핵심 소스코드 역할인 커널
  - **OS = App + Shell + Kernel**
- 리눅스에 App, Shell을 추가하여 만든 하나의 운영체제를 리눅스 배포판이라 함

#### 우분투란
- 리눅스 배포판 중 **가장 널리 쓰이는 배포판**

#### 리눅스의 활용
- 서버
  - 2020년 기준 Unix + Linux가 서버의 70% 차지
  - W3Techs.com 자료에는 Linux가 Unix 계열이기에 Unix로 표기
    - Unix : C 언어 제작자가 만든 OS, 이 계열에 대표적으로 iOS, macOS, Linux 등이 있음
    - Linux : Unix 계열 운영체제로, 리누즈토발즈가 Unix를 토대로 만든 OS
- 모바일
  - iOS : Unix 계열
  - Android : Linux 계열
- 임베디드
  - 임베디드 운영체제는 Non-OS, RTOS, Linux 등이 사용
  - 고성능 임베디드 장치에는 Linux가 자주 쓰임
  - 임베디드 회사의 Linux 사용 이유
    - 구글링 시 **레퍼런스가 많이 존재**
    - 개발자를 구하기 쉬움
    - 무료이면서 역사로 검증된 안정성 보유
  - Linux를 사용하지 않는 이유
    - Linux를 동작하는 HW를 구성하는데 임베디드 **제품 단가**가 올라감
  - **Busy Box**
    - 리눅스 기본 명령어 모음
  - GUI shell이 없는 리눅스 커널 + CLI shell + Busy Box

---

### 패키지 관리 시스템
- 예시
  - iOS의 앱스토어
  - Android의 플레이스토어
- 역할
  - 프로그램 설치
  - 다운로드
  - 실행
  - 제거

#### 리눅스의 패키지 관리 시스템
- 빌드 완료된 바이너리 패키지라면 그대로 실행
- 소스코드 패키지라면 빌드 후 사용
- 우분투 패키지 관리 시스템
  - APT
    - 바이너리 형태로 배포
    - 소스코드 형태로 배포
  - Gnome Software
    - 바이너리 형태로 배포

---

### 리눅스 파일시스템
- 파일시스템이란
  - **파일을 관리**하는 방법
- 리눅스에서 폴더 = **Directory**
- 우분투 GUI에서는 폴더라고 부름

  | Windows | Linux |
  | --- | --- |
  | Program Files | /bin |
  | Windows\System | /sbin |
  | 사용자 | Home |

- 링크 파일 : 윈도우의 바로가기

---

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

#### 명령어(쉘 명령어, /bin에 존재)
- ls : 디렉토리 명령보기
  - -a : all, 숨김파일까지 출력
  - -l : list, 리스트 형태로 상세 표시
  - -h : 용량을 보기 쉬운 K, G 단위로 나타냄
- pwd : 현재 디렉토리 확인
- clear : 화면 지우기
- cd : 디렉토리 이동하기
- touch : 새로운 빈 파일을 생성 / 이미 존재하는 파일이라면, 변경된 시간을 업데이트
- rm : 파일을 삭제
  - -r : 디렉토리 내부 파일까지 모두 삭제
- mkdir : 디렉토리 생성
  - -p : 디렉토리 하위메뉴까지 모두 한꺼번에 생성
- rmdir : 디렉토리 삭제
- mv : 파일 이동
- cp : 파일 복사
  - -r : 디렉토리 복사 
- echo : 문자열 출력(쉘 스크립트 명령어)
- cat : 파일 내용을 출력
- find : 파일을 찾는 명령어 
  - find [경로] -name [파일명]
  - 파일명 wild card 사용 가능
  - -type f : 파일만 찾기
  - -type d : 디렉토리만 찾기
- grep : 문자열 검색
  - grep [찾을내용] [경로]
  - -r : 내부 디렉토리에 있는 파일들도 모두 검색
- history : 이전 기록들을 확인
  - ![번호] : 기록된 명령어를 그대로 수행
- ping : 네트워크 신호 
- date : 현재 시간을 출력
- uptime : 현재시간과 부팅된 후 지난 시간 출력
- apt install : 패키지 설치
- apt list : 전체 패키지 목록 확인
  - --installed옵션 : 설치된 패키지 확인
- apt show "패키지이름" : 패키지 정보 확인
- apt purge : 패키지 삭제
- apt remove : 설정 파일은 남겨두고, 파일을 삭제
- apt로 설치한 프로그램은 /usr에 설치됨

  | apt | apt-cache | apt-get |
  | --- | --- | --- |
  | apt-cache와 apt-get의 기능을 합친 멍령어 | 패키지 검색, 상세정보 확인 | 패키지 설치, 삭제 |

---

### Shell
- **사용자**와 **커널** 사이의 **인터페이스**
  - 컴퓨터를 키면 OS가 부팅된 후 실행됨
  - 사용자는 **Shell을 통해서 커널에 명령**
  - Shell을 통해서 명령에 대한 결과 확인
-  인터페이스
  - 사용자가 쉽게 동작 및 사용하는데 도움을 주는 시스템

#### 종류
- sh : 본 쉘, 쉘들의 기반
- bash : 본 쉘 업그레이드 형 쉘
- rbash : restricted bash(제한된 사용자의 쉘)
- dash : 암키스트쉘(구 버전 리눅스에 사용됨)
  - 임베디드 리눅스에서 자주 쓰임

#### 정의
- Shell은 프로그램
  - 운영체제 내부에 접근하기 위한 프로그램
  - 커널을 감싼다는 의미에서 **껍데기**라는 용어를 사용

#### 임베디드에서 Shell
- Shell은 OS에 반드시 포함되어야 되는 것은 아님
  - 전자제품들은 컴퓨팅 장치
  - 따라서, OS 또는 Firmware를 포함
- 사용자에게 Shell은 필요없는 장치
  - 메모리, 에어컨 등은 터미널이 없는 장치
  - 하지만 개발자는 필요 

#### Bash
- 우분투 기본 CLI Shell
- Bourne Again Shell

#### 환경변수
- 쉘스크립트의 시스템 전역 변수
- printenv라는 명령어를 통해 전역변수 들을 볼 수 있음 

#### HOST의 이해
- Host
  - 네트워크에 연결된 **PC(장치)** 이름
  - 네트워크의 최소단위(Node)
- 현재 host명 출력 : hostname

---

### 사용자 계정
- 종류
  - Superuser
  - User
  - System 계정
    - 시스템 운영을 위한 계정
    - 로그인 불가능
- 확인 : cat /etc/passwd
- 현재 사용자 확인 : users
- 사용자 추가 : adduser [계정명]
- 사용자 제거 : deluser --remove-home [계정명]
- 사용자 전환 : su [계정명]
- 사용 종료 : exit
- 루트로 사용자 전환 : sudo su

  | adduser | useradd|
  | --- | ---|
  | 편리한 자동설정(모든 값을 default로 설정) | 세부 설정 가능 |

---

### 사용자 그룹
- 규칙
  - 1 : User를 생성하면 **그룹이 함께** 생성됨
  - 2 : 한 그룹에 여러개의 계정이 포함될 수 있음
  - 3 : 한 유저는 여러개의 그룹에 참여 가능
- 사용 이유
  - 그룹 단위로 단체 설정이 가능함
  - 특정 그룹만 읽고 쓸 수 있는 파일 설정 가능
  - 특정 그룹만 쓸 수 있는 디렉토리 설정 가능
  - 특정 그룹만 실행 시킬 수 있는 프로그램 설정 가능
- 확인 : groups [계정명]
- 그룹에 포함된 유저 확인 : cat /etc/group | grep [그룹명]
- 그룹을 추가 : addgroup [그룹명]
- 그룹을 삭제 : delgroup [그룹명]
- 그룹에 사용자 추가 : gpasswd -a [계정명] [그룹명]
- 그룹에 사용자 제거 : gpasswd -d [계정명] [그룹명]

---

### 파일과 소유권
#### 파일의 종류
- Regular File
  - 일반 파일
  - **-**로 표기됨
- Directory File
  - 리눅스 내부에서는 **디렉토리도 '파일'**로 취급
- Symbolic Link File
  - 윈도우의 **바로가기** 역할 파일
- Device File
  - **HW 장치에 접근**하기 위한 파일
  - Unix 시스템의 독특한 동작
  - file write : 연결된 장치에 동작 신호를 보냄
  - file read : 연결된 장치에 상태 값을 읽음
- 파일 종류의 확인 : file [파일명]
  - ELF 파일 : 리눅스 Binary파일의 Format 이름
    - 0과 1로 이뤄진 Binary 파일 내부에 구간별 어떤 정보인지 나타내는 규격화된 표준
  - "character special", "block special"은 Device 파일
- 파일 위치 확인 : which [파일명]

#### 파일 소유권
- 리눅스는 **다중 사용자 시스템** : 여러명이 동시에 접속하여 사용할 수 있는 시스템
- 파일의 소유자
  - 여러 사람이 쓰는 Host에 존재하는 파일
  - ls -al을 통해 확인 가능
  - [소유자 user] [소유자 group]
    - user : 누구의 파일인지를 나타냄
    - group : 어느 그룹의 파일인지 나타냄
    - 소유 user와 소유 group은 독립적
    - user는 group에 반드시 속하지 않음
    - user와 group에 속한 user들은 파일을 이용 가능
- 파일 소유권 변경하기 : chown [소유 user]:[소유 group] [파일명]
  - 유저만 변경 : chown [소유 user] [파일명]
  - -R 옵션 : 디렉토리 내부에 있는 모든 파일들 한꺼번에 설정

#### 링크 파일
- 링크 생성 : ln
  - -s : 심볼링 링크 
- **프로그램을 /usr/bin/ 내부에 링크하면 어디서든 프로그램 실행** 가능

  | ./[프로그램명] | [프로그램명] |
  | --- | --- |
  | /home/[유저]/[프로그램명] | /usr/bin/[프로그램명] |

---

### 파일 권한 이해하기
- 소유 User의 파일 사용 권한 설정
- 소유 Group의 파일 사용 권한 설정
- 소유자가 아닌 user들(other)에 대해 권한 설정

#### 권한 확인
- r : 읽기
- w : 쓰기
- x : 실행
- rwx : 777 등 이진수로 표현
- 권한 확인 : ls -al
  - 첫 문자를 제외한 처음 세 글자 : 소유 user의 권한
  - 다음 세 글자 : 소유 group의 권한
  - 마지막 세 글자 : 소유 user가 아닌 사람들의 권한
- 권한 설정 : chmod [권한] [파일명]

---

### 리눅스 배포방법
- 압축 파일 형태로 배포하는 경우가 잦음
- 패키지관리 도구로 배포
  - apt로 배포
  - 우분투 소프트웨어 배포
- Binary 파일을 tar.xz로 압축하여 배포
- Source Code를 압축하여 배포
- dpkg 파일로 배포

#### zip
- zip으로 압축하기 : zip [압축명] [Target 파일]
  - -r 옵션 : 디렉토리 내부 파일을 모두 압축한다는 뜻
  - zip -r ./all.zip ./*
- zip 압축풀기 : unzip [압축파일명]
  - -d 옵션 : 특정 디렉토리로 압축 풀기
  - unzip [압축파일명] -d [디렉토리]

#### gzip과 xz
- 리눅스 **단일 파일** 압축
  - 원본 파일이 압축 파일로 변경
  - 단 하나의 파일만 압축
- gzip으로 압축하기 : gzip [파일명]
- gzip으로 압축풀기 : gunzip [파일명]
- xz로 압축하기 : xz [파일명]
- xz로 압축풀기 : xz -d [파일명]

#### tar
- 하나의 파일로 만들기
  - 압축되지 않음
  - 파일 모으기 : tar -cvf [파일명.tar] [파일들]
    - -c : 하나로 모음
    - -f : 파일이름을 지정
    - -v : 진행상황을 보여줌
  - tar 해제 : tar -xvf [파일명.tar] -C [압축 풀 디렉토리 경로]
    - -x : tar 해제
    - -C : 경로지정
- tar.xz 사용법
  - 한 파일로 모으고 압축 : tar -Jcvf
  - 압축 풀고 모은 것 풀기 : tar -Jxvf
- tar.gz 사용법
  - 한 파일로 모으고 압축 : tar -zcvf
  - 압축 풀고 모은 것 풀기 : tar -zxvf

#### dpkg
- 확장자 : .deb
  - debian 패키지 관리 시스템
  - dpkg 명령어로 설치, 제거, 관리 가능
- 패키지 설치 : dpkg -i [경로]
- 패키지 제거 : dpkg -P [패키지이름]
- 설치된 패키지 목록 보기 : dpkg -l
- 의존성 문제
  - 필요한 파일들을 자동으로 설치해주지 않음
  - 이 단점을 보안하고자 apt 사용

#### 리눅스에서 많이 압축되는 방법
1. tar + xz
2. zip
3. tar + gz
4. tar + bz2
- 압축률 : zip < gz < bz2 < xz

---

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
