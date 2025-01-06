Docker를 효율적으로 다루기 위해 알아야 할 Linux 명령어를 정리해보았습니다. Docker는 컨테이너 관리 도구로, 주로 Linux 환경에서 실행되기 때문에 기본적인 Linux 명령어 이해가 필수적입니다.

---

## **1. 파일 및 디렉토리 관련 명령어**

Docker 컨테이너의 파일 시스템을 관리하거나, 호스트와의 볼륨을 연결할 때 필요.

- `ls` : 파일 및 디렉토리 목록 보기
  - 예: `ls -l /var/lib/docker`
- `cd` : 디렉토리 이동
  - 예: `cd /path/to/directory`
- `pwd` : 현재 작업 디렉토리 경로 확인
- `mkdir` : 디렉토리 생성
  - 예: `mkdir /mydata`
- `rm` : 파일 및 디렉토리 삭제
  - 예: `rm -rf /path/to/delete`
- `cp` : 파일 복사
  - 예: `cp source_file destination_file`
- `mv` : 파일 이동 및 이름 변경
  - 예: `mv old_name new_name`
- `cat` : 파일 내용 출력
  - 예: `cat /etc/hosts`
- `touch` : 빈 파일 생성
  - 예: `touch myfile.txt`

---

## **2. 프로세스 및 네트워크 관리 명령어**

컨테이너 프로세스와 네트워크 상태를 확인 및 관리.

- `ps` : 실행 중인 프로세스 확인
  - 예: `ps aux | grep docker`
- `top` : 실시간 프로세스 상태 확인
  - 예: `top`
- `kill` : 프로세스 종료
  - 예: `kill -9 <PID>`
- `netstat` : 네트워크 연결 상태 확인
  - 예: `netstat -tuln`
- `ss` : 네트워크 소켓 정보 확인
  - 예: `ss -tuln`
- `ping` : 네트워크 연결 확인
  - 예: `ping google.com`
- `curl` : HTTP 요청 전송 및 확인
  - 예: `curl http://localhost:8080`
- `ifconfig` / `ip` : 네트워크 인터페이스 설정 및 확인
  - 예: `ip addr show`

---

## **3. 디스크 및 스토리지 관리 명령어**

Docker 볼륨, 이미지, 컨테이너 저장 공간 관리에 유용.

- `df` : 디스크 사용량 확인
  - 예: `df -h`
- `du` : 디렉토리별 디스크 사용량 확인
  - 예: `du -sh /var/lib/docker`
- `mount` / `umount` : 파일 시스템 마운트 및 언마운트
  - 예: `mount /dev/sdb1 /mnt`
- `lsblk` : 블록 디바이스 확인
  - 예: `lsblk`
- `fdisk` : 디스크 파티션 관리
  - 예: `fdisk -l`

---

## **4. 권한 및 사용자 관리 명령어**

컨테이너 실행 시 권한 문제 해결과 보안 관리.

- `chmod` : 파일 권한 변경
  - 예: `chmod 755 myscript.sh`
- `chown` : 파일 소유자 변경
  - 예: `chown user:group myfile`
- `sudo` : 관리자 권한으로 명령 실행
  - 예: `sudo docker ps`
- `whoami` : 현재 사용자 확인
  - 예: `whoami`
- `id` : 사용자 및 그룹 ID 확인
  - 예: `id`

---

## **5. 시스템 정보 및 로그 관리 명령어**

컨테이너 성능 문제 진단 및 시스템 상태 모니터링.

- `uname` : 시스템 정보 확인
  - 예: `uname -a`
- `dmesg` : 커널 메시지 출력
  - 예: `dmesg | grep docker`
- `uptime` : 시스템 가동 시간 확인
- `free` : 메모리 사용량 확인
  - 예: `free -h`
- `vmstat` : 시스템 성능 모니터링
  - 예: `vmstat`
- `journalctl` : 시스템 로그 확인
  - 예: `journalctl -u docker.service`
- `tail` : 파일의 마지막 몇 줄 출력 (로그 모니터링에 유용)
  - 예: `tail -f /var/log/docker.log`

---

## **6. 압축 및 백업 관련 명령어**

Docker 볼륨 백업 및 이미지 저장에 활용.

- `tar` : 파일 압축 및 해제
  - 압축: `tar -cvf backup.tar /mydata`
  - 해제: `tar -xvf backup.tar`
- `gzip` : 파일 압축
  - 예: `gzip myfile`
- `rsync` : 파일 동기화
  - 예: `rsync -av /source /destination`

---

## **7. 기타 유용한 명령어**

Docker 작업 효율성을 높이는 데 도움.

- `grep` : 텍스트 검색
  - 예: `docker ps | grep my-container`
- `awk` : 텍스트 데이터 처리
  - 예: `docker ps | awk '{print $1}'`
- `sed` : 텍스트 편집
  - 예: `sed 's/old/new/g' file`
- `env` : 환경 변수 확인
  - 예: `env | grep DOCKER`

---
