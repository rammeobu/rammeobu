Backend Developer
강원대학교 컴퓨터공학과 · Spring Boot / REST API / 서버 인프라
![GitHub](https://img.shields.io/badge/GitHub-rammeobu-181717?style=flat&logo=github)
---
소개
서버 쪽 작업 전반을 맡아왔습니다. API 설계, DB 모델링뿐 아니라 라즈베리파이로 직접 서버를 세팅하고
Cloudflare Tunnel, systemd 같은 걸로 배포까지 끝내는 일을 주로 했습니다. withact는 캡스톤으로 시작했지만
지금도 계속 유지보수하고 있고, 최근엔 AI 부트캠프·해커톤을 통해 RAG/LLM을 백엔드 로직에 붙이는 작업도
몇 번 해봤습니다.
---
기술 스택
Backend
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=swagger&logoColor=black)
Database
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat&logo=supabase&logoColor=white)
Infra / DevOps
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat&logo=raspberrypi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_Tunnel-F38020?style=flat&logo=cloudflare&logoColor=white)
![Linux](https://img.shields.io/badge/systemd/Linux-FCC624?style=flat&logo=linux&logoColor=black)
Crawling / Data
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
Frontend(협업)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
Auth
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![OAuth](https://img.shields.io/badge/OAuth-카카오·구글-EB5424?style=flat&logo=oauth&logoColor=white)
---
프로젝트
DevStep — AI 커리어 로드맵 플랫폼
`Next.js` `FastAPI` `Gemini API` `PostgreSQL + pgvector` `Celery` `Docker Compose` `Supabase`
KIT 바이브 코딩 대회 출품작 (3인 팀, 백엔드 담당). 대학생이 자기 포트폴리오를 넣으면 AI가 역량 격차를
분석해서 로드맵과 대외활동을 추천해주는 서비스입니다.
FastAPI로 Gemini API를 붙이고, 추천 매칭은 pgvector로 벡터 유사도 검색을 돌리는 식으로 구현했습니다.
로드맵 생성처럼 시간이 걸리는 작업은 Celery+Redis로 비동기 처리했고, 대외활동 크롤링·Supabase DB 구축,
토큰 기반 회원가입과 카카오/구글 소셜 로그인도 같이 맡았습니다. 배포는 Docker Compose로 프론트/AI 백엔드/DB/Redis를
한 번에 띄우는 구조로 짰습니다.
🔗 github.com/rammeobu/AI-LMS-Assistant
---
withact — 대외활동 탐색 & 팀원 모집 플랫폼
`Spring Boot` `JPA` `MariaDB` `Flutter` `Raspberry Pi 5` `Python/Playwright`
강원대 컴퓨터공학과 캡스톤 프로젝트로 시작해서 지금도 계속 손보고 있는 사이드 프로젝트입니다.
3인 팀에서 백엔드·DB·서버 인프라·배포를 혼자 맡았습니다.
Party / PartyRole / Application / AvailableTime / Notification / Member 등 도메인 CRUD API 전체 설계·구현
라즈베리파이 5에 직접 MariaDB 설치, Cloudflare Tunnel로 `backend.withact.xyz` 도메인 연결, systemd로 서비스 등록
새벽 3시마다 자동으로 도는 대외활동 크롤러(Python/Playwright)
Swagger로 API 문서화, GlobalExceptionHandler·DTO 패턴 적용
한 번은 `spring.jpa.hibernate.ddl-auto=update` 때문에 `loginId`(카멜케이스)와 `login_id`(스네이크케이스)
컬럼이 중복 생성되는 문제가 있었는데, 원인은 Hibernate가 두 네이밍 방식을 섞어서 인식한 거였고
`physical-strategy`를 명시적으로 지정해서 해결했습니다. ERD랑 아키텍처 다이어그램도 캡스톤 발표용으로
직접 그렸습니다.
🔗 github.com/rammeobu/withact_project
---
Met U — 예산 기반 AI 여행 플래너
`Flutter` `Next.js` `Spring Boot` `Supabase` `RAG/LLM`
강원대 여름 계절학기 AI 부트캠프에서 4인 팀으로 만들었고, 부트캠프 내에서 1등을 했습니다.
팀장 겸 백엔드/배포 담당이었습니다.
예산·인원·일정·스타일을 입력하면 항공/숙소 실측 데이터로 고정비를 먼저 계산하고, 남은 예산을
스타일 가중치에 따라 카테고리별로 나눠주는 서비스입니다. 단순히 LLM에 한 번 물어보고 끝내는 게 아니라
판별 → 검색(RAG) → 계산 → 검증 순서로 단계를 나눠서 설계했고, 배포는 팀원들이 로컬에서도 바로
접근할 수 있는 구조로 맞췄습니다.
🔗 github.com/rammeobu/metu
---
스마트팜 데이터 백엔드
`Raspberry Pi 4` `Mobius`
일경험 프로젝트로 진행한 스마트팜 데이터 백엔드입니다. 라즈베리파이 4로 서버를 구축하고 각종 센서 데이터를
수집해서 Mobius 플랫폼과 실시간으로 주고받도록 연동했습니다. 이 프로젝트로 수상했습니다.
---
Contact
GitHub: @rammeobu
