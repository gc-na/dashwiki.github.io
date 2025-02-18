# [리눅스] Debian Almquist Shell (dash) nohup 사용법: 백그라운드에서 프로세스를 실행하고 세션 종료 시에도 계속 실행

## Overview
`nohup` 명령어는 사용자가 로그아웃하거나 세션을 종료하더라도 프로세스가 계속 실행되도록 하는 데 사용됩니다. 주로 장시간 실행되는 작업을 백그라운드에서 실행할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
nohup [options] [arguments]
```

## Common Options
- `&`: 명령어를 백그라운드에서 실행합니다.
- `-h`: 도움말을 표시합니다.
- `-p`: 프로세스 ID를 표시합니다.

## Common Examples
다음은 `nohup` 명령어의 몇 가지 일반적인 예입니다:

1. **백그라운드에서 스크립트 실행하기**
   ```bash
   nohup ./my_script.sh &
   ```

2. **출력을 파일로 리다이렉트하기**
   ```bash
   nohup ./long_running_task > output.log &
   ```

3. **명령어 실행 후 세션 종료하기**
   ```bash
   nohup python my_script.py &
   ```

4. **여러 명령어를 한 번에 실행하기**
   ```bash
   nohup bash -c 'command1; command2' &
   ```

## Tips
- `nohup`을 사용할 때는 출력 파일을 지정하여 로그를 확인할 수 있도록 하는 것이 좋습니다.
- 명령어 뒤에 `&`를 추가하여 백그라운드에서 실행되도록 하세요.
- 실행 중인 프로세스를 확인하려면 `ps` 명령어를 사용할 수 있습니다.