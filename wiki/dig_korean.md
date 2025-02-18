# [리눅스] Debian Almquist Shell (dash) dig 사용법: DNS 쿼리 수행

## Overview
`dig` 명령어는 DNS(Domain Name System) 쿼리를 수행하는 도구로, 도메인 이름을 IP 주소로 변환하거나 그 반대의 작업을 수행하는 데 사용됩니다. 네트워크 문제를 진단하거나 DNS 정보를 확인하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
dig [options] [arguments]
```

## Common Options
- `@server`: 특정 DNS 서버에 쿼리를 보냅니다.
- `-t type`: 쿼리할 레코드의 유형을 지정합니다 (예: A, AAAA, MX 등).
- `+short`: 간단한 출력 형식으로 결과를 표시합니다.
- `-x`: IP 주소에 대한 역방향 DNS 쿼리를 수행합니다.

## Common Examples
- 기본 A 레코드 쿼리:
  ```bash
  dig example.com
  ```

- 특정 DNS 서버에 쿼리 보내기:
  ```bash
  dig @8.8.8.8 example.com
  ```

- MX 레코드 쿼리:
  ```bash
  dig -t MX example.com
  ```

- 간단한 출력 형식으로 A 레코드 쿼리:
  ```bash
  dig +short example.com
  ```

- IP 주소에 대한 역방향 DNS 쿼리:
  ```bash
  dig -x 93.184.216.34
  ```

## Tips
- DNS 문제를 해결할 때 `+trace` 옵션을 사용하면 DNS 쿼리의 전체 경로를 추적할 수 있습니다.
- `dig` 명령어의 결과를 파일로 저장하려면 리다이렉션을 사용할 수 있습니다:
  ```bash
  dig example.com > output.txt
  ```
- 주기적으로 DNS 레코드를 확인해야 하는 경우, 스크립트를 작성하여 자동화할 수 있습니다.