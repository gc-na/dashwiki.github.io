# [리눅스] Debian Almquist Shell (dash) netstat 사용법: 네트워크 연결 상태 확인

## Overview
`netstat` 명령어는 네트워크 통계 및 연결 상태를 표시하는 도구입니다. 이 명령어를 사용하면 현재 시스템에서 활성화된 네트워크 연결, 라우팅 테이블, 인터페이스 통계 등을 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다.

```bash
netstat [options] [arguments]
```

## Common Options
- `-a`: 모든 연결 및 수신 대기 포트를 표시합니다.
- `-t`: TCP 연결만 표시합니다.
- `-u`: UDP 연결만 표시합니다.
- `-n`: 주소와 포트를 숫자로 표시합니다.
- `-l`: 수신 대기 중인 소켓만 표시합니다.
- `-p`: 각 연결에 대한 프로세스 ID와 프로그램 이름을 표시합니다.

## Common Examples
다음은 `netstat` 명령어의 몇 가지 일반적인 사용 예입니다.

1. 모든 활성 연결 및 수신 대기 포트 보기:
   ```bash
   netstat -a
   ```

2. TCP 연결만 표시하기:
   ```bash
   netstat -t
   ```

3. UDP 연결만 표시하기:
   ```bash
   netstat -u
   ```

4. 숫자 형식으로 주소와 포트 표시하기:
   ```bash
   netstat -n
   ```

5. 수신 대기 중인 소켓만 표시하기:
   ```bash
   netstat -l
   ```

6. 각 연결에 대한 프로세스 정보 표시하기:
   ```bash
   netstat -p
   ```

## Tips
- `netstat` 명령어는 루트 권한으로 실행할 때 더 많은 정보를 제공할 수 있습니다.
- `netstat`의 출력 결과를 `grep`과 함께 사용하여 특정 포트나 주소를 필터링할 수 있습니다.
- 시스템의 네트워크 성능을 모니터링하기 위해 주기적으로 `netstat`를 실행하는 것이 좋습니다.