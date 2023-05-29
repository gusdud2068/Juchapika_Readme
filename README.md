# 주차삐카 Juchapika

<img src="./주차삐카 Juchapika ff0a0992375a4304b41db6558d93eb59/logo2.png" width="800px" height="400px">

### 프로젝트 소개

[개요] 불법주정차단속 로봇 (터틀봇)
[기간] 2023.04.10~2023.05.19 (7주)

[소속] SSAFY 8기 2학기 공통 프로젝트

### 기획의도

불법주정차량으로 인해 일어난 사고와 공무원의 인력부족/ 감정노동과 같은 어려움을 해결하고자 자율주행 기술을 활용한 로봇을 개발하였습니다

### **🛠️**기술스택 및 환경


## **Stacks**

BackEnd

FrontEnd

- Javascript
- React

Database

- Firebase

#### **Environment**

<div style='display:flex;margin-bottom:20px'>
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/VScode-007ACC?style=for-the-badge&logo=visualstudio&logoColor=white">
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/intelliJ-000000?style=for-the-badge&logo=intellijidea&logoColor=white">
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white">
<img  style="margin:0 5px 0 0"src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
</div>

#### **CI/CD**

<div style='display:flex;margin-bottom:20px'>
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white">
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white">
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/EC2-ff9900?style=for-the-badge&logo=amazonec2&logoColor=white">
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white">
<img style="margin:0 5px 0 0" src="https://img.shields.io/badge/docker-2496ed?style=for-the-badge&logo=docker&logoColor=white">

</div>


### **💻**사용기술

EMBEDDED

- AWS kinesis Video stream 실시간 비디오 스트리밍
    
    : 라즈베리 카메라로 촬영하는 영상을 실시간으로 외부서버로 송신
    
- 배터리 잔량 전송
    
    : Firebase/웹페이지와 ROS간의 통신으로 현재 배터리 잔량 값을 전송
    
- SLAM
    
    : 로봇의 LiDar센서와 SLAM을 통해 주변 장애물과 벽을 인식후 맵을 생성
    
    : 생성된 맵과 시각화 툴인 rviz를 통해 목표지점으로 자율주행 가능
    
## 프로젝트 파일 구조 ✔
### Backend
```
└── Supervision
    ├── SupervisionApplication.java
    ├── config
    ├── controller
    ├── dto
    │   ├── jwt
    │   ├── request
    │   └── response
    ├── entity
    │   ├── battery
    │   ├── car
    │   ├── record
    │   └── user
    ├── repository
    │   ├── car
    │   ├── record
    │   └── user
    ├── security
    └── service
        ├── car
        ├── fee
        ├── record
        └── user


### Frontend



├── Dockerfile
├── README.md
├── deploy_conf
│   └── nginx.conf
├── firebase.json
├── firestore.indexes.json
├── package-lock.json
├── package.json
├── public
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
├── src
│   ├── App.css
│   ├── App.js
│   ├── App.test.js
│   ├── ConfigOptions.ts
│   ├── Peer.ts
│   ├── components
│   │   ├── Nav
|   |   |---
│   │   └── Table
│   ├── constants.ts
│   ├── debug.ts
│   ├── firebase-config.js
│   ├── hooks
│   │   ├── index.ts
│   │   ├── useIceServers.spec.ts
│   │   ├── useIceServers.ts
│   │   ├── useLocalMedia.spec.ts
│   │   ├── useLocalMedia.ts
│   │   ├── useMaster.spec.ts
│   │   ├── useMaster.ts
│   │   ├── usePeerReducer.ts
│   │   ├── useSignalingChannelEndpoints.spec.ts
│   │   ├── useSignalingChannelEndpoints.ts
│   │   ├── useSignalingClient.spec.ts
│   │   ├── useSignalingClient.ts
│   │   ├── useViewer.spec.ts
│   │   └── useViewer.ts
│   ├── index.css
│   ├── index.js
│   ├── index.ts
│   ├── logger.ts
│   ├── logo.svg
│   ├── pages
│   │   ├── EnrollmentCar
│   │   ├── Fire.jsx
│   │   ├── FirstPage
│   │   ├── ForPerson
│   │   ├── LiveStream
│   │   ├── Main.jsx
│   │   ├── Main.module.css
│   │   └── VideoStorage
│   ├── reportWebVitals.js
│   ├── rollup.config.js
│   ├── setupTests.js
│   ├── tsconfig.json
│   ├── tslint.json
│   ├── useViewer.jsx
│   └── withErrorLog.ts
├── webpack.config.js
├── webpack.debug.config.js
├── webpack.dev.config.js
└── webpack.dist.config.js
```
<br/>
<br/>
<br/>
<br/>

## 아키텍처 설계도

![아키텍처 설계도](/%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/Architecture.PNG)
<br>

## 사이트맵

![사이트 맵](/%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/SiteMap.PNG)

<br/>
<br/>
<br/>
<br/>

## 시스템 기술서

## 1. 프로젝트 핵심 기술
- Spring Web
- Spring Secutiry + JWT
- Spring Data JPA
- Let’s Encrypt
- Lombok
- MySQL MariaDB
- AWS (EC2)
- Jenkins

<br/>

## 2. 핵심 기술 소개

### 2-1. Spring Data JPA (+ QureyDsl)

<br/>

ORM(Object Relational Mapping) 기술을 기반하는 JPA를 활용하여 객체와 테이블을 매핑하였습니다. 추가적으로 동적 쿼리문를 통한 유연한 쿼리문을 생성하기 위해서 QueryDsl을 활용하였습니다. 또한, Pagable 을 이용하여 무한 스크롤을 구현하였습니다.

<br/>

### 2-2. Spring Security (+ JWT)

<br/>

사용자가 로그인을 하게 되면, 서버는 JWT 토큰을 생성하고 클라이언트에게 반환합니다. 클라이언트는 이 JWT 토큰을 저장하고, 서버에 요청할 때마다 헤더에 포함하여 서버에 전송합니다. 서버는 JWT 토큰을 검증하여 사용자를 인증하고, 필요한 권한을 확인하여 해당 작업을 수행합니다. 

이 JWT 토큰은 클라이언트가 자원 서버에 접근할 때 Access Token으로 사용합니다. 자원 서버는 Access Token을 검증하여 클라이언트의 권한을 확인하고, 요청을 처리할 수 있습니다.

<br/>

### 2-3. YOLOv5(객체 탐지 알고리즘) 를 활용한 번호판 인식

<br/>

실시간으로 촬영되는 영상을 프레임별로 나누어 YOLOv5를 활용하여 번호판을 인식했습니다. (학습 모델: https://github.com/gyupro/EasyKoreanLpDetector/blob/main/lp_det.pt) 한국어를 포함한 글자를 추출하기 위해 EasyOCR(문자 영역 인식(Detection) + 문자 인식(Recognition)기능을 모두 하는 프레임워크)을 사용했고, 인식률이 80% 이상인 번호판의 번호를 추출하였습니다.

<br/>

![SYS3](/%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/detecting.PNG)

<br/>

### 2-4. AWS Kinesis 실시간 비디오 스트리밍

<br/>

TurtleBot에서 촬영하는 영상을 분석 및 스트리밍을 위해서, 실시간 데이터 스트리밍을 처리하는 데 중점을 둔 완전 관리형 서비스 AWS Kinesis를 사용하였습니다. (참고 문헌: https://www.smarthome-diy.info/blog/developper/smarthome/2020/10/2417/)


<br/>
<br/>
<br/>
<br/>

### **📋**API명세서

![API.png](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/API.png)

### **✔️ ERD**

![ERD.PNG](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/ERD.png)

### **✔️와이어프레임**

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/Untitled.png)

### **✔️**주요기능소개

**1️⃣ 메인페이지**

1. **날짜별 + 구/동 지역별 불법주정차차량 조회 리스트**

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/Untitled%201.png)

1. 엑셀 파일 다운

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/Untitled%202.png)

1. 통계

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/Untitled%203.png)

1. 검색창기능
    
![ezgif.com-video-to-gif.gif](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/ezgif.com-video-to-gif.gif)
    

**2️⃣ 차량등록페이지**

1. 불법차량등록전 확인/수정
    
    ![ezgif.com-video-to-gif (2).gif](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/ezgif.com-video-to-gif_(2).gif)
    
2. 고지서 보내기전 확인용 ( 납세자의 상세정보 및 납부이력 )
    
    ![ezgif.com-video-to-gif (1).gif](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/ezgif.com-video-to-gif_(1).gif)
    
3. 납세자 문자메세지 전송 / 삭제
    
    ![ezgif.com-video-to-gif (1).gif](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/ezgif.com-video-to-gif_(1)%201.gif)
    

  ****

※ **납세자 문자**

**(고지서 링크 첨부: 납세자의 상세고지서내용 및 납부이력 확인용/**~~개인정보 유출 방지 암호화 구현~~ **)**

![message.png](/%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/message.png)

![ezgif.com-video-to-gif (1).gif](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/ezgif.com-video-to-gif_(1)%202.gif)

**3️⃣ 실시간화면**
<br>
실시간 화면 송출

![detecting.gif](/%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/detecting.gif)
<br>
번호판 인식

![live.gif](/%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%E1%84%88%E1%85%B5%E1%84%8F%E1%85%A1%20Juchapika%20ff0a0992375a4304b41db6558d93eb59/live.gif)

<br>
<br>

> **JIRA Convention**
> 

- **에픽**
    - 큰 단위의 업무(여러 User Story, Task 등을 묶은 단위)
    - **생성 Convention**
        - Epic을 생성할 때 파트를 적어준다.
        - ex) BE 개발, FE 개발
- **스토리**
    - 해당 Epic의 하위 단위 작업으로 직접적인 개발과 기능 구현을 기본으로 한다.
    - User Story의 크기는 sprint내에 완료 가능한 단위로 분할 필요
    - **생성 Convention**
        - ex) 로그인 기능
            - 로그인 기능 개발
            - UI/UX 구현
            - 합의 알고리즘 구현
- **부작업**
    - Story, Task를 더 작은 단위로 나눈 업무
    - **생성 Convention**
        - 작업을 직관적으로 알 수 있도록 작성
        - ex) 자동 로그인 기능 구현
- **작업**

<br/>
<br/>
<br/>
<br/>


## 팀원 소개


| [BE 이원석👑] | [BE 정우영] | [FE 박현영] | [EB 김상래] | [EB 이영도] | [EB 이준호] |

<br/>
<br/>