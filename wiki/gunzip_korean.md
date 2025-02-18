# [한국어] Debian Almquist Shell (dash) gunzip 사용법: 압축 해제

## Overview
`gunzip` 명령어는 Gzip 형식으로 압축된 파일을 해제하는 데 사용됩니다. 이 명령어는 파일의 크기를 줄이기 위해 Gzip 알고리즘으로 압축된 파일을 원래의 상태로 복원합니다.

## Usage
기본 구문은 다음과 같습니다:
```
gunzip [옵션] [인수]
```

## Common Options
- `-c`: 압축 해제된 내용을 표준 출력으로 보냅니다.
- `-f`: 강제로 압축 해제를 수행합니다. 이미 존재하는 파일을 덮어쓸 수 있습니다.
- `-k`: 원본 압축 파일을 삭제하지 않고 유지합니다.
- `-r`: 디렉토리 내의 모든 파일을 재귀적으로 압축 해제합니다.

## Common Examples
- 단일 파일 압축 해제:
    ```bash
    gunzip example.txt.gz
    ```

- 압축 해제된 내용을 표준 출력으로 보기:
    ```bash
    gunzip -c example.txt.gz
    ```

- 원본 파일 유지하면서 압축 해제:
    ```bash
    gunzip -k example.txt.gz
    ```

- 디렉토리 내의 모든 Gzip 파일 압축 해제:
    ```bash
    gunzip -r /path/to/directory
    ```

## Tips
- `-f` 옵션을 사용할 때는 주의하세요. 기존 파일이 덮어씌워질 수 있습니다.
- 대량의 파일을 압축 해제할 때는 `-k` 옵션을 사용하여 원본 파일을 유지하는 것이 좋습니다.
- `gunzip` 명령어를 사용할 때, 압축 해제할 파일의 경로를 정확히 지정해야 합니다.