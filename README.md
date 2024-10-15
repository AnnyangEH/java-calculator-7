# 문자열 덧셈 계산기 📟
## 과제 진행 요구 사항 📋
- 미션은 문자열 덧셈 계산기 저장소를 포크하고 클론하는 것으로 시작한다.
- 기능을 구현하기 전 README.md에 구현할 기능 목록을 정리해 추가한다.
- Git의 커밋 단위는 앞 단계에서 README.md에 정리한 기능 목록 단위로 추가한다.
    - AngularJS Git Commit Message Conventions을 참고해 커밋 메시지를 작성한다.
- 자세한 과제 진행 방법은 프리코스 진행 가이드 문서를 참고한다.

## 기능 요구 사항 🎯
입력한 문자열에서 숫자를 추출하여 더하는 계산기를 구현한다.

- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다.
	- 예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6
앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는
- 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
	- 예를 들어 "//;\n1;2;3"과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.
## 입출력 요구 사항 🖨️
입력
- 구분자와 양수로 구성된 문자열

출력
- 덧셈 결과

`결과 : 6`

실행 결과 예시
```
덧셈할 문자열을 입력해 주세요.
1,2:3
결과 : 6
```
## 구현할 기능 목록 ✅


- 구분자 지정 함수

	 - 쉼표(,)와 콜론(:)을 기본 구분자로 지정하여 문자열을 분리할 수 있는 함수를 구현합니다.

- 문자열 분리 함수
	- 주어진 문자열을 지정된 구분자를 기준으로 분리하여 숫자 목록으로 변환하는 함수를 구현합니다.

- 커스텀 구분자 지정 함수
	- 문자열 앞부분의 //와 \n 사이에 위치하는 문자를 커스텀 구분자로 사용하여 문자열을 분리할 수 있는 함수를 구현합니다.

- 계산 함수
	- 분리된 숫자 목록을 더해 결과를 반환하는 함수를 구현합니다.

- 예외 처리 함수
	 - 입력 문자열이 유효하지 않은 경우 IllegalArgumentException을 발생시키고 애플리케이션을 종료하는 예외 처리 로직을 구현합니다.