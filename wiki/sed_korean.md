# [한국어] Debian Almquist Shell (dash) sed 사용법: 텍스트 변환 및 편집

## Overview
`sed`는 스트림 편집기(stream editor)로, 입력된 텍스트 데이터를 읽고, 지정된 명령에 따라 변환하거나 편집하는 데 사용됩니다. 주로 파일의 내용을 수정하거나 특정 패턴을 찾아 대체하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
sed [options] [arguments]
```

## Common Options
- `-e`: 여러 개의 편집 명령을 지정할 때 사용합니다.
- `-i`: 파일을 직접 수정합니다. 백업 파일을 생성할 수도 있습니다.
- `-n`: 기본 출력 모드를 비활성화하여 명시적으로 출력할 내용을 지정할 수 있습니다.
- `s/pattern/replacement/`: 패턴을 찾아 대체하는 명령입니다.

## Common Examples
1. **파일에서 특정 문자열 대체하기**
   ```bash
   sed 's/old-text/new-text/' filename.txt
   ```

2. **파일을 직접 수정하기 (백업 생성)**
   ```bash
   sed -i.bak 's/old-text/new-text/' filename.txt
   ```

3. **여러 개의 대체 명령 사용하기**
   ```bash
   sed -e 's/first/second/' -e 's/third/fourth/' filename.txt
   ```

4. **특정 패턴이 포함된 줄만 출력하기**
   ```bash
   sed -n '/pattern/p' filename.txt
   ```

5. **행 번호와 함께 출력하기**
   ```bash
   sed = filename.txt | sed 'N;s/\n/ /'
   ```

## Tips
- `-i` 옵션을 사용할 때는 항상 백업 파일을 생성하는 것이 좋습니다. 실수로 데이터를 잃는 것을 방지할 수 있습니다.
- 복잡한 패턴을 사용할 때는 정규 표현식을 활용하여 더욱 강력한 검색 및 대체가 가능합니다.
- `sed`는 파이프와 함께 사용하여 다른 명령의 출력을 처리할 수 있습니다. 이를 통해 여러 명령을 조합하여 강력한 데이터 처리 작업을 수행할 수 있습니다.