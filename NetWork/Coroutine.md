## Coroutine
- 필요에 따라 일시중단이 가능한 작업의 단위

### 사용이유
- 동시성 프로그래밍을 가능하게 하기위해
- 쓰레드를 만드는 대신 하나의 쓰레드상에서 자신을 일시중지할 수 있도록 하여 쓰레드 생성비용을 줄임 
- 하나의 쓰레드에서 여러개의 코루틴을 실행할 수 있음
- 
### 사용법
- 특정 [scope](#Scope)에 실행될 [dispatcher](#Dispatcher)를 넘겨주고 [launch](#Launch), [async](#Async)등을 이용해서 이를 실행함
- [suspend 함수](#Suspend)는 중지되거나 취소될 수 있기 때문에 코루틴 안에서 실행되어야함

-----

#### Scope <a id="Scope"></a>
- 모든 코루틴은 스코프 내에서 실행되어야 함
- 스코프를 통해서 액티비티 또는 프래그먼트의 생명주기에 따라 소멸될 때 관련된 코루틴을 한번에 취소할 수 있음
- 이를 통해 메모리 누수를 방지
- 커스텀 or 내장된 범위를 사용할 수 있음 
- CoroutineScope, GlobalScope, LifeCycleScope, ViewModelScope가 존재

##### CoroutineScope
- 코루틴 라이브러리에서 기본적으로 제공하는 스코프
- 액티비티 or 클래스의 인스턴스가 사라지면 메모리에서 해제

##### GlobalScope
- 코루틴을 앱 전체에서 작동시키기 위해 사용
- 앱의 생명주기와 함께 동작
- 별도의 생명주기 관리가 필요없음
- 앱이 실행되는 동안 장기적 or 주기적으로 실행되어야 하는 코루틴에 적합
##### LifeCycleScope
- 


-----
#### Dispatcher <a id="Dispatcher"></a>
- 쓰레드에 코루틴을 보내는 역할
- 받은 코루틴을 Thread Pool에서 자원이 남는 쓰레드에 배분
- 안드로이드에서는 Main, IO, Default 3가지로 생성되어있음

##### Dispatchers.Main
- UI와 상호작용을 하는 작업을 위해서만 사용

##### Dispatchers.IO
- 디스크 또는 네트워크 I/O 작업을 실행하는데 최적화

##### Dispatchers.Default
- CPU를 많이 사용하는 작업을 기본 쓰레드 외부에서 실행하도록 최적화
- 정렬작업, JSON파싱 등에 최적화
------

#### launch <a id="Launch"></a>
- 결과 반환이 없는 단순작업에 사용
- 수행시 [Job](#Job) 반환
#### async <a id="Async"></a>
- 결과 반환이 필요한 작업에 사용
- 결과값을 Deferred로 감싸서 반환

##### Deferred
- 미래에 올 수 있는 값을 담아놓을 수 있는 객체
-----

#### job <a id="Job"></a>
- 결과가 없는 비동기 작업
- 예외가 발생하지 않는 이상 끝까지 수행
- 생성 후 바로 실행됨

-----
##### suspend fun <a id="Suspend"></a>
- 일시중단 가능한 함수를 지칭
- 해당 함수내에 일시중단이 가능한 작업이 있다는것을 의미
