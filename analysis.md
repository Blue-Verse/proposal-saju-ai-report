# 사주 명리학 기반 AI 리포트 자동화 웹 구축 — 제안 분석 로그

> 생성일: 2026-03-11
> 공고 URL: https://www.wishket.com/project/153342/

## 1. 공고 파싱 결과

```yaml
job:
  title: "사주 명리학 기반 AI 리포트 자동화 웹 구축"
  category: "웹 기타(IT 서비스 구축)"
  budget_range: "15,000,000원"
  duration: "60일"
  tech_stack: [AWS, Express.js, MongoDB, Node.js, Python, React]
  description: >
    내부 운영진 2~3명 사용 폐쇄형 웹.
    고객 데이터 입력 → KASI/상업용 사주 API → 자체 로직 연산 →
    LLM 초안 생성 → 웹 에디터 수정 → 고해상도 PDF 출력
  requirements:
    - 관리자 로그인 (폐쇄형 웹)
    - 고객 데이터 수급 (생년월일, 태어난 시간)
    - API 연동 (KASI 또는 상업용 사주 명리학 API)
    - 데이터 정규화 엔진 (엑셀 If-Then 로직 이식)
    - AI 리포트 초안 생성 (LLM, 30/100페이지)
    - 웹 에디터 (운영진 수정/보완)
    - 고해상도 PDF 퍼블리싱 (Puppeteer, 30/100페이지 템플릿)
    - 관리자 전용 대시보드 (이력 관리, 다운로드)
  client_questions: []
  deadline: "2026-03-23"
  job_post_url: "https://www.wishket.com/project/153342/"
  urls: ["https://min-inter.co.kr/data-analysis/saju-palja-four-pillars-destiny"]
  images: []
```

특이사항:
- 예비창업패키지 서류 심사 단계 (선정 시 5월 중순 착수)
- 상세 견적 + 기술적 구현 방안 제안 필요
- MVP 제안 환영
- 선정 시 우선 협상 대상자 혜택

## 2. URL/이미지 분석

### min-inter.co.kr (사주팔자 운세 분석 — AI 기반 명리학 상담)
- **사이트 유형**: B2C 사주 분석 서비스 (참고용 레퍼런스)
- **기술 스택**: Next.js SPA
- **디자인 스타일**: 다크 테마, 네온/비비드 컬러 액센트
- **핵심 UI 패턴**:
  - 생년월일 입력 폼 → 자동 사주 분석 결과 생성
  - 오행(五行) 색상 코딩 (목=초록, 화=빨강, 토=노랑, 금=흰색, 수=파랑)
  - 연주/월주/일주/시주 4기둥 데이터 그리드
  - 대운/세운 타임라인형 시각화
  - 매우 긴 스크롤 기반 상세 리포트 (수십 개 섹션)
- **기능 복잡도**: 중상 — 사주 연산 로직 + 데이터 시각화 + 장문 분석 텍스트
- **제안서 반영**: 클라이언트는 이 수준의 분석을 내부 도구 + PDF로 구현 원함. 공개 서비스가 아닌 내부 업무 자동화이므로 UI 복잡도 절감 가능. 오행 색상 코딩, 4기둥 구조 등 PDF 템플릿 디자인에 반영.

## 3. 실현 가능성 분석 (내부용)

- **프로젝트 유형**: 풀스택 웹앱 + 외부 API 연동
- **Feasibility**: "가능" + 버퍼 +10~15%
- **기본 공수**: 45 M/D
- **AI 반영 공수**: 21.1 M/D (평균 53% 절감)
- **버퍼 +12% 적용**: ~24 M/D
- **달력 일수**: 24 × (7/5) = ~34일
- **클라이언트 예상 기간**: 60일
- **판정**: 산정 기간(34일) ≤ 예상 기간(60일) → 클라이언트 기간 그대로 사용

### 공수 상세 (내부용)

| 작업 영역 | 기본 공수 | AI 절감률 | 조정 공수 |
|-----------|----------|----------|---------|
| 기획/설계 | 5 M/D | 35% | 3.3 |
| Figma 디자인 | 3 M/D | 15% | 2.6 |
| FE 개발 | 15 M/D | 65% | 5.3 |
| BE 개발 | 18 M/D | 55% | 8.1 |
| QA/배포 | 4 M/D | 55% | 1.8 |
| **합계** | **45 M/D** | **~53%** | **21.1 M/D** |

## 4. 포트폴리오 매칭

| 순위 | 프로젝트 | 매칭 점수 | 근거 |
|------|---------|----------|------|
| 1 | Fortune App | 95점 | 사주(四柱) 분석 엔진 연동, 생년월일/시간 입력 기반 운세 분석 — 도메인 완전 일치 |
| 2 | Series-B | 88점 | AI 보고서 자동 생성(ChatGPT), Lexical 에디터, 7중 PDF 파이프라인, 관리 대시보드 |
| 3 | EZ-Approve | 75점 | 관리자 대시보드, Lexical 에디터(170파일), 내부 업무 자동화, PDF 문서 처리 |
| 4 | AI Agent | 65점 | 멀티 LLM 오케스트레이션(Claude/Gemini/GPT), React 대시보드, 문서 인텔리전스 |
| 5 | Harmony Link | 55점 | OpenAI AI 건강 분석, RBAC 관리 대시보드, AWS CDK 인프라, 140+ API |

### 매칭 점수 산출 기준
- 기술 스택 일치 (40%): Fortune App은 Node.js 백엔드로 일치, Series-B는 Next.js+NestJS+PDF로 높은 일치
- 도메인 유사성 (30%): Fortune App이 사주 도메인 완전 일치로 만점
- 기능 유사성 (20%): Series-B의 AI 보고서+에디터+PDF가 핵심 파이프라인과 동일
- 규모 적합성 (10%): 내부 도구 특성상 EZ-Approve의 관리 도구 경험이 적합

### 매칭 커버리지 맵
| 요구사항 | Fortune App | Series-B | EZ-Approve | AI Agent | Harmony Link |
|---------|:-----------:|:--------:|:----------:|:--------:|:------------:|
| 사주 도메인 | ● | | | | |
| LLM/AI 연동 | | ● | | ● | ● |
| 리치 에디터 | | ● | ● | | |
| PDF 파이프라인 | | ● | | | |
| 관리자 대시보드 | | ● | ● | ● | ● |
| AWS 인프라 | | ● | | | ● |
| 내부 업무 도구 | | | ● | | ● |

## 5. 최종 제안 요약

- **지원 금액**: 13,500,000원 (VAT 별도) — 클라이언트 예상 15,000,000원의 90%
- **지원 기간**: 60일
- **핵심 제안 포인트**:
  1. 사주 분석 앱 직접 개발 경험 (Fortune App)
  2. AI 보고서 자동 생성 시스템 구축 경험 (Series-B)
  3. 7중 PDF 파이프라인 + 170파일 리치 에디터 구현 경험
  4. 참고 사이트 분석 결과를 PDF 템플릿 디자인에 반영
  5. 멀티 LLM 통합 및 프롬프트 엔지니어링 전문성 (AI Agent)

## 6. 최종 산출물

### 제안서 사이트 URL
https://proposal-saju-ai-report.pages.dev/

### 지원 금액
13,500,000

### 지원 기간
60

### 지원 내용

안녕하세요, 사주 명리학 기반 AI 리포트 자동화 웹 구축 프로젝트에 지원합니다.

본 프로젝트에 대한 상세 제안서(견적서, 공수계산서, PRD, 일정, 포트폴리오)를 별도 페이지로 준비하였습니다. 아래 링크에서 확인해 주시면 감사하겠습니다.
▶ 제안서 상세 페이지: https://proposal-saju-ai-report.pages.dev/
▶ 위시켓 포트폴리오: https://www.wishket.com/partners/p/blueverse1/portfolio/

---

<프로젝트 진행 제안>

■ 프로젝트 분석
본 프로젝트는 내부 운영진(2~3명)이 사용하는 폐쇄형 웹 시스템으로, 고객의 생년월일/시간 데이터를 입력하면 KASI/상업용 사주 API 연동 → 자체 명리학 If-Then 로직 연산 → LLM(Gemini/OpenAI) 리포트 초안 생성 → 웹 에디터 수정 → 고해상도 PDF 출력까지의 원스톱 파이프라인을 구축하는 프로젝트입니다.

참고 사이트(min-inter.co.kr) 분석 결과, 사주 데이터의 시각적 표현(오행 색상 코딩, 4기둥 간지 구조, 대운/세운 타임라인)에 대한 구체적인 UX 패턴을 파악하였으며, 이를 PDF 리포트 템플릿 디자인에 직접 반영하겠습니다.

■ 작업 일정

[Phase 1: 기획/설계] Day 1~15 (15일)
- 요구사항 상세화, 엑셀 알고리즘 분석, DB 스키마 설계, API 명세서, 와이어프레임

[Phase 2: UI/UX 디자인] Day 8~18 (11일)
- 관리자 화면 UI 디자인, PDF 리포트 템플릿 디자인 (마스터 가이드라인 기반)

[Phase 3: 백엔드 개발] Day 12~42 (31일)
- 인증 API, 사주 API 연동, 정규화 엔진, LLM 연동, PDF 생성 엔진

[Phase 4: 프론트엔드 개발] Day 16~48 (33일)
- 로그인, 고객 데이터 입력, 웹 에디터, 대시보드, PDF 미리보기

[Phase 5: QA/배포] Day 48~60 (13일)
- 통합 테스트, 실 데이터 검증, AWS 서버 배포, 운영자 교육

■ 마일스톤 및 산출물
- M1 (Day 15): 설계 완료 — PRD, ERD, API 명세서 승인
- M2 (Day 18): 디자인 확정 — UI 디자인, PDF 템플릿 시안 승인
- M3 (Day 35): 엔진 완성 — 정규화 엔진 + LLM 연동 데모
- M4 (Day 48): 전체 기능 통합 — 통합 테스트, PDF 출력 검증
- M5 (Day 60): 최종 납품 — 운영 서버 배포, 소스 코드 이관

■ 미팅 시 협의 필요 사항
- 엑셀 기반 명리학 If-Then 로직 파일 사전 공유
- 리포트 마스터 템플릿 가이드라인 공유
- 사주 API 선택 (KASI vs 상업용) 협의
- LLM 선택 (Gemini vs OpenAI) 및 API 키 준비
- 30/100페이지 리포트 항목 구성 상세 협의

---

<유사 프로젝트 진행 경험>

▶ Fortune App — 사주 기반 운세 앱 (2024.07~2024.09, 3개월)
- 프로젝트 유형: B2C 앱 / 엔터테인먼트 / 라이프스타일
- 핵심 기능: 사주(四柱) 분석 엔진 연동, 생년월일/시간 입력 기반 운세 분석
- 유사점: 사주 명리학 도메인 직접 경험
- 기술 스택: Flutter, Firebase, Node.js, BLoC

▶ Series B — VC 펀드 관리 플랫폼 (2023.11~2024.12, 14개월)
- 프로젝트 유형: B2B SaaS / 핀테크
- 핵심 기능: AI 투자심사보고서 자동 생성(ChatGPT), Lexical 에디터, 7중 PDF 파이프라인
- 유사점: AI 보고서 자동 생성 + 에디터 + PDF 파이프라인
- 기술 스택: Next.js, NestJS, TypeScript, MySQL, Lexical, AWS

▶ EZ-Approve — 전자결재 SaaS (2026.01~2026.03, 9주)
- 프로젝트 유형: B2B SaaS / 업무 자동화
- 핵심 기능: 170파일 Lexical 에디터, 관리자 대시보드(50+ 페이지)
- 유사점: 리치 에디터 + 관리자 내부 업무 도구
- 기술 스택: Next.js, NestJS, TypeScript, MySQL, Lexical, Docker

▶ AI Agent — AI-Native 개발 프레임워크 (2025~, 47일간 236 커밋)
- 프로젝트 유형: AI / 자동화 / 개발 도구
- 핵심 기능: 멀티 LLM 오케스트레이션(Claude, Gemini, GPT), 문서 인텔리전스
- 유사점: LLM 통합 및 프롬프트 엔지니어링 전문성
- 기술 스택: TypeScript, Node.js 20, React 19, Claude SDK, Gemini SDK

▶ Harmony Link — 시니어 주간보호 관리 플랫폼 (2025, 6개월)
- 프로젝트 유형: B2B SaaS / 헬스케어
- 핵심 기능: OpenAI AI 건강 분석, 관리 대시보드, 140+ API 엔드포인트
- 유사점: OpenAI 연동 + 관리 시스템 + AWS 인프라
- 기술 스택: Flutter, NestJS, Next.js, TypeScript, AWS CDK, OpenAI

---

<사용 기술과 툴>

▶ 개발 기술
- 프론트엔드: React 18, Next.js 14, TailwindCSS, TipTap Editor
- 백엔드: Node.js, Express.js, Python (정규화 엔진)
- 데이터베이스: MongoDB
- AI/LLM: OpenAI GPT-4o / Google Gemini
- PDF: Puppeteer
- 인프라: AWS, Docker

▶ 개발 도구 및 인프라
- 버전 관리: GitHub
- CI/CD: GitHub Actions
- 클라우드: AWS
- 컨테이너: Docker

▶ 커뮤니케이션
- 일일 진행 공유: Slack 또는 카카오톡
- 주간 미팅: Zoom / Google Meet
- 문서 공유: Notion 또는 Google Docs
- 이슈 트래킹: GitHub Issues

### 관련 포트폴리오 추천
1. Fortune App — 사주(四柱) 분석 엔진 연동 (도메인 완전 일치)
2. Series B — AI 보고서 자동 생성 + 에디터 + PDF (핵심 기능 일치)
3. EZ-Approve — 리치 에디터 + 관리자 대시보드 (에디터/대시보드 일치)
4. AI Agent — 멀티 LLM 오케스트레이션 (LLM 통합 전문성)
5. Harmony Link — OpenAI 연동 + 관리 시스템 + AWS (AI+인프라 경험)
