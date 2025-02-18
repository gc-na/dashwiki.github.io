# [리눅스] Debian Almquist Shell (dash) xz 사용법: 파일 압축 및 해제

## Overview
`xz` 명령어는 파일을 압축하고 해제하는 데 사용되는 도구입니다. 주로 높은 압축률을 제공하며, `.xz` 확장자를 가진 파일을 생성합니다.

## Usage
기본 구문은 다음과 같습니다:
```
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: 압축 해제 모드로 실행합니다.
- `-k`, `--keep`: 원본 파일을 삭제하지 않고 유지합니다.
- `-f`, `--force`: 압축 해제 시, 기존 파일을 덮어씁니다.
- `-z`, `--compress`: 기본적으로 압축 모드로 실행합니다. (명시할 필요 없음)

## Common Examples
- 파일 압축하기:
```bash
xz example.txt
```

- 압축 해제하기:
```bash
xz -d example.txt.xz
```

- 원본 파일을 유지하면서 압축하기:
```bash
xz -k example.txt
```

- 압축 해제 시 기존 파일 덮어쓰기:
```bash
xz -df example.txt.xz
```

## Tips
- `xz`는 높은 압축률을 제공하지만, 압축 속도는 느릴 수 있습니다. 필요한 경우 다른 압축 도구를 고려하세요.
- 대용량 파일을 다룰 때는 `-T` 옵션을 사용하여 멀티스레딩을 활성화하면 성능을 향상시킬 수 있습니다.
- 압축된 파일을 확인하고 싶다면 `xz -l example.txt.xz` 명령어를 사용하여 압축된 파일의 정보를 확인할 수 있습니다.