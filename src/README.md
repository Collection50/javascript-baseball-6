# 기능 요구 사항

## 클래스 레벨

- 몇 개의 객체가 책임을 분리할 것인가 관점에서 고민

### 컴퓨터 객체

- 게임 진행 관리
- 입력값 매칭

### 유저 객체

- 입력 관리

<br/>

## 함수 레벨

- 각 객체의 함수 및 `util` 함수 관점에서 고민

### 입출력

- `Console.readLineAsync` 사용
- `Promise` 객체를 반환하므로 비동기 기반의 입력 함수
- 에러 핸들링 처리 필요
- 모듈화 관점 고민

### 난수 생성하기

- `Random.pickNumberInRange()` 사용
- **겹치지 않는** 3개 랜덤 뽑기

### 입력 비교하여 결과 반환하기

- 컴퓨터의 난수(랜덤 값)와 유저 입력값 비교하여 `볼`, `스트라이크`, `낫싱`에 해당하는 객체 생성
- 해당 객체 반환 => 출력 값은 컨트롤러에서 처리

<br/>

# 예외 사항

- [] 유저의 입력값이 숫자가 아닌 경우
- [] 유저의 입력값이 3자리가 아닌 경우
- [] 게임 재시작할 때는 `1`, `2`가 아닌 경우
- [] `'[ERROR]'`로 시작하는 에러 메시지

<br/>

# 더 나아가서

## 변경에 유연하게 대처하고 싶다

- 맞추는 개수가 3개에서 변경된다면?
- 재시작/종료를 구분하는 값이 변경된다면?
- 책임을 분리해 의존성을 조금 줄이는 방식으로 고민