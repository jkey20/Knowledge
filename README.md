# Knowledge
배운 지식들을 정리합니다

### Layout

#### ConstraintLayout은 언제 사용하는가?
- 복잡한 레이아웃을 단순한 계층구조로 이용하여 만들때 사용


#### LinearLayout은 언제 사용하는가?
- 가로 혹은 세로로 하위 뷰를 정렬하는 경우 사용한다.

#### RelativeLayout이란?
- 레이아웃내의 자식뷰들이 서로간의 상대적인(relative)위치 관계를 정의하여 UI를 배치하는 레이아웃

#### FrameLayout이란?
- 여러 개의 뷰를 중첩으로 배치하고 그중 하나를 레이아웃의 전면에 표시할 때 사용하는 레이아웃


### Android

#### 암시적, 명시적 Intent
- 명시적 인텐트: Intent에 클래스 객체나 컴포넌트 이름을 지정하여 호출할 대상을 확실하게 지정할 수 있을 때  
- 암시적 인텐트: Intent를 호출할 대상이 달라질 수 있는경우 암시적 인텐트  
- ex) 사용자가 메일을 읽을때 메일을 gmail로 읽을 수 있게 암시적 인텐트를 사용  

#### MVC란?
Model, View, Controller로 구성
- Model - 데이터, 상태, 데이터를 가공하는 로직
- View - UI, mvc에서는 xml을 의미
- Controller - Model과 View를 연결해주고 유저에게 액션을 받으면 처리하는 역할(Activity or Fragment)

단점: View와 Model사이의 결합도가 높아 유지보수하기 힘들다.

#### MVP란?
Model, View, Presenter로 구성
View와 Model이 Presenter를 통해서 동작하도록하여 View와 Model의 의존성을 제거
MVC에 Controller에 해당하던 것들이 View에오고 View를 관리하는 인터페이스를 추가하여 Presenter가 독립이게 함 

viewModel에 context가 있으면 안되는 이유
- 

자바와 코틀린의 차이
-

DataBinding은 왜 사용하는가
-

Data binding과 View binding의 차이
-

Retrofit을 사용하면 얻는 이점?
-

BaseActivity, Fragment 등 만드는 이유
-

Room 구성
-

DAO, DTO는 무엇인가?
-

RxJava 사용이유
- 비동기 프로그래밍을 쉽게 하기위해
- 콜백방식의 문제점을 개선하기위해

코루틴 사용이유
- 동시성 프로그래밍을 가능하게 하기위해

<소프트웨어적>
결합도란 무엇인가?
-  클래스의 변경사항이 생겼을 때 다른 클래스에게도 영향을 주는 정도



