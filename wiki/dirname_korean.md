# [리눅스] Debian Almquist Shell (dash) dirname 사용법: 경로에서 디렉토리 이름 추출

## Overview
`dirname` 명령은 주어진 파일 경로에서 디렉토리 이름을 추출하는 데 사용됩니다. 이 명령은 파일의 전체 경로에서 마지막 슬래시(`/`) 이전의 부분을 반환합니다.

## Usage
기본 구문은 다음과 같습니다:
```
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: 입력 경로를 널 문자로 구분합니다.
- `--help`: 사용법 정보를 표시합니다.
- `--version`: 버전 정보를 표시합니다.

## Common Examples
다음은 `dirname` 명령의 몇 가지 실용적인 예입니다.

1. 기본 사용법:
   ```sh
   dirname /home/user/document.txt
   ```
   출력: `/home/user`

2. 여러 경로 처리:
   ```sh
   dirname /var/log/syslog /usr/local/bin/script.sh
   ```
   출력:
   ```
   /var/log
   /usr/local/bin
   ```

3. 널 문자로 구분된 입력 사용:
   ```sh
   printf "/path/to/file1\n/path/to/file2" | xargs -0 dirname
   ```
   출력:
   ```
   /path/to
   /path/to
   ```

## Tips
- `dirname` 명령은 스크립트에서 파일 경로를 처리할 때 유용하게 사용됩니다.
- 경로가 슬래시로 끝나는 경우, `dirname`은 빈 문자열을 반환합니다.
- 여러 경로를 한 번에 처리할 수 있으므로, 반복적인 작업을 줄이는 데 도움이 됩니다.