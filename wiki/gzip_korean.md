# [리눅스] Debian Almquist Shell (dash) gzip 사용법: 파일 압축 및 해제

## Overview
gzip는 파일을 압축하여 저장 공간을 절약하는 데 사용되는 명령어입니다. 이 명령어는 주로 텍스트 파일을 압축하는 데 유용하며, 압축된 파일의 확장자는 `.gz`입니다.

## Usage
기본 구문은 다음과 같습니다:
```
gzip [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: 압축 해제 모드로 실행합니다.
- `-k`, `--keep`: 원본 파일을 유지하면서 압축합니다.
- `-v`, `--verbose`: 압축 과정에서 자세한 정보를 출력합니다.
- `-r`, `--recursive`: 디렉토리 내의 모든 파일을 재귀적으로 압축합니다.

## Common Examples
- **파일 압축하기**:
  ```bash
  gzip example.txt
  ```
  이 명령어는 `example.txt` 파일을 압축하여 `example.txt.gz`로 저장합니다.

- **압축 해제하기**:
  ```bash
  gzip -d example.txt.gz
  ```
  이 명령어는 `example.txt.gz` 파일의 압축을 해제하여 원본 파일인 `example.txt`를 복원합니다.

- **원본 파일 유지하며 압축하기**:
  ```bash
  gzip -k example.txt
  ```
  이 명령어는 `example.txt` 파일을 압축하되, 원본 파일은 그대로 유지합니다.

- **디렉토리 내 모든 파일 압축하기**:
  ```bash
  gzip -r my_directory/
  ```
  이 명령어는 `my_directory` 내의 모든 파일을 재귀적으로 압축합니다.

## Tips
- gzip으로 압축된 파일은 `gunzip` 명령어를 사용하여 쉽게 해제할 수 있습니다.
- 대용량 파일을 압축할 때는 `-v` 옵션을 사용하여 진행 상황을 확인하는 것이 유용합니다.
- 압축된 파일을 전송할 때는 압축을 통해 전송 시간을 단축할 수 있습니다.