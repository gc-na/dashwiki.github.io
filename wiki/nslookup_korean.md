# [리눅스] Debian Almquist Shell (dash) nslookup 사용법: 도메인 이름의 IP 주소 조회

## Overview
`nslookup` 명령어는 도메인 이름 시스템(DNS)에서 도메인 이름에 대한 IP 주소를 조회하는 데 사용됩니다. 이 명령어는 네트워크 문제를 진단하거나 도메인 이름과 관련된 정보를 확인하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE`: 조회할 레코드의 유형을 지정합니다. 예: `A`, `MX`, `CNAME` 등.
- `-timeout=SECONDS`: 응답을 기다리는 최대 시간을 설정합니다.
- `-retry=COUNT`: 요청 실패 시 재시도 횟수를 설정합니다.

## Common Examples
- 기본 도메인 이름 조회:
```bash
nslookup example.com
```

- 특정 DNS 서버를 사용하여 조회:
```bash
nslookup example.com 8.8.8.8
```

- MX 레코드 조회:
```bash
nslookup -type=MX example.com
```

- CNAME 레코드 조회:
```bash
nslookup -type=CNAME www.example.com
```

## Tips
- DNS 문제를 해결할 때, 여러 DNS 서버를 사용하여 결과를 비교해 보세요.
- `nslookup` 명령어는 대소문자를 구분하지 않지만, 도메인 이름은 소문자로 입력하는 것이 일반적입니다.
- 결과를 분석할 때, 응답 시간과 오류 메시지를 주의 깊게 살펴보세요.