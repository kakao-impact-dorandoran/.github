# 🏠 도란도란 (Doran-Doran)

## 사용자 가이드 (User Guide)

### 서비스 소개
**방해금지 모드 웹 서비스**는 집중 시간을 방해하는 웹사이트를 차단하고, 할 일을 관리하며, 집중 세션을 기록할 수 있는 서비스입니다.  
이 서비스는 **집중력 향상**, **목표 달성**, **시간 관리**를 돕습니다.

---

## 주요 기능

### 🚫 사이트 차단
*   차단할 사이트 URL을 등록하면, 선택한 시간 동안 해당 사이트 접속이 차단됩니다.
*   URL은 여러 개 등록할 수 있으며, 삭제 및 수정 가능합니다.
*   자주 차단하는 사이트는 자동으로 저장되어 다음에 쉽게 선택할 수 있습니다.

### ⏲️ 집중 세션
*   원하는 시간을 설정해 집중 세션을 시작할 수 있습니다.
*   집중 중에는 등록된 사이트가 차단됩니다.
*   긴급 상황 시 **"긴급 종료 요청"** 기능으로 세션을 조기 종료할 수 있습니다.

### 📝 할 일 플래너
*   오늘의 할 일을 작성하고 완료 여부를 체크할 수 있습니다.
*   완료한 항목과 남은 항목을 한눈에 볼 수 있습니다.

### 👤 마이페이지
*   오늘의 총 집중 시간 조회
*   완료한 할 일 개수 / 전체 할 일 개수 통계
*   차단된 사이트 목록 및 세션 기록 확인

---

## 시작 방법
1.  **회원가입/로그인** 후 사용 가능합니다.
2.  **차단할 사이트 URL**을 등록하세요.
3.  **집중 세션**을 시작하세요.
4.  **할 일 플래너**에 오늘의 할 일을 작성하세요.
5.  필요하면 **긴급 종료**를 요청할 수 있습니다.

---

## 사용 환경
*   **Web:** 크롬(Chrome) 등 현대적인 웹 브라우저
*   **Device:** PC, 노트북

---

# 개발자 가이드 (Developer Guide)

## 🛠 기술 스택
*   **Backend:** NestJS, TypeScript
*   **DB:** MySQL (Prisma ORM)
*   **Frontend:** React, JavaScript
*   **Deployment:** AWS EC2, RDS, GitHub Actions

---

## 🚀 주요 API 명세 (간단 요약)

| 리소스 | 메서드/엔드포인트 | 설명 |
| :--- | :--- | :--- |
| **Auth** | `POST /api/auth/google/login` | 구글 로그인 |
| **Block** | `POST /api/block` | 차단 URL 등록 |
| | `GET /api/block` | 차단 URL 조회 |
| | `DELETE /api/block/{id}` | 차단 URL 삭제 |
| **Focus** | `POST /api/focus` | 집중 세션(타이머) 시작 |
| | `GET /api/focus?date=YYYY-MM-DD` | 오늘 세션 조회 |
| **Emergency** | `GET /api/emergency` | 긴급 요청 목록 조회 |
| | `POST /api/emergency` | 긴급 종료 요청 |
| **Todo** | `POST /api/todo` | 오늘의 플래너 작성 |
| | `GET /api/todo?date=YYYY-MM-DD` | 오늘의 플래너 목록 조회 |
| | `PATCH /api/todo/{id}` | 플래너 수정 |
| | `DELETE /api/todo/{id}` | 플래너 항목 삭제 |
| **MyPage** | `GET /api/my-page` | 통계/마이페이지 조회 |

> 💡 **자세한 API 명세는 아래 주소를 참조하세요.**  
> `http://ec2-3-35-37-148.ap-northeast-2.compute.amazonaws.com:3000/api-docs`

---

## 🗄 DB 테이블 구조
*   `User`, `Block`, `Focus`, `Todo`, `EmergencyRequest`, `UserSetting`, `FocusLog`

---

## 📂 페이지 구조
```text
/pages
  ├── login.js   # 로그인 페이지
  ├── main.js    # 메인 대시보드
  ├── mypage.js  # 사용자 통계
  ├── record.js  # 집중 기록 관리
  └── timer.js   # 집중 타이머 화면
