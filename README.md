# Deployment

# Key Learning
1. 자바 스크립트 DOM에 대해 배웠고, querySelector 같은 함수들을 통해 자바 스크립트에서 html에 어떤 방식으로 접근하는지 를 배웠다.DOM객체를 통해 접근함. Select - event - change
2. java 어레이를 다루는 함수들에 대해 알아 보았다. (push(),find(),slice())
3. 자바 스크립트 함수를 다룰때 부모 클래스 하위의 자식 클래스에 element를 집어넣으려면, appendChild를 사용하고, ParentElement.remove();로 부모 요소를 포함하여 한번에 삭제 시킬 수 있다. 또한, innerHtml이나 innerText등 Html의 내부요소를 수정할 수 있다 DOM객체를 통해서.

# CRUD Service
- 구현 서비스 주제 : 축구 선수 관리 프로그램
- 사용 데이터 필드 : 선수 이름 , 사는 국가, 선수 포지션, 키, 몸무게
- Create는 우선 입력 폼의 내용이 validation이 맞는 지 먼저 체크한다.(필수 입력 요소 입력했는지, 키의 크기는 230이하로 잘 적었는지, 이름의 길이는 5자 이하로 잘 적었는지) 그리고, newplayer로 MAP 형식으로 변수를 선언하고(폼으로 입력받은 값을 map변수에 저장함),그리고 지금 폼입력이 edit을 위한 건지 add를 위한건지를 확인하기위해 edit index를 확인하고 그것이 null일 경우 players.push()로 새롭게 만든 변수를 넣어준다. 
- Update는 edit button이 클릭되는 이벤트 발생시, create와 같이 validation이 맞는지 체크하고, i번 째 editindex를 저장해두고, 거기에 맞는 index의 player array에 값을 새로 넣어준다. 그리고render()로 다시 띄워줌.
- delete는 delete 버튼 클릭 이벤트 발생시, configure로 삭제할건지 한번 물어보고 players.splice(i,1) i번째 즉 클릭한 버튼의 index의 array값을 삭제하고 다시 render()을 호출하여 띄운다.
- Read는 입력받은 데이터가 들어있는 array를 들어있는 데이터값 만큼 반복하면서, render()함수를 통해, table의 tr요소를 생성하여, i번째 array의 데이터를 tr에 innerHTML로 넣어준다. tbody.appendChild(tr);그리고 tr 값을 tbody의 하위 클래스로 넣어주면 , render함수를 호출 했을때, 화면의 tbody영역에 새로운 요소들이 뜬다.

# JavaScript
1. querySelector() : html을 읽고, 파라미터에 들어있는 id값을 불러와서 새로운 변수에 저장해주는 역할을 한다.
2. addEventListener() : 버튼이나, 로드 등 특정 이벤트를 읽고, 그것이 발생하면 내부의 function을 호출하여 change하는 역할을 한다.
3. createElement() : 이번 과제에는 tr,td,button 등의 요소를 추가하여서 객체로써 사용했다.
4. appendChild() : createElement로 만든 요소들에 특정 값을 저장하면 그 요소를 다른 요소의 하위 요소로 넣어주는 역할을 한다.
5. Array : script에서 find(),push(),slice()같은 함수들로 쉽게 array를 다룰 수 있게 함.
6. render() : render 함수를 사용하여, create나 delete, update를 하면 render()를 호출하여 화면에 list상태를 보여주는 역할을 수행했다.

# AI / Search Usage
AI를 사용하여, table-hover라는 부트스트랩 css속성을 찾아 보았고, innerHTML로 특정 index의 array 값을 넣을 때, ' ' 를 사용하여 넣는 방법을 배웠다. 또한 수정할 경우, 임시 저장해두는 index를 만들어서 수정/추가 후 그 index를 저장해두는 방식을 배웠다. 또한 slice()함수를 통해 array값을 삭제하는 메커니즘을 익혔다.

# Problem & Solution
구현 중, name length validation을 구현 할 때, name.value.trim()>5로 구현해서 옳게 작동하지 않았었다. 그러나 name.value.trim().length>5로 수정하여 해결했다.

# Reflection
이번 과제를 통해서, javascript DOM의 개념과 다양한 접근 방식에 대해 알 수 있었고, CRUD의 작동원리 및, render()함수 구성에 대해 자세히 알아보고 연습해 볼 수 있었다.

