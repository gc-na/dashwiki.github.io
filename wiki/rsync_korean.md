# [한국어] Debian Almquist Shell (dash) rsync 사용법: 파일 및 디렉토리 동기화

## 개요
`rsync` 명령은 파일과 디렉토리를 효율적으로 동기화하고 전송하는 데 사용됩니다. 로컬 및 원격 시스템 간에 데이터를 복사할 수 있으며, 변경된 부분만 전송하여 대역폭을 절약합니다.

## 사용법
기본 구문은 다음과 같습니다:
```bash
rsync [옵션] [소스] [대상]
```

## 일반 옵션
- `-a`: 아카이브 모드로, 파일의 권한, 소유자, 타임스탬프 등을 유지합니다.
- `-v`: 진행 상황을 자세히 출력합니다.
- `-z`: 전송 중 데이터를 압축합니다.
- `-r`: 하위 디렉토리를 재귀적으로 복사합니다.
- `--delete`: 대상에서 소스에 없는 파일을 삭제합니다.

## 일반 예제
1. 로컬 디렉토리 동기화:
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. 원격 서버로 파일 전송:
   ```bash
   rsync -av /local/file.txt user@remote:/path/to/destination/
   ```

3. 원격 서버에서 로컬로 파일 다운로드:
   ```bash
   rsync -av user@remote:/path/to/file.txt /local/destination/
   ```

4. 하위 디렉토리 포함하여 동기화:
   ```bash
   rsync -avz /path/to/source/ user@remote:/path/to/destination/
   ```

5. 동기화 시 삭제 옵션 사용:
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## 팁
- `-n` 또는 `--dry-run` 옵션을 사용하여 실제로 파일을 전송하기 전에 어떤 파일이 전송될지를 미리 확인할 수 있습니다.
- 정기적인 백업을 위해 `cron`과 함께 사용할 수 있습니다.
- 대량의 파일을 전송할 때는 `-z` 옵션을 사용하여 전송 속도를 개선할 수 있습니다.