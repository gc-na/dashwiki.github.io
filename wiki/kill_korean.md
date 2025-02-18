# [리눅스] Debian Almquist Shell (dash) kill 사용법: 프로세스 종료

## Overview
`kill` 명령어는 특정 프로세스를 종료하는 데 사용됩니다. 프로세스 ID(PID)를 지정하여 해당 프로세스를 강제로 종료할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
kill [options] [arguments]
```

## Common Options
- `-l`: 신호 목록을 출력합니다.
- `-s SIGNAL`: 종료할 신호를 지정합니다. 기본값은 `TERM`입니다.
- `-n NUMBER`: 신호 번호를 사용하여 신호를 지정합니다.

## Common Examples
1. 특정 PID의 프로세스를 종료합니다:
   ```bash
   kill 1234
   ```

2. 프로세스에 `SIGKILL` 신호를 보내 강제로 종료합니다:
   ```bash
   kill -9 1234
   ```

3. 모든 프로세스를 종료하는 `SIGTERM` 신호를 보냅니다:
   ```bash
   kill -TERM 1234
   ```

4. 프로세스 이름을 사용하여 종료합니다 (예: `pkill` 명령어 사용):
   ```bash
   pkill myprocess
   ```

5. 신호 목록을 확인합니다:
   ```bash
   kill -l
   ```

## Tips
- 프로세스를 종료하기 전에 해당 프로세스가 안전하게 종료될 수 있도록 `SIGTERM` 신호를 먼저 보내는 것이 좋습니다.
- `kill` 명령어를 사용할 때는 항상 PID를 정확히 확인하고 사용하세요. 잘못된 PID를 종료하면 시스템에 문제가 발생할 수 있습니다.
- `pkill` 명령어를 사용하면 프로세스 이름으로 쉽게 종료할 수 있습니다.