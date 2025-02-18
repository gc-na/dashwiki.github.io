# [리눅스] Debian Almquist Shell (dash) export 사용법: 환경 변수를 설정하고 내보내기

## Overview
`export` 명령은 셸에서 환경 변수를 설정하고 이를 하위 프로세스에 전달하는 데 사용됩니다. 이 명령을 통해 특정 변수의 값을 설정하면, 그 변수는 현재 셸 세션과 그 하위 프로세스에서 모두 사용할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
export [options] [arguments]
```

## Common Options
- `-p`: 현재 환경 변수 목록을 출력합니다.
- `-n`: 지정된 변수의 내보내기를 취소합니다.

## Common Examples
다음은 `export` 명령의 몇 가지 일반적인 사용 예입니다.

1. **환경 변수 설정하기**
   ```bash
   export MY_VAR="Hello, World!"
   ```

2. **환경 변수 확인하기**
   ```bash
   echo $MY_VAR
   ```

3. **여러 변수 설정하기**
   ```bash
   export VAR1="Value1" VAR2="Value2"
   ```

4. **변수 내보내기 취소하기**
   ```bash
   export -n MY_VAR
   ```

5. **현재 환경 변수 목록 보기**
   ```bash
   export -p
   ```

## Tips
- 환경 변수를 설정할 때, 변수 이름은 대문자로 작성하는 것이 일반적입니다.
- 설정한 환경 변수는 현재 셸 세션이 종료되면 사라지므로, 지속적으로 사용하려면 셸 초기화 파일에 추가해야 합니다.
- `export` 명령은 스크립트 내에서 하위 프로세스에 변수를 전달할 때 유용합니다.