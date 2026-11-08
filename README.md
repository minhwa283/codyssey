마크다운 문법
개행은 줄 끝에 두 칸 띄우기  
개행  
_기울림꼴_ , **굵게**
>인용구  
>개별적으로 붙여야됨
---
### 추가내용
검증 방법(어떤 명령으로 무엇을 확인했는지) + 결과 위치 링크
트러블슈팅 2건 이상(문제 → 원인 가설 → 확인 → 해결/대안)
기술 문서만 읽어도 전체 수행 내용을 파악할 수 있어야 한다.

---  
_[올인원 - 입학연수 E1-1]_
<img width="846" height="260" alt="image" src="https://github.com/user-attachments/assets/7da59523-9c41-43b1-9eef-f0a92ad35dc8" />

# 📌 프로젝트 개요

개발은 **환경을 세팅하는 순간부터 시작**됩니다.  
개발자의 첫 번째 기반인 **개발 워크스테이션을 직접 구축**하는 실습으로 코드가 "내 컴퓨터에서만" 돌아가는 문제를 줄이고, 팀원 누구나 같은 방식으로 실행, 배포, 디버깅할 수 있는 환경 구성을 목표로 합니다.

    📚 학습도구
    리눅스 CLI(터미널), Docker(컨테이너), Git/GitHub(버전 관리 및 협업)
    
<br>  

# 📌 학습 목표

- ✅ 터미널(CLI)로 작업 디렉토리와 파일 권한 관리
- ✅ Docker를 이용한 재현 가능한 실행 환경 구축
- ✅ Git/GitHub를 통한 버전 관리 및 협업 기반 마련
- ✅ "내 컴퓨터에서만 돌아가는 문제" 해결  

<br><br><br>     



## 🖥️ 실행 환경
| 항목 | 내용 |
|------|------|
| OS | Windows 11 + WSL2 |
| 배포판 | Ubuntu 22.04 LTS |
| 쉘 | bash |
| 터미널 | Windows Terminal |
| 컨테이너 | Docker |
| Docker 버전 | Docker version 29.9.2 |
| Git 버전 | 확인 후 작성 |
<img width="553" height="32" alt="image" src="https://github.com/user-attachments/assets/5f0d6dfd-eee8-4d30-a136-53902b09d083" />

<br><br>    

## 🖥️ 수행 항목 체크리스트

✅ 터미널 기본 조작
- [x] pwd - 현재 경로 확인
- [x] ls - 파일 목록 확인
- [x] mkdir - 디렉토리 생성
- [x] cd - 디렉토리 이동

✅ 파일 권한
- [x] chmod 644 - 파일 읽기/쓰기 권한 설정
- [x] chmod 755 - 실행 권한 설정
- [x] ls -l - 권한 확인

✅ Docker 설치 및 검증
- [x] Docker 엔진 설치
- [x] docker --version 확인
- [x] docker run hello-world 실행  
      
 ✅ Dockerfile 작성 및 빌드
- [x] Dockerfile 작성
- [x] docker build 이미지 빌드
- [x] docker images 이미지 확인

✅ 포트 매핑 및 컨테이너 실행
- [x] docker run -p 8080:80 실행
- [x] localhost:8080 브라우저 접속 확인
- [x] docker ps 컨테이너 상태 확인

✅ 볼륨 / 바인드 마운트
- [x] 바인드 마운트 (-v) 실습
- [x] 파일 수정 실시간 반영 확인
- [x] 볼륨 마운트 실습
- [x] 컨테이너 재시작 후 데이터 유지 확인

✅ Git
- [x] git init
- [x] git add
- [x] git commit
- [x] git push

✅ GitHub
- [x] Repository 생성
- [x] README.md 작성
- [x] 원격 저장소 연결 및 push 완료

<br><br>

------
**🖥️ 실습 목록**
# STEP 1. 터미널 & Docker 설치
 
    ✅ 1단계 - WSL2 설치 : PowerShell(관리자 권한)에서 WSL2 설치 명령 실행 후 컴퓨터 재부팅  
    ✅ 2단계 - Ubuntu 설치  
    ✅ 3단계 - 환경 설정  
    ✅ 4단계 - 패키지 업데이트 : sudo apt update 실행 -> 32.4MB 다운로드 완료 -> 133개 업그레이드 가능 패키지 확인  


<br>

 ## 1. WSL2 및 Ubuntu 설치 : 리눅스 CLI (터미널)  
   - PowerShell을 이용하여 WSL 및 Ubuntu 설치한다.
<img width="1255" height="621" alt="image" src="https://github.com/user-attachments/assets/8c2ff85e-46c6-4250-a18c-f1990f332fd1" />
<img width="1099" height="246" alt="image" src="https://github.com/user-attachments/assets/cfec0886-36f6-4f06-80de-da8394d145f8" />
<img width="1546" height="904" alt="image" src="https://github.com/user-attachments/assets/10e64058-da2c-4527-84b3-f021cd528e63" />

<br>

## 2. Docker 설치
    - Docker를 쓰는 이유 : 나중에 배울 데이터베이스, 서버 등을 복잡한 설치없이 바로 실행할 수 있음  
    
 ### (1) 필수 패키지 설치  
<img width="855" height="229" alt="image" src="https://github.com/user-attachments/assets/265f0b27-b083-401e-8b7f-ca5c6fc5d584" />

### (2) Docker 공식 GPG 키 추가
<img width="1568" height="188" alt="image" src="https://github.com/user-attachments/assets/95a3618a-d4be-441b-902c-ac673ef8b70d" />

 ### (3) Docker 저장소 추가
 <img width="857" height="59" alt="image" src="https://github.com/user-attachments/assets/2a24531d-5153-4bdf-9c57-d74cb4257fdd" />

 ### (4) Docker 엔진 설치
 <img width="848" height="239" alt="image" src="https://github.com/user-attachments/assets/18304909-e576-41ca-a51c-bf6aff944e9f" />

 ### (5) 설치완료
 <img width="358" height="31" alt="image" src="https://github.com/user-attachments/assets/f0fc18c8-4815-4f90-afe8-82282b2e8216" />

<br><br>

### 📝 Docker 운영 검증 로그
<img width="587" height="176" alt="image" src="https://github.com/user-attachments/assets/4c8590c7-8a32-47fd-88ea-b8149b1250ec" />
<img width="851" height="90" alt="image" src="https://github.com/user-attachments/assets/72439e50-e272-4c3f-b1b8-b5f465fea57b" />      

<br>

 ### 👉 용어정리
    1️⃣ CLI (Command Line Interface) : 텍스트 명령어로 컴퓨터를 조작하는 방식  
    2️⃣ PowerSell : 윈도우 명령어 창(CLI)  
    3️⃣ WSL(Windows Subsystem for Linux) : Windows 안에서 Linux를 쓸 수 있게 해주는 도구  
    4️⃣ Ubuntu : 리눅스 운영체제 종류  
    5️⃣Docker : 프로그램을 어디서든 똑같이 실행할 수 있게 해주는 도구 

<br><br>

# STEP 2. 작업 디렉토리 & 권한 정리
<img width="1323" height="336" alt="image" src="https://github.com/user-attachments/assets/2de90437-afe5-4432-acbd-53411ff76edf" />
<img width="880" height="189" alt="image" src="https://github.com/user-attachments/assets/1e39f7cc-c182-4fc0-a5b7-c73f40c09158" />


<br><br>

# STEP 3. Dockerfile로 웹서버 만들기
<img width="1198" height="121" alt="image" src="https://github.com/user-attachments/assets/60aadf35-6fb9-47db-9795-8d4e31237960" />
<img width="527" height="116" alt="image" src="https://github.com/user-attachments/assets/24add6b5-dcc2-4ea1-b796-41ba68ff3977" />

<img width="1224" height="334" alt="image" src="https://github.com/user-attachments/assets/8844c599-40bf-4f97-9310-fa224c12139e" />
<img width="899" height="154" alt="image" src="https://github.com/user-attachments/assets/0d2a7d8d-b1b2-4d34-bc1c-5cffab1115fa" />
<img width="1568" height="669" alt="image" src="https://github.com/user-attachments/assets/4ca7a86c-4c9c-4e15-8ac1-dd2f303c3ced" />


<br><br>

# STEP 4. 포트 매핑으로 접속 확인
* 브라우저 직접 접속
<img width="1568" height="139" alt="image" src="https://github.com/user-attachments/assets/b3ca8ea2-a2c4-4655-a17a-175d2e930654" />
<img width="1470" height="88" alt="image" src="https://github.com/user-attachments/assets/49b2c6a8-a99d-415d-9178-405a11a3a0db" />

<br><br>

# STEP 5. 바인드 마운트 / 볼륨
* 코드 변경 즉시 반영
* 데이터 영속성 확인

<img width="1568" height="655" alt="image" src="https://github.com/user-attachments/assets/b6617c48-d57a-4095-bcaf-79d4d488ee29" />
<img width="1568" height="1161" alt="image" src="https://github.com/user-attachments/assets/8de1591e-717e-4cc4-8462-68015baa6a23" />
<img width="1568" height="1052" alt="image" src="https://github.com/user-attachments/assets/b7afe40f-3965-4684-b116-6efa4c8c2b7c" />
<img width="1568" height="619" alt="image" src="https://github.com/user-attachments/assets/3cdcfd9d-0e28-4974-85c1-b3b0396b3a1c" />

<br><br>

# STEP 6. Git / GitHub 연동
* 버전 관리 & 팀 협업
### Git 초기회 & 파일 등록
<img width="658" height="185" alt="image" src="https://github.com/user-attachments/assets/d207f9fa-3ce1-4b5c-86d6-a2d984761b86" />
<img width="767" height="100" alt="image" src="https://github.com/user-attachments/assets/1b0c4792-c58a-4180-831b-3e34e5b32b32" />




-------
### 1. 터미널(WSL2) + Ubuntu 설치
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
