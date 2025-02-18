# [한국어] Debian Almquist Shell (dash) scp 사용법: 파일 전송

## 개요
`scp` 명령어는 안전한 복사(Secure Copy Protocol)를 사용하여 네트워크를 통해 파일을 안전하게 전송하는 데 사용됩니다. 이 명령어는 SSH 프로토콜을 기반으로 하여 데이터를 암호화하여 전송합니다.

## 사용법
기본 구문은 다음과 같습니다:
```
scp [옵션] [소스] [대상]
```

## 일반 옵션
- `-r`: 디렉토리를 재귀적으로 복사합니다.
- `-P`: 원격 호스트의 포트를 지정합니다 (대문자 P).
- `-i`: 특정 SSH 키 파일을 사용하여 인증합니다.
- `-v`: 자세한 출력을 활성화하여 진행 상황을 확인할 수 있습니다.

## 일반 예제
1. 로컬 파일을 원격 서버로 복사하기:
   ```bash
   scp localfile.txt user@remotehost:/path/to/destination/
   ```

2. 원격 서버에서 로컬로 파일 복사하기:
   ```bash
   scp user@remotehost:/path/to/remotefile.txt /local/destination/
   ```

3. 디렉토리를 재귀적으로 복사하기:
   ```bash
   scp -r localdir/ user@remotehost:/path/to/destination/
   ```

4. 특정 포트를 사용하여 파일 복사하기:
   ```bash
   scp -P 2222 localfile.txt user@remotehost:/path/to/destination/
   ```

## 팁
- 대용량 파일을 전송할 때는 `-C` 옵션을 사용하여 압축을 활성화하면 전송 속도를 높일 수 있습니다.
- 원격 서버에 자주 접속하는 경우 SSH 키를 설정하여 비밀번호 입력을 생략할 수 있습니다.
- `-v` 옵션을 사용하여 문제 발생 시 디버깅 정보를 확인할 수 있습니다.