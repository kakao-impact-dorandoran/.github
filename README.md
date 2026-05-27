# 🏡 도란도란 (Doran-Doran)

> 은둔·고립 청년과 어르신을 대화 기반 활동으로 연결하는 세대 공감 플랫폼

도란도란은 사회적 관계 형성에 어려움을 겪는 청년이 어르신과의 정기적인 말벗 활동을 통해 사회 참여 경험을 쌓고, 어르신은 정서적 교류와 돌봄을 받을 수 있도록 돕는 서비스입니다.

청년, 보호자, 어르신 전용 기기, 관리자 역할을 중심으로 매칭, 일정, 통화, 활동 기록, 증명서, 신고 및 운영 관리를 제공합니다.

---

## ✨ 주요 기능

### 👥 청년

- 청년 프로필 등록 및 관리자 승인 상태 확인
- 매칭 가능한 어르신 목록 조회
- 어르신 상세 정보 확인 및 매칭 신청
- 가능 시간 등록 및 일정 관리
- 어르신과의 통화 활동
- 활동 기록 작성
- 누적 활동 시간 확인
- 사회참여 활동 증명서 발급 및 조회
- 신고 및 매칭 중단 요청

### 👨‍👩‍👧 보호자

- 등록된 어르신 정보 확인
- 어르신 가능 시간 관리
- 보호자 일정 조회
- 청년-어르신 매칭 현황 확인
- 매칭 상세 정보 조회
- 활동 기록 확인
- 신고 및 매칭 중단 요청

### 📱 어르신 전용 기기

- Device Token 기반 전용 기기 인증
- 어르신 메인 화면 제공
- 통화 시작 및 종료
- 청년 접속 URL 안내
- 도움 요청 생성

### 🛠 관리자

- 청년 프로필 승인 및 반려
- 도움 요청 처리
- 매칭 중단 요청 승인 및 반려
- 신고 처리
- 신고 대상 사용자 제재
- 운영 현황 확인

---

## 🧩 서비스 흐름

```text
청년 회원가입/로그인
→ 청년 프로필 등록
→ 관리자 승인
→ 어르신 탐색 및 매칭 신청
→ 일정 등록 및 통화
→ 활동 기록 작성
→ 누적 시간 반영
→ 증명서 발급
```

```text
보호자 로그인
→ 어르신 정보 확인
→ 일정/매칭 현황 확인
→ 활동 기록 확인
→ 필요 시 신고 또는 매칭 중단 요청
```

```text
관리자 로그인
→ 청년 가입 검수
→ 도움 요청 처리
→ 신고 처리
→ 매칭 중단 요청 처리
→ 사용자 제재
```

---

## 🛠 기술 스택

### Frontend

- React
- TypeScript
- Vite
- Tailwind CSS
- React Router
- PWA 기반 화면 구성

### Backend

- Spring Boot
- Java 21
- Spring Security
- JPA / Hibernate
- MySQL
- JWT 인증

### Database

- MySQL
- JPA Entity 기반 도메인 모델링

### Collaboration

- GitHub Organization
- GitHub Pull Request 기반 협업
- 역할별 기능 단위 브랜치 전략

---

## 📁 Repository

| Repository | Description |
| --- | --- |
| `frontend` | 도란도란 프론트엔드 애플리케이션 |
| `backend` | 도란도란 백엔드 API 서버 |
| `.github` | Organization 소개 및 공통 문서 관리 |

---

## 🚀 실행 개요

### Backend

```bash
cd backend
./gradlew bootRun
```

Windows PowerShell:

```powershell
cd backend
.\gradlew bootRun
```

기본 API 서버 주소:

```text
http://localhost:8080
```

### Frontend

```bash
cd frontend/frontend
pnpm install
pnpm dev
```

기본 프론트 주소:

```text
http://localhost:5173
```

---

## 🔐 시연 계정

로컬 백엔드 실행 시 `DataInitializer`를 통해 seed 계정이 생성됩니다.

| 역할 | 이메일 | 비밀번호 |
| --- | --- | --- |
| 청년 승인 완료 | `youth_approved@test.com` | `test1234!` |
| 보호자 | `guardian@test.com` | `test1234!` |
| 관리자 | `admin@test.com` | `test1234!` |
| 청년 승인 대기 | `youth_pending@test.com` | `test1234!` |
| 청년 반려 | `youth_rejected@test.com` | `test1234!` |
| 청년 제재 | `youth_banned@test.com` | `test1234!` |

> 위 계정은 로컬 개발 및 시연용 seed 계정입니다.

---

## 🌱 프로젝트 목표

도란도란은 단순한 대화 매칭 서비스가 아니라,  
청년에게는 사회 참여와 회복의 기회를,  
어르신에게는 정서적 연결과 일상 속 대화 경험을 제공하는 것을 목표로 합니다.

세대 간 대화를 통해 서로의 일상에 자연스럽게 스며드는 따뜻한 연결을 만들어갑니다.

© 2026 Kakao Tech for Impact - Team Doran-Doran
