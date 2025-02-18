# [리눅스] Debian Almquist Shell (dash) dstat 사용법: 시스템 성능 모니터링

## Overview
dstat 명령어는 시스템의 성능을 실시간으로 모니터링할 수 있는 도구입니다. CPU, 메모리, 디스크 I/O, 네트워크 트래픽 등 다양한 시스템 자원의 사용 현황을 한눈에 확인할 수 있습니다.

## Usage
dstat의 기본 구문은 다음과 같습니다:
```bash
dstat [options] [arguments]
```

## Common Options
- `-c`: CPU 사용량을 표시합니다.
- `-d`: 디스크 I/O 통계를 표시합니다.
- `-n`: 네트워크 통계를 표시합니다.
- `-m`: 메모리 사용량을 표시합니다.
- `-t`: 타임스탬프를 추가하여 출력합니다.

## Common Examples
- CPU와 메모리 사용량을 모니터링하기:
```bash
dstat -c -m
```

- 디스크 I/O와 네트워크 트래픽을 모니터링하기:
```bash
dstat -d -n
```

- 모든 통계를 실시간으로 모니터링하기:
```bash
dstat -cdnm
```

- 타임스탬프와 함께 CPU, 메모리, 디스크 사용량을 모니터링하기:
```bash
dstat -t -c -m -d
```

## Tips
- dstat를 사용할 때는 필요한 옵션만 선택하여 시스템 자원 사용을 최소화하는 것이 좋습니다.
- 장기적인 모니터링을 위해 dstat 출력을 파일로 저장할 수 있습니다. 예를 들어, `dstat -cdmn > output.txt`와 같이 사용할 수 있습니다.
- dstat의 출력 형식을 사용자 정의하여 필요한 정보만 표시하도록 설정할 수 있습니다.