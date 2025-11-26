# 작업 완료 시 체크리스트

## 새 블로그 포스트 작성 시

1. **파일명 규칙 확인**
   - 형식: `YYYY-MM-DD-카테고리-설명.md`
   - 적절한 카테고리 디렉토리에 저장 (`_posts/java/`, `_posts/cpp/`, `_posts/spring/`)

2. **Front Matter 검증**
   - 필수 필드 포함 확인: title, categories, tags, date
   - YAML 문법 오류 없는지 확인

3. **마크다운 검증**
   - 코드 블록에 언어 지정 확인
   - 링크 및 이미지 경로 확인
   - 헤딩 구조 적절한지 확인

4. **로컬 테스트**
   ```bash
   bundle exec jekyll serve
   ```
   - http://localhost:4000 에서 포스트 렌더링 확인
   - 레이아웃 및 스타일 정상 작동 확인
   - 목차(ToC) 정상 생성 확인

## 스타일 변경 시

1. **Sass 파일 수정**
   - `_sass/` 디렉토리에서 작업
   - 커스텀 스타일은 `_sass/_portfolio.scss` 사용

2. **빌드 확인**
   - Jekyll 서버 재시작하여 변경사항 반영 확인
   - 브라우저 캐시 클리어

3. **반응형 테스트**
   - 다양한 화면 크기에서 확인

## JavaScript 변경 시

1. **소스 파일 수정**
   - `assets/js/` 디렉토리의 소스 파일 수정
   - `assets/js/main.min.js`는 직접 수정 금지 (생성 파일)

2. **빌드 실행**
   ```bash
   npm run build:js
   ```

3. **테스트**
   - 브라우저에서 기능 정상 작동 확인
   - 콘솔 에러 없는지 확인

## Git 커밋 전

1. **변경사항 확인**
   ```bash
   git status
   git diff
   ```

2. **불필요한 파일 제외**
   - `_site/`, `.jekyll-cache/`, `.sass-cache/` 커밋 금지
   - `.gitignore` 파일 참고

3. **의미있는 커밋 메시지 작성**
   - 변경사항을 명확히 설명
   - 예: "style : 디자인 개선", "feat : 새 포스트 추가"

## 배포 전 확인사항

1. **빌드 성공 확인**
   ```bash
   bundle exec jekyll build
   ```
   - 에러 메시지 없이 빌드 완료 확인

2. **설정 파일 검증**
   - `_config.yml` 문법 오류 없는지 확인
   - 필수 플러그인 (특히 jekyll-include-cache) 포함 확인

3. **링크 확인**
   - 내부 링크 정상 작동 확인
   - 이미지 경로 정확한지 확인

4. **메타데이터 확인**
   - SEO 관련 정보 적절한지 확인
   - Open Graph 이미지 설정 확인

## GitHub Pages 배포 후

1. **사이트 접근 확인**
   - kimyt990501.github.io 정상 접근 확인

2. **포스트 렌더링 확인**
   - 새 포스트가 목록에 표시되는지 확인
   - 카테고리/태그 아카이브 정상 작동 확인

3. **댓글 시스템 확인**
   - utterances 정상 작동 확인

4. **Analytics 확인**
   - Google Analytics 추적 정상 작동 확인 (선택사항)

## 주의사항

- `_config.yml` 변경 시 Jekyll 서버 재시작 필수
- GitHub Pages는 특정 플러그인만 지원하므로 새 플러그인 추가 시 호환성 확인
- remote_theme 사용 중이므로 테마 업데이트 시 변경사항 확인
- 로컬 테스트 없이 직접 배포하지 않기
