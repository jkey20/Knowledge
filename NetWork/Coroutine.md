### Coroutine
- 필요에 따라 일시중단이 가능한 작업의 단위

#### 사용이유
- 동시성 프로그래밍을 가능하게 하기위해

#### 사용법
- 특정 scope에 실행될 dispatcher를 넘겨주고 launch, async등을 이용해서 이를 실행함
- suspend 함수는 중지되거나 취소될 수 있기 때문에 코루틴 안에서 실행되어야함

