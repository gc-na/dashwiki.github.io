# [리눅스] Debian Almquist Shell (dash) rmdir 사용법: 빈 디렉토리 삭제

## Overview
`rmdir` 명령은 빈 디렉토리를 삭제하는 데 사용됩니다. 이 명령은 디렉토리가 비어 있을 때만 작동하며, 디렉토리에 파일이나 다른 디렉토리가 존재하는 경우에는 삭제할 수 없습니다.

## Usage
기본 구문은 다음과 같습니다:
```
rmdir [옵션] [인수]
```

## Common Options
- `--ignore-fail-on-non-empty`: 비어 있지 않은 디렉토리에 대해 오류를 무시합니다.
- `--verbose`: 삭제된 디렉토리에 대한 자세한 정보를 출력합니다.

## Common Examples
다음은 `rmdir` 명령의 몇 가지 일반적인 예입니다.

### 예제 1: 빈 디렉토리 삭제
```bash
rmdir my_empty_directory
```

### 예제 2: 여러 빈 디렉토리 삭제
```bash
rmdir dir1 dir2 dir3
```

### 예제 3: 오류 무시하고 비어 있지 않은 디렉토리 삭제
```bash
rmdir --ignore-fail-on-non-empty my_non_empty_directory
```

### 예제 4: 삭제된 디렉토리 정보 출력
```bash
rmdir --verbose my_empty_directory
```

## Tips
- `rmdir` 명령은 빈 디렉토리만 삭제할 수 있으므로, 삭제하기 전에 디렉토리 안에 파일이 없는지 확인하세요.
- 여러 디렉토리를 한 번에 삭제할 수 있지만, 모든 디렉토리가 비어 있어야 합니다.
- 비어 있지 않은 디렉토리를 삭제하려면 `rm -r` 명령을 사용해야 합니다.