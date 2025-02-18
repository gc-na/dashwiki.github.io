# [한국어] Debian Almquist Shell (dash) batch 사용법: 작업을 예약하여 실행하기

## Overview
`batch` 명령은 시스템이 여유가 있을 때 지정된 작업을 예약하여 실행하는 데 사용됩니다. 이 명령은 주로 시스템 부하가 적은 시간에 스크립트나 명령을 실행하고자 할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
batch [options] [arguments]
```

## Common Options
- `-f`: 파일에서 명령을 읽어옵니다.
- `-l`: 명령을 실행하기 전에 대기할 시간을 설정합니다.

## Common Examples
다음은 `batch` 명령의 몇 가지 실용적인 예입니다.

1. 기본 사용법:
   ```sh
   echo "echo 'Hello, World!'" | batch
   ```

2. 특정 스크립트 파일 실행하기:
   ```sh
   batch < myscript.sh
   ```

3. 여러 명령을 한 번에 실행하기:
   ```sh
   echo -e "date\nuptime" | batch
   ```

4. 파일에서 명령 읽어오기:
   ```sh
   batch -f mycommands.txt
   ```

## Tips
- `batch` 명령은 시스템의 부하가 적을 때만 작업을 실행하므로, 중요한 작업은 이 명령을 통해 예약하는 것이 좋습니다.
- 명령이 실행될 때의 시스템 상태를 고려하여 예약하는 것이 최적의 성능을 보장합니다.
- 예약된 작업이 실행되는 시간을 확인하려면 `atq` 명령을 사용할 수 있습니다.