# 우테코 프리코스 3주차 [자동차 게임]
## 과제 수행 체크리스트
#### 개발 과정 준수 사항
- [ ] 코드 포매팅 사용
- [ ] README.MD 기능 목록 수시로 업데이트
- [ ] 자바스크립트 코드 컨벤션 준수
- [ ] 코드의 목적이 들어나는 변수명 고려

#### 코드 준수 사항
- [ ] let 선언 줄이기, const 사용
- [ ] 접근제어자 표시 
- [ ] 값 하드 코딩 금지, 상수화
- [ ] 들여쓰기 depth 2이내
- [ ] else 문 지양
- [ ] 함수 길이 15라인 이내 유지 (한 가지 기능)
- [ ] 구현 순서 준수(클래스 : 필드, 생성자, 매서드 순)
- [ ] 메서드가 한 가지 기능을 담당하는지 확인하는 기준 세우기 (ex: 15줄 이내)
- [ ] 예외 처리 (validation) 를 따로 분류하여 관리하기

#### 테스트 코드 준수 사항
- [ ] 테스트를 작성하는 이유에 대해 생각하기
- [ ] Jest 이용 테스트코드 
- [ ] 기능의 단위 테스트 작성 (UI(System.out, System.in, Scanner) 로직은 제외한다.)

## 기능 구현 목록
### 입력
- #### 사용자 입력
    - [x] 로또 구입 금액을 입력한다.
    - [x] 당첨번호를 입력한다. 
    - [x] 보너스 번호를 입력한다. 
- #### 입력 처리
    - [x] 로또 구입 금액을 통해 로또 구입 개수 계산한다.
    - [x] 당첨 번호 입력을 구분자로 구분한다.
    - [x] 사용자의 구입 금액을 저장한다.
    - [x] 사용자의 당첨 번호를 저장한다.
    - [x] 사용자의 보너스 번호를 저장한다.

- #### 입력 조건
    - 로또 구입 금액은 1000원 단위로 입력 받는다.
    - 당첨 번호는 쉼표를 기준으로 구분한다.
    - 로또 번호는 1에서 45사이의 숫자여야 한다. 
    - 로또 번호의 중복이 있으면 안된다. (보너스도 마찬가지)
    - 로또 번호는 6자리이다.
    - 보너스 번호는 숫자 하나이다.

- #### 입력 예외 처리 목록
    - 구입 금액
        - [x] 로또 구입 금액이 숫자가 아닌 값이 입력된 경우.
        - [x] 로또 구입 금액이 1000원 단위가 아닐 경우.
        - [x] 로또 구입 금액이 소수인 경우.
    - 로또 번호
        - [x] 로또 번호 중 숫자가 아닌 특수문자가 있을 경우. 로또 번호 입력형식에 맞지 않은 경우.
        - [x] 로또 번호가 1에서 45사이의 숫자가 아닐 경우.
        - [ ] 로또 번호에 중복이 있을 경우. + 보너스 번호 포함.
        - [x] 로또 번호가 보너스 제외하고 6자리가 아닐 경우.
        - [x] 로또 번호가 소수일 경우
    - 보너스 번호
        - [ ] 보너스 번호가 숫자가 아닌 특수문자일 경우.
        - [x] 보너스 번호가 1에서 45사이의 숫자가 아닐 경우.
        - [ ] 보너스 번호가 중복일 경우
        - [x] 보너스 번호가 소수일 경우

### 로또 게임 진행
- #### 당첨 로또 번호 생성
    - [x] 랜덤한 당첨 번호를 생성한다.
    - [x] 랜덤한 보너스 번호를 생성한다.
- #### 사용자의 로또 당첨 여부 확인
    - [ ] 사용자의 당첨 번호와 비교했을 때 일치하는 개수를 구한다.
    - [ ] 사용자의 보너스 번호와 비교했을 때 일치하는지 확인한다.
- #### 사용자의 로또 게임 결과 판단
    - [ ] 사용자의 로또가 몇 등 당첨인지 판단한다.
    - [ ] 당첨 금액 및 투입 금액에 따른 사용자의 수익률을 계산한다.

### 출력
- #### 안내 메시지
    - [ ] 구매한 로또의 개수를 출력한다.
    - [ ] 당첨 통계 안내 메시지를 출력한다.
- #### 로또 결과 출력
    - [ ] 정해진 당첨 등수를 모두 출력한다. 그와 함께 사용자가 각 등수에 당첨된 개수를 출력한다.
    - [ ] 사용자의 수익률을 출력한다.