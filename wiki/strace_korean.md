# [리눅스] Debian Almquist Shell (dash) strace 사용법: 시스템 호출 추적

## Overview
`strace` 명령어는 프로그램이 수행하는 시스템 호출과 신호를 추적하는 도구입니다. 이를 통해 개발자는 프로그램의 동작을 분석하고, 문제를 진단하며, 성능을 최적화할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: 각 시스템 호출의 통계 정보를 요약하여 출력합니다.
- `-e trace=SYSCALL`: 특정 시스템 호출만 추적합니다. SYSCALL은 추적할 시스템 호출의 이름입니다.
- `-o FILE`: 출력 결과를 지정한 파일에 저장합니다.
- `-p PID`: 이미 실행 중인 프로세스의 시스템 호출을 추적합니다. PID는 프로세스 ID입니다.

## Common Examples
- 기본적인 strace 사용 예:
```bash
strace ls
```
이 명령은 `ls` 명령어가 실행되는 동안의 시스템 호출을 출력합니다.

- 특정 시스템 호출만 추적하기:
```bash
strace -e trace=open ls
```
이 명령은 `ls` 명령어가 실행되는 동안 `open` 시스템 호출만 추적합니다.

- 출력 결과를 파일에 저장하기:
```bash
strace -o output.txt ls
```
이 명령은 `ls` 명령어의 시스템 호출 결과를 `output.txt` 파일에 저장합니다.

- 실행 중인 프로세스 추적하기:
```bash
strace -p 1234
```
이 명령은 PID가 1234인 프로세스의 시스템 호출을 추적합니다.

## Tips
- `strace`의 출력이 너무 많을 경우, `-c` 옵션을 사용하여 요약 정보를 확인하는 것이 유용합니다.
- 특정 오류를 추적할 때는 `-e trace=error` 옵션을 사용하여 오류 관련 시스템 호출만 집중적으로 분석할 수 있습니다.
- 성능 문제를 진단할 때는 `-tt` 옵션을 사용하여 각 시스템 호출의 타임스탬프를 포함시켜 분석할 수 있습니다.