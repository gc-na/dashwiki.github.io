# [한국어] Debian Almquist Shell (dash) comm 명령어: 두 개의 정렬된 파일 비교

## Overview
`comm` 명령어는 두 개의 정렬된 파일을 비교하여 공통된 줄과 각 파일에만 있는 줄을 출력하는 데 사용됩니다. 이 명령어는 텍스트 파일의 차이를 분석할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
comm [옵션] [인수]
```

## Common Options
- `-1`: 첫 번째 파일에만 있는 줄을 출력하지 않습니다.
- `-2`: 두 번째 파일에만 있는 줄을 출력하지 않습니다.
- `-3`: 두 파일 모두에 있는 줄을 출력하지 않습니다.
- `-i`: 대소문자를 무시하고 비교합니다.

## Common Examples
1. 두 개의 파일을 비교하여 모든 줄을 출력합니다:
   ```bash
   comm file1.txt file2.txt
   ```

2. 첫 번째 파일에만 있는 줄을 출력하지 않습니다:
   ```bash
   comm -1 file1.txt file2.txt
   ```

3. 두 번째 파일에만 있는 줄을 출력하지 않습니다:
   ```bash
   comm -2 file1.txt file2.txt
   ```

4. 두 파일 모두에 있는 줄을 출력하지 않습니다:
   ```bash
   comm -3 file1.txt file2.txt
   ```

5. 대소문자를 무시하고 비교합니다:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- `comm` 명령어를 사용하기 전에 비교할 파일이 반드시 정렬되어 있어야 합니다. 정렬되지 않은 파일을 비교하면 예상치 못한 결과가 나올 수 있습니다.
- 파일을 정렬하려면 `sort` 명령어를 사용할 수 있습니다. 예를 들어, `sort file1.txt > sorted_file1.txt`와 같이 사용할 수 있습니다.
- 결과를 파일로 저장하려면 리다이렉션을 사용할 수 있습니다. 예: `comm file1.txt file2.txt > output.txt`