# [리눅스] Debian Almquist Shell (dash) curl 사용법: 웹에서 데이터 전송

## Overview
curl 명령어는 URL을 통해 데이터를 전송하거나 수신하는 데 사용됩니다. 주로 HTTP, FTP와 같은 프로토콜을 통해 웹 서버와 상호작용할 수 있도록 도와줍니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
curl [options] [arguments]
```

## Common Options
- `-X`: 요청 메서드를 지정합니다 (예: GET, POST).
- `-d`: POST 요청 시 전송할 데이터를 지정합니다.
- `-H`: HTTP 헤더를 추가합니다.
- `-o`: 응답을 파일로 저장합니다.
- `-I`: HTTP 헤더만 요청합니다.

## Common Examples
- **웹 페이지 가져오기**:
  ```bash
  curl http://example.com
  ```

- **파일 다운로드**:
  ```bash
  curl -o myfile.txt http://example.com/file.txt
  ```

- **POST 요청 보내기**:
  ```bash
  curl -X POST -d "name=John&age=30" http://example.com/api
  ```

- **헤더 정보 확인**:
  ```bash
  curl -I http://example.com
  ```

## Tips
- curl 명령어는 다양한 프로토콜을 지원하므로, 필요한 프로토콜에 맞게 옵션을 조정하세요.
- 대량의 데이터를 전송할 때는 `-o` 옵션을 사용하여 파일로 저장하는 것이 유용합니다.
- API와 상호작용할 때는 `-H` 옵션을 사용하여 필요한 헤더를 추가하는 것을 잊지 마세요.