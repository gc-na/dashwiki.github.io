# [리눅스] Debian Almquist Shell (dash) umask 사용법: 파일 생성 시 기본 권한 설정

## Overview
`umask` 명령어는 새로운 파일이나 디렉토리가 생성될 때 기본적으로 적용되는 권한을 설정하는 데 사용됩니다. 이 명령어를 통해 사용자는 파일의 기본 권한을 조정하여 보안을 강화할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```sh
umask [options] [arguments]
```

## Common Options
- `-S`: 현재 umask 값을 심볼릭 형태로 표시합니다.
- `-p`: 현재 프로세스의 umask 값을 표시합니다.

## Common Examples
1. 현재 umask 값 확인하기:
   ```sh
   umask
   ```

2. umask 값을 022로 설정하기 (새 파일의 기본 권한을 rw-r--r--로 설정):
   ```sh
   umask 022
   ```

3. umask 값을 007로 설정하기 (새 파일의 기본 권한을 rw-r-----로 설정):
   ```sh
   umask 007
   ```

4. 심볼릭 형태로 현재 umask 값 확인하기:
   ```sh
   umask -S
   ```

5. umask 값을 영구적으로 설정하기 위해 `~/.profile` 파일에 추가하기:
   ```sh
   echo "umask 027" >> ~/.profile
   ```

## Tips
- umask 값을 설정할 때, 숫자가 낮을수록 더 많은 권한이 부여됩니다. 예를 들어, 000은 모든 권한을 부여합니다.
- 보안을 강화하고 싶다면, umask 값을 높게 설정하는 것이 좋습니다.
- umask 설정은 현재 세션에만 적용되므로, 영구적으로 설정하려면 초기화 파일에 추가해야 합니다.