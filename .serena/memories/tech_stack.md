# 기술 스택

## 주요 기술

### Jekyll (정적 사이트 생성기)
- **버전**: >= 3.7
- **역할**: 마크다운 파일을 정적 HTML로 변환
- **설정 파일**: `_config.yml`

### Ruby 기반
- **Bundler**: 의존성 관리
- **Gemfile**: Ruby gem 의존성 정의
- **minimal-mistakes-jekyll**: 테마 gem

### JavaScript 관련
- **Node.js**: >= 0.10.0
- **npm 패키지**:
  - `npm-run-all`: ^4.1.5
  - `onchange`: ^7.1.0
  - `uglify-js`: ^3.13.6

### 마크다운 처리
- **Markdown 엔진**: kramdown
- **문법 강조**: rouge
- **마크다운 확장자**: markdown, mkdown, mkdn, mkd, md

### 스타일링
- **Sass/SCSS**: CSS 전처리기
- **Sass 디렉토리**: `_sass`
- **스타일**: compressed
- **커스텀 스타일**: `_sass/_portfolio.scss`

### Jekyll 플러그인
- jekyll-paginate: 페이지네이션
- jekyll-sitemap: 사이트맵 생성
- jekyll-gist: GitHub Gist 임베딩
- jekyll-feed: RSS 피드 생성
- jekyll-include-cache: include 캐싱 (필수)

### 외부 서비스
- **GitHub Pages**: 호스팅
- **utterances**: 댓글 시스템 (photon-dark 테마)
- **Google Analytics**: Google Tag Manager (gtag)

### JavaScript 라이브러리
- jQuery 3.6.0
- FitVids.js
- Magnific Popup
- Smooth Scroll
- Gumshoe
- GreedyNav
