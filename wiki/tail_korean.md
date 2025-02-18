# [리눅스] Debian Almquist Shell (dash) tail 사용법: 파일의 마지막 부분을 출력합니다.

## Overview
`tail` 명령어는 파일의 마지막 몇 줄을 출력하는 데 사용됩니다. 주로 로그 파일을 모니터링하거나 파일의 최근 내용을 확인할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
tail [options] [arguments]
```

## Common Options
- `-n [number]`: 출력할 줄 수를 지정합니다. 기본값은 10줄입니다.
- `-f`: 파일의 끝에서 새로운 내용을 실시간으로 출력합니다. 로그 파일 모니터링에 유용합니다.
- `-c [number]`: 바이트 수를 지정하여 출력합니다.

## Common Examples
- 기본적으로 마지막 10줄 출력하기:
  ```bash
  tail filename.txt
  ```

- 마지막 20줄 출력하기:
  ```bash
  tail -n 20 filename.txt
  ```

- 파일의 끝에서 새로운 내용을 실시간으로 출력하기:
  ```bash
  tail -f logfile.log
  ```

- 마지막 50바이트 출력하기:
  ```bash
  tail -c 50 filename.txt
  ```

## Tips
- `-f` 옵션을 사용할 때는 `Ctrl + C`를 눌러서 프로세스를 종료할 수 있습니다.
- 여러 파일을 동시에 모니터링할 수 있으며, 각 파일의 이름이 출력됩니다.
- `tail`과 `grep`을 조합하여 특정 패턴이 포함된 마지막 줄을 찾을 수 있습니다.