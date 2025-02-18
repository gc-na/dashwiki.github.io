# [한국어] Debian Almquist Shell (dash) diff 사용법: 파일 간의 차이점 비교

## Overview
`diff` 명령은 두 파일 간의 차이점을 비교하여 어떤 부분이 다른지를 보여주는 유용한 도구입니다. 이 명령은 주로 소스 코드의 변경 사항을 추적하거나 텍스트 파일의 수정 내용을 확인하는 데 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
diff [옵션] [파일1] [파일2]
```

## Common Options
- `-u`: 통합 형식으로 출력하여 변경된 내용을 더 쉽게 읽을 수 있도록 합니다.
- `-i`: 대소문자를 무시하고 비교합니다.
- `-w`: 공백 문자를 무시하고 비교합니다.
- `-q`: 파일이 다를 경우에만 다르다는 메시지를 출력합니다.

## Common Examples
- 두 파일 간의 기본 비교:
    ```bash
    diff file1.txt file2.txt
    ```

- 대소문자를 무시하고 비교:
    ```bash
    diff -i file1.txt file2.txt
    ```

- 공백을 무시하고 비교:
    ```bash
    diff -w file1.txt file2.txt
    ```

- 통합 형식으로 변경 사항 보기:
    ```bash
    diff -u file1.txt file2.txt
    ```

- 파일이 다를 경우에만 메시지 출력:
    ```bash
    diff -q file1.txt file2.txt
    ```

## Tips
- 변경 사항을 쉽게 이해하기 위해 `-u` 옵션을 사용하는 것이 좋습니다.
- 비교할 파일이 많을 경우, 스크립트를 작성하여 자동으로 `diff`를 실행하도록 설정할 수 있습니다.
- `diff` 명령의 결과를 파일로 저장하려면 리다이렉션을 사용할 수 있습니다:
    ```bash
    diff file1.txt file2.txt > differences.txt
    ```