### MVVM
Model, View, ViewModel로 구성

#### Model
- 데이터 상태, 데이터를 가공하는 로직

#### View
- UI(Activty or Fragment)
- UI 변경과 관련된 로직은 포함될 수 있음
- ViewModel을 관찰하고 상태변화가 전달되면 화면을 갱신

#### ViewModel
- View와 Model사이에서 데이터를 전달
- 모든 View와 관련된 비즈니스 로직이 들어가있음
- 데이터를 가공해서 View에서 표시되게할 Model로 바꾸는 역할
- ViewModel과 View는 1:N 관계를 가질 수 있음
- 여러개의 Fragment가 하나의 ViewModel을 가질 수 있음

##### 장점
- Model과 View사이, ViewModel과 View 사이의 의존성이 없다.
- DataBinding을 사용하여 View와 ViewModel의 의존성을 낮추고 유닛테스트가 더욱 쉬워짐

##### 단점
- DataBinding의 추가적인 코드들이 필요해진다
- 설계하기 어렵다