# 프로젝트 이름
 #### 짭플렉스(vue.js 기반 영화 정보 제공하는 웹 애플리케이션)
--------------------------
## 📖 소개
 ##### 짭플렉스는 Vue.js로 개발된 영화 정보 제공 웹 애플리케이션입니다. 사용자들은 인기 영화, 장르별 영화, 검색 기능 등을 통해 다양한 영화를 찾아볼 수 있으며, 회원가입 및 로그인 기능을 통해 개인화된 위시리스트를 관리할 수 있습니다.
--------------------------
## 프로젝트 목적
- 최신 프론트엔드 기술 습득: React.js 또는 Vue.js를 활용하여 SPA를 개발함으로써 최신 프론트엔드 프레임워크에 대한 이해와 실무 능력을
향상.
- GPT 활용 능력 강화: GPT를 최대한 활용하여 개발 과정에서 AI 도구를 적용하고, 효율적인 코딩 및 문제 해결 능력을 기름.
- 정적 웹사이트 배포 경험: Github Pages를 이용하여 정적 웹사이트를 배포하는 과정을 실습하여, 배포 프로세스와 호스팅에 대한 이해를 높
임.
- UI/UX 디자인 이해: Netflix와 유사한 프론트엔드 데모 사이트를 제작하면서 사용자 경험 중심의 디자인 원칙을 학습하고 적용함 (+css
transition 등).
- 오픈소스 및 라이브러리 활용 능력 향상: React.js 또는 Vue.js와 같은 오픈소스 프레임워크와 라이브러리를 활용하여 개발 역량을 강화함.
- 자기 주도적 학습 역량 배양: GPT와 오픈소스 도구를 활용하여 독립적으로 학습하고 문제를 해결하는 능력을 향상시킴.
- 웹 개발 및 배포 흐름 이해: SPA 개발부터 정적 웹사이트 배포까지의 전체 과정을 경험하여 웹 개발 프로세스 전반에 대한 이해를 높임.
--------------------------
## 🛠 기술스택
 - 프론트 프레임워크 : Vue.js
 - 상태관리 : Vuex
 - 라우팅 : Vue Router
 - HTTP 통신 : Axios
 - 스타일  :CSS
 - 아이콘 : Font Awesome
 - API : The Movie Database (TMDB) API
 - 패지키 매니저 : npm
 - 빌드도구 : Vue CLI
 - 📦추가 라이브러리 :
    - Vue Toastification: 사용자에게 알림 메시지 제공
    - Vuex Persisted State: 상태를 로컬 스토리지에 저장하여 새로고침 후에도 데이터 유지

--------------------------

## 목차
- [소개](#소개)
- [기술스택](#기술스택) 
- [설치 및 실행](#설치-및-실행)
- [프로젝트 구조](#프로젝트-구조)
- [주요 기능](#주요-기능)
- [사용전략](#전략)
- [기여 방법](#기여-방법)


##  🚀 설치 및 실행
-----------------------
### 📋 1. 사전 요구 사항
- Node.js >= 14.x
- npm >= 6.x
- npm 또는 yarn패키지 매니저

### 📂 2. 설치 방법
-------------------------------

1. git clone https://github.com/your-repo.git
2. cd your-repo => 프로젝트 디렉토리로 이동
3. npm install  => 의존성 설치
    - 라이브러리 설치
        - Vue Toastification : 
            - npm install vue-toastification@2
        - Vuex Persisted State
            - npm install vuex-persistedstate
4. VUE_APP_TMDB_API_KEY=your_tmdb_api_key
    - .env 파일 생성하고 아래 내용을 추가해주세요.
    - your_tmdb_api_key를 TMDB API 키로 대체하세요.
5. npm run serve  => 개발 서버 실행

----------------------------------


## 📂 프로젝트 구조
    - **`public/`**: 정적 파일을 보관하는 디렉토리입니다.
        - index.html: 애플리케이션의 기본 HTML 파일입니다.
    - src/: 소스 코드가 위치한 디렉토리입니다.
        - assets/: 이미지, 폰트 등 정적 자산이 위치합니다.
            - images/: 이미지 파일 보관 디렉토리입니다.
        - components/: 재사용 가능한 Vue 컴포넌트들이 위치합니다.
            - common/: Header, Footer, MovieCard 등 공통 컴포넌트들이 위치합니다.
        - hooks/: 재사용 가능한 로직을 위한 커스텀 훅이 위치합니다.
            - useFetch.js: API 호출을 위한 커스텀 훅입니다.
            - useWishlist.js: 위시리스트 관리를 위한 커스텀 훅입니다.
        - router/: Vue Router 설정이 위치합니다.
            - index.js: 라우터 설정 파일입니다.
        - services/: 외부 API와의 통신을 위한 파일이 위치합니다.
            - api.js: Axios 인스턴스를 생성하고 인터셉터를 설정합니다.
        - store/: Vuex 상태 관리와 관련된 파일이 위치합니다.
            - index.js: Vuex 스토어 설정 파일입니다.
            - modules/: Vuex 모듈들이 위치합니다.
                - auth.js: 인증 관련 상태 관리 모듈입니다.
                - movies.js: 영화 데이터 상태 관리 모듈입니다.
                - wishlist.js: 위시리스트 상태 관리 모듈입니다.
        - utils/: 유틸리티 함수들이 위치합니다.
            - auth.js: 로그인 및 회원가입 로직을 담은 유틸리티 파일입니다.
            - constants.js: 상수값들이 정의되어 있습니다.
        - views/: 페이지 단위의 컴포넌트들이 위치합니다.
            - Home.vue: 홈 페이지 컴포넌트입니다.
            - Popular.vue: 인기 영화 페이지 컴포넌트입니다.
            - Search.vue: 검색 페이지 컴포넌트입니다.
            - SignIn.vue: 로그인 및 회원가입 페이지 컴포넌트입니다.
            - Wishlist.vue: 위시리스트 페이지 컴포넌트입니다.
    - App.vue: 최상위 앱 컴포넌트입니다.
    - main.js: 애플리케이션의 진입점 파일입니다.
    -.env: 환경 변수 파일로, API 키 등이 저장됩니다.
    -package.json: 프로젝트의 의존성 목록과 스크립트가 정의되어 있습니다.
    -README.md: 프로젝트에 대한 설명서입니다.

---------------------------------



## 🎬 주요기능
1. 사용자 인증 및 로그인 기능

    - 회원가입 및 로그인: 사용자는 이메일과 비밀번호로 회원가입을 할 수 있으며, 기존 계정으로 로그인할 수 있습니다.
    - 인증 상태 유지: 로그인 시 Vuex 상태 관리와 로컬 스토리지를 활용하여 사용자의 인증 상태를 유지합니다.
        - localStorage와 sessionStorage 활용: 사용자가 "Remember me" 옵션을 선택하면 localStorage에 인증 정보를 저장하여 브라우저를 재시작해도 로그인 상태가 유지됩니다. 그렇지 않으면 sessionStorage에 저장되어 세션이 종료되면 로그아웃됩니다.
    - 로그아웃 기능: 사용자는 언제든지 로그아웃하여 인증 정보를 삭제할 수 있습니다.
    - 접근 제어: 인증된 사용자만 접근할 수 있는 라우트를 설정하여 보안성을 높였습니다
        - 예: 홈, 인기 영화, 검색, 위시리스트 페이지는 로그인한 사용자만 접근 가능하며, 그렇지 않은 경우 로그인 페이지로 리디렉션됩니다.


2. 로컬 스토리지 및 상태관리
    - 사용자 데이터 저장: 회원가입한 사용자 정보는 로컬 스토리지에 저장되어 이후 로그인 시 검증에 사용됩니다.
    - 위시리스트 관리: 사용자가 위시리스트에 추가한 영화 목록은 Vuex와 localStorage를 통해 유지됩니다.
        -Vuex Persisted State: 이 라이브러리를 활용하여 애플리케이션 상태를 로컬 스토리지에 저장하고, 페이지 새로고침 후에도 상태를 복원합니다.
    - 다국어 설정 저장: 사용자가 선택한 언어 설정은 localStorage에 저장되어, 다음 방문  시에도 동일한 언어로 콘텐츠를 볼 수 있습니다.

3. API 통신 및 오류 처리
    - TMDB API 연동: Axios를 사용하여 The Movie Database (TMDB) API와 통신합니다.
    - API 요청 관리:
        - 요청 인터셉터: Axios의 인터셉터를 활용하여 모든 요청에 API 키와 언어 설정을 자동으로 포함시킵니다.
        - 응답 캐싱 및 최적화: 반복되는 요청을 최소화하고 응답 데이터를 효율적으로 관리합니다.
    - 오류 메시지 처리:
        - 네트워크 오류 처리: API 호출 중 발생할 수 있는 네트워크 오류를 감지하고 사용자에게 알림 메시지를 표시합니다.
        - HTTP 오류 코드 처리: 404, 500 등 HTTP 오류 코드에 따른 적절한 대응을 합니다.
        - 사용자 친화적인 메시지: 기술적인 오류 메시지 대신 이해하기 쉬운 형태로 사용자에게 안내합니다.
            - 예: "데이터를 불러오는 중 에러가 발생했습니다. 잠시 후 다시 시도해주세요."
    - 로딩 상태 관리:
        - API 호출 중 로딩 인디케이터를 표시하여 사용자에게 진행 상황을 알립니다.
        - 로딩 상태는 Vue의 ref와 컴포넌트의 loading 변수를 통해 관리됩니다

4. 영화 검색 및 필터링
    - 장르, 평점, 언어 기반 필터링: 사용자는 원하는 조건을 선택하여 영화를 검색할 수 있습니다.
        - 장르 필터링: 다양한 장르(액션, 로맨스, 애니메이션 등) 중에서 선택 가능
        - 평점 필터링: 특정 평점 이상의 영화만 검색
        - 언어 필터링: 영어, 한국어, 일본어 등 원어 기준 필터링
    - 실시간 검색 결과 업데이트: 사용자가 필터를 변경할 때마다 결과가 즉시 업데이트됩니다.
    - 검색 결과 표시: 검색된 영화들은 카드 형태로 화면에 표시됩니다


5. 인기 영화 조회 가능
    - 인기 영화 목록 제공: TMDB API를 통해 현재 인기 있는 영화를 가져와 사용자에게 제공합니다.
    - 보기 모드 선택:
        - 테이블 형태: 영화의 포스터, 제목, 줄거리를 표 형태로 볼 수 있습니다.
        - 무한 스크롤: 스크롤을 내릴 때마다 새로운 인기 영화가 로드되어 연속적으로 볼 수 있습니다.
    - 페이지네이션: 테이블 형태에서는 이전/다음 버튼을 통해 페이지를 이동하며 영화를 탐색할 수 있습니다.

6. 위시리스트 기능
    - 영화 추가 및 제거: 사용자들은 마음에 드는 영화를 위시리스트에 추가하거나 제거할 수 있습니다.
    - 위시리스트 상태 유지: localStorage와 Vuex를 활용하여 사용자의 위시리스트를 지속적으로 관리합니다.
    - 위시리스트 페이지: 사용자가 저장한 영화들을 한눈에 볼 수 있는 전용 페이지를 제공합니다.
    - 아이콘 표시: 위시리스트에 추가된 영화는 따봉(👍) 아이콘이 표시되어 구분됩니다.

7. 다국어 지원
    - 언어 선택 기능: 헤더에서 한국어, 영어, 일본어 중 원하는 언어를 선택할 수 있습니다.
    - 언어 설정 유지: 선택한 언어는 localStorage에 저장되어 다음 방문 시에도 동일하게 적용됩니다.
    - API 언어 파라미터 적용: TMDB API 호출 시 선택한 언어에 따라 응답 데이터를 가져옵니다


8. 반응형 및 디자인 및 사용자 경험 향상
    - 반응형 UI: 다양한 디바이스(데스크톱, 태블릿, 모바일)에 최적화된 레이아웃을 제공합니다.
        - 미디어 쿼리 활용: 화면 크기에 따라 레이아웃과 스타일이 적절히 조정됩니다.
    - 애니메이션 및 인터랙션:
        - 호버 효과: 영화 카드에 마우스를 올리면 확대되는 효과를 줘서 시각적인 즐거움을 제공합니다.
        - 버튼 및 메뉴 인터랙션: 사용자 행동에 반응하는 부드러운 전환 효과를 적용했습니다.
    - 모달 창 활용:
        - 배너 영화의 상세 정보나 알림을 모달 창으로 표시하여 집중도를 높였습니다.

9. 네비게이션 및 라우팅
    - Vue Router를 통한 페이지 전환: 싱글 페이지 애플리케이션으로서 페이지 리로드 없이 부드러운 화면 전환을 제공합니다.
    - 네비게이션 가드: 인증이 필요한 페이지에 비인증 사용자가 접근하려 할 때 로그인 페이지로 리디렉션합니다.
    - 오류 처리 라우트: 존재하지 않는 경로로 접근 시 홈 또는 로그인 페이지로 리디렉션합니다.

10. 사용자 알림 시스템
    - Toast 메시지 제공: Vue Toastification 라이브러리를 사용하여 사용자에게 중요한 이벤트(로그인 성공/실패, 회원가입 성공/실패 등)를 알려줍니다.
    - 일관된 알림 스타일: 성공, 오류 등의 상황에 맞는 디자인과 메시지로 사용자 경험을 향상시켰습니다.

--------------------------------------
### 사용전략
1. Git Flow 브랜치 전략 적용
    - 브랜치 구조:
        - main : 배포 가능한 상태를 유지하는 브랜치입니다
        - develop : 개발 중인 기능들을 통합하는 브랜치입니다.
        - feature : 새로운 기능을 개발하기 위한 브랜치입니다.
        
2. Pull Request

3. CI 구축 및 자동화
    - 빌드 및 테스트 워크플로우 :
        - 코드가 develop 브랜치에 병합될 때 자동으로 빌드와 테스트를 수행합니다.
    - 배포 워크 플로우 : 
        - main 브랜치에 변경 사항이 발생하면 자동으로 프로덕션 환경에 배포합니다.
    - Slack 알림 연동 : 
        - 워크플로우의 결과를 Slack 채널에 알림으로 전송하여 팀원들이 실시간으로 확인할 수 있도록 하였습니다.

---------------------------------------
### 🤝 기여방법

1. fork 저장소를 합니다

2. Clone 한 저장소를 로컬로 가져옵니다.
    - git clone https://github.com/yourusername/yourproject.git

3. 새로운 브랜치를 생성합니다.
    - git checkout -b feature/your-feature

4. 변경사항을 커밋합니다.
    - git commit -m "feat: 설명"

5. 원격 저장소에 푸쉬합니다.
    - git push origin feature/your-feature



