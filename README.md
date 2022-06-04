
# 리눅스 명령어

### __top__

- 시스템의 상태를 실시간으로 빠르게 파악 가능(CPU, Memory, --Process)
- 옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여줌

!<img src="https://user-images.githubusercontent.com/106691667/171565535-ba5ecdc5-0831-4d56-bb2e-e03feed78f79.jpg" width="70%" height="70%"/>

- top 실행 전 옵션
순간의 정보를 확인하려면 -b 옵션 추가(batch 모드)
-n : top 실행 주기 설정(반복 횟수)

- top 실행 후 명령어

shift + p : CPU 사용률 내림차순(높은 프로세스 순서대로/기본)

shit + m : 메모리 사용률 내림차순

shift + t : 프로세스가 돌아가고 있는 시간 순

-k : kill. k 입력 후 PID 번호 작성. signal은 9

-f : sort field 선택 화면 -> q 누르면 RES순으로 정렬

-a : 메모리 사용량에 따라 정렬

-b : Batch 모드로 작동

숫자 1 : CPU Core별로 사용량 보여줌

등

어떤 프로세스가 CPU를 과다하게 잡고있는지 분석 가능!

### __ps(process status)__

- 현재 실행중인 프로세스의 상태를 알고 싶을때 사용
- ps는 프로세스에 대한 많은 정보를 담고 있고 매우 많이 사용되는 명령으로 에는 세가지 종류가 있음

!<img src="https://user-images.githubusercontent.com/106691667/171565560-a7799d7c-cc70-4ab9-aaf8-e69e0faa4115.jpg" width="50%" height="50%"/>

1. Unix Option : 앞에 '-' (dash)가 붙는 옵션 표기방법입니다.  
2. BSD Option : '-' 를 붙이지 않습니다.
3. GNU Option : 명령어 앞에 '--' (double dash)를 붙입니다.

- ps 실행 후 명령어

-e, -A : 모든 프로세스를 보여줍니다. 

-a : 세션 리더와 터미널과 연관된 프로세스들을 제외한 모든 프로세스를 보여줍니다.

-d : 세션 리더를 제외한 모든 프로세스를 보여줍니다.

-f : full format으로 세션의 정보를 표시합니다. 

-ef : -e와 -f의 옵션 조합인데, 모든 프로세스를 full format으로 보여줍니다. 아래는 그 결과를 보여줍니다. UID, PID, PPID, C, STIME, TTY, TIME, CMD의 정보를 볼 수 있네요. TTY(연결 터미널)가 없으면 대부분 데몬 혹은 커널 프로세스입니다. 

#### __ps와 top의 차이점__

|차이점|ps|top|
|---|---|---|
|사용량 출력 시점|ps한 시점|일정 주기 합산|


### __jobs__

- 백그라운드로 실행되는 작업목록(작업번호, 상태, 명령어)을 보여주는 리눅스 명령어
- 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력됨
- 각 작업에는 번호가 붙어있어 kill명령어 뒤에 '%작업번호'를 입력하여 종료시킬 수 있음 (작업번호: PID와는 달리, 별도로 부여되는 백그라운드 작업목록 상의 번호)

!<img src="https://user-images.githubusercontent.com/106691667/171998467-adc4de15-3f63-46dd-9e5e-ac48f5e1afe5.jpg" width="60%" height="60%"/>


### __kill__

- 프로세스를 종료시키는 리눅스 명령어 (kill 명령어는 이름 때문에 프로세스를 강제로 종료시키는 명령어로 오해를 사기 쉬운데, 실제로는 프로세스에 시그널(signal)을 보내는 명령어입니다. 이름이 kill 인 이유는 어떤 시그널을 보낼 지 지정하지 않으면 기본적으로 SIGTERM 시그널을 보내게 되는데 SIGTERM의 기본 동작이 프로그램 종료이기 때문입니다.)
- 프로세스에 종료 메시지를 보냄
- 
!<img src="https://user-images.githubusercontent.com/106691667/171998784-f6824efb-e82d-48aa-893d-304d46f5545e.jpg" width="70%" height="70%"/>

- kill 명령어에 -l 옵션을 주면 위와 같이 시그널의 숫자(number)와 이름이 출력됨
 
- 시그널을 보낼 때는 kill -(보낼 시그널) PID 이렇게 사용하는데, 지정된 PID를 갖는 프로세스에 지정된 시그널이 전달되는 구조로 시그널은 숫자로 지정해도 되고 앞에 SIG를 빼고 이름을 넣어도 됨 

--------------------

# vim 에디터에서 매크로 
