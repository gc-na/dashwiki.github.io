# [리눅스] Debian Almquist Shell (dash) getopts 사용법: 명령행 옵션 파싱

## Overview
`getopts` 명령은 스크립트에서 명령행 옵션을 파싱하는 데 사용됩니다. 이 명령은 옵션과 인수를 처리하여 스크립트의 동작을 제어할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:

```sh
getopts optstring variable
```

- `optstring`: 허용되는 옵션을 정의하는 문자열입니다.
- `variable`: 옵션의 값을 저장할 변수입니다.

## Common Options
- `-a`: 추가적인 옵션을 정의할 수 있습니다.
- `-b`: 옵션을 비활성화합니다.
- `-c`: 특정 조건에 따라 옵션을 처리합니다.

## Common Examples

### 예제 1: 기본 옵션 파싱
```sh
#!/bin/dash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "옵션 A가 선택되었습니다."
      ;;
    b)
      echo "옵션 B가 선택되었습니다. 인수: $OPTARG"
      ;;
    c)
      echo "옵션 C가 선택되었습니다. 인수: $OPTARG"
      ;;
    *)
      echo "잘못된 옵션입니다."
      ;;
  esac
done
```

### 예제 2: 여러 옵션 처리
```sh
#!/bin/dash

while getopts "abc:" opt; do
  case $opt in
    a)
      echo "A 옵션"
      ;;
    b)
      echo "B 옵션"
      ;;
    c)
      echo "C 옵션, 인수: $OPTARG"
      ;;
  esac
done
```

### 예제 3: 기본값 설정
```sh
#!/bin/dash

option_a=false
option_b=false

while getopts "ab" opt; do
  case $opt in
    a)
      option_a=true
      ;;
    b)
      option_b=true
      ;;
  esac
done

if [ "$option_a" = true ]; then
  echo "A 옵션이 활성화되었습니다."
fi

if [ "$option_b" = true ]; then
  echo "B 옵션이 활성화되었습니다."
fi
```

## Tips
- `getopts`는 옵션을 처리할 때 자동으로 위치 인수를 관리하므로, 스크립트의 나머지 부분에서 인수에 쉽게 접근할 수 있습니다.
- 옵션 문자열에서 `:`를 사용하여 인수가 필요한 옵션을 정의할 수 있습니다.
- `OPTARG` 변수를 사용하여 현재 옵션의 인수 값을 참조할 수 있습니다.