# Linux

## 목차
- [운영체제](https://github.com/KimUJin3359/Linux#%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C)
- [리눅스란](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4%EB%9E%80)
- [패키지 관리 시스템](https://github.com/KimUJin3359/Linux#%ED%8C%A8%ED%82%A4%EC%A7%80-%EA%B4%80%EB%A6%AC-%EC%8B%9C%EC%8A%A4%ED%85%9C)
- [리눅스 파일시스템](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4-%ED%8C%8C%EC%9D%BC%EC%8B%9C%EC%8A%A4%ED%85%9C)
- [쉘이란](https://github.com/KimUJin3359/Linux#shell)
- [쉘 프로그래밍](https://github.com/KimUJin3359/Linux/blob/master/README.md#shell-programming)
- [쉘 명령어](https://github.com/KimUJin3359/Linux/blob/master/README.md#%EC%89%98-%EB%AA%85%EB%A0%B9%EC%96%B4)
- [사용자 계정](https://github.com/KimUJin3359/Linux#%EC%82%AC%EC%9A%A9%EC%9E%90-%EA%B3%84%EC%A0%95)
- [사용자 그룹](https://github.com/KimUJin3359/Linux#%EC%82%AC%EC%9A%A9%EC%9E%90-%EA%B7%B8%EB%A3%B9)
- [파일과 소유권](https://github.com/KimUJin3359/Linux#%ED%8C%8C%EC%9D%BC%EA%B3%BC-%EC%86%8C%EC%9C%A0%EA%B6%8C)
- [권한 이해하기](https://github.com/KimUJin3359/Linux#%ED%8C%8C%EC%9D%BC-%EA%B6%8C%ED%95%9C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)
- [시스템 모니터링](https://github.com/KimUJin3359/Linux#%EC%8B%9C%EC%8A%A4%ED%85%9C-%EB%AA%A8%EB%8B%88%ED%84%B0%EB%A7%81)
- [시스템 모니터링 - 프로세스란?](https://github.com/KimUJin3359/Linux#%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4)
- [VI Editor](https://github.com/KimUJin3359/Linux#vi-editor)
- [Build System](https://github.com/KimUJin3359/Linux#build-system)
- [Makefile](https://github.com/KimUJin3359/Linux/blob/master/README.md#make-%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8)
- [리눅스 배포방법](https://github.com/KimUJin3359/Linux#%EB%A6%AC%EB%88%85%EC%8A%A4-%EB%B0%B0%ED%8F%AC%EB%B0%A9%EB%B2%95)
- [리눅스 통신](https://github.com/KimUJin3359/Linux/blob/master/README.md#%EB%A6%AC%EB%88%85%EC%8A%A4-%ED%86%B5%EC%8B%A0)

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

### Shell
- **사용자**와 **커널** 사이의 **인터페이스**
  - 컴퓨터를 키면 OS가 부팅된 후 실행됨
  - 사용자는 **Shell을 통해서 커널에 명령**
  - Shell을 통해서 명령에 대한 결과 확인
-  인터페이스
  - 사용자가 쉽게 동작 및 사용하는데 도움을 주는 시스템

#### 종류
- sh : 본 쉘, 쉘들의 기반
- **bash : 본 쉘 업그레이드 형 쉘**
- rbash : restricted bash(제한된 사용자의 쉘)
- dash : 암키스트쉘(구 버전 리눅스에 사용됨)
  - 임베디드 리눅스에서 자주 쓰임

#### 정의
- Shell은 프로그램
  - **운영체제 내부에 접근**하기 위한 프로그램
  - 커널을 감싼다는 의미에서 껍데기라는 용어를 사용

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

### Shell Programming
- 쉘 스크립트
  - 쉘에서 **한줄씩 순서대로 실행**하는 script 파일
  - **조건문, 반복문, 변수, 함수 등 포함** 가능
  - 컴파일 되지 않음
- 쉘 타입
  - **Bourne Shell** : Prompt가 **$**로 시작
    - /bin/sh라는 이름을 주로 사용
    - sh
    - bash
  - C Shell : Prompt가 %로 시작
- 쉘 스크립트 만들기
  - 규칙
    - 모든 쉘 **스크립트 확장자 : .sh**
    - 파일 맨 위에는 반드시 **#!/bin/sh(본쉘), #!/bin/bash(배쉬 쉘)**
- 쉘 스크립트 실행
  - . 명령어로 실행
    - . ./run.sh
  - source 명령어로 실행
    - source ./run.sh
  - 바로실행
    - ./run.sh
  - bash 명령어로 실행
    - bash ./run.sh
  - source 명령어 사용을 권장(가독성 측면, 성능상 이득 없음)

#### Bourn Shell Script
- 변수 생성
  - 변수이름=값
  - 모든 값들은 **문자열로** 취급
  ```
  #!/bin/bash
  
  temp=string
  echo $temp
  temp=$temp+str
  echo $temp
  - 출력 결과 : string, string+str
  ```
- 인자
  - $1, $2, ...
- 산술 연산
  - 본 쉘에서는 사칙연산 불가능
  - 산술연산 프로그램을 사용
    - expr 프로그램
    - 어퍼스트로피(`) 사용
    ```
    num=50
    num=`expr $num + 50`
    echo $num
    - 출력 결과 : 150
    ```
- 주석 : #
- if문
  - == : 같다
  - != : 다르다
  - -gt : >
  - -lt : <
  ```
  if [ 조건 ]
  then
    명령어
  elif [ 조건 ]
  then
    명령어
  else
    명령어
  fi
  ```

#### Bash Shell Script
- Bourne Shell Script 호환성
- C언어와 비슷한 문법 제공
- 띄어쓰기가 자유로움
  ```
  echo $((10* 35))
  ```
- 변수를 감쌀 때는 이중 괄호
  ```
  echo $((15))
  echo $(($1))
  ```
- if문
  - (()) 사이, C언어 스타일로 조건 사용 가능
  - 숫자비교 : 숫자 비교일 때만 Bash 전용 문법 (()) 사용 가능
    - 대소비교 : <, > 사용 가능
  - 문자열비교 : 띄어쓰기가 엄격한 본쉘 문법 [] 사용
  ```
  if (($a==10)); then 
    ...
  
  if [ $1 == "bash" ]; then
    ...
  ```
- printf : C언어의 printf와 비슷
  ```
  a=1
  b=2
  c=3
  
  printf "%d, %d, %d" $a $b $c
  ```
- 배열
  - {} 괄호 필수
  ```
  arr=(10 20 30)
  echo ${arr[0]}
  ```
- for
  ```
  for ((i=0;i<10;i++))
  do
    ...
  done
  ```
  ```
  #!/bin/bash

  arr=(30 50 10 30 40 25) 
  idx=0

  for((i=0;i<${#arr[@]};i++))
  do
    if((${arr[i]} >= 30))
    then
      idx=$((idx + 1))
    fi  
  done
  echo $((idx))
  ```
- 함수
  ```
  msg()
  {
    ...
  }
  
  msg
  ```

#### 둘 다 공부하는 이유
- 임베디드 리눅스에선느 기본적으로 **bash가 아닌 본쉘이 사용**
  - busybox에서 sh가 기본적으로 사용
- bash는 편리하고 임베디드를 제외하여 널리 사용됨
---

### 쉘 명령어

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
- stat : 특정 파일에 대한 세부 정보를 확인
  - stat [파일명]
  - stat [디렉토리명]
  - Inode : 파일의 고유 번호
  - Uid : 파일 소유권이 있는 User의 고유 번호
  - Gid : 파일 소유권이 있는 Group의 고유 번호
  - Modify : 파일 내용 변경 시간
  - Change : 파일 권한, 소유권 변경 시간
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

### 사용자 계정
- 종류
  - Superuser
  - User
  - System 계정
    - 시스템 운영을 위한 계정
    - 로그인 불가능
- **확인 : cat /etc/passwd**
- 현재 사용자 확인 : users
- **사용자 추가 : adduser [계정명]**
- **사용자 제거 : deluser --remove-home [계정명]**
- **사용자 전환 : su [계정명]**
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
- **그룹에 포함된 유저 확인 : cat /etc/group | grep [그룹명]**
- **그룹을 추가 : addgroup [그룹명]**
- **그룹을 삭제 : delgroup [그룹명]**
- **그룹에 사용자 추가 : gpasswd -a [계정명] [그룹명]**
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
- **파일 소유권 변경하기 : chown [소유 user]:[소유 group] [파일명]**
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

### 권한 이해하기
- 소유 **User**의 파일 사용 권한 설정
- 소유 **Group**의 파일 사용 권한 설정
- 소유자가 아닌 user들(**other**)에 대해 권한 설정

#### 권한 확인
- 권한 확인 : ls -al
  - 첫 문자를 제외한 처음 세 글자 : 소유 user의 권한
  - 다음 세 글자 : 소유 group의 권한
  - 마지막 세 글자 : 소유 user가 아닌 사람들의 권한
- 권한 설정 : chmod [권한] [파일명]
  - rwx : 777 등 이진수로 표현

#### 파일 권한 이해하기
- r : 파일을 **읽을 수 있는** 권한
- w : 파일을 **쓸 수 있는** 권한
- x : 파일을 **실행할 수 있는** 권한

#### 디렉토리 권한 이해하기
- r : **디렉토리 내부 파일 확인** 권한
- w : **디렉토리 내 파일 생성, 삭제** 권한
- x : 디렉토리로 **진입 여부** 결정

---

### 시스템 모니터링
#### 컴퓨터 성능 확인
- 컴퓨터 성능
  - **CPU** : CPU 이름 / 정보
  - **Memory** : Memory 용량 / 정보
  - **Disk** : Disk 용량 / 정보

#### 시스템 정보확인
- /proc 디렉토리
  - 실제 존재하는 디렉토리가 아닌 **가상 디렉토리**
  - **커널이 가지고 있는 정보**를 파일처럼 열어서 확인 가능
  - 커널이 관리하는 정보를 읽을 때사용
    - **프로세스, 하드웨어 등 관련 정보**
- cpuinfo
  - /proc/cpuinfo
  - 각 코어의 정보, 클럭 수, 모델명 등 주요정보
- meminfo
  - /proc/meminfo
  - 메모리 정보를 확인
- free -h
  - **메모리 요약된 정보** 확인
  - total = used + free + cache
  - available : 하나의 app이 현재 사용할 수 있는 메모리 추정 계산치 
  - 스왑 : RAM이 부족한 경우, 하드디스크를 일시적으로 메모리처럼 사용하는 공간
- scsi
  - /proc/scsi/scsi
  - **디스크 장치**의 정보
  - 저장장치(SCSI)
    - 리눅스에서는** SSD, HDD 모두 SCSI 장치로 인식**
    - 과거 컴퓨터에서 장치를 Serial방식으로 연결하는 인터페이스 표준 중 하나
    - 현재는 SATA와 같은 SCSI Interface보다 빠른 성능을 가진 인터페이스 사용
- fdisk -l
  - 디스크 세부 정보 확인
  - fdisk : 파티션 관리 유틸리티
- proc 대신 **lscpu, lsmem, lsscsi, lsusb 등을 사용하여 쉽게 정보 확인** 가능
- lsscsi
  - scsi 장치 명령어
  - scsi 장비 별 연결된 Device File 확인 가능
  - Device File : HW와 연결된 파일, 이 파일에 신호를 주면 연결된 HW에 영향을끼침
    - 디스크 장치파일 이름 짓는 규칙
    - 빨리 발견하는 것부터 이름 선정
    - sd* (SCSI DISK) 
    - sr* (SCSI CD-ROM) : 리눅스 커널이 발견하는 SCSI CD-ROM 장치의 이름
    - sg* (SCSI GENERIC) : SCSI 인터페이스를 사용하는 기타 장치들
- lsusb
  - USB에 연결된 장치 목록을 알 수 있음
  - -t 옵션 : 계층 구조로 USB 디바이스 정보를 보여줌

#### OS 정보 확인
- 리눅스 배포판 버전 
  - /etc/os-release
  - 배포판 마다 파일 이름이 바뀔 수 있음 (Centos의 경우 : /etc/centos-release)
  - **LSB(Linux Standard Base)**
    - Linux 배포판들 끼리 표준화 (ISO)
    - POSIX, File System, System Call, Package Format
  - lsb_release -a
    - 리눅스 배포판의 상세 정보를 출력
    - lsb_release 명령어는 모든 배포판마다 같음
- 리눅스 커널 버전
  - /proc/version
  - uname -r
    - 예시 : 5.4.0-47-generic
    - **디바이스 드라이버 개발 > 커널 버전을 확인**하면서 환경 세팅
    - 현재 **커널버전에 맞는 프로그램 등을 설치**할 때 확인 필수
- OS 32/64 bit
  - lscpu의 Architecture
  - 18.04 LTS버전부터 32 bit 리눅스 지원하지 않음
- User 정보
  - who
    - Host에 접속한 사용자 보기
    - 접속한 시간이 출력
    - -r 옵션 : 사용자의 run level 확인 가능
    
    | Level 5 | Level 3 |
    | --- | --- |
    | 그래픽 User | SSH 같은 Terminal로 접속한 CLI 유저 |
    
#### 네트워크 설정 확인
- ip addr
  - ip 주소를 확인하는 명령어
- **ifconfig**
  - net-tools 패키지 설치 필요
  - NIC별 설정정보 확인
    - 네트워크 인터페이스 : 네트워크 설정, 네트워크 카드 정보를 포함한 연결 통로, 인터페이스
  - lo : 루프백 네트워크 인터페이스

#### 디렉토리 용량 확인
- ls -alh
  - 읽기 쉽게 KB / MB 등 단위로 출력
  - 용량 확인시 **정확하지 않음**
  - 실제 Disk에 저장될 때는 **4KB 단위로 저장**됨
    - File System 및 SSD에서 최소 저장 사이즈를 4KB 단위로 취급(다량 데이터 관리를 위함)
- du
  - **실제 저장되는 크기**로 표기
  - -h 옵션 : 사람이 보기좋은 형식으로 표현 

---

### 프로세스
#### 프로세스 모니터링
- **프로그램 : CPU 명령어(2진수)들이 모여있는 파일**
  - CPU는 **하나의 명령어**씩 처리
- Disk에비해 **Memor**y의 수행속도가 빠름
  - CPU + 메모리 : 폰 노이만 구조
  - 프로그램을 실행시키자마자, 즉시 **메모리에 적재(Loading)**
- 프로세스 : **Disk**로부터 **메모리에 적재**된 프로그램을 프로세스
  - **메모리에 적재되어 현재 실행중인 프로그램**
  - 메모리
    - Kernel Space : **커널**이 동작하는 메모리 공간
    - User Space : **app**이 동작하는 메모리 공간
  - User Level Process
    - User Space에 생성되는 프로세스를 뜻함
    - App을 수행하면, 유저 레벨 프로세스가 됨
  - Kernel Level Process
    - Kerner Space에 생성되는 프로세스를 뜯ㅅ함
    - 커널이 사용하는 프로세스
    - 커널 쓰레드라고도 함

#### 프로세스 관리
- PID : Process ID
  - PID 1번 (systemd)
    - 커널을 초기화 하는 동작들을 수행(로그인 세션 관리/ 장치 관리/ 로그 처리 수행)
    - 부트로더 -> 커널 -> systemd 프로세스
    - 커널 부팅 후 첫번째로 실행
  - PID 2번 (kthreadd)
    - 커널 공간에서 실행하는 커널 프로세스의 생성을 담당
    - 모든 커널 스레드의 부모 스레드
- Foreground Process : **사용자가 Run**하거나, **상호작용 가능**한 프로세스
- Background Process : 사용자와 **독립적으로 실행**되는 프로세스
  - 명렁어에 &를 넣으면 Background Process로 동작
- **ps**
  - **프로세스 정보 및 관리** 명령어
  - User Space에 있는 User Level Process 정보가 출력
  - -e 옵션: Kernel Space Process까지 출력
- **fg**
  - Background Process를 Foreground로 이동
  - 가장 최근에 **Background로 이동한 프로세스를 다시 꺼내옴** 
- **kill**
  - 죽이는 명령어가 아니라 하나의 프로세스에 **특정 시그널을 보내는 명령어**
  - **-9 옵션 : SIGKILL** 시그널을 보냄
- **ctrl + Z**
  - 현재 프로세스를 **백그라운드로 전환**
  - Stopped 상태로 표기
    - 일반적인 OS에 없는 Process State
    - Background 모드 진입시 사용자 입력을 기다리는 stdin으로 인해 "STOP" signal 발생
    - "CONT" signal로 재개
  - fg를 누르면 돌아옴

#### 실시간 모니터링 유틸리티
- **top**
  - **시스템 모니터링**에 대표적인 유틸리티
  - 윈도우의 작업 관리자에 해당
  - top : uptime(시간 / 부팅 후 시간 / 현재 접속자 / CPU 부하 정도)
  - load average : loadavg(시스템이 받고있는 부하정도 - 1분, 5분, 15분 시스템 부하 평균)
  - tasks
    - total : 전체 프로세스의 개수
    - running : 실행 중 프로세스의 개수
    - sleeping : I/O나 event를 기다리는 프로세스의 개수
    - stopped : ctrl z와 같은 stop 시그널을 받은 프로세스의 개수
    - zombie : 프로세스가 종료되었지만 OS 내부 시스템 자원 해지가 안된 프로세스의 개수
- 좀비 프로세스
  - program은 multi process, multi threading을 통해 여러개를 실행
  - 부모 process가 자식 process 들의 PID 등 정보를 관리
  - 스스로 만들어진 process가 아니라서, PID를 알 수 없고 부모가 존재하지 않는 프로세스
  - 그렇기 때문에 할당된 디바이스나 자원을 반환할 수 없음
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

---

### Build System
- 빌드 프로세스를 설정해주고, 그대로 수행하는 프로그램

#### Build
- 소스코드에서 실행 가능한 Software로 변환하는 과정(Process)
- 소스코드에서 실행 가능한 Software로 변환하는 산출물(결과물)
- Build 과정
  - 프리 컴파일링
  - 컴파일
  - 링킹
- Build 동작
  - 실행
  - 테스트
  - 배포
  - 문서 생성

#### 리눅스 Build System
- Tool Chain : Build를 하기 위한 Tool들의 모음
- GCC
  - gcc만으로 거대한 프로젝트에 대한 빌드 자동화는 어려움
- make
  - 리눅스 Build System의 1인자
  - make 명령어로 미리 지정된 프로세스대로 자동화 가능
  - 속도 향상
    - 수정된 파일만 재 컴파일하는 기능
    - 재컴파일된 파일에서 의존성 있는 파일만 재컴파일

---

### make 스크립트
- Target이 반드시 1개 이상 존재해야 함
  - make : 가장 위에 존재하는 Target 수행
- Target 내부 들여쓰기는 Tab으로 처리
  - 띄어쓰기 불가 
- @ : 수행할 명령어 입력을 생략하고 결과만 출력
  ```
  FILE:
    @gcc main.c -o main
    @./main
  ```
- 의존성 타겟
  ```
  FIR: SEC THI
    ...
  SEC:
    ...
  THI:
    ...
  - SEC, THI 먼저 수행 후 FIR의 내용 수행 
  ```
- 변수 추가
  - Make에서 매크로를 변수라고 부름
  - 매크로 변수는 아무곳에 넣을 수 있음
    - 가독성을 위해 최상단에 적어주는 것이 좋음
  ```
  CC = gcc
  CFLAGS = -Werror -Wextra -Wall
  
  FILE:
    $(CC) $(CFLAGS) ... -o main
  ```
- \# : 주석
- += : 변수 대입 기호
  - 자동으로 띄어쓰기 한 칸이 추가됨
  ```
  SEN = "I"
  SEN += "AM"
  SEN += "AN"
  SEN += "IRONMAN"
  ```
- := : Simple Equal
  - Script 순서대로 현재 기준에서 값을 대입
- = : Recursive Equal
  ```
  SEN = "I"
  SEN += "AM"
  SIMPLE := ${SEN}
  RECUR = ${SEN}
  SEN += "AN"
  SEN += "IRONMAN"
  
  PRI:
    @echo ${SIMPLE}
    @echo ${RECUR}
  - SIMPLE : I AM, RECUR : I AM AN IRONMAN 출력
  ```
- $@ : Target을 나타내는 변수
  ```
  OK :
    echo "This Is $@"
  - This Is OK 출력  
  ```
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

### 리눅스 통신
#### Telnet
- Tel + net : **통신 + 네트워크** 프로토콜
- 원격지 컴퓨터를 CLI로 원격접속할 때 쓰임
- ASCII 코드를 사용한 통신
- 주로 **23번 포트** 사용
- 국내 텔넷 서비스
  - 천리안, 나우누리, 유니텔, 하이텔 등 4대 유료 텔넷 서비스
  - 웹페이지를 브라우저로 볼 수 있는 HTTP 프로토콜 더 인기가 많았음
- 텔넷 서버 설치 : sudo apt install telnetd
- 특징
  - 장점 : 암호화가 필요 없는 곳에서는 **빠르게 통신 가능**
  - 단점 : 암호화가 되어있지 않아 **보안이 약함**

#### SSH 
- 컴퓨터와 컴퓨터가 인터넷과 같이 network를 통해 서로 통신하는 프로토콜
- **보안 측면에서 안전하게 통신**하기 위해 사용
- 다른 컴퓨터에 원격 접속시 사용
- 주로 **22번 포트** 사용
- 사용 이유
  - **데이터 전송**
  - **원격 제어**
  - **보안**
    - SSH는 암호화된 안전한 채널을 구성한 뒤 정보를 교환하기 떄문에 보안이 뛰어남
    - 클라이언트와 서버는 암호화되어있기 때문에 중간에 정보가 노출되어도 데이터를 알 수 없음 
- 리눅스에서는 가벼운 **텔넷과** 보안에 좋은 **SSH 모두 자주 사용**

#### 임베디드 리눅스 사용 방법
- **UART**라는 유선 Serial 통신으로 Shell을 사용
  - 네트워크에 연결이 불가능함
    - 유선/무선 랜 포트, 모뎀 칩이 보드 내 존재하지 않음(SSH, 텔넷 사용 불가)
  - 유선 연결을 통해 임베디드 보드 제어, 개발, 동작 Log 확인
- **텔넷, SSH** 사용
  - 네트워크 접속이 가능
  - 유선 없이 편리하게 개발 가능
  - UART보다 빠름

#### SCP
- secure copy
  - 원격지에 있는 **파일을 복사**하는 프로그램
- 네트워크를 통해 파일을 복사
- 주로 ssh연결을 통해 접속한 컴퓨터에 파일을 복사하기 위해 사용
- 파일 보내기 : scp 파일 계정@서버주소:목적경로

#### FTP
- File Transfer Protocol
  - TCP/IP 프로토콜을 사용한 **파일 전송 프로토콜**
- 보안에 약함
  - **암호화되지 않음**
  - 수많은 보안 취약점이 존재
    - 무차별 대입 공격
    - FTP 바운스 어택
    - 패킷 가로채기
    - 포트 훔치기
    - 스푸핑 공격 등

#### TFTP
- Trivial File Transfer Protocol
  - **간단한** 파일 전송 프로토콜
- FTP와 마찬가지로 파일을 전송하기 윟나 프로토콜이지만, 더 단순한 방식으로 파일을 전송
- 데이터 전송 과정에서 데이터가 손실될 수 있는 등 불안정함
- FTP처럼 복잡한 프로토콜을 사용하지 않기 때문에 구현이 간단
- 임베디드 시스템에서 운영체제 업로드로 주로 사용

#### SFTP
- Secure File Transfer Protocol
  - FTP보다 **보안이 좋음**
- FTP와 같이 파일을 전송할 때 사용되며, 내용을 **암호화시켜 전송**
- SSH에 있는 부가적인 기능들 중 하나
- SSH와 같은 포트를 사용(22번 Port)
  - SSH가 접속이 되면 SFTP도 접속이 가능
  - SSH Server가 운영되면 SFTP Server를 따로 설치할 필요 없음
 
  | SCP | SFTP |
  | --- | --- |
  | 파일 전송에만 사용(비대화식) | 디렉토리 및 파일 삭제 등 작업도 수행(대화식) |
  | 전송속도가 빠름 | 비교적 전송속도가 느림 |
  | 한번 실행되면 중단 불가능 | 전송도중 중단 가능 |
  
  
