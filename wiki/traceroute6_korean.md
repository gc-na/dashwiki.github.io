# [리눅스] Debian Almquist Shell (dash) traceroute6 사용법: IPv6 경로 추적

## Overview
traceroute6 명령은 IPv6 네트워크에서 패킷이 목적지에 도달하기까지 거치는 경로를 추적하는 데 사용됩니다. 이 명령은 각 홉(hop)에서의 응답 시간을 측정하여 네트워크의 성능을 분석하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
traceroute6 [옵션] [목적지]
```

## Common Options
- `-m <최대 홉 수>`: 추적할 최대 홉 수를 설정합니다.
- `-p <포트>`: 사용할 포트 번호를 지정합니다.
- `-w <타임아웃>`: 각 홉에 대한 응답 대기 시간을 설정합니다.
- `-n`: 호스트 이름 대신 IP 주소를 표시합니다.

## Common Examples
1. 기본 사용법:
   ```bash
   traceroute6 example.com
   ```

2. 최대 홉 수를 15로 설정:
   ```bash
   traceroute6 -m 15 example.com
   ```

3. 특정 포트를 사용하여 추적:
   ```bash
   traceroute6 -p 80 example.com
   ```

4. IP 주소만 표시:
   ```bash
   traceroute6 -n example.com
   ```

5. 응답 대기 시간을 2초로 설정:
   ```bash
   traceroute6 -w 2 example.com
   ```

## Tips
- traceroute6 명령은 네트워크 문제를 진단하는 데 유용하므로, 문제가 발생했을 때 자주 사용해 보세요.
- 여러 옵션을 조합하여 사용하면 더욱 효과적으로 네트워크 경로를 분석할 수 있습니다.
- 결과를 해석할 때는 각 홉의 응답 시간을 비교하여 병목 현상을 찾아보세요.