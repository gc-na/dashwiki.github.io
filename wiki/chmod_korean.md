# [리눅스] Debian Almquist Shell (dash) chmod 사용법: 파일 권한 변경

## Overview
`chmod` 명령어는 파일이나 디렉토리의 접근 권한을 변경하는 데 사용됩니다. 이 명령어를 통해 사용자는 파일에 대한 읽기, 쓰기 및 실행 권한을 설정할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
chmod [옵션] [인수]
```

## Common Options
- `-R`: 하위 디렉토리와 파일에 대해 재귀적으로 권한을 변경합니다.
- `-v`: 변경된 권한에 대한 정보를 출력합니다.
- `-c`: 변경된 권한에 대한 정보를 출력하지만, 변경이 없었던 경우는 출력하지 않습니다.

## Common Examples
- 파일에 읽기 및 쓰기 권한 부여:
  ```bash
  chmod u+rw filename.txt
  ```

- 모든 사용자에게 실행 권한 부여:
  ```bash
  chmod a+x script.sh
  ```

- 디렉토리와 그 하위 파일의 권한을 재귀적으로 변경:
  ```bash
  chmod -R 755 /path/to/directory
  ```

- 특정 사용자에게만 권한 제거:
  ```bash
  chmod g-w filename.txt
  ```

## Tips
- 권한 설정을 변경하기 전에 현재 권한을 확인하려면 `ls -l` 명령어를 사용하세요.
- `chmod` 명령어를 사용할 때는 항상 필요한 최소한의 권한만 부여하는 것이 좋습니다.
- 스크립트 파일에 실행 권한을 부여할 때는 `chmod +x script.sh`와 같이 간단하게 사용할 수 있습니다.