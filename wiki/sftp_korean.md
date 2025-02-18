# [리눅스] Debian Almquist Shell (dash) sftp 사용법: 파일 전송을 위한 안전한 프로토콜

## Overview
sftp(Secure File Transfer Protocol) 명령은 네트워크를 통해 파일을 안전하게 전송하기 위한 프로토콜입니다. sftp는 ssh(Secure Shell)를 기반으로 하며, 파일 전송뿐만 아니라 원격 서버와의 상호작용을 지원합니다.

## Usage
sftp 명령의 기본 구문은 다음과 같습니다.

```bash
sftp [options] [user@]host
```

## Common Options
- `-b batchfile`: 비대화식 모드에서 사용할 배치 파일을 지정합니다.
- `-C`: 전송 중 데이터 압축을 활성화합니다.
- `-i identity_file`: 인증에 사용할 개인 키 파일을 지정합니다.
- `-o option`: ssh_config 옵션을 설정합니다.

## Common Examples
다음은 sftp 명령의 몇 가지 실용적인 예입니다.

1. 원격 서버에 연결하기:
   ```bash
   sftp user@hostname
   ```

2. 파일 업로드하기:
   ```bash
   put localfile.txt
   ```

3. 파일 다운로드하기:
   ```bash
   get remotefile.txt
   ```

4. 디렉토리 목록 보기:
   ```bash
   ls
   ```

5. 원격 디렉토리 변경하기:
   ```bash
   cd /path/to/remote/directory
   ```

## Tips
- sftp 세션을 종료하려면 `bye` 또는 `exit` 명령을 사용하세요.
- 대량의 파일을 전송할 때는 `-b` 옵션을 사용하여 배치 파일을 활용하면 유용합니다.
- 전송 속도를 개선하기 위해 `-C` 옵션으로 압축을 활성화하는 것을 고려하세요.