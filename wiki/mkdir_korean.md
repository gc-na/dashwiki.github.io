# [한국어] Debian Almquist Shell (dash) mkdir 사용법: 디렉토리 생성

## Overview
`mkdir` 명령어는 새로운 디렉토리를 생성하는 데 사용됩니다. 이 명령어를 통해 사용자는 파일 시스템 내에서 원하는 위치에 새로운 폴더를 만들 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
mkdir [옵션] [인수]
```

## Common Options
- `-p`: 상위 디렉토리가 없는 경우, 상위 디렉토리도 함께 생성합니다.
- `-v`: 생성된 각 디렉토리에 대한 메시지를 출력합니다.
- `-m`: 생성할 디렉토리의 권한을 설정합니다.

## Common Examples
- 기본 디렉토리 생성:
```bash
mkdir my_directory
```

- 여러 개의 디렉토리 동시에 생성:
```bash
mkdir dir1 dir2 dir3
```

- 상위 디렉토리와 함께 생성:
```bash
mkdir -p parent_directory/child_directory
```

- 생성된 디렉토리 출력:
```bash
mkdir -v new_directory
```

## Tips
- 디렉토리를 생성할 때, 항상 경로를 확인하여 원하는 위치에 생성되도록 하세요.
- `-p` 옵션을 사용하면 중첩된 디렉토리를 쉽게 생성할 수 있어 유용합니다.
- 권한 설정이 필요한 경우, `-m` 옵션을 활용하여 적절한 권한을 부여하세요.