# 코드베이스 구조

## 루트 디렉토리
```
kimyt990501.github.io/
├── _config.yml           # Jekyll 메인 설정 파일
├── index.html           # 홈페이지
├── package.json         # npm 의존성
├── Gemfile             # Ruby gem 의존성
├── Rakefile            # Rake 작업 정의
└── banner.js           # JavaScript 배너 추가 스크립트
```

## 주요 디렉토리

### `_posts/` - 블로그 포스트
```
_posts/
├── java/      # Java 학습 포스트
├── cpp/       # C++ 학습 포스트
└── spring/    # Spring 프레임워크 포스트
```
- 마크다운 형식의 블로그 글
- 파일명: `YYYY-MM-DD-제목.md`

### `_layouts/` - 레이아웃 템플릿
```
_layouts/
├── default.html          # 기본 레이아웃
├── single.html          # 단일 포스트 레이아웃
├── home.html           # 홈페이지 레이아웃
├── archive.html        # 아카이브 레이아웃
├── archive-taxonomy.html # 카테고리/태그 아카이브
├── posts.html          # 포스트 목록
├── categories.html     # 카테고리 페이지
├── tags.html          # 태그 페이지
├── portfolio.html     # 포트폴리오 레이아웃
└── ...
```

### `_includes/` - 재사용 가능한 HTML 조각
```
_includes/
├── head.html                 # HTML head 섹션
├── header.html              # 사이트 헤더
├── footer.html              # 사이트 푸터
├── masthead.html           # 상단 네비게이션
├── sidebar.html            # 사이드바
├── author-profile.html     # 저자 프로필
├── comments.html           # 댓글 섹션
├── analytics.html          # Analytics 스크립트
├── toc.html               # 목차
├── scripts.html           # JavaScript 로딩
├── head/                  # head 관련 하위 include
├── footer/               # footer 관련 하위 include
├── comments-providers/   # 댓글 제공자별 템플릿
├── analytics-providers/  # Analytics 제공자별 템플릿
└── search/              # 검색 관련 템플릿
```

### `_sass/` - Sass 스타일시트
```
_sass/
├── minimal-mistakes.scss     # 메인 Sass 파일
├── _portfolio.scss          # 커스텀 포트폴리오 스타일
└── minimal-mistakes/        # 테마 Sass 컴포넌트
```

### `assets/` - 정적 자산
```
assets/
├── css/              # 컴파일된 CSS
├── js/              # JavaScript 파일
│   ├── main.min.js     # 압축된 메인 JS (생성 파일)
│   ├── _main.js        # 메인 JS 소스
│   ├── vendor/         # 외부 라이브러리 (jQuery 등)
│   └── plugins/        # jQuery 플러그인
├── codingcat.jpeg   # 프로필/OG 이미지
└── logo.ico/        # 파비콘
```

### `_pages/` - 정적 페이지
- 카테고리, 태그, About 페이지 등
- Jekyll에 의해 include됨

### `_data/` - 데이터 파일
- YAML, JSON, CSV 형식의 데이터
- 네비게이션, 작성자 정보 등

### `_codes/` - 코드 관련
- 코드 샘플이나 코드 컬렉션

### `docs/` - 문서
- Minimal Mistakes 테마 문서
- 빌드 시 제외됨

## 생성된 디렉토리 (Git 제외)

### `_site/`
- Jekyll이 생성한 최종 정적 사이트
- GitHub Pages에 배포되는 내용
- `.gitignore`에 포함

### `.sass-cache/`, `.jekyll-cache/`, `.jekyll-metadata`
- Jekyll 및 Sass 캐시 파일
- `.gitignore`에 포함

### `vendor/`
- Bundle로 설치된 gem들
- `.gitignore`에 포함

## 설정 파일

### `_config.yml`
- Jekyll 메인 설정
- 사이트 메타데이터
- 테마 설정
- 플러그인 설정
- 빌드 설정

### `package.json`
- npm 의존성
- JavaScript 빌드 스크립트

### `Gemfile`
- Ruby gem 의존성
- Jekyll 및 플러그인

### `.gitignore`
- Git에서 제외할 파일/디렉토리

## 기타 파일

- `sitemap.xml` - 사이트맵
- `robots.txt` - 검색 엔진 크롤러 설정
- `google412bc11572fe3a7c.html` - Google 사이트 인증
- `staticman.yml` - Staticman 댓글 설정 (현재 미사용)
- `LICENSE` - MIT 라이선스
- `README.md` - 프로젝트 설명
- `CHANGELOG.md` - 변경 이력
