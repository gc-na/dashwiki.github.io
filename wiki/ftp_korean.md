# [리눅스] Debian Almquist Shell (dash) ftp 사용법: 파일 전송을 위한 명령어

## Overview
`ftp` 명령어는 파일 전송 프로토콜(File Transfer Protocol)을 사용하여 원격 서버와 파일을 전송하는 데 사용됩니다. 이 명령어를 통해 사용자는 서버에 연결하고, 파일을 업로드하거나 다운로드할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
ftp [options] [arguments]
```

## Common Options
- `-i`: 바이너리 모드로 전송, 파일이 손실되지 않도록 함.
- `-n`: 자동 로그인 방지, 수동으로 로그인해야 함.
- `-v`: 자세한 출력 모드, 전송 과정의 정보를 더 많이 보여줌.

## Common Examples
1. 원격 FTP 서버에 연결하기:
   ```sh
   ftp ftp.example.com
   ```

2. 사용자 이름과 비밀번호를 입력하여 로그인하기:
   ```sh
   ftp -n ftp.example.com
   ```

3. 파일 다운로드하기:
   ```sh
   get filename.txt
   ```

4. 파일 업로드하기:
   ```sh
   put filename.txt
   ```

5. 여러 파일을 한 번에 다운로드하기:
   ```sh
   mget *.txt
   ```

## Tips
- FTP 연결 후 `binary` 명령어를 사용하여 바이너리 모드로 전환하는 것을 잊지 마세요. 이는 이미지나 비디오 파일을 전송할 때 중요합니다.
- FTP 사용 시 보안에 유의하고, 가능한 경우 SFTP(SSH File Transfer Protocol)를 사용하는 것이 좋습니다.
- 대량의 파일을 전송할 때는 `mput` 및 `mget` 명령어를 활용하여 효율성을 높이세요.