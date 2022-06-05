# homework-20195143 윤정민

# *ps: 현재 실행중인 프로세스를 확인할 수 있는 리눅스 명령어다.*
|ps|옵션|설명|
|---|---|---|
|   |-A|모든 프로세스를 출력한다.|
|   |a|터미널과 연관된 프로세스를 출력한다.|
|   |-a|데몬 프로세스처럼 터미널에 종속되지 않은 모든 프로세스를 출력한다.|
|   |-e|커널 프로세스를 제외한 모든 프로세스를 출력한다.|
|   |-f|풀 포맷으로 보여준다.|
|   |-I|긴 포맷으로 보여준다.|
|   |I|프로세스의 정보를 길게 보여준다.|
|   |-o|출력 포맷을 지정한다.|
|   |-M|64비트 프로세스들을 보여준다.|
|   |-m|커널 스레드를 보여준다.|
|   |-p|특정 PID를 지정할 때 사용한다.|

**ps의 예시**

![ps명령어](https://user-images.githubusercontent.com/104884552/172041958-d52aa737-207e-4340-90e6-ea67328855f6.PNG)


**ps-e의 예시**

![ps-e명령어](https://user-images.githubusercontent.com/104884552/172042043-04f28892-0bc0-41b8-895e-c86cf7056cbd.PNG)


# *top: 시스템 프로세스와 메로리 사용 현황을 실시간으로 출력하는 리눅스 명렁어다.*
-시스템 상태를 전반적으로 가장 빠르게 파악이 가능하다.

|top|옵션|설명|
|---|---|---|
|   |shift+p|cpu 사용률이 높은 프로세스 순서대로|
|   |shift+m|메모리 사용률이 높은 프로세스 순서대로|
|   |shift+t|프로세스가 돌아가고 있는 시간 순서대로|
|   |a|메모리 사용량에 따라 정렬|
|   |b|Batch 모드 작동|
|   |d|지연 시간 간격|
|   |h|도움말|


**top의 예시**

![top](https://user-images.githubusercontent.com/104884552/172042225-9dafb88a-1a32-4244-83fd-1a8989f9e594.PNG)


# *jobs: 작업이 중지된 상태나 백그라운드로 진행 중인 상태를 표시한다.*

|jobs|옵션|설명|
|---|---|---|
|   |-l|프로세스 그룹 ID를 state 필드 앞에 출력한다.|
|   |-n|프로세스 그룹 중에 대표 프로세스 ID를 출력한다.|
|   |-p|각 프로세스 ID에 대해 한 행씩 출력한다.|
|   |command|지정한 명렁어를 실행한다.|

**jobs으로 출력되는 백그라운드 작업 상태값?**
|jobs|예시|설명|
|---|---|---|
|   |Running|작업 진행중|
|   |Done|작업이 완료되어 0을 반환|
|   |Stopped|작업 일시중단|


**jobs의 예시**

![jobs](https://user-images.githubusercontent.com/104884552/172042476-e618ced1-a586-4ec0-9af1-f557e4596f45.PNG)


# *kill: 프로세스에 종료 시그널을 보낸다. -9는 강제 종료다.*
-killall: 프로세스 이름으로 종료하는 명령어다.

|kill|시그널 및 영어|설명|
|---|---|---|
|   |SIGHUP & hang up|세션이 종료될 때 시스템이 내리는 시그널|
|   |SIGINT & interrupt|종료 요청 시그널|
|   |SIGKILL & kill|강제 종료 시그널|
|   |SIGSEGV & segment violation|메모리 침범이 일어날 때 시스템이 보내는 시그널|
|   |SIGTERM & terminate|종료 요청 시그널|
|   |SIGTSTP & temporary stop|일시 중지 요청 시그널|


**kill 시그널 리스트**

![kill](https://user-images.githubusercontent.com/104884552/172042733-d87a1868-ac1d-4c72-8ac8-9075c1d655e2.PNG)


**프로세스에 시그널 보내기**
>$ kill [option] PID
># 1234(PID) 프로세스 종료
>$ kill -9 1234
>$ kill -SIGKILL 1234
