# [한국어] Debian Almquist Shell (dash) test 사용법: 조건 평가

## Overview
`test` 명령어는 주어진 조건을 평가하여 참(true) 또는 거짓(false)을 반환하는 유틸리티입니다. 주로 스크립트 내에서 조건문을 작성할 때 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```
test [options] [arguments]
```

## Common Options
- `-e FILE`: 파일이 존재하는지 확인합니다.
- `-d FILE`: 주어진 경로가 디렉토리인지 확인합니다.
- `-f FILE`: 주어진 경로가 일반 파일인지 확인합니다.
- `-z STRING`: 문자열이 비어 있는지 확인합니다.
- `-n STRING`: 문자열이 비어 있지 않은지 확인합니다.
- `STRING1 = STRING2`: 두 문자열이 같은지 비교합니다.

## Common Examples
- 파일 존재 여부 확인:
  ```sh
  test -e /path/to/file && echo "파일이 존재합니다."
  ```

- 디렉토리인지 확인:
  ```sh
  test -d /path/to/directory && echo "디렉토리입니다."
  ```

- 일반 파일인지 확인:
  ```sh
  test -f /path/to/file && echo "일반 파일입니다."
  ```

- 문자열 비어 있는지 확인:
  ```sh
  str="Hello"
  test -n "$str" && echo "문자열이 비어 있지 않습니다."
  ```

- 두 문자열 비교:
  ```sh
  str1="test"
  str2="test"
  test "$str1" = "$str2" && echo "두 문자열이 같습니다."
  ```

## Tips
- `test` 명령어는 `[`와 `]`로 대체할 수 있습니다. 예를 들어, `test -e file`는 `[ -e file ]`로 쓸 수 있습니다.
- 조건문을 사용할 때는 `&&`와 `||`를 활용하여 여러 조건을 조합할 수 있습니다.
- 스크립트 내에서 `if` 문과 함께 사용할 때, `test`의 결과를 활용하여 흐름 제어를 할 수 있습니다.