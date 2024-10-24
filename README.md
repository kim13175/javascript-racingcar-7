# javascript-racingcar-precourse

### design goal
---
```
큰 함수를 단일 역할을 수행하는 작은 함수로 분리
 - 단일 책임의 원칙을 지켜야 한다.
테스트 도구를 사용하는 방법을 배우고 프로그램이 제대로 작동하는지 테스트 해야 한다.
```
### 구현할 기능 목록 정리
---
#### feature 1. 전진 또는 멈출 수 있는 자동차를 생성

1-1. 자동차마다 이름을 부여할 수 있음
```
/* 자동차의 이름은 쉼표를 기준으로 구분됨 */
string = Console.readLineAsync
Car.name = string.split(",")
```
1-2. 자동차 이름의 제한 글자 수는 5이다.
```
LIMITS_CAR_NAME_LEN = 5;
if (Car.name.length > LIMITS_CAR_NAME_LEN){ throw new Error ["msg"] }
```

#### feature 2. 차의 이동 기준은 입력 값으로 받는다.
2-1. 시도할 횟수를 입력으로 받는다.
```
시도할 횟수는 몇 회인가요?
(시도할 횟수 입력 입력해야 함)
```
2-2. 전진하는 조건은 0에서 9사이의 무작위 값 중 4 이상일 경우이다.
```
/* 0에서 9까지의 정수 중 한 개의 정수 반환 */
MissionUtils.Random.pickNumberInRange(0, 9);
```
#### feature 3. 실행 결과를 매번 출력한다.
```
실행 결과
pobi : -
woni : 
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----
```
#### feature 4. 최종 우승자를 알려주기 위해 최종 우승자를 출력한다.
4-1. 공동 우승자가 있는 경우가 있다.
 - 이경우는 쉼표를 이용하여 이름을 구분하고 우승자를 모두 출력해준다.
```
/* 단독 우승자 안내 문구 */
최종 우승자 : pobi
/* 공동 우승자 안내 문구 */
최종 우승자 : pobi, jun
```
#### feature 5. 사용자가 잘못된 값을 입력할 경우 에러 메시지를 출력한다.
```
[ERROR]로 시작하는 메시지를 출력하고 Error를 발생시키고 프로그램을 종료해야 한다.
```
