<div align="center">

# 🌉 SilverBridge · CareAI

**혼자 사는 어르신의 안전 · 건강 · 마음을 AI가 곁에서 돌봅니다**

AI 기반 독거노인 통합 케어 플랫폼 - 동양미래대학교 캡스톤디자인

[![Service](https://img.shields.io/badge/서비스_체험-devdmu.gosky.kr-B7472A?style=for-the-badge)](https://devdmu.gosky.kr)
[![YouTube](https://img.shields.io/badge/YouTube-시연_영상-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=mdapIXzJaoo)
[![PDF](https://img.shields.io/badge/브로셔-PDF-EC1C24?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](docs/실버브릿지_브로셔.pdf)

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_4-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

</div>

---

## 📑 목차

1. [💡 프로젝트 소개](#-1-프로젝트-소개)
2. [✨ 핵심 기능](#-2-핵심-기능)
3. [📱 실제 화면](#-3-실제-화면)
4. [📊 AI 성과](#-4-ai-성과)
5. [🏗️ 시스템 구성](#️-5-시스템-구성)
6. [🧰 기술 스택](#-6-기술-스택)
7. [🚧 한계](#-7-한계)
8. [👥 팀 구성](#-8-팀-구성)
9. [🎬 시연 영상 · 발표 자료](#-9-시연-영상--발표-자료)
10. [📦 저장소](#-10-저장소)

---

## 💡 1. 프로젝트 소개

> **여러분은 부모님의 위험한 순간을 제때 알아차릴 수 있다고 확신하십니까?**

CareAI는 혼자 사는 어르신을 위한 **AI 통합 케어 플랫폼**입니다.
집 안 카메라 영상에서 AI가 화재 · 흉기 · 낙상을 찾아 가족에게 바로 알리고,
AI 의료 챗봇이 증상 상담부터 병원 예약까지 돕고, AI가 하루 다섯 번 먼저 안부를 물어 기분을 살핍니다.

### ❓ 왜 필요한가

| 수치 | 내용 |
| :---: | --- |
| 👵 **40%** | 2050년 시니어 인구 비중 - 대한민국 인구 10명 중 4명, 약 1,900만 명 |
| 🧠 **52.6%** | 혼자 사는 어르신의 치매 유병률 - 2인 가구(33.7%)보다 1.6배 |
| 🏠 **90.6%** | 고독사가 집 안에서 일어난 비율 - 2023년 3,661건, 매년 최고치 |

<sub>출처: 국가데이터처(KOSIS 국가통계포털) · 보건복지부 고독사 실태조사</sub>

---

## ✨ 2. 핵심 기능

| 영역 | 기능 | 내용 |
| :---: | --- | --- |
| 🛡️ **안전** | 🚨 AI 이상 감지 | 카메라 영상에서 화재 · 흉기 · 낙상을 찾아 보호자에게 바로 알림 |
| | 🆘 긴급 SOS | 버튼 한 번으로 가족에게 알림, 119 화면 바로 열기 |
| 💊 **건강** | 🩺 AI 의료 챗봇 | 증상 상담 → 진료과 안내 → 병원 예약까지 한 번에 |
| | 💊 복약 관리 | 약 봉투 사진 한 장으로 등록, 먹을 시간에 알림 |
| 💛 **마음** | 😊 AI 기분체크 | AI가 먼저 안부를 묻고 대화 · 표정으로 기분 분석 |
| | 🧩 치매 예방 게임 | 짝 맞추기 · 미로 찾기 · 사칙연산 · 초성 퀴즈 4종 |
| 🛠️ **운영** | 🖥️ 관리자 | 회원 · 병원 · AI 상태 · 통계를 웹 화면 하나에서 관리 |

---

## 📱 3. 실제 화면

> 어르신은 iPad(태블릿 웹), 보호자는 휴대폰 웹, 관리자는 PC 웹으로 사용합니다. 아래는 실제 서버에서 캡쳐한 화면입니다.

### 🚨 3.1 AI 이상 감지

**집에 있는 기기를 카메라로 등록하면, AI가 지켜보기 시작합니다.**

![카메라 등록](./images/camera-register.png)

**AI가 위험으로 판정하면, 보호자 휴대폰에 바로 알림이 옵니다.**

- 카메라 영상을 초당 15장씩 분석해 화재 · 흉기 · 낙상을 찾습니다. 낙상은 6초 이상 쓰러져 있을 때 위험으로 봅니다.
- 위험하면 5초 영상을 저장하고, 10분 안의 같은 감지는 1건으로 묶어 알림이 쏟아지지 않게 합니다.
- 보호자가 "실제 상황 / 오탐"으로 답하면 그 판정이 AI 오탐률 통계로 쌓입니다.

![이상 감지 알림](./images/anomaly-alert.png)

### 🔔 3.2 알림 채널

**앱 푸시는 늘 보내고, 카카오 알림톡 · 문자 · 이메일은 보호자가 켠 대로 함께 보냅니다.**

![알림 채널](./images/alert-channels.png)

### 🆘 3.3 긴급 SOS

**SOS 버튼도, 가족 전화도 누르는 즉시 보호자에게 알림이 가고 이력에 남습니다.**

- 실수로 눌러도 한 번 더 확인하고, 보낸 뒤에는 119 번호가 입력된 화면을 바로 엽니다(전화를 자동으로 걸지는 않습니다).
- 앱 푸시가 닿지 않으면 문자로 대신 보냅니다.

![긴급 SOS](./images/sos.png)

### 🩺 3.4 AI 의료 챗봇

**어르신은 버튼으로 답하며 진료과 안내를 받고, 보호자도 같은 챗봇으로 상담합니다.**

![챗봇 상담](./images/chatbot-consult.png)

**위험한 말이 나오면 상담 대신 119 · 109 버튼을 바로 띄웁니다.**

![챗봇 119 · 109](./images/chatbot-emergency.png)

**챗봇으로 예약하면, 보호자 화면에 '병원 가는 날'로 바로 보입니다.** (제휴 병원 46곳)

![챗봇 병원 예약](./images/chatbot-reservation.png)

### 💊 3.5 복약 관리

**먹을 시간에 알려 주고, 체크하지 않으면 보호자가 압니다.**

- 보호자가 약 봉투를 사진 한 장으로 찍으면 AI가 약 이름 · 복용 시간을 읽고, 허가 약 목록과 대조해 비슷한 글자를 바로잡습니다.

![복약 관리](./images/medication.png)

### 😊 3.6 AI 기분체크

**AI가 먼저 안부를 묻고, 보호자는 기분을 날짜별로 봅니다.**

- 하루 다섯 번(9 · 12 · 15 · 18 · 21시) AI가 먼저 말을 겁니다.
- 어르신의 말을 받아쓰고(Whisper), 말 내용으로 기분을 판단하며(EXAONE 기분 모델) 표정 분석(HSEmotion)은 보조로 씁니다.
- 위험 신호가 보이면 보호자에게 알립니다.

![AI 기분체크](./images/mood-check.png)

### 🧩 3.7 치매 예방 게임

**어르신이 직접 고르고 바로 즐기는 인지 훈련 게임 4종, 기록은 보호자 화면에 쌓입니다.**

![치매 예방 게임](./images/brain-game.png)

### 🖥️ 3.8 관리자

**회원 · AI 상태 · 통계를 웹 화면 하나에서 봅니다.** 변경 조작은 모두 감사 로그로 남고, 영상 · 대화 내용은 관리자도 볼 수 없습니다.

![관리자](./images/admin.png)

---

## 📊 4. AI 성과

### 🚨 4.1 AI 이상 감지

여러 차례 다시 학습하며, 실제 영상에서 더 잘 찾는 모델만 골라 배포했습니다.

| 위험 | 모델 | 탐지율 | 오탐률 | 학습 데이터 |
| --- | :---: | :---: | :---: | --- |
| 🔥 화재 | YOLO26 nano | **83.3%** | 10% | 사진 6.5만 장 · 영상 2,500개 |
| 🔪 흉기 | YOLO26 medium | **89.8%** | 10% | 사진 6만 장 · 영상 74개 |
| 🧍 낙상 | YOLO26 nano | **75.7%** | 8.5% | 사진 14만 장 · 영상 4.8만 개 |

<sub>낙상은 오탐(앉기 · 눕기를 낙상으로 착각)을 38.7%에서 8.5%로 줄이는 쪽을 택해, 탐지율이 92.6%에서 75.7%로 낮아졌습니다.</sub>

**🧮 이 %는 이렇게 계산했습니다** - 학습에 쓰지 않은 실제 영상으로 시험했습니다.

| 위험 | 탐지율 = 잡은 수 ÷ 위험 영상 | 오탐률 = 잘못 울린 수 ÷ 위험 없는 영상 |
| --- | --- | --- |
| 🔥 화재 | 불이 난 영상 24개 중 20개 → **83.3%** | 불 없는 영상 10개 중 1개 → **10%** |
| 🔪 흉기 | 주거 CCTV 흉기 장면 2,212개 중 1,987개 → **89.8%** | 부엌 요리 칼 영상 597개 중 60개 → **10%** |
| 🧍 낙상 | 낙상 영상 140개 중 106개 → **75.7%** | 넘어짐 없는 영상 82개 중 7개 → **8.5%** |

**📚 학습 데이터 출처**

| 위험 | 출처 |
| --- | --- |
| 🔥 화재 | ![AI Hub](https://img.shields.io/badge/AI_Hub-0064FF?style=flat-square) ![Science Data Bank](https://img.shields.io/badge/Science_Data_Bank-1F6FB2?style=flat-square) ![Roboflow](https://img.shields.io/badge/Roboflow-6706CE?style=flat-square&logo=roboflow&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![Zenodo](https://img.shields.io/badge/Zenodo-1682D4?style=flat-square&logo=zenodo&logoColor=white) ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat-square&logo=kaggle&logoColor=white) ![계명대학교](https://img.shields.io/badge/계명대학교-003876?style=flat-square) |
| 🔪 흉기 | ![AI Hub](https://img.shields.io/badge/AI_Hub-0064FF?style=flat-square) ![Roboflow](https://img.shields.io/badge/Roboflow-6706CE?style=flat-square&logo=roboflow&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![LVIS](https://img.shields.io/badge/LVIS-4A5568?style=flat-square) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) |
| 🧍 낙상 | ![AI Hub](https://img.shields.io/badge/AI_Hub-0064FF?style=flat-square) ![ETRI](https://img.shields.io/badge/ETRI-00A0E9?style=flat-square) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![Harvard Dataverse](https://img.shields.io/badge/Harvard_Dataverse-A51C30?style=flat-square) ![Toyota Smarthome](https://img.shields.io/badge/Toyota_Smarthome-EB0A1E?style=flat-square&logo=toyota&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![Open Images](https://img.shields.io/badge/Open_Images-4285F4?style=flat-square&logo=google&logoColor=white) |

### 🩺 4.2 AI 의료 챗봇

AI에게 주는 **지시문(프롬프트)을 두 갈래로 고쳤습니다.**
질문을 나누는 AI(Claude)는 응급 · 자해 판단을, 답을 쓰는 의료 AI(MedGemma)는 일반 증상 답을 맡습니다.

![지시문 개선](./images/prompt-rules.png)

| ① Claude 지시문에 더한 규칙 | ② MedGemma 지시문에 더한 규칙 |
| --- | --- |
| ➕ **응급** - 즉시 119가 필요한 신호가 있으면 응급으로 판단 | ➕ **119** - 숨참 · 가슴 통증 같은 위험 신호가 있을 때만 |
| ➕ **자해** - 자해 생각이 보이면 위기로, 화제가 바뀌면 평소 대화로 | ➕ **진료 기준** - 언제 꼭 진료받을지 기준 하나 (기간 · 수치 · 함께 생긴 증상) |
| ➕ **심정지** - 반응이 없고 숨을 쉬지 않으면 심정지 의심으로 | ➕ **약 질문** - 단정하지 말고, 조심할 이유 + 약사 · 의사에게 확인할 것 |
| ➕ **오늘 진료** - 오늘 진료가 필요한 질환은 따로 표시 | ➕ **예시** - 예시 문장을 그대로 쓰지 말고 지금 질문에 맞게 새로 |

<sub>규칙은 실제 지시문을 줄여 적은 것입니다.</sub>

**📈 고친 뒤 결과**

| 확인한 것 | 처음 | 지금 |
| --- | :---: | :---: |
| 🚑 응급 질문에 119를 안내하나요? | 63% (19/30) | **100%** (37/37) |
| ❤️‍🩹 숨을 안 쉬는 상황에 가슴압박 · AED를 안내하나요? | 0% (0/24) | **100%** (30/30) |
| 🏥 병원에 갈 기준을 알려 주나요? | 38% (18/48) | **88%** (42/48) |
| 🔕 필요 없는데 119를 말하나요? (낮을수록 좋음) | 46% (21/46) | **4%** (3/77) |

**📚 검증 문항 근거** &nbsp;
![질병관리청](https://img.shields.io/badge/질병관리청-0B4EA2?style=flat-square)
![2025 응급처치 가이드라인](https://img.shields.io/badge/2025_응급처치_가이드라인-D32F2F?style=flat-square)
![국가건강정보포털](https://img.shields.io/badge/국가건강정보포털-2E7D32?style=flat-square)

<sub>위 근거로 만든 어르신 건강 질문 597문항으로 채점했습니다. 응급 · 자해 안내는 응급 낱말 규칙과 함께 동작합니다.</sub>

### 😊 4.3 AI 기분체크

| 확인한 것 | 처음 | 지금 |
| --- | :---: | :---: |
| 🎙️ 어르신 말을 틀리게 받아쓰나요? (글자 오류율, 낮을수록 좋음) | 14.8% | **2.4%** |
| ⚠️ 돌려 말한 자살 신호를 찾나요? (40문장) | 14% | **93%** |
| 💬 대답만 듣고 기분을 맞히나요? (800문장) | 75.4% | **83.8%** |
| 🔕 안전한 날에 알림이 잘못 울리나요? (27명 × 7일, 낮을수록 좋음) | 33% | **4%** |

**📚 검증 자료** &nbsp;
![AI Hub 어르신 대화 음성](https://img.shields.io/badge/AI_Hub-어르신_대화_음성-0064FF?style=flat-square)
![AI Hub 감성대화](https://img.shields.io/badge/AI_Hub-감성대화-0064FF?style=flat-square)
![NAVER CareCall](https://img.shields.io/badge/NAVER-CareCall_안부_전화-03C75A?style=flat-square&logo=naver&logoColor=white)

### ✅ 4.4 AI 성능 검증 방법

근거와 출처가 있는 자료로, **"이렇게 시험하고 → 이러면 정답"** 으로 채점했습니다.

![AI 성능 검증](./images/verification.png)

| | 🚨 AI 이상 감지 | 🩺 AI 의료 챗봇 | 😊 AI 기분체크 |
| --- | --- | --- | --- |
| **근거 자료** | 계명대학교 화재 영상 · ETRI 부엌 칼 사용 영상 · CCTV · 어르신 낙상 영상 | 질병관리청 · 2025 응급처치 가이드라인 · 국가건강정보포털 | AI Hub 어르신 대화 음성 · AI Hub 감성대화 · 네이버 CareCall 안부 전화 |
| **① 이렇게 시험** | 불이 난 영상 24개를 AI에게 보여 주고 | "가슴이 쪼이고 식은땀이 나요" 같은 질문 597개를 묻고 | "자식들한테 짐이 되기 싫어" 같은 말을 들려주고 |
| **② 이러면 정답** | 불을 찾아 알리면 정답 (24개 중 20개 → 83.3%) | 119를 안내하면 정답 | 위험 신호로 알리면 정답 |
| **검수** | 학습에 쓰지 않은 영상만 사용 | 팀원 2명이 문항 검수 | 팀원 2명이 정답 검수 |

---

## 🏗️ 5. 시스템 구성

어르신 · 보호자 · 관리자 화면이 하나의 서버로 이어집니다.

![시스템 구성](./images/architecture.png)

| 서버 | 역할 | 사양 |
| --- | --- | --- |
| 🚀 운영 · AI 서버 | 서비스 운영 · AI 추론 (Docker) | Ryzen 5 7500F · RTX 4070 SUPER 12GB · RAM 32GB · Ubuntu 22.04 |
| 🧪 개발 서버 | 개발 · 검증 | HPE ProLiant DL360 Gen10 · Xeon Silver 4112 · RAM 62GB · Rocky Linux 9.7 |
| 🧠 AI 학습 서버 | 모델 학습 → 운영 서버에 배포 | NVIDIA DGX Spark · GB10 · 128GB 통합 메모리 · Ubuntu 24.04 |

---

## 🧰 6. 기술 스택

| 분류 | 기술 |
| --- | --- |
| 🎨 **Frontend** | ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white) |
| ⚙️ **Backend** | ![Java 21](https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot 4](https://img.shields.io/badge/Spring_Boot_4-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![JPA](https://img.shields.io/badge/JPA_·_Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white) ![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white) ![WebSocket](https://img.shields.io/badge/WebSocket_·_STOMP-010101?style=flat-square) ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) ![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) |
| 🤖 **AI** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![YOLO26](https://img.shields.io/badge/YOLO26-111F68?style=flat-square) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![MedGemma](https://img.shields.io/badge/MedGemma-4285F4?style=flat-square&logo=google&logoColor=white) ![EXAONE](https://img.shields.io/badge/EXAONE-A50034?style=flat-square&logo=lg&logoColor=white) ![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat-square) ![HSEmotion](https://img.shields.io/badge/HSEmotion-FF7043?style=flat-square) ![Claude API](https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white) ![Gemini TTS](https://img.shields.io/badge/Gemini_TTS-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) |
| 🗄️ **Database** | ![PostgreSQL 17](https://img.shields.io/badge/PostgreSQL_17-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) |
| 🔔 **Notification** | ![Firebase FCM](https://img.shields.io/badge/Firebase_FCM-DD2C00?style=flat-square&logo=firebase&logoColor=white) ![Solapi](https://img.shields.io/badge/Solapi_문자_·_알림톡-3B82F6?style=flat-square) ![SMTP](https://img.shields.io/badge/SMTP_이메일-EA4335?style=flat-square&logo=gmail&logoColor=white) ![Kakao](https://img.shields.io/badge/카카오_로그인-FFCD00?style=flat-square&logo=kakaotalk&logoColor=black) |
| 🐳 **DevOps** | ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![NVIDIA DGX Spark](https://img.shields.io/badge/NVIDIA_DGX_Spark-76B900?style=flat-square&logo=nvidia&logoColor=white) |

---

## 🚧 7. 한계

학생 프로젝트로는 넘기 어려웠던 한계 3가지입니다.

<table>
<tr>
<th width="33%">🖥️ 서버 하드웨어</th>
<th width="33%">🏥 병원 시스템 연동</th>
<th width="33%">🩺 전문가 검증</th>
</tr>
<tr valign="top">
<td>

**GPU 1장(12GB)을 AI 3개가 나눠 씀**

- 이상 감지 · 의료 AI · AI 기분체크가 한 장을 공유
- 카메라는 전체 3대까지
- 의료 AI 답은 약 11초, 동시에 물으면 뒷사람이 대기

</td>
<td>

**병원 46곳 · 가상 데이터**

- 실제 병원 예약과 연결되지 않음
- 예약은 우리 서비스에만 저장
- 실제 진료 시간 · 휴진일과 다를 수 있음

</td>
<td>

**의사 검토 0건**

- 팀원이 각자 100문항씩 검수
- 정답 기준은 공식 자료(질병관리청 등)로
- 검수로 찾은 13곳은 직접 고침

</td>
</tr>
<tr valign="top">
<td>

**왜** 장비를 늘릴 수 없어 서버 한 대로 운영

</td>
<td>

**왜** 병원 전산(EMR) 연동은 계약 · 허가가 필요

</td>
<td>

**왜** 의료진 검토는 병원 · 기관 협력이 필요

</td>
</tr>
</table>

---

## 👥 8. 팀 구성

🎓 동양미래대학교 · 지도교수 **이희진** 교수님

#### 👑 이하늘 &nbsp;`팀장` `PM` `인프라`

- 프로젝트 기획 · 일정 관리, 서버 인프라(Docker · Nginx 도메인, dev · prod 분리)
- 병원 예약 서비스(NestJS · Prisma, 병원 관리 화면, 예약 연동 브리지)
- AI 서버 기본 구조(FastAPI), MedGemma 의료 챗봇 서버, 챗봇 예약 연동
- 치매 예방 게임(게임 API · 게임 화면 · 보호자 게임 관리)

#### ⚙️ 남궁명진 &nbsp;`백엔드` `AI 개선`

- Spring Boot 백엔드 전반 - 인증(JWT · 카카오), 보호자 연결, SOS, 이상 감지 판정 · 알림, 복약, 관리자, WebSocket
- 알림 채널 연동(FCM 웹 푸시 · Solapi 문자 · 알림톡 · 이메일)
- AI 의료 챗봇 개선 - 응급 · 자해 판단, 지시문(프롬프트) 개선, 근거 있는 시험지
- 이상 감지 모델 재학습(DGX Spark), AI 기분체크 성능 개선, 실제 화면 E2E QA 자동화

#### 🤖 이재희 &nbsp;`AI 엔지니어`

- 초기 AI 서버 - 화재 · 연기 · 흉기 · 낙상 통합 감지기
- AI 기분체크(말벗 · 정서 분석) AI 서버 구현 - 대화, 받아쓰기, 기분 판정, 위험 신호 판정
- EXAONE 감정 분석과 표정 결합 판정, 평가 세트 · 채점기

#### 🎨 이윤아 &nbsp;`프론트엔드`

- Next.js 화면 전반 - 회원가입 · 로그인(카카오), 보호자 · 피보호자 · 관리자 화면
- 이상 감지 모니터링 · 카메라 화면, 보호자 연결 관리, SOS 흐름
- 화면 디자인 정리(CareAI 디자인 통일), 서비스 · 훅 구조 정리

---

## 🎬 9. 시연 영상 · 발표 자료

### ▶️ 시연 영상

**🆕 CareAI v2 시연 영상 (4분 47초)** - 재생 버튼을 누르면 바로 볼 수 있습니다.

https://github.com/user-attachments/assets/8ff00f4b-a7fb-4111-b036-1b9f94667594

<sub>🎞️ 고화질(1080p) 영상은 [여기](videos/CareAI_v2_시연영상.mp4)에서 내려받을 수 있습니다.</sub>

**📺 YouTube 시연 영상**

[![CareAI 시연 영상](https://img.youtube.com/vi/mdapIXzJaoo/maxresdefault.jpg)](https://www.youtube.com/watch?v=mdapIXzJaoo)

<sub>그림을 누르면 YouTube로 이동합니다.</sub>

| AI 이상 감지 테스트 (실제 가정 환경 촬영) | |
| --- | --- |
| [🔪 흉기 감지 테스트](videos/흉기감지_테스트.mp4) | [🧍 낙상 감지 테스트](videos/낙상감지_테스트.mp4) |

### 📂 발표 자료

| 구분 | 파일 |
| --- | --- |
| 📰 프로젝트 브로셔 | [![PDF](https://img.shields.io/badge/PDF-EC1C24?style=flat-square&logo=adobeacrobatreader&logoColor=white)](docs/실버브릿지_브로셔.pdf) |
| 📝 1학기 중간발표 (프로젝트 제안서) | [![PPT](https://img.shields.io/badge/PPT-B7472A?style=flat-square&logo=microsoftpowerpoint&logoColor=white)](docs/실버브릿지_중간발표.pptx) |
| 🏁 1학기 최종발표 | [![PPT](https://img.shields.io/badge/PPT-B7472A?style=flat-square&logo=microsoftpowerpoint&logoColor=white)](docs/실버브릿지_최종발표.pptx) |
| 🗓️ 2학기 프로젝트 계획서 | [![PPT](https://img.shields.io/badge/PPT-B7472A?style=flat-square&logo=microsoftpowerpoint&logoColor=white)](docs/실버브릿지_2학기_프로젝트계획서.pptx) |
| 📈 2학기 중간평가 | [![PPT](https://img.shields.io/badge/PPT-B7472A?style=flat-square&logo=microsoftpowerpoint&logoColor=white)](https://download.gosky.kr/d/SilverBridgeSky/%EC%8B%A4%EB%B2%84%EB%B8%8C%EB%A6%BF%EC%A7%80_2%ED%95%99%EA%B8%B0_%EC%A4%91%EA%B0%84%ED%8F%89%EA%B0%80.pptx) |

---

## 📦 10. 저장소

| 저장소 | 설명 |
| --- | --- |
| 🎨 [SilverBridgeFe](https://github.com/Dongyang-Mirae-University-software/SilverBridgeFe) | 프론트엔드 (Next.js) |
| ⚙️ [SilverBridgeBe](https://github.com/Dongyang-Mirae-University-software/SilverBridgeBe) | 백엔드 (Spring Boot 4) |
| 🤖 [SilverBridgeAiServer](https://github.com/Dongyang-Mirae-University-software/SilverBridgeAiServer) | AI 서버 (이상 감지 · 의료 챗봇 · AI 기분체크 · 게임) |
| 🏥 [SilverBridgeReservation](https://github.com/Dongyang-Mirae-University-software/SilverBridgeReservation) | 병원 예약 서비스 (NestJS) |
| 🎯 [AiSilverBridgeSky](https://github.com/Dongyang-Mirae-University-software/AiSilverBridgeSky) | YOLO 이상 감지 모델 학습 · 추론 |
| 🩺 [ChatSilverBridge](https://github.com/Dongyang-Mirae-University-software/ChatSilverBridge) | MedGemma 의료 챗봇 서버 |
| ✅ [SilverBridgeQA](https://github.com/Dongyang-Mirae-University-software/SilverBridgeQA) | 실제 화면 E2E QA 자동화 (Playwright) |
| 🧪 [SilverBridgeAi](https://github.com/Dongyang-Mirae-University-software/SilverBridgeAi) | AI 서버 (초기 버전) |
