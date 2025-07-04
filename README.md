#### 20256751_이가은

## 리눅스 명령어 조사 (top, ps, jobs, kill)

## 1. top

'top'은 현재 실행 중인 프로세스와 시스템 자원 사용 상태를 실시간으로 모니터링할 수 있는 명령어이다. 시스템 관리자나 개발자가 성능을 점검할 때 자주 사용된다.

---
### 주요기능
- 현재 실행 중인 프로세스 출력
- 실시간 CPU 및 메모리 사용량 확인
- 사용자별 프로세스 정보 확인
---
### 특징
- CPU, 메모리, 스왑 사용량을 실시간으로 모니터링 가능
- 시스템의 부하 상태를 파악할 수 있어 문제 진단에 유용
---
### top 명령어 실행 시 화면 구성
| 상단 정보 | 하단 정보 |
|-----------|-----------|
|**시스템의 전반적인 상황**| **각 프로세스에 대한 정보** |
|-현재 시간, 시스템의 부팅 시간, 업타임|-PID, 사용자|
|- cpu, 메모리, 스왑 사용량|-CPU 사용량, 메모리 사용량|

---

### top 명령어 주요 옵션
| 옵션 |  정보 |
|:-------:|:-------:|
| top **-d** [time] | 화면 갱신 간격 설정|
| top **-p** [PID]| 특정 프로세스 ID만 모니터링|
| top **-u** [user_name]| 특정 사용자의 프로세스만 표시|

---
---
## 2. ps

'ps'는 리눅스 시스템에서 실행 중인 프로세스의 상태를 확인하는 명령어이다.
-프로세스란 프로그램이 실행되면서 시스템에서 하나의 작업 단위로 처리되는 것을 의미한다.

---
### 주요기능
- 사용자별 프로세스 조회
- 모든 프로세스 출력
- PID, CPU, 메모리 사용량 출력
---
### 특징
- 조건부 검색 가능
- 실행 시점의 프로세스 정보를 출력
- 시스템에 부담을 적게 줌

---

### ps 명령어 주요 옵션
| 옵션 |  정보 |
|:-------:|:-------:|
| ps **-e** (ps **-A**) | 시스템의 모든 프로세스 출력|
| ps **-f** |풀 포맷(full format)으로 상세 정보 출력|
| ps **-u** [user_name]| 특정 사용자 프로세스만 출력|

---
---
## 3. jobs

'jobs'는 현재 쉘 세션에서 실행 중이거나 일시 중지된 프로세스를 확인할 때 사용된다. 다수의 작업을 동시에 처리할 때 효과적으로 관리할 수 있도록 돕는다.

---
### 주요 기능
- 백그라운드나 포그라운드에서 실행되는 작업들을 목록으로 보여줌
- 각 작업에 대해 작업 번호, 프로세스 ID, 작업 상태, 명령어 이름 등을 출력

---
### jobs 명령어 주요 옵션
| 옵션 |  정보 |
|:-------:|:-------:|
| jobs **-l** | 작업의 PID(Process ID)까지 상세히 출력|
| jobs **-p** |작업의 PID만 출력|
| jobs **-r** | 실행 중인 작업만 출력|

---
---
## 4. kill

'kill' 명령어는 프로세스에 종료 시그널을 보낸다. 시스템에 얘기치 않은 문제가 생긴 프로세스를 종료시킬 수 있다.

---
### 주요 기능
- 특정 프로세스에 시그널을 전송
- 기본 시그널(SIGTERM)로 프로세스 정상 종료를 요청
- SIGKILL 시그널을 보내 프로세스를 강제 종료
- 가능한 시그널 목록을 출력
-프로세스 ID(PID)를 지정해 원하는 프로세스에 시그널을 전달
---
### kill 명령어 주요 옵션
| 옵션 |  정보 |
|:-------:|:-------:|
| kill **-9** | 강제 종료|
| kill **-15** |정상 종료 요청|
| kill **-l** | 시그널 목록 출력|
