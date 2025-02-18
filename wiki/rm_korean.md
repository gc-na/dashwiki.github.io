# [한국어] Debian Almquist Shell (dash) rm 사용법: 파일 삭제

## Overview
`rm` 명령어는 파일이나 디렉토리를 삭제하는 데 사용됩니다. 이 명령어는 주의해서 사용해야 하며, 삭제된 파일은 복구할 수 없습니다.

## Usage
기본 구문은 다음과 같습니다:
```
rm [옵션] [인수]
```

## Common Options
- `-f`: 강제로 삭제합니다. 파일이 존재하지 않더라도 오류 메시지를 표시하지 않습니다.
- `-i`: 삭제하기 전에 사용자에게 확인을 요청합니다.
- `-r`: 디렉토리와 그 안의 모든 내용을 재귀적으로 삭제합니다.
- `-v`: 삭제되는 파일의 이름을 출력합니다.

## Common Examples
- 단일 파일 삭제:
  ```bash
  rm example.txt
  ```

- 여러 파일 삭제:
  ```bash
  rm file1.txt file2.txt file3.txt
  ```

- 디렉토리와 그 안의 모든 파일 삭제:
  ```bash
  rm -r my_directory
  ```

- 강제로 파일 삭제:
  ```bash
  rm -f unwanted_file.txt
  ```

- 삭제 전에 확인 요청:
  ```bash
  rm -i important_file.txt
  ```

## Tips
- 항상 `-i` 옵션을 사용하여 실수로 중요한 파일을 삭제하지 않도록 하세요.
- 삭제할 파일이나 디렉토리를 확인한 후에 명령어를 실행하세요.
- 중요한 파일은 삭제하기 전에 백업하는 것이 좋습니다.