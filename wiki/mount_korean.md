# [리눅스] Debian Almquist Shell (dash) mount 사용법: 파일 시스템을 연결합니다.

## Overview
`mount` 명령은 파일 시스템을 특정 디렉토리에 연결하여 사용자가 해당 파일 시스템의 파일에 접근할 수 있도록 합니다. 주로 외부 저장 장치나 네트워크 파일 시스템을 사용할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
mount [options] [arguments]
```

## Common Options
- `-t` : 파일 시스템의 유형을 지정합니다.
- `-o` : 마운트 옵션을 설정합니다. 예를 들어, 읽기 전용으로 마운트할 수 있습니다.
- `-a` : `/etc/fstab` 파일에 정의된 모든 파일 시스템을 마운트합니다.
- `-r` : 파일 시스템을 읽기 전용으로 마운트합니다.

## Common Examples
1. **USB 드라이브 마운트하기**
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```
   `/dev/sdb1`에 연결된 USB 드라이브를 `/mnt/usb` 디렉토리에 마운트합니다.

2. **읽기 전용으로 마운트하기**
   ```bash
   mount -o ro /dev/sdb1 /mnt/usb
   ```
   USB 드라이브를 읽기 전용으로 마운트합니다.

3. **특정 파일 시스템 유형 지정하기**
   ```bash
   mount -t vfat /dev/sdb1 /mnt/usb
   ```
   FAT 파일 시스템으로 형식화된 USB 드라이브를 마운트합니다.

4. **모든 파일 시스템 마운트하기**
   ```bash
   mount -a
   ```
   `/etc/fstab`에 정의된 모든 파일 시스템을 마운트합니다.

## Tips
- 마운트하기 전에 항상 해당 디렉토리가 존재하는지 확인하세요.
- 마운트 해제를 원할 경우 `umount` 명령을 사용하세요.
- 시스템 부팅 시 자동으로 마운트하려면 `/etc/fstab` 파일을 수정하세요.