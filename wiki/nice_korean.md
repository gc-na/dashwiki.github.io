# [리눅스] Debian Almquist Shell (dash) nice 사용법: 프로세스 우선 순위 조정

## Overview
`nice` 명령어는 프로세스의 우선 순위를 조정하는 데 사용됩니다. 이 명령어를 통해 CPU 자원을 보다 효율적으로 사용할 수 있으며, 특정 프로세스가 시스템의 다른 작업에 미치는 영향을 줄일 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
nice [options] [arguments]
```

## Common Options
- `-n, --adjustment=N`: 프로세스의 우선 순위를 N만큼 조정합니다. 기본값은 10입니다.
- `-h, --help`: 도움말을 표시합니다.
- `--version`: 버전 정보를 표시합니다.

## Common Examples
1. 기본 우선 순위로 프로세스 실행:
    ```bash
    nice myscript.sh
    ```

2. 우선 순위를 낮춰서 프로세스 실행 (우선 순위 15로 설정):
    ```bash
    nice -n 15 myscript.sh
    ```

3. 우선 순위를 높여서 프로세스 실행 (우선 순위 -5로 설정):
    ```bash
    nice -n -5 myscript.sh
    ```

4. 우선 순위를 조정하여 백그라운드에서 실행:
    ```bash
    nice -n 10 long_running_task & 
    ```

## Tips
- `nice` 명령어는 기본적으로 우선 순위를 높이는 것보다 낮추는 데 더 유용합니다. 시스템의 반응성을 유지하면서 리소스를 많이 사용하는 작업을 조정하세요.
- `renice` 명령어를 사용하여 이미 실행 중인 프로세스의 우선 순위를 변경할 수 있습니다.
- 우선 순위를 조정할 때는 시스템의 전체 성능에 미치는 영향을 고려하세요.