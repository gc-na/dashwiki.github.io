# [한국어] Debian Almquist Shell (dash) traceroute 사용법: 네트워크 경로 추적

## 개요
traceroute 명령은 네트워크에서 데이터 패킷이 목적지에 도달하기까지 거치는 경로를 추적하는 데 사용됩니다. 이 명령은 각 홉(hop)에서의 응답 시간을 측정하여 네트워크 성능을 분석하는 데 유용합니다.

## 사용법
기본 구문은 다음과 같습니다:

```
traceroute [옵션] [인수]
```

## 일반 옵션
- `-m <최대 홉 수>`: 패킷이 도달할 수 있는 최대 홉 수를 설정합니다.
- `-w <타임아웃>`: 각 홉에 대한 응답 대기 시간을 설정합니다.
- `-q <쿼리 수>`: 각 홉에 대해 전송할 패킷 수를 설정합니다.

## 일반 예제
다음은 traceroute 명령의 몇 가지 실용적인 예입니다.

1. 기본 traceroute 사용:
   ```bash
   traceroute example.com
   ```

2. 최대 홉 수를 15로 설정:
   ```bash
   traceroute -m 15 example.com
   ```

3. 각 홉에 대한 응답 대기 시간을 2초로 설정:
   ```bash
   traceroute -w 2 example.com
   ```

4. 각 홉에 대해 3개의 패킷을 전송:
   ```bash
   traceroute -q 3 example.com
   ```

## 팁
- traceroute를 사용할 때, 방화벽 설정으로 인해 일부 홉에서 응답이 없을 수 있으므로 이를 감안해야 합니다.
- 네트워크 문제를 진단할 때, traceroute의 결과를 분석하여 특정 홉에서의 지연이나 패킷 손실을 확인할 수 있습니다.
- traceroute는 IPv4와 IPv6 모두 지원하므로, 필요에 따라 적절한 프로토콜을 선택하여 사용하세요.