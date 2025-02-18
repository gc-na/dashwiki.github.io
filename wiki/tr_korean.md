# [리눅스] Debian Almquist Shell (dash) tr 사용법: 문자 변환 및 삭제

## Overview
`tr` 명령어는 입력된 텍스트에서 특정 문자나 문자열을 변환하거나 삭제하는 데 사용됩니다. 주로 파이프라인에서 다른 명령어와 함께 사용되어 텍스트 처리 작업을 수행합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
tr [options] [arguments]
```

## Common Options
- `-d`: 지정한 문자를 삭제합니다.
- `-s`: 연속된 중복 문자를 하나로 압축합니다.
- `-c`: 지정한 문자 집합의 보충 집합을 사용합니다.

## Common Examples
1. **문자 변환**: 소문자를 대문자로 변환
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```

2. **문자 삭제**: 숫자 삭제
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```

3. **중복 문자 압축**: 연속된 공백을 하나로 압축
   ```bash
   echo "This    is a    test." | tr -s ' '
   ```

4. **특정 문자 변환**: 공백을 콤마로 변환
   ```bash
   echo "apple orange banana" | tr ' ' ','
   ```

## Tips
- `tr` 명령어는 파이프라인에서 다른 명령어와 함께 사용할 때 가장 유용합니다.
- 대문자와 소문자 변환을 자주 사용할 경우, `tr`을 스크립트에 포함시켜 자동화할 수 있습니다.
- 복잡한 텍스트 변환이 필요할 경우, `sed`와 같은 다른 도구와 함께 사용하는 것도 고려해 보세요.