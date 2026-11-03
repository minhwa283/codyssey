# Codyssey

## 프로젝트 개요
Windows WSL2 환경에서 Docker를 활용한 개발환경 구축 실습

---

## 실행 환경
| 항목 | 내용 |
|------|------|
| OS | Windows + WSL2 (Ubuntu) |
| 컨테이너 | Docker |
| 웹서버 | Nginx |
| 포트 | 8080:80 |

## 실행 환경
| 항목 | 내용 |
|------|------|
| OS | Windows 11 + WSL2 |
| 배포판 | Ubuntu 22.04 LTS |
| 쉘 | bash |
| 터미널 | Windows Terminal |
| Docker 버전 | 확인 후 작성 |
![Docker 버전 확인](https://github.com/user-attachments/assets/9cd24b5e-aaac-4bb2-8765-a92120eb5d5b)
| Git 버전 | 확인 후 작성 |

---

## 실습 목록

### 1. WSL2 + Ubuntu 설치
- Windows에 WSL2 설치
- Ubuntu 배포판 설치 및 초기 설정

### 2. Docker 설치 및 검증
- Docker 엔진 설치
- 설치 확인 명령어 실행

### 3. 터미널 기본 조작
- pwd, ls, mkdir, cd 명령어 실습

### 4. 파일 권한 실습
- 파일 권한 변경 (644, 755)
- chmod 명령어 사용

### 5. Dockerfile 작성 및 빌드
- Dockerfile 작성
- 이미지 빌드 성공

### 6. 컨테이너 실행 및 포트 매핑
- 포트 매핑 (8080:80)
- 브라우저 접속 확인 (localhost:8080)

### 7. 바인드 마운트 실습
- 파일 실시간 반영 확인

### 8. 볼륨 마운트 실습
- 컨테이너 재시작 없이 변경 반영 확인

---

## 주요 명령어 정리

### Docker 명령어
\```bash
# 이미지 빌드
docker build -t 이미지명 .

# 컨테이너 실행 (포트 매핑)
docker run -d -p 8080:80 이미지명

# 바인드 마운트 실행
docker run -d -p 8080:80 -v $(pwd):/usr/share/nginx/html 이미지명

# 실행 중인 컨테이너 확인
docker ps

# 컨테이너 중지
docker stop 컨테이너ID
\```

### 터미널 명령어
\```bash
pwd       # 현재 위치 확인
ls        # 파일 목록 확인
mkdir     # 폴더 생성
cd        # 폴더 이동
chmod 644 파일명   # 파일 권한 변경
chmod 755 파일명   # 실행 권한 부여
\```

---

## 수행 로그
| 항목 | 상태 |
|------|------|
| WSL2 설치 | ✅ 완료 |
| Docker 설치 | ✅ 완료 |
| 터미널 실습 | ✅ 완료 |
| 파일 권한 실습 | ✅ 완료 |
| Dockerfile 빌드 | ✅ 완료 |
| 포트 매핑 확인 | ✅ 완료 |
| 바인드 마운트 | ✅ 완료 |
| 볼륨 마운트 | ✅ 완료 |
| GitHub 저장소 생성 | ✅ 완료 |
