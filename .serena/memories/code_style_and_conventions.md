# 코드 스타일 및 규칙

## 블로그 포스트 규칙

### 파일명 규칙
- 형식: `YYYY-MM-DD-카테고리-설명.md`
- 예시: `2023-01-05-java-first.md`
- 위치: `_posts/카테고리명/` 디렉토리 내

### Front Matter 규칙
모든 포스트는 YAML front matter로 시작해야 함:

```yaml
---
title: "포스트 제목"
excerpt: "간단한 설명"

categories:
 - 카테고리명
tags:
 - [태그1, 태그2]

toc: true
toc_sticky: true

date: YYYY-MM-DD
last_modified_at: YYYY-MM-DD
---
```

### 필수 필드
- `title`: 포스트 제목
- `categories`: 카테고리 (Java, Spring, C++ 등)
- `tags`: 태그 배열
- `date`: 작성일

### 선택 필드
- `excerpt`: 포스트 요약
- `toc`: 목차 표시 여부
- `toc_sticky`: 고정 목차 여부
- `last_modified_at`: 최종 수정일

## 레이아웃 규칙

### 기본 레이아웃
- 포스트: `single` 레이아웃 사용
- 저자 프로필: 자동 표시
- 읽기 시간: 자동 계산 (200 단어/분)
- 댓글: utterances 사용
- 공유 버튼: 활성화
- 관련 포스트: 자동 표시
- 수학 수식: mathjax 지원

## 디렉토리 구조 규칙

### Jekyll 기본 디렉토리
- `_posts/`: 블로그 포스트 (카테고리별 하위 디렉토리)
- `_layouts/`: HTML 레이아웃 템플릿
- `_includes/`: 재사용 가능한 HTML 조각
- `_sass/`: Sass 스타일시트
- `_data/`: 데이터 파일
- `_pages/`: 정적 페이지
- `assets/`: 이미지, CSS, JS 등 정적 자산

### 제외된 파일/디렉토리
- `vendor/`
- `node_modules/`
- `_site/` (생성된 사이트)
- `.jekyll-cache/`
- `/docs/`, `/test/`

## 코딩 규칙

### JavaScript
- ES5 호환성 유지
- UglifyJS로 압축 및 최소화
- Banner 주석 자동 추가

### Sass/SCSS
- 압축된 스타일로 출력
- 파일 구조는 Minimal Mistakes 테마 구조 따름
- 커스텀 스타일은 `_portfolio.scss` 사용

### 마크다운
- GFM (GitHub Flavored Markdown) 사용
- 코드 블록은 펜스드 코드 블록 (```) 사용
- 언어 지정으로 문법 강조 활성화
