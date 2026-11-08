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
    
<br>  

# 📌 과제 목표
 ### 👉 (1) 절대 경로와 상대 경로의 차이를 예시를 들어 설명할 수 있다.
<img width="564" height="370" alt="image" src="https://github.com/user-attachments/assets/1b45bb10-c761-4423-8874-696d6d0e7cc6" />

<br><br>   
### 👉 (2) 파일 권한의 의미(r/w/x)와 755, 644 같은 표기가 어떤 규칙으로 해석되는지 설명할 수 있다.
<img width="645" height="320" alt="image" src="https://github.com/user-attachments/assets/90a74b49-2826-42e2-a186-0fb8e8b7aa74" />  
<img width="284" height="128" alt="image" src="https://github.com/user-attachments/assets/7978676d-5b4a-4cc9-9dec-c47e1159a7be" />

<br><br> 
### 👉 (3) 기존 Dockerfile을 기반으로 “커스텀 이미지”를 만들 수 있다.
<img width="645" height="340" alt="image" src="https://github.com/user-attachments/assets/e9309e77-6afc-48a1-813b-bc3f869840d4" />
<img width="350" height="230" alt="image" src="https://github.com/user-attachments/assets/e1d318cd-889b-4537-9dd7-ecd260c98d54" />


<br><br> 
### 👉 (4) 포트 매핑이 필요한 이유를 설명할 수 있다.
<img width="645" height="340" alt="image" src="https://github.com/user-attachments/assets/ef407415-3cec-4774-8677-94f2e9ea0c76" />

<br><br> 
### 👉 (5) Docker 볼륨(영속 데이터)을 설명할 수 있다.
<img width="645" height="340" alt="image" src="https://github.com/user-attachments/assets/c0bc4247-2e5f-4c0f-beb0-fd5ddbb55ee0" />

<br><br> 
### 👉 (6) Git과 GitHub의 역할 차이(로컬 버전관리 vs 원격 협업 플랫폼)를 설명할 수 있다.
<img width="645" height="340" alt="image" src="https://github.com/user-attachments/assets/e81f11c3-1d3a-4639-b279-5c508d0e0231" />

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
| Git 버전 | git version 2.53.0 |


```bash
# Docker 설치 및 버전 확인
docker --version
# 실행 결과: Docker version 29.9.2, build a82e528

# Git 설치 및 버전 확인
git --version
# 실행 결과: git version 2.53.0
```
  
<img width="553" height="32" alt="image" src="https://github.com/user-attachments/assets/5f0d6dfd-eee8-4d30-a136-53902b09d083" />
<img width="408" height="35" alt="image" src="https://github.com/user-attachments/assets/707eb2bc-563a-4b26-a180-e7670e8e6e63" />


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

```powershell
# 1. WSL2 설치 (Windows PowerShell을 관리자 권한으로 실행)
wsl --install

# 실행 결과: Linux용 Windows 하위 시스템 3.0.3 설치 완료
# VirtualMachinePlatform 설치 완료
# 시스템 재시작 필요 안내 출력

# 2. Ubuntu 설치
wsl --install -d Ubuntu

# 실행 결과: Ubuntu 다운로드 및 설치 완료
# Ubuntu 초기 실행 및 사용자 계정 생성 진행

# 3. Ubuntu 패키지 다운로드
# Ubuntu 초기 설정 중 패키지 목록 다운로드 진행
# 실행 결과: Ubuntu 패키지 저장소에서 패키지 정보 다운로드
```

<img width="1255" height="621" alt="image" src="https://github.com/user-attachments/assets/8c2ff85e-46c6-4250-a18c-f1990f332fd1" />
<img width="1099" height="246" alt="image" src="https://github.com/user-attachments/assets/cfec0886-36f6-4f06-80de-da8394d145f8" />
<img width="1546" height="904" alt="image" src="https://github.com/user-attachments/assets/10e64058-da2c-4527-84b3-f021cd528e63" />

<br>

## 2. Docker 설치
    - Docker를 쓰는 이유 : 나중에 배울 데이터베이스, 서버 등을 복잡한 설치없이 바로 실행할 수 있음  
    
```bash
# (1) 필수 패키지 설치
# Docker 설치에 필요한 인증서, 다운로드 및 GPG 관리 도구 설치
sudo apt install -y ca-certificates curl gnupg
# 실행 결과: 필요한 패키지 다운로드 및 업그레이드 진행

# (2) Docker 공식 GPG 키 추가
# GPG 키를 저장할 디렉터리 생성
sudo install -m 0755 -d /etc/apt/keyrings

# Docker 공식 GPG 키 다운로드 및 등록
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

# GPG 키 파일에 읽기 권한 추가
sudo chmod a+r /etc/apt/keyrings/docker.gpg
# 실행 결과: 오류 메시지 없이 명령어 완료

# (3) Docker 저장소 추가
# Ubuntu 환경에 Docker 공식 패키지 저장소 등록
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
# 실행 결과: Docker 저장소 등록 명령 실행

# (4) Docker 엔진 설치
# 패키지 목록 업데이트
sudo apt-get update
# 실행 결과: Docker 저장소를 포함한 패키지 목록 업데이트 완료

# Docker 엔진, CLI, containerd 및 관련 플러그인 설치
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
# 실행 결과: Docker 관련 패키지 설치 진행

# (5) Docker 설치 확인
# 설치된 Docker 버전 확인
docker --version
# 실행 결과: Docker version 29.9.2, build a82e528
```

    
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

```bash
# (1) Docker 실행 환경 확인
# Docker 클라이언트 및 플러그인 정보 확인
docker info
# 실행 결과: Docker Engine Community 버전 29.9.2
# Buildx 버전 v0.38.1, Compose 버전 v5.7.0 확인

# (2) Docker 이미지 목록 확인
# 로컬에 저장된 Docker 이미지 목록 조회
docker images
# 실행 결과: docker-mission:latest 이미지 확인
# hello-world:latest 이미지 확인
# nginx:alpine 이미지 확인
```

<img width="587" height="176" alt="image" src="https://github.com/user-attachments/assets/4c8590c7-8a32-47fd-88ea-b8149b1250ec" />
<img width="851" height="90" alt="image" src="https://github.com/user-attachments/assets/72439e50-e272-4c3f-b1b8-b5f465fea57b" />      

<br>

 ### 👉 용어정리
    1️⃣ CLI (Command Line Interface) : 텍스트 명령어로 컴퓨터를 조작하는 방식  
    2️⃣ PowerSell : 윈도우 명령어 창(CLI)  
    3️⃣ WSL(Windows Subsystem for Linux) : Windows 안에서 Linux를 쓸 수 있게 해주는 도구  
    4️⃣ Ubuntu : 리눅스 운영체제 종류  
    5️⃣ Docker : 프로그램을 어디서든 똑같이 실행할 수 있게 해주는 도구 

<br><br>

# STEP 2. 작업 디렉토리 & 권한 정리

```bash
# (1) 작업 디렉터리 생성
mkdir -p ~/projects/docker-mission
# 실행 결과: docker-mission 디렉터리 생성

# (2) 작업 디렉터리로 이동
cd ~/projects/docker-mission
# 실행 결과: docker-mission 디렉터리로 이동

# (3) 현재 작업 경로 확인
pwd
# 실행 결과: /home/minhwa/projects/docker-mission

# (4) 디렉터리 및 파일 권한 확인
ls -al
# 실행 결과: test.sh 파일 확인
# 파일 권한: -rwxr-xr-x (755)
```

<img width="1323" height="336" alt="image" src="https://github.com/user-attachments/assets/2de90437-afe5-4432-acbd-53411ff76edf" />
<img width="880" height="189" alt="image" src="https://github.com/user-attachments/assets/1e39f7cc-c182-4fc0-a5b7-c73f40c09158" />


<br><br>

# STEP 3. Dockerfile로 웹서버 만들기

```bash
# Docker 프로젝트 작업 디렉터리로 이동
cd ~/projects/docker-mission

# Dockerfile 생성 및 편집
nano Dockerfile

# Dockerfile 내용 확인
cat Dockerfile
# 실행 결과: Ubuntu 기반 Nginx 웹서버 설정 확인

# dockerfile
# Ubuntu 22.04를 베이스 이미지로 사용
FROM ubuntu:22.04

# 패키지 목록 업데이트 및 Nginx 설치
RUN apt-get update && apt-get install -y nginx

# HTML 파일을 컨테이너의 웹서버 디렉터리로 복사
COPY index.html /var/www/html/index.html

# 컨테이너에서 사용할 웹서버 포트 지정
EXPOSE 80

# 컨테이너 실행 시 Nginx를 포그라운드로 실행
CMD ["nginx", "-g", "daemon off;"]

# 웹페이지 파일 생성 및 편집 (HTML 파일 작성)
nano index.html

#html
<!DOCTYPE html>
<html>
  <head>
    <title>Docker Mission</title>
  </head>
  <body>
    <h1>Hello, Docker!</h1>
  </body>
</html>

#Docker 이미지 빌드
# Docker 그룹 권한 적용
newgrp docker

# 현재 디렉터리의 Dockerfile로 커스텀 이미지 생성
docker build -t docker-mission .

# 실행 결과: Docker 이미지 빌드 완료
# 이미지 이름: docker-mission
# 태그: latest
# 빌드 단계: 8/8 FINISHED
```

<img width="1198" height="121" alt="image" src="https://github.com/user-attachments/assets/60aadf35-6fb9-47db-9795-8d4e31237960" />
<img width="527" height="116" alt="image" src="https://github.com/user-attachments/assets/24add6b5-dcc2-4ea1-b796-41ba68ff3977" />

<img width="1224" height="334" alt="image" src="https://github.com/user-attachments/assets/8844c599-40bf-4f97-9310-fa224c12139e" />
<img width="899" height="154" alt="image" src="https://github.com/user-attachments/assets/0d2a7d8d-b1b2-4d34-bc1c-5cffab1115fa" />
<img width="1568" height="669" alt="image" src="https://github.com/user-attachments/assets/4ca7a86c-4c9c-4e15-8ac1-dd2f303c3ced" />


<br><br>

# STEP 4. 포트 매핑으로 접속 확인

```bash
# (1) Docker 컨테이너 포트 매핑 확인
docker port my-nginx
# 실행 결과: 컨테이너 80번 포트가 호스트 8080번 포트에 연결됨
# 80/tcp -> 0.0.0.0:8080
# 80/tcp -> [::]:8080

# (2) 작업 디렉터리 및 파일 확인
cd ~/projects/docker-mission && ls
# 실행 결과: Dockerfile, index.html, test.sh 파일 확인
```
* 브라우저 직접 접속
<img width="1568" height="139" alt="image" src="https://github.com/user-attachments/assets/b3ca8ea2-a2c4-4655-a17a-175d2e930654" />
<img width="1470" height="88" alt="image" src="https://github.com/user-attachments/assets/49b2c6a8-a99d-415d-9178-405a11a3a0db" />

<br><br>

# STEP 5. 바인드 마운트 / 볼륨
* 바인드 마운트와 볼륨은 둘 다 컨테이너 외부에 데이터를 저장하지만 저장 공간을 누가 관리하는지가 다릅니다.
  여기서 중요한 건 마운트와 볼륨을 서로 반대되는 개념으로 외우면 안 된다는 것입니다.

```bash
# (1) 기존 Nginx 컨테이너 중지
docker stop my-nginx
# 실행 결과: my-nginx 컨테이너 중지

# (2) 바인드 마운트를 적용한 새 컨테이너 생성 및 실행
# 호스트의 docker-mission 폴더를 컨테이너의 웹서버 폴더에 연결
# 호스트 8080번 포트를 컨테이너 80번 포트에 연결
docker run -d \
  --name my-nginx-vol \
  -p 8080:80 \
  -v ~/projects/docker-mission:/usr/share/nginx/html \
  nginx:alpine
# 실행 결과: nginx:alpine 이미지 다운로드 및 컨테이너 생성

# (3) 실행 중인 컨테이너 확인
docker ps
# 실행 결과: my-nginx-vol 컨테이너 실행 중(Up)
# 포트 매핑: 8080 -> 80

# (4) HTML 파일 내용 변경
# 호스트의 index.html 파일을 수정
echo "<h1>Hello, Volume!</h1>" > ~/projects/docker-mission/index.html
# 실행 결과: index.html 파일 내용 변경

# (5) 브라우저에서 변경 내용 확인
# 접속 주소: http://localhost:8080
# 실행 결과: Hello, Volume! 화면 출력
# 바인드 마운트로 연결된 파일의 변경 내용이 웹페이지에 반영됨

# (6) 컨테이너 중지
docker stop my-nginx-vol
# 실행 결과: my-nginx-vol 컨테이너 중지

# (7) 전체 컨테이너 상태 확인
docker ps -a
# 실행 결과: my-nginx-vol -> Exited (0)
# 실행 결과: my-nginx -> Exited (0)
# 실행 결과: hello-world 컨테이너 -> Exited (0)
```
  
<img width="582" height="387" alt="image" src="https://github.com/user-attachments/assets/5ba6edfc-4aed-49e4-8367-6b343cbcf6f9" />
<img width="582" height="194" alt="image" src="https://github.com/user-attachments/assets/6b26e1b1-b8e3-4506-8739-383157ba20a6" />

<br><br>   
<img width="1568" height="655" alt="image" src="https://github.com/user-attachments/assets/b6617c48-d57a-4095-bcaf-79d4d488ee29" />
<img width="1568" height="1161" alt="image" src="https://github.com/user-attachments/assets/8de1591e-717e-4cc4-8462-68015baa6a23" />
<img width="1568" height="1052" alt="image" src="https://github.com/user-attachments/assets/b7afe40f-3965-4684-b116-6efa4c8c2b7c" />
<img width="1568" height="619" alt="image" src="https://github.com/user-attachments/assets/3cdcfd9d-0e28-4974-85c1-b3b0396b3a1c" />

<br><br>

# STEP 6. Git / GitHub 연동
* 버전 관리 & 팀 협업
<img width="533" height="466" alt="image" src="https://github.com/user-attachments/assets/b4459151-5bb9-475d-9635-ac924bb7cc60" />

### (1) Git 초기화 & 파일 등록
```bash
# Git 프로젝트 디렉터리로 이동
cd ~/my-docker-project

# Git 저장소 초기화
git init
# 실행 결과: 기존 Git 저장소 재초기화

# 현재 디렉터리의 모든 파일을 스테이징 영역에 추가
git add .

# Git 파일 상태 확인
git status
# 실행 결과: master 브랜치, 아직 커밋 없음
# Dockerfile, index.html 파일이 커밋 대기 상태로 등록됨

# Git 사용자 이메일 설정 (실제 이메일 주소 입력)
git config --global user.email "본인 이메일 주소"

# Git 사용자 이름 설정
git config --global user.name "minhwa"

# 변경 사항을 로컬 저장소에 커밋
git commit -m "first commit: Docker 웹서버 실습 완료"
# 실행 결과: 첫 번째 커밋 생성 (e9a03af)
# 2 files changed, 11 insertions(+)
# Dockerfile, index.html 파일 등록 완료

# GitHub 원격 저장소의 main 브랜치로 업로드
git push origin main

# 실행 과정: GitHub 사용자 이름 및 PAT 인증
# PAT는 비밀번호 입력란에 입력 (README에 토큰 기록 금지)

# 실행 결과: GitHub 원격 저장소로 업로드 완료
# To https://github.com/minhwa283/codyssey.git
# main -> main
```
<img width="658" height="185" alt="image" src="https://github.com/user-attachments/assets/d207f9fa-3ce1-4b5c-86d6-a2d984761b86" />
<img width="767" height="100" alt="image" src="https://github.com/user-attachments/assets/1b0c4792-c58a-4180-831b-3e34e5b32b32" />

### (2) GitHub 로그인 및 Personal Access Token(PAT) 입력
<img width="514" height="152" alt="image" src="https://github.com/user-attachments/assets/deec2166-0be4-448a-af47-a9ae9ff55c9b" />

### (3)GitHub push 완료 확인
<img width="688" height="301" alt="image" src="https://github.com/user-attachments/assets/d69a66ff-4983-4571-be7f-3003235f6232" />
<img width="728" height="287" alt="image" src="https://github.com/user-attachments/assets/025bb5e2-9dc1-41fc-a0bc-118fb89a5a1d" />

<br><br>  

# STEP 7. VSCode GitHub 연결
<img width="952" height="393" alt="image" src="https://github.com/user-attachments/assets/30c1e6e7-4ffc-47c6-bed0-736511889a75" />
<img width="956" height="623" alt="image" src="https://github.com/user-attachments/assets/304f3f26-64d8-4f8b-9efc-3fc4741474db" />



------
# ※ 트러블 슈팅
  ### 1. Docker 권한 문제  
* 문제:    docker 명령어 실행 시 "permission denied" 오류 발생  
* 원인 가설: 현재 사용자가 docker 그룹에 미포함  
* 확인:    sudo docker ps → 정상 작동 확인  
* 해결:    sudo usermod -aG docker $USER  
           newgrp docker (재로그인 없이 적용)
<br><br>

```bash
# (1) Docker 이미지 빌드 시도
docker build -t docker-mission .
# 실행 결과: permission denied 오류 발생
# 원인: Docker 소켓에 접근할 권한이 부족함

# (2) Docker 그룹 권한 설정
# 현재 사용자를 docker 그룹에 추가
sudo usermod -aG docker $USER
# 실행 결과: docker 그룹 추가 명령 실행

# (3) 권한 적용을 위한 패키지 설치
# newgrp 명령어 사용을 위한 util-linux-extra 설치
sudo apt install util-linux-extra
# 실행 결과: 패키지 설치 완료

# (4) Docker 그룹 권한 적용
newgrp docker
# 실행 결과: 오류 없이 새 셸 실행

# (5) Docker 이미지 빌드 재시도
docker build -t docker-mission .
# 이전 실습 화면에서 이미지 빌드 완료 확인
```
 
<img width="1494" height="87" alt="image" src="https://github.com/user-attachments/assets/1b5d628a-f784-42ac-93ae-e8a61d6392d7" />
<br>
<img width="339" height="584" alt="image" src="https://github.com/user-attachments/assets/3d2fabfb-e23e-4fc3-99fa-605f3011cf06" />
<br>
<img width="1568" height="1089" alt="image" src="https://github.com/user-attachments/assets/2d923ecd-d63b-4c1e-a7cf-2cc5ac3f3099" />
<br><br>

  ### 2. 서브모듈 문제  
* 문제:    docker-mission 폴더 클릭 시 404 오류 발생  
* 원인 가설: docker-mission 안에 .git 폴더가 남아있어서 GitHub가 폴더를 서브모듈로 인식  
* 확인:    폴더 아이콘에 화살표(→) 표시 확인  
* 해결:    git rm --cached docker-mission  
           git add docker-mission/  
           git commit & push  
<br><br>

```bash
# (1) GitHub 폴더 접근 오류 발생
# 실행 결과: 404 - page not found
# 원인: docker-mission 폴더 안에 .git 폴더가 있어
# GitHub에서 일반 폴더가 아닌 서브모듈로 인식함

# (2) 기존 서브모듈 등록 제거
cd ~/codyssey
git rm --cached docker-mission
# 실행 목적: Git 인덱스에서 서브모듈 등록 제거

# (3) 일반 폴더로 다시 등록
git add docker-mission/
# 실행 목적: docker-mission 폴더를 Git에 다시 추가

# (4) 변경 사항 커밋 및 GitHub 업로드
git commit -m "fix: docker-mission 서브모듈 해제"
git push origin main

# (5) 실행 결과 확인
# GitHub에서 docker-mission 폴더 정상 접근
# Dockerfile, index.html 파일 표시 확인
```

<img width="1568" height="493" alt="image" src="https://github.com/user-attachments/assets/82e0da5e-d1d7-4bdc-ac48-947f7dea5f98" />
<br>
<img width="323" height="493" alt="image" src="https://github.com/user-attachments/assets/aa9943dd-7eed-4fe8-be48-791928b488b9" />
<br>
<img width="1455" height="573" alt="image" src="https://github.com/user-attachments/assets/431c9a04-5911-4644-ba8a-e52e075210c8" />
<br><br>
    
        


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
