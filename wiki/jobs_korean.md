# [한국어] Debian Almquist Shell (dash) jobs 사용법: 백그라운드 작업 관리

## Overview
`jobs` 명령어는 현재 셸 세션에서 실행 중인 백그라운드 작업의 상태를 표시합니다. 이를 통해 사용자는 어떤 작업이 실행 중인지, 중지되었는지, 또는 완료되었는지를 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
jobs [options] [arguments]
```

## Common Options
- `-l`: 각 작업에 대한 프로세스 ID(PID)를 함께 표시합니다.
- `-n`: 최근에 상태가 변경된 작업만 표시합니다.
- `-p`: 작업의 프로세스 ID만 출력합니다.

## Common Examples
다음은 `jobs` 명령어의 몇 가지 일반적인 예입니다.

1. 현재 실행 중인 모든 작업 보기:
   ```sh
   jobs
   ```

2. 프로세스 ID와 함께 작업 보기:
   ```sh
   jobs -l
   ```

3. 최근에 상태가 변경된 작업만 보기:
   ```sh
   jobs -n
   ```

4. 작업의 프로세스 ID만 출력하기:
   ```sh
   jobs -p
   ```

## Tips
- 백그라운드에서 실행 중인 작업을 확인할 때 `jobs` 명령어를 사용하면 유용합니다.
- 작업을 중지하고 싶다면 `Ctrl+Z`를 사용하여 작업을 일시 중지한 후, `bg` 명령어로 백그라운드에서 계속 실행할 수 있습니다.
- `fg` 명령어를 사용하여 백그라운드 작업을 포그라운드로 가져올 수 있습니다.