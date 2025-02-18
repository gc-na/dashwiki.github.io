# [리눅스] Debian Almquist Shell (dash) mtr 사용법: 네트워크 경로 추적

## Overview
mtr (My Traceroute) 명령은 네트워크 경로를 추적하고, 패킷 손실 및 지연 시간을 측정하는 도구입니다. 이 명령은 traceroute와 ping의 기능을 결합하여 실시간으로 네트워크 상태를 모니터링할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: 보고서를 생성하여 결과를 출력합니다.
- `-c <count>`: 지정한 횟수만큼 패킷을 전송합니다.
- `-i <interval>`: 패킷 전송 간격을 설정합니다.
- `-p`: 포트 번호를 지정하여 특정 포트에 대해 테스트합니다.

## Common Examples
1. 기본 mtr 사용:
   ```bash
   mtr google.com
   ```

2. 5회 패킷 전송 후 결과 출력:
   ```bash
   mtr -c 5 google.com
   ```

3. 특정 간격으로 패킷 전송:
   ```bash
   mtr -i 2 google.com
   ```

4. 보고서 형식으로 결과 출력:
   ```bash
   mtr -r google.com
   ```

5. 특정 포트에 대해 mtr 실행:
   ```bash
   mtr -p 80 google.com
   ```

## Tips
- mtr 명령을 실행할 때, 관리자 권한이 필요할 수 있으므로 `sudo`를 사용하는 것이 좋습니다.
- 결과를 분석할 때, 패킷 손실이 발생하는 지점을 주의 깊게 살펴보세요.
- mtr의 결과는 실시간으로 업데이트되므로, 네트워크 상태를 지속적으로 모니터링할 수 있습니다.