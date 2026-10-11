<div align="center">

# 권용현 · Yonghyun Kwon

### 오류가 실행되기 전에 막는 백엔드 개발자

원인은 측정으로 찾고, 해결은 재발하지 않는 구조로 남깁니다.

<a href="https://kwonyonghyun.vercel.app"><img src="https://img.shields.io/badge/Portfolio-0F172A?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"/></a>
<a href="https://github.com/kwonyonghyun"><img src="https://img.shields.io/badge/이전_계정-kwonyonghyun-181717?style=for-the-badge&logo=github&logoColor=white" alt="kwonyonghyun"/></a>

</div>

<br/>

## 👋 About

- **측정으로 원인을 찾습니다.** 응답이 느려지면 로그부터 요청 유형별로 집계하고, 병목이 드러난 곳만 고칩니다.
- **재발하지 않는 구조로 남깁니다.** 한 번 해결한 문제는 규칙과 테스트로 고정해, 같은 문제가 운영 환경에 다시 나가지 않게 합니다.
- **실행 전에 막습니다.** 되돌리기 어려운 동작 앞에는 검사와 승인 단계를 둡니다.

<br/>

## 🛠 Tech Stack

<p>
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/>
<img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white"/>
</p>
<p>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/>
</p>

<br/>

## 🚀 Featured Projects

### Modulo · 맞춤형 이력서 서비스 백엔드
> Java · Spring Boot · Spring Security(JWT) · JPA · MySQL · Redis · Docker · GitHub Actions · AWS EC2

경험을 모듈로 한 번만 저장하고, 이력서에는 모듈의 순서와 배치만 저장하는 이력서 서비스의 백엔드를 설계부터 운영까지 맡았습니다.

| 문제 | 해결 | 결과 |
|---|---|---|
| 운영 중 응답 지연 | 로그 집계로 조회 요청 95% 확인, 조회 경로에 Redis 캐시 적용 | 평균 응답 **300ms → 39ms** (캐시 적중률 94%) |
| 접속 기록 동기 저장으로 Connection Pool 고갈 | Redis Set에 모아 하루 한 번 저장하는 Write-Back으로 전환 | 초당 처리량 **200 → 1,200** (6배) |
| N+1 쿼리 | 쿼리 분리 후 쿼리 수를 테스트로 검증, 테스트 통과 시에만 배포 | 같은 문제가 운영에 다시 나가지 않는 구조 |

🔗 [kwonyonghyun/Modulo_be](https://github.com/kwonyonghyun/Modulo_be)

---

### Filient · AI 파일 자동 정리 서비스 서버 (소프트웨어 마에스트로 16기)
> Python · FastAPI · LangChain · Chroma · AWS Bedrock(Claude) · Redis · Docker · GitHub Actions

사용자가 문장으로 쓴 파일 정리 방식을 실행 가능한 규칙으로 바꾸는 AI 서버를 맡았습니다.

- 파일은 기기에 두고 **문장만 서버로 받는 구조**로 개인 파일이 서버를 거치지 않게 설계
- 실제 파일이 옮겨지기 전 **미리보기와 사용자 승인** 단계 배치
- 정답을 정한 평가 데이터로 실패를 유형별로 분류해 **규칙 정합률 88%**로 출시
- 출시 후 **디스콰이엇 주간 프로덕트 1위**

🔗 [BlueGreenSWM/Filient_Server_2](https://github.com/BlueGreenSWM/Filient_Server_2)

---

### Tunely · 자연어 데이터 조회 콘솔
> TypeScript · Next.js · Anthropic SDK(Claude) · Supabase · SSE

비개발자가 문장으로 질문하면 AI가 SQL을 만들어 운영 데이터베이스에서 실행하는 콘솔을 기획부터 운영까지 맡았습니다.

- AI가 만든 SQL은 **조회 전용 지시 + 실행 직전 코드 검사**의 2단계를 통과해야 DB에 도달
- OAuth 토큰 암호화 저장과 만료 전 자동 갱신

---

### iOS 앱 4종 App Store 출시
> Swift · SwiftUI · StoreKit 2 · WidgetKit · Firebase

- 앱마다 반복되던 시작, 온보딩, 구독 결제 흐름을 공통 모듈로 분리해 **심사 기간 5.67일 → 1일**
- 실기기에서만 발생한 재잠금 실패의 근본 원인을 로그와 하트비트로 규명
- App Store 결제 알림의 서명 인증서 체인을 검증하는 서버 함수 구현

<br/>

## 🌱 Open Source

| 프로젝트 | 기여 | 릴리스 |
|---|---|---|
| **Spring Security** | [#15898 Improve readability of empty collection checks](https://github.com/spring-projects/spring-security/pull/15898) | 6.4.0 |
| **Spring Kafka** | [#3550 Refactor ProducerFactory to use constant for repeated exception message](https://github.com/spring-projects/spring-kafka/pull/3550) | 3.3.0 |
| **Apache Kafka** | [#17464 Improve code consistency and readability](https://github.com/apache/kafka/pull/17464) | 4.0.0 |

<br/>

## 🧪 Backend Lab

| 저장소 | 내용 |
|---|---|
| [**rush**](https://github.com/takeallusername/rush) | 선착순 쿠폰 발급 시스템. Caffeine 로컬 캐시로 품절 요청을 먼저 거르고, Redis Lua 스크립트로 재고 확인·중복 체크·차감을 원자적으로 처리한 뒤 큐에 쌓아 JDBC Batch로 저장 |
| [**Tunely-stock**](https://github.com/takeallusername/Tunely-stock) | DART 공시·재무 데이터와 주가를 모아 보는 관심 기업 대시보드. NestJS · MikroORM · MySQL · Next.js, k6 부하 테스트 |
| [**Tunely-CourseRegistration**](https://github.com/takeallusername/Tunely-CourseRegistration) | 강의·세션 관리와 수강 신청 REST API. Spring Boot 3.5 · JPA |

<br/>

## 🏆 Awards & Education

- **캡스톤디자인 성과발표회 대상** · 인하대학교 (2025)
- **디지랩 챌린지 해커톤 대상** · 제주지역혁신플랫폼 지능형서비스사업단 (2024)
- **AWS와 함께하는 소중한 상명 해커톤 우수상** · 상명대학교 (2024)
- **소프트웨어 마에스트로 16기** · 정보통신기획평가원 (2025)
- 인하대학교 컴퓨터공학과 졸업 (2026)
