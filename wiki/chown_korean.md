# [리눅스] Debian Almquist Shell (dash) chown 사용법: 파일 소유자 변경

## Overview
`chown` 명령어는 파일이나 디렉토리의 소유자와 그룹을 변경하는 데 사용됩니다. 이 명령어를 통해 시스템의 파일 권한을 관리할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
chown [options] [owner][:group] [file...]
```

## Common Options
- `-R`: 하위 디렉토리와 파일을 포함하여 재귀적으로 소유자를 변경합니다.
- `-v`: 변경된 내용을 자세히 출력합니다.
- `--reference=FILE`: 지정한 파일과 동일한 소유자 및 그룹으로 변경합니다.

## Common Examples
- 특정 파일의 소유자를 변경하기:
```bash
chown username file.txt
```

- 특정 파일의 소유자와 그룹을 동시에 변경하기:
```bash
chown username:groupname file.txt
```

- 디렉토리와 그 하위 파일들의 소유자를 재귀적으로 변경하기:
```bash
chown -R username directory/
```

- 파일의 소유자를 다른 파일과 동일하게 변경하기:
```bash
chown --reference=reference.txt file.txt
```

## Tips
- 소유자를 변경하기 전에 현재 파일의 소유자와 권한을 확인하는 것이 좋습니다.
- `sudo`를 사용하여 관리자 권한으로 명령어를 실행해야 할 수 있습니다.
- 변경 사항을 확인하기 위해 `ls -l` 명령어를 사용하여 파일의 소유자와 그룹을 확인하세요.