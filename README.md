# 🎬 영화데모 제작

> **Vue.js 기반 영화 정보 제공 SPA 웹 애플리케이션**  
> The Movie Database(TMDb) 및 Kakao API를 활용하여 사용자 맞춤 영화 탐색, 위시리스트, 다국어 지원, 소셜 로그인 기능제공

---

## ✔️ 프로젝트 개요

| 항목        | 내용                                    |
| ----------- | --------------------------------------- |
| 프레임워크  | Vue.js (SPA 구성)                       |
| 상태관리    | Vuex + vuex-persistedstate              |
| 라우팅      | Vue Router                              |
| API 연동    | TMDB API, Kakao Developers API          |
| 배포        | GitHub Pages, GitHub Actions            |
| 인증        | 이메일/비밀번호, Kakao 소셜 로그인      |
| 로컬 저장소 | localStorage/sessionStorage             |
| 반응형      | 데스크탑/태블릿/모바일 완전 대응        |
| UI 효과     | CSS Transition 및 애니메이션            |
| AI 도구     | ChatGPT를 통한 Prompt 설계 및 코드 개선 |

---

## 🚀 주요 기능 요약

### ✔️ 사용자 인증

- 이메일/비밀번호 기반 로그인 및 회원가입
- Kakao 소셜 로그인 연동
- Remember Me, 자동 로그인 기능
- 로그인 성공 시 `/`으로 이동
- 로그인 상태에 따른 UI 분기 처리
- 미로그인 사용자의 접근 차단 및 리디렉션

### 🎁 위시리스트

- 영화 추천/취소 및 UI 반영
- localStorage 저장
- 추천된 영화는 별도 스타일로 표시

### 🔍 영화 검색 및 필터링

- 장르, 평점, 정렬, 언어 등 복합 필터
- 실시간 필터링 및 초기화 기능

### 🔥 인기 콘텐츠

- `/popular` 페이지
- Table View / 무한 스크롤 선택 가능
- 페이지네이션 및 Top 버튼 포함

### 🎬 홈

- TMDB API 기반 영화 정보 출력 (4개 이상 엔드포인트)
- 영화 상세, 설명, 장르, 평점 등 출력
- 포스터 Hover 확대, 추천 기능 포함

### 💬 알림 시스템

- Vue Toastification 기반 피드백 메시지
- 성공/실패 상황에 따른 메시지 제공

### 🌐 다국어 지원

- 한/영/일 언어 선택
- 선택 언어 localStorage 저장
- TMDB API 언어 파라미터 자동 반영

### 🛠 API 연동

- Axios 인터셉터 적용
- TMDB & Kakao API 인증 처리
- 네트워크 에러 핸들링, 사용자 피드백 제공

### 📱 반응형 웹

- 미디어쿼리 기반 반응형 UI
- 모바일에서도 완벽 작동
- 영화 카드 애니메이션 및 스크롤 인터랙션

---

## ⚙️ GitHub Actions 기반 CI/CD

프로젝트는 **GitHub Actions**를 활용해 자동화된 빌드, 테스트, 배포 파이프라인을 구성

### ✔️ 워크플로우 구성

| 브랜치      | 동작 내용                                 |
| ----------- | ----------------------------------------- |
| `develop`   | 코드 병합 시 자동 빌드 및 테스트 수행     |
| `main`      | 병합 시 GitHub Pages로 자동 배포          |
| 모든 브랜치 | PR 생성/병합 시 CI 실행 및 상태 확인 가능 |

### 🔔 Slack 연동

- 모든 워크플로우 결과는 Slack Webhook을 통해 실시간으로 알림 전송
-  CI/CD 결과를 빠르게 확인 가능

### 🔐 보안 및 최적화

- `.env` 파일은 환경에 따라 `.env-dev`, `.env-prod`로 분리
- GitHub Secrets를 통해 API 키 및 민감 정보 관리
- 브랜치 보호 설정: main 브랜치 직접 푸시 제한 및 PR 승인 필수

---

## ✨ 주요 기능

### 🔐 사용자 인증 및 로그인

- 이메일/비밀번호 회원가입 및 로그인
- "Remember me" 기능 (localStorage/sessionStorage 분기 저장)
- 로그인 상태 Vuex 및 로컬 스토리지 기반 유지
- 로그아웃 및 인증 해제 기능
- 인증 사용자만 접근 가능한 라우팅 가드 적용

---

### 🧠 상태 관리 및 로컬 저장소

- Vuex 및 vuex-persistedstate로 상태 유지
- localStorage에 사용자 정보 및 위시리스트 저장
- 새로고침 후에도 사용자 정보와 선호 설정 유지
- 선택한 언어 및 테마 설정 localStorage 저장

---

### 🔌 API 연동 및 에러 처리

- TMDB API를 Axios로 연동
- 요청 인터셉터를 통한 API 키/언어 자동 포함
- 중복 요청 최소화 및 응답 캐싱 전략 적용
- 네트워크 및 HTTP 오류 시 사용자 친화적 메시지 출력
- 로딩 상태 표시(로딩 스피너 등)

---

### 🔍 영화 검색 및 필터링

- 장르, 평점, 언어 등 필터 조합 기능
- 실시간 필터 반영 및 결과 표시
- 조건 초기화 버튼 제공
- 카드 형태로 검색 결과 시각화

---

### 📈 인기 영화 목록

- TMDB 인기 영화 데이터 표시
- 두 가지 보기 모드 제공:
  - **Table View**: 고정된 테이블 + 페이지네이션
  - **Infinity Scroll**: 스크롤 기반 자동 로딩
- 상단 이동 버튼(Top) 제공

---

### ❤️ 위시리스트

- 영화 추천 등록 및 해제 기능
- 추천 영화는 Vuex + localStorage로 상태 유지
- 위시리스트 전용 페이지 제공
- 추천된 영화는 별도 UI(👍 아이콘 등)로 표시

---

### 🌐 다국어 지원

- 한국어, 영어, 일본어 중 선택 가능
- 선택 언어 localStorage 저장
- TMDB API의 언어 파라미터 자동 반영

---

### 📱 반응형 UI 및 디자인

- 데스크톱, 태블릿, 모바일 최적화
- 미디어 쿼리 및 레이아웃 유연성 고려
- CSS 애니메이션 및 transition 적용
  - 영화 카드 hover 확대
  - 로그인/회원가입 컴포넌트 전환 효과
  - 버튼, 메뉴 인터랙션 등 시각적 효과 강화

---

### 💬 사용자 알림 시스템

- Vue Toastification 기반 Toast 메시지 제공
- 로그인, 회원가입, 오류 등 이벤트 상황에 맞는 피드백 표시
- 일관된 디자인으로 UX 향상

---

### 🧭 네비게이션 및 라우팅

- Vue Router를 활용한 SPA 구조 구현
- 인증 필요 페이지 접근 시 로그인 페이지로 리디렉션
- 존재하지 않는 경로 접근 시 홈 또는 로그인 페이지로 이동
- 라우팅 간 전환 애니메이션 효과 적용

---

## 🌿 Git 전략

프로젝트는 **Git Flow 전략**을 도입하여 체계적인 버전 관리와 협업을 위한 브랜치 전략을 적용

### ✔️ 브랜치 구조

| 브랜치      | 역할                                 |
| ----------- | ------------------------------------ |
| `main`      | 배포용 브랜치 (제품 릴리스)          |
| `develop`   | 기능 통합 브랜치 (개발 중 코드 병합) |
| `feature/*` | 기능 개발용 브랜치 (기능 단위 작업)  |

---

## 🧪 개발 및 배포 환경 구성

### ⛅ 개발/배포 환경 분리

- `.env-dev`, `.env-prod` 환경 파일 관리
- dotenv로 환경 변수 로딩
- `package.json` 내 실행 스크립트 구분

```bash
npm run serve:dev     # 개발
npm run serve:prod    # 배포
```
