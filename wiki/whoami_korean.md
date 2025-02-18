# [한국어] Debian Almquist Shell (dash) whoami 사용법: 현재 사용자 확인

## Overview
`whoami` 명령어는 현재 로그인한 사용자의 이름을 출력합니다. 이는 시스템에서 현재 어떤 사용자로 작업하고 있는지를 확인하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
whoami [옵션] [인수]
```

## Common Options
- `--help`: 사용법을 보여줍니다.
- `--version`: 버전 정보를 출력합니다.

## Common Examples
1. 현재 사용자 이름 확인:
   ```sh
   whoami
   ```

2. 도움말 보기:
   ```sh
   whoami --help
   ```

3. 버전 정보 확인:
   ```sh
   whoami --version
   ```

## Tips
- `whoami` 명령어는 스크립트에서 현재 사용자 정보를 확인할 때 유용합니다.
- 다른 사용자로 전환한 후 `whoami`를 사용하여 올바른 사용자로 전환되었는지 확인할 수 있습니다.