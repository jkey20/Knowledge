### MVP
Model, View, Presenter로 구성

#### Model
- 데이터 상태, 데이터를 가공하는 로직

#### View
- UI(Activity, Fragment도 View의 일부로 간주)
- Model에서 처리된 데이터를 Presenter를 통해 받아서 유저에게 보여줌
- 유저가 발생시킨 Action을 Presenter에 보냄

#### Presenter
- Model과 View 사이에서 데이터를 전달하는 역할
- MVC의 Controller와 다르게 인터페이스로 연결됨

##### 장점 
- Model과 View간의 결합도가 낮아짐

##### 단점
- View와 Presenter간의 의존성이 강해짐