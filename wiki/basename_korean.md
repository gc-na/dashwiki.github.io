# [한국어] Debian Almquist Shell (dash) basename 사용법: 파일 경로에서 파일 이름 추출

## Overview
`basename` 명령어는 주어진 경로에서 파일 이름을 추출하는 데 사용됩니다. 이 명령어는 파일 경로에서 디렉토리 부분을 제거하고, 순수한 파일 이름만 반환합니다.

## Usage
기본 구문은 다음과 같습니다:
```
basename [options] [arguments]
```

## Common Options
- `-a`: 여러 인수를 받아 각 인수에 대해 basename을 반환합니다.
- `-s`: 지정된 접미사를 제거하고 파일 이름을 반환합니다.

## Common Examples
1. 기본 사용법:
   ```sh
   basename /usr/local/bin/script.sh
   ```
   출력:
   ```
   script.sh
   ```

2. 여러 파일 이름 추출:
   ```sh
   basename -a /usr/local/bin/script.sh /home/user/document.txt
   ```
   출력:
   ```
   script.sh
   document.txt
   ```

3. 접미사 제거:
   ```sh
   basename -s .sh /usr/local/bin/script.sh
   ```
   출력:
   ```
   script
   ```

## Tips
- `basename` 명령어는 스크립트에서 파일 이름을 처리할 때 유용합니다.
- 여러 파일을 한 번에 처리할 수 있는 `-a` 옵션을 활용하면 효율적입니다.
- 접미사를 제거할 때는 정확한 접미사를 지정하여 원하는 결과를 얻도록 하세요.