# [리눅스] Debian Almquist Shell (dash) awk 사용법: 텍스트 처리 및 데이터 분석

## Overview
`awk`는 텍스트 파일이나 데이터 스트림에서 패턴을 검색하고 처리하는 데 사용되는 강력한 프로그래밍 언어입니다. 주로 데이터 분석과 보고서 생성에 유용하며, 필드 기반의 데이터 처리에 적합합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
awk [options] [arguments]
```

## Common Options
- `-F`: 필드 구분자를 지정합니다. 기본값은 공백입니다.
- `-v`: 변수를 설정합니다.
- `-f`: awk 스크립트 파일을 지정합니다.
- `-e`: 명령줄에서 awk 프로그램을 직접 지정합니다.

## Common Examples
1. **파일에서 특정 필드 출력하기**
   ```bash
   awk '{print $1}' filename.txt
   ```
   이 명령은 `filename.txt` 파일의 첫 번째 필드를 출력합니다.

2. **특정 패턴 필터링하기**
   ```bash
   awk '/pattern/ {print}' filename.txt
   ```
   이 명령은 `filename.txt`에서 "pattern"이 포함된 모든 행을 출력합니다.

3. **필드 구분자 지정하기**
   ```bash
   awk -F, '{print $2}' filename.csv
   ```
   이 명령은 쉼표로 구분된 `filename.csv` 파일의 두 번째 필드를 출력합니다.

4. **조건부 출력하기**
   ```bash
   awk '$3 > 50 {print $1, $3}' filename.txt
   ```
   이 명령은 세 번째 필드가 50보다 큰 행의 첫 번째와 세 번째 필드를 출력합니다.

## Tips
- `awk`의 기본 필드는 `$1`, `$2`, ... 형태로 접근할 수 있습니다.
- 여러 조건을 결합할 때는 `&&`와 `||` 연산자를 사용할 수 있습니다.
- 복잡한 스크립트는 파일에 저장하고 `-f` 옵션으로 실행하는 것이 좋습니다.