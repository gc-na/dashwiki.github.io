# [한국어] Debian Almquist Shell (dash) sort 사용법: 파일 정렬

## Overview
`sort` 명령어는 텍스트 파일의 내용을 정렬하는 데 사용됩니다. 이 명령어는 기본적으로 각 줄을 알파벳 순서 또는 숫자 순서로 정렬하여 출력합니다.

## Usage
기본 구문은 다음과 같습니다:
```
sort [options] [arguments]
```

## Common Options
- `-r`: 역순으로 정렬합니다.
- `-n`: 숫자 값에 따라 정렬합니다.
- `-k`: 특정 키(열)를 기준으로 정렬합니다.
- `-u`: 중복된 줄을 제거하고 유일한 줄만 출력합니다.

## Common Examples
- 기본 정렬:
  ```sh
  sort file.txt
  ```
- 역순 정렬:
  ```sh
  sort -r file.txt
  ```
- 숫자 정렬:
  ```sh
  sort -n numbers.txt
  ```
- 특정 열을 기준으로 정렬 (예: 두 번째 열):
  ```sh
  sort -k 2 file.txt
  ```
- 중복 제거 후 정렬:
  ```sh
  sort -u file.txt
  ```

## Tips
- 정렬할 파일이 크면, 결과를 다른 파일로 리디렉션하여 저장하는 것이 좋습니다. 예를 들어:
  ```sh
  sort file.txt > sorted_file.txt
  ```
- 여러 옵션을 조합하여 사용할 수 있습니다. 예를 들어, 숫자 정렬 후 역순으로 정렬하려면:
  ```sh
  sort -n -r numbers.txt
  ```
- 정렬할 때 대소문자를 무시하려면 `-f` 옵션을 사용할 수 있습니다.