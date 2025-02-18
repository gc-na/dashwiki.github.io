# [한국어] Debian Almquist Shell (dash) pgrep 사용법: 프로세스 ID 찾기

## Overview
pgrep 명령은 주어진 패턴과 일치하는 프로세스의 프로세스 ID(PID)를 검색하는 데 사용됩니다. 이 명령은 시스템에서 실행 중인 프로세스를 필터링하고, 특정 프로세스를 쉽게 찾을 수 있도록 도와줍니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
pgrep [옵션] [인수]
```

## Common Options
- `-u, --euid <user>`: 특정 사용자에 의해 실행된 프로세스만 검색합니다.
- `-f, --full`: 프로세스의 전체 명령줄을 사용하여 검색합니다.
- `-n, --newest`: 가장 최근에 시작된 프로세스의 PID만 반환합니다.
- `-o, --oldest`: 가장 오래된 프로세스의 PID만 반환합니다.

## Common Examples
- 특정 프로세스 이름으로 PID 찾기:
```bash
pgrep bash
```

- 특정 사용자가 실행한 프로세스 찾기:
```bash
pgrep -u 사용자이름
```

- 전체 명령줄을 사용하여 프로세스 찾기:
```bash
pgrep -f "python script.py"
```

- 가장 최근에 시작된 프로세스의 PID 찾기:
```bash
pgrep -n httpd
```

- 가장 오래된 프로세스의 PID 찾기:
```bash
pgrep -o sshd
```

## Tips
- pgrep 명령은 스크립트에서 특정 프로세스를 확인할 때 유용합니다.
- 여러 옵션을 조합하여 더 정교한 검색이 가능합니다.
- PID를 직접 사용하여 프로세스를 종료할 때 `kill $(pgrep 프로세스명)` 형식으로 사용할 수 있습니다.