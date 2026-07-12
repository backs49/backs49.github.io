# 권만구 · Side Projects

> 생활의 문제를 직접 만들어 해결합니다.

투자 판단, 가게 운영, 콘텐츠 큐레이션, 공모주 가계부 — 일상에서 반복되는 일을 발견하면 AI와 함께 서비스로 만듭니다. 17년차 엔지니어의 사이드 프로젝트 기록.

**Live**: https://backs49.github.io/

## About

권만구(Mangu Kwon)는 17년차 엔지니어로, 백엔드와 대규모 시스템을 다뤄왔습니다. 퇴근 후에는 Claude·Grok과 AI 페어코딩을 하며 사이드 프로젝트를 만듭니다. 투자, 가게 운영, 콘텐츠 큐레이션, 공모주 관리처럼 일상에서 반복적으로 마주치는 문제를 발견하면, 직접 서비스로 빚어내는 것을 즐깁니다. 주로 Python · TypeScript · Next.js · Node 스택을 사용합니다.

## Projects

### 01. ai-trader

`Python` `LangGraph` `Streamlit`

**FLAGSHIP · AI 에이전트 시스템**

> 거장 4명이 토론하고, 결정은 내가 한다

벤 그레이엄, 버핏, 린치, 캐시 우드 — 네 명의 거장 투자자 페르소나를 가진 AI가 한국·미국 주식을 두고 합의 분석을 진행하는 반자동 투자 시스템입니다. AI들이 논의 끝에 도출한 제안은 Telegram으로 전달되고, 사람이 직접 승인해야만 실제 주문으로 이어집니다. 모든 신호를 값비싼 LLM으로 분석하지 않도록, 먼저 무료인 기술적 신호로 1차 필터링을 한 뒤 유료 LLM 분석은 2단계에서만 태우는 게이팅 구조로 토큰을 아낍니다. 손실이 커지거나 시스템 장애가 발생하면 KillSwitch가 즉시 전 포지션을 청산합니다.

- pytest 633개 통과
- 거장 페르소나 4명 합의
- 대시보드 9면
- 매일 새벽 01:00 종목 발굴

태그: `LangGraph` `claude-agent-sdk` `증권사 OpenAPI × 2` `Telegram Bot` `SQLite` `APScheduler`

레포: 비공개

### 02. nuknuk-dessert

`Next.js` `Supabase` `Toss`

**FULL-STACK COMMERCE · 실사용 서비스**

> 주문받고 결제받고, 알림까지

동네 디저트 가게를 위해 만든 실사용 주문·결제 시스템입니다. 토스 결제위젯으로 결제를 처리하고, 쿠폰과 포인트로 단골 손님을 관리하며, 카카오 알림톡으로 주문 상태를 실시간으로 알려줍니다. 메뉴·주문·고객·매출 현황을 한눈에 파악할 수 있는 관리자 패널까지 갖춘 풀커머스 서비스입니다.

태그: `토스 결제위젯` `쿠폰·포인트` `카카오 알림톡` `관리자 패널`

레포: https://github.com/backs49/nuknuk-dessert

### 03. grok-x-curator (dongpirang-grok-x-curator)

`Python` `Grok API` `Streamlit`

**AI 콘텐츠 큐레이터 · 커뮤니티 실사용**

> X 추천 알고리즘을 읽어, 내 글을 채점한다

X(구 트위터)가 공개한 추천 알고리즘을 시스템 프롬프트로 인코딩해, 작성한 포스트가 알고리즘 기준으로 얼마나 노출되기 좋은지 채점하고 개선안을 제시하는 Streamlit 앱입니다. 8개의 탭으로 다양한 추천 요소를 분석하며 3개 언어를 지원하고, pytest 76개로 검증을 마쳤습니다. 실제 커뮤니티 사용자들과 함께 라이브로 사용 중입니다.

- 추천 탭 8개
- 지원 언어 3개
- pytest 76개 통과
- 커뮤니티 실사용 중(Live)

태그: `Grok API` `시스템 프롬프트 인코딩` `Streamlit` `다국어 지원`

레포: https://github.com/backs49/dongpirang-grok-x-curator

### 04. gongmoX (gongmox-showcase)

`TypeScript` `Hono` `React PWA`

**FULL-STACK PWA · 실사용 서비스**

> 부부가 함께 쓰는 공모주 장부

공모주 청약 일정을 매일 자동으로 수집해 청약·상장 타이밍을 푸시 알림으로 알려주고, 수익 스크린샷을 AI vision으로 파싱해 자동으로 기록하는 가계부 PWA입니다. 크롤러, Web Push, 인증, AI 파싱까지 전 영역을 혼자 풀스택으로 개발했습니다.

태그: `Web Push` `크롤러(EUC-KR)` `Claude Vision` `모노레포 · zod 계약`

레포: https://github.com/backs49/gongmox-showcase

### 05. More Experiments (만들면서 배운다)

#### ai-ropan-factory

`Next.js 16` `Supabase` `AI×3`

장르와 키워드만 입력하면 AI가 로맨스 판타지(로판) 웹소설을 기획 단계부터 연재까지 생성해주는 SaaS입니다. Claude·Gemini·Grok을 스트리밍으로 통합해 사용하고, 토스 정기결제로 구독 모델을 구현했으며, 원자적(atomic) 쿼터 설계로 사용량을 안전하게 관리합니다.

레포: https://github.com/backs49/ai-ropan-factory

#### emotion-diary

`Next.js` `Supabase`

아이가 쓰고 부모가 조용히 읽는 가족 감정 일기 PWA입니다. 음성 입력(STT)과 사진 기록을 지원하며, 자녀와 부모 간 권한 분리를 Postgres RLS(Row Level Security)로 강제합니다. Vitest · Playwright · RLS SQL 테스트로 3층에 걸쳐 검증했습니다.

레포: https://github.com/backs49/emotion-diary

#### dongpirang-meme-factory

`Python` `Streamlit`

키워드 하나만 입력하면 밈 이미지, 웹툰 스크립트, SNS 캡션을 한 번에 생성해주는 도구입니다. API 키가 없어도 Mock 모드로 완전히 동작하도록 Strategy 패턴으로 설계했습니다.

레포: https://github.com/backs49/dongpirang-meme-factory

## Tech Stack

Python · TypeScript · Next.js · Node를 기본 스택으로, Claude · Grok과 AI 페어코딩하며 사이드 프로젝트를 만듭니다.

## Contact

- Email: backs49@gmail.com
- GitHub: [github.com/backs49](https://github.com/backs49)
