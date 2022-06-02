###### 리눅스 명령어

### __top__

- 시스템의 상태를 실시간으로 빠르게 파악 가능(CPU, Memory, --Process)
- 옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여줌

![20220602_151712](https://user-images.githubusercontent.com/106691667/171565535-ba5ecdc5-0831-4d56-bb2e-e03feed78f79.jpg)

- top 실행 전 옵션
순간의 정보를 확인하려면 -b 옵션 추가(batch 모드)
-n : top 실행 주기 설정(반복 횟수)

- top 실행 후 명령어

shift + p : CPU 사용률 내림차순(높은 프로세스 순서대로)

shit + m : 메모리 사용률 내림차순

shift + t : 프로세스가 돌아가고 있는 시간 순

-k : kill. k 입력 후 PID 번호 작성. signal은 9

-f : sort field 선택 화면 -> q 누르면 RES순으로 정렬

-a : 메모리 사용량에 따라 정렬

-b : Batch 모드로 작동

숫자 1 : CPU Core별로 사용량 보여줌

등

어떤 프로세스가 CPU를 과다하게 잡고있는지 분석 가능!

### __ps__

ps(process status)
- 프로세스의 상태를 알고 싶을때 사용
- ps는 프로세스에 대한 많은 정보를 담고 있고 매우 많이 사용되는 명령으로 에는 세가지 종류가 있음

![20220602_151813](https://user-images.githubusercontent.com/106691667/171565560-a7799d7c-cc70-4ab9-aaf8-e69e0faa4115.jpg)

1. Unix Option : 앞에 '-' (dash)가 붙는 옵션 표기방법입니다.  
2. BSD Option : '-' 를 붙이지 않습니다.
3. GNU Option : 명령어 앞에 '--' (double dash)를 붙입니다.

- ps 실행 후 명령어

-e, -A : 모든 프로세스를 보여줍니다. 

-a : 세션 리더와 터미널과 연관된 프로세스들을 제외한 모든 프로세스를 보여줍니다.

-d : 세션 리더를 제외한 모든 프로세스를 보여줍니다.

-f : full format으로 세션의 정보를 표시합니다. 

-ef : -e와 -f의 옵션 조합인데, 모든 프로세스를 full format으로 보여줍니다. 아래는 그 결과를 보여줍니다. UID, PID, PPID, C, STIME, TTY, TIME, CMD의 정보를 볼 수 있네요. TTY(연결 터미널)가 없으면 대부분 데몬 혹은 커널 프로세스입니다. 

__ps와 top의 차이점__

ps는 ps한 시점에 proc에서 검색한 cpu 사용량
top은 proc에서 일정 주기로 합산해 cpu 사용율 출력!

### __jobs__

### __kill__

-----

###### 매크로 사용법
