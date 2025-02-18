# [리눅스] Debian Almquist Shell (dash) socat 사용법: 데이터 전송 및 변환

## Overview
socat은 소켓을 통해 데이터를 전송하고 변환하는 데 사용되는 강력한 도구입니다. 이 명령은 다양한 프로토콜과 데이터 스트림 간의 연결을 설정할 수 있으며, 네트워크와 로컬 데이터 간의 브리지 역할을 합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
socat [options] [arguments]
```

## Common Options
- `-d`: 디버그 모드를 활성화하여 자세한 정보를 출력합니다.
- `-v`: 전송되는 데이터를 자세히 출력합니다.
- `TCP:<host>:<port>`: TCP 소켓을 사용하여 지정된 호스트와 포트에 연결합니다.
- `UDP:<host>:<port>`: UDP 소켓을 사용하여 지정된 호스트와 포트에 연결합니다.
- `STDIN`: 표준 입력을 사용하여 데이터를 읽습니다.
- `STDOUT`: 표준 출력을 사용하여 데이터를 씁니다.

## Common Examples
- **TCP 연결 설정**
```bash
socat TCP:example.com:80 STDOUT
```
위 명령은 example.com의 80번 포트에 TCP 연결을 설정하고, 그 결과를 표준 출력으로 보냅니다.

- **UDP 데이터 전송**
```bash
socat -u UDP:localhost:1234 -
```
이 명령은 로컬호스트의 1234번 포트로 UDP 패킷을 전송합니다.

- **파일을 소켓으로 전송**
```bash
socat -u FILE:/path/to/file TCP:example.com:80
```
지정된 파일을 example.com의 80번 포트로 전송합니다.

- **서버와 클라이언트 간의 데이터 전송**
```bash
socat TCP-LISTEN:1234,reuseaddr,fork STDOUT
```
1234번 포트에서 수신 대기하며, 클라이언트의 데이터를 표준 출력으로 보냅니다.

## Tips
- socat의 디버그 모드를 활성화하여 문제를 해결하는 데 유용한 정보를 얻을 수 있습니다.
- 다양한 프로토콜을 조합하여 복잡한 데이터 전송 작업을 수행할 수 있습니다.
- 보안이 중요한 경우, SSH 터널링과 함께 socat을 사용하는 것이 좋습니다.