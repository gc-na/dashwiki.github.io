# [한국어] Debian Almquist Shell (dash) file 사용법: 파일 유형 확인

## Overview
`file` 명령어는 주어진 파일의 유형을 식별하는 데 사용됩니다. 이 명령어는 파일의 내용을 분석하여 텍스트 파일, 바이너리 파일, 이미지 파일 등 다양한 유형으로 분류합니다.

## Usage
기본 구문은 다음과 같습니다:
```sh
file [옵션] [파일 경로]
```

## Common Options
- `-b`: 파일 유형을 간단하게 출력합니다. (파일 이름 제외)
- `-i`: MIME 타입을 출력합니다.
- `-f FILE`: FILE에 나열된 파일의 유형을 확인합니다.

## Common Examples
- 특정 파일의 유형 확인:
```sh
file example.txt
```

- 여러 파일의 유형 확인:
```sh
file example1.txt example2.jpg example3
```

- MIME 타입 확인:
```sh
file -i example.pdf
```

- 파일 목록에서 유형 확인:
```sh
file -f file_list.txt
```

## Tips
- `file` 명령어는 파일의 확장자에 의존하지 않으므로, 실제 파일 내용을 기반으로 정확한 유형을 제공합니다.
- 스크립트에서 파일 유형을 확인할 때 유용하게 사용할 수 있습니다.