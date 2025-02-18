# [리눅스] Debian Almquist Shell (dash) tee 사용법: 표준 입력을 파일에 기록하고 출력

## Overview
`tee` 명령은 표준 입력을 받아서 파일에 기록하고 동시에 표준 출력을 통해 출력하는 기능을 제공합니다. 이를 통해 데이터 흐름을 분기할 수 있어, 여러 파일에 동시에 내용을 기록할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
tee [옵션] [인수]
```

## Common Options
- `-a`, `--append`: 파일에 내용을 추가합니다. 기본적으로는 파일을 덮어씁니다.
- `-i`, `--ignore-interrupts`: 인터럽트를 무시합니다.
- `-p`, `--output-error`: 출력 오류를 처리하는 방법을 지정합니다.

## Common Examples
- **기본 사용법**: 표준 입력을 파일에 기록하고 출력합니다.
  ```bash
  echo "Hello, World!" | tee output.txt
  ```

- **파일에 추가하기**: 기존 파일에 내용을 추가합니다.
  ```bash
  echo "Another line" | tee -a output.txt
  ```

- **여러 파일에 기록하기**: 여러 파일에 동시에 내용을 기록합니다.
  ```bash
  echo "Logging to multiple files" | tee file1.txt file2.txt
  ```

- **출력 오류 처리**: 오류를 처리하며 출력합니다.
  ```bash
  command | tee -p output.txt
  ```

## Tips
- `tee` 명령은 파이프라인에서 유용하게 사용될 수 있습니다. 여러 명령의 출력을 동시에 기록하고 싶을 때 활용하세요.
- `-a` 옵션을 사용하여 로그 파일에 데이터를 추가할 수 있어, 이전 데이터를 보존할 수 있습니다.
- 스크립트에서 `tee`를 사용하여 디버깅 정보를 기록하면, 문제를 추적하는 데 도움이 됩니다.