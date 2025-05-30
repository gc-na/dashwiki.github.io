# [한국어] Debian Almquist Shell (dash) cp 사용법: 파일 복사

## Overview
`cp` 명령어는 파일이나 디렉토리를 복사하는 데 사용됩니다. 이 명령어를 통해 원본 파일을 지정한 위치에 새로운 파일로 복사할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
cp [옵션] [원본] [대상]
```

## Common Options
- `-r`: 디렉토리를 재귀적으로 복사합니다.
- `-i`: 대상 파일이 존재할 경우, 덮어쓸 것인지 확인합니다.
- `-u`: 원본 파일이 대상 파일보다 새롭거나 대상 파일이 존재하지 않을 경우에만 복사합니다.
- `-v`: 복사하는 동안 진행 상황을 출력합니다.

## Common Examples
- 단일 파일 복사:
```bash
cp file1.txt file2.txt
```
- 디렉토리 복사 (재귀적):
```bash
cp -r dir1/ dir2/
```
- 덮어쓰기 확인:
```bash
cp -i file1.txt file2.txt
```
- 최신 파일만 복사:
```bash
cp -u file1.txt file2.txt
```
- 복사 진행 상황 보기:
```bash
cp -v file1.txt file2.txt
```

## Tips
- 복사할 파일이 많은 경우 `-v` 옵션을 사용하여 진행 상황을 확인하는 것이 좋습니다.
- 중요한 파일을 복사할 때는 `-i` 옵션을 사용하여 실수로 덮어쓰는 것을 방지하세요.
- 디렉토리를 복사할 때는 항상 `-r` 옵션을 잊지 마세요.