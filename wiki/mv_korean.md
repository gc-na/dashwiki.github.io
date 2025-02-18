# [리눅스] Debian Almquist Shell (dash) mv 사용법: 파일 및 디렉토리 이동 및 이름 변경

## Overview
`mv` 명령어는 파일이나 디렉토리를 이동하거나 이름을 변경하는 데 사용됩니다. 이 명령어는 간단하면서도 매우 유용한 기능을 제공합니다.

## Usage
기본 구문은 다음과 같습니다:
```
mv [options] [arguments]
```

## Common Options
- `-i`: 덮어쓰기 전에 확인을 요청합니다.
- `-u`: 대상 파일이 소스 파일보다 오래된 경우에만 이동합니다.
- `-v`: 이동하는 파일의 이름을 출력합니다.

## Common Examples
1. 파일 이름 변경:
   ```bash
   mv oldname.txt newname.txt
   ```

2. 파일 이동:
   ```bash
   mv file.txt /path/to/destination/
   ```

3. 디렉토리 이동:
   ```bash
   mv /path/to/source_directory/ /path/to/destination_directory/
   ```

4. 덮어쓰기 확인:
   ```bash
   mv -i file.txt /path/to/destination/
   ```

5. 오래된 파일만 이동:
   ```bash
   mv -u file.txt /path/to/destination/
   ```

## Tips
- 파일을 이동하기 전에 항상 현재 작업 디렉토리를 확인하세요.
- 중요한 파일을 덮어쓰지 않도록 `-i` 옵션을 사용하는 것이 좋습니다.
- 여러 파일을 한 번에 이동하려면 파일 이름을 공백으로 구분하여 나열할 수 있습니다.