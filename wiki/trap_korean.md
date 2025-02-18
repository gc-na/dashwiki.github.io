# [한국어] Debian Almquist Shell (dash) trap 사용법: 신호 처리

## Overview
`trap` 명령은 셸 스크립트에서 특정 신호를 처리할 수 있도록 해주는 기능입니다. 이를 통해 스크립트가 종료되기 전에 특정 작업을 수행하거나, 예외 상황에 대처할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```sh
trap [options] [arguments]
```

## Common Options
- `-l`: 사용할 수 있는 신호 목록을 표시합니다.
- `-p`: 현재 설정된 trap을 출력합니다.
- `SIGNAL`: 특정 신호를 지정하여 해당 신호가 발생했을 때 실행할 명령을 설정합니다.

## Common Examples
1. **SIGINT 신호 처리하기**
   ```sh
   trap 'echo "프로그램이 중단되었습니다."' SIGINT
   while true; do
       sleep 1
   done
   ```

2. **종료 시 클린업 작업 수행하기**
   ```sh
   trap 'rm -f /tmp/tempfile; echo "정리 완료."' EXIT
   touch /tmp/tempfile
   ```

3. **신호 목록 보기**
   ```sh
   trap -l
   ```

4. **현재 trap 설정 확인하기**
   ```sh
   trap -p
   ```

## Tips
- 스크립트의 시작 부분에 trap을 설정하여 모든 신호에 대해 일관된 처리를 할 수 있습니다.
- 여러 신호를 동시에 처리할 수 있으므로, 필요한 경우 여러 개의 trap을 설정하는 것을 고려하세요.
- 스크립트가 종료될 때 항상 클린업 작업을 수행하도록 EXIT 신호를 사용하는 것이 좋습니다.