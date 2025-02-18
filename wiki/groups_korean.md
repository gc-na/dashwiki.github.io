# [한국어] Debian Almquist Shell (dash) groups 사용법: 사용자 그룹 정보 확인

## Overview
`groups` 명령어는 현재 사용자 또는 지정된 사용자가 속한 그룹 정보를 출력합니다. 이 명령어는 시스템의 사용자 관리 및 권한 설정에 유용하게 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```
groups [options] [arguments]
```

## Common Options
- `-a`: 모든 그룹을 나열합니다.
- `--help`: 도움말을 출력합니다.
- `--version`: 버전 정보를 출력합니다.

## Common Examples
1. 현재 사용자가 속한 그룹 확인:
   ```bash
   groups
   ```

2. 특정 사용자가 속한 그룹 확인:
   ```bash
   groups username
   ```

3. 모든 그룹 나열:
   ```bash
   groups -a
   ```

## Tips
- `groups` 명령어는 사용자 권한을 확인할 때 유용합니다. 시스템 관리 시 자주 사용하세요.
- 특정 사용자의 그룹 정보를 확인할 때는 사용자 이름을 정확히 입력해야 합니다.
- 여러 사용자의 그룹 정보를 한 번에 확인하려면 각 사용자 이름을 공백으로 구분하여 입력할 수 있습니다.