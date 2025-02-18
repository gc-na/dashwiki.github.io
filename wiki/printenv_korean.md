# [리눅스] Debian Almquist Shell (dash) printenv 사용법: 환경 변수 출력

## Overview
`printenv` 명령어는 현재 세션의 환경 변수를 출력하는 데 사용됩니다. 이 명령어를 통해 시스템에서 설정된 다양한 환경 변수의 값을 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```sh
printenv [options] [arguments]
```

## Common Options
- `-0`, `--null`: 출력 결과를 널 문자로 구분합니다.
- `NAME`: 특정 환경 변수의 값을 출력합니다. 변수 이름을 인자로 제공하면 해당 변수의 값만 표시됩니다.

## Common Examples
- 모든 환경 변수 출력:
```sh
printenv
```

- 특정 환경 변수 출력 (예: `HOME` 변수):
```sh
printenv HOME
```

- 여러 환경 변수를 출력 (예: `PATH`와 `USER` 변수):
```sh
printenv PATH USER
```

- 널 문자로 구분된 출력:
```sh
printenv -0
```

## Tips
- `printenv` 명령어는 스크립트에서 환경 변수를 확인할 때 유용합니다.
- 특정 환경 변수를 확인하고 싶을 때는 변수 이름을 인자로 제공하여 간편하게 사용할 수 있습니다.
- 환경 변수의 값을 변경하고 싶다면 `export` 명령어를 사용하여 새로운 값을 설정한 후 `printenv`로 확인할 수 있습니다.