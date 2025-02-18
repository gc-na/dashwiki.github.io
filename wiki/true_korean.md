# [리눅스] Debian Almquist Shell (dash) true 사용법: 항상 성공하는 명령어

## Overview
`true` 명령어는 항상 성공하는 상태 코드를 반환하는 간단한 명령어입니다. 주로 스크립트에서 조건문이나 반복문에서 사용되며, 특정 작업이 필요하지 않을 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```sh
true [options] [arguments]
```

## Common Options
`true` 명령어는 특별한 옵션이 필요하지 않지만, 다음과 같은 일반적인 사용 방법이 있습니다:
- `--help`: 사용법을 보여줍니다.
- `--version`: 버전 정보를 표시합니다.

## Common Examples
다음은 `true` 명령어의 몇 가지 실용적인 예입니다:

1. **조건문에서 사용하기**
   ```sh
   if true; then
       echo "이 메시지는 항상 출력됩니다."
   fi
   ```

2. **무한 루프에서 사용하기**
   ```sh
   while true; do
       echo "이 메시지는 계속 출력됩니다."
       sleep 1
   done
   ```

3. **명령어의 성공을 강제로 반환하기**
   ```sh
   command_that_might_fail || true
   ```

## Tips
- `true` 명령어는 스크립트에서 조건을 항상 참으로 만들고 싶을 때 유용합니다.
- `false` 명령어와 함께 사용하여 조건문을 테스트할 수 있습니다.
- 스크립트의 가독성을 높이기 위해 `true`를 적절히 사용하세요.