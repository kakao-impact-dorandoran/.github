제공해주신 이미지(image_69483d.png)의 구성과 스타일을 참고하여, 현재 진행 중인 '도란도란' 프로젝트의 오가니제이션 프로필용 README.md 초안을 작성해 드립니다. 이 내용을 .github 레포지토리의 profile/README.md에 복사해서 사용하시면 됩니다.

🏠 도란도란 (Doran-Doran)
사용자 가이드 (User Guide)
서비스 소개
은둔 청년들이 사회로 한 발자국씩 나아갈 수 있도록 돕는 단계별 사회 재진입 지원 서비스입니다. 심리적 장벽을 낮추기 위해 '퀘스트' 형식의 게이미피케이션 요소를 도입하였습니다.

주요 기능
단계별 퀘스트: 은둔 상태에서 벗어나기 위한 단계별 행동 지침을 퀘스트 형태로 제공합니다.

마이크로 워크 매칭: 청년들이 작은 일부터 경험하며 성취감을 느낄 수 있도록 소규모 일자리를 연결합니다.

게이미피케이션 레벨 시스템: 활동 결과에 따른 레벨업과 랭킹 시스템을 통해 지속적인 동기를 부여합니다.

피드백 시스템: 멘토와 멘티 간의 원활한 소통과 계획 관리를 지원합니다.

시작 방법
카카오 계정을 통해 간편하게 로그인합니다.

현재 본인의 상태에 맞는 초기 퀘스트를 선택합니다.

매일 주어지는 작은 미션들을 수행하고 인증합니다.

경험치를 쌓아 새로운 마이크로 워크에 도전합니다.

사용 환경
Web: 크롬(Chrome) 및 최신 브라우저 최적화

Mobile: 모바일 반응형 웹 지원

개발자 가이드 (Developer Guide)
기술 스택
Backend: Java 17, Spring Boot, Spring Data JPA

Frontend: React, Next.js (예정)

Database: MySQL

AI Tools: GitHub Copilot, Cursor (AI-First Workflow 도입)

주요 API 명세 (간단 요약)
리소스	메서드/엔드포인트	설명
Auth	POST /api/auth/kakao	카카오 소셜 로그인
Quest	GET /api/quests	현재 진행 가능한 퀘스트 목록 조회
Quest	POST /api/quests/{id}/complete	퀘스트 수행 인증 및 완료 처리
Work	GET /api/works	맞춤형 마이크로 워크 목록 조회
User	GET /api/users/me	내 프로필 및 레벨/경험치 조회
DB 테이블 구조
User: 사용자 기본 정보 및 현재 레벨 정보

Quest: 퀘스트 내용, 난이도 및 보상 경험치

UserQuest: 사용자가 수락한 퀘스트의 진행 상태

MicroWork: 일자리 정보 및 매칭 현황

페이지 구조
Plaintext
/pages
  ├── index.js (랜딩 및 메인)
  ├── login.js (로그인)
  ├── quests.js (퀘스트 목록)
  ├── works.js (일자리 매칭)
  └── mypage.js (성장 대시보드)
사용한 오픈소스
Spring Boot: 견고한 백엔드 아키텍처 구축을 위한 프레임워크

Lombok: 자바 코드 다이어트를 위한 라이브러리

SpringDoc OpenAPI: Swagger를 통한 API 명세 자동화

배포 환경
Backend: AWS EC2 기반의 독립 서버 배포 (Docker 활용 예정)

Frontend: Vercel 또는 Netlify를 통한 자동 배포

기여 가이드 (Contribution Guide)
Branch Strategy: main (배포), develop (개발), feature/{기능명} (기능별 작업)

Code Review: 모든 PR은 팀원 1명 이상의 승인이 있어야 Merge 가능합니다.

Commit Convention: feat:, fix:, chore:, docs: 등의 머리말을 사용합니다.

© 2026 Kakao Tech for Impact - Team Doran-Doran
