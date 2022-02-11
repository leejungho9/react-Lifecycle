# react-Lifecycle

### 리액트 라이프사이클
리액트가 브라우저에 그려지는 순간부터 사라지는 순간까지 여러 지점에서 메소드를 오버라이딩 할수 있게 도움을 줌 

### 리액트 버전16.3 이전의 라이프사이클

### Component 생성 및 마운트 
- constructor
- componentWillMount 
- **render**
- componentDidMount

### Component props, state 변경
- componentWillReceviceProps 
- shouldComponentUpdate
- componentWillUpdate
- **render**
- componentDidUpdate
-
```
componentWillReceviceProps
props를 새로 지정했을 때 바로 호출되며 state의 변경에 반응하지 않는다.
여기서 props 값에 E따라 state를 변경해야 한다먄, setState를 이용해 state를 변경한다.
그러면 다음 이벤트로 가는 것이 아니라 한번에 변경
```

```
shouldComponentUpdate
true, false를 리턴해 실제 render를 조절할 수 있음
불필요한 render를 방지하고 리액트 컴포넌트 성능 최적화에 중요한 역할
props, state 변경되면 실행, new Props와  new State를 인자로 해서 호출
```

### Component 언마운트
- componentWillUnmpunt

### 리액트 버전16.3 이후의 라이프사이클

### Component 생성 및 마운트 
- constructor
- ~~getDerivedStateFromProps~~ => getDerivedStateFromProps
- render
- componentDidMount

### Component props, state 변경
- ~~getDerivedStateFromProps~~ =>getDrerivedStateFromProps
- shouldComponentUpdate
- render
- ~~componentWillUpdate~~ => getSnapshotBeforeUpdate
- componentDidUpdate

### Component 언마운트
componentWillUnmpunt

### Component 에러 캐치
componentDidCatch
문제가 생겼을 때 에러화면을 보여주거나 어떤 동작이 가능해짐 하지만 자기 자신의 문제는 캐치하지 못함
