# react-Lifecycle

### 리액트 라이프사이클
리액트가 브라우저에 그려지는 순간부터 사라지는 순간까지 여러 지점에서 메소드를 오버라이딩 할수 있게 도와줌  

### 리액트 버전16.3 이전의 라이프사이클

### Component 생성 및 마운트 
- constructor
- componentWillMount 
- render
- componentDidMount

### Component props, state 변경
- componentWillReceviceProps 
- shouldComponentUpdate
- componentWillUpdate
- render
- componentDidUpdate

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
