# [한국어] Debian Almquist Shell (dash) hostname 사용법: 호스트 이름 표시 및 설정

## Overview
`hostname` 명령어는 시스템의 호스트 이름을 표시하거나 설정하는 데 사용됩니다. 호스트 이름은 네트워크에서 장치를 식별하는 데 중요한 역할을 합니다.

## Usage
기본 구문은 다음과 같습니다:
```
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: 전체 자격이 있는 도메인 이름(FQDN)을 표시합니다.
- `-i`, `--ip-address`: 호스트 이름에 대한 IP 주소를 표시합니다.
- `-s`, `--short`: 짧은 호스트 이름만 표시합니다.
- `-V`, `--version`: 버전 정보를 표시합니다.

## Common Examples
- 현재 호스트 이름 표시:
  ```sh
  hostname
  ```

- 전체 자격이 있는 도메인 이름 표시:
  ```sh
  hostname -f
  ```

- 호스트 이름에 대한 IP 주소 표시:
  ```sh
  hostname -i
  ```

- 짧은 호스트 이름 표시:
  ```sh
  hostname -s
  ```

- 호스트 이름 변경:
  ```sh
  hostname new-hostname
  ```

## Tips
- 호스트 이름을 변경한 후에는 시스템을 재부팅하거나 네트워크 서비스를 재시작해야 변경 사항이 적용될 수 있습니다.
- 호스트 이름은 영문자, 숫자, 하이픈(-)만 포함할 수 있으며, 공백이나 특수 문자는 피해야 합니다.
- `/etc/hostname` 파일을 수정하여 부팅 시 자동으로 호스트 이름을 설정할 수 있습니다.