# 권장 명령어

## Ruby/Jekyll 명령어

### 의존성 설치
```bash
bundle install
```
프로젝트의 Ruby gem 의존성을 설치합니다.

### 의존성 업데이트
```bash
bundle update
```
번들된 gem들을 업데이트합니다.

### 로컬 서버 실행 (개발용)
```bash
bundle exec rake preview
```
테스트 디렉토리를 사용하여 http://localhost:4000/test/ 에서 Jekyll 서버를 시작합니다.
파일 변경 시 자동으로 재생성됩니다.

또는 표준 Jekyll 서버:
```bash
bundle exec jekyll serve
```
기본 포트 4000에서 로컬 서버를 실행합니다.

### 사이트 빌드
```bash
bundle exec jekyll build
```
정적 사이트를 `_site/` 디렉토리에 생성합니다.

## Node.js/npm 명령어

### npm 의존성 설치
```bash
npm install
```

### JavaScript 빌드
```bash
npm run build:js
```
JavaScript 파일들을 uglify하고 banner를 추가하여 `assets/js/main.min.js`를 생성합니다.

### JavaScript uglify만 실행
```bash
npm run uglify
```

### JavaScript 파일 감시
```bash
npm run watch:js
```
JavaScript 파일 변경 시 자동으로 빌드합니다.

## Git 명령어

### 상태 확인
```bash
git status
```

### 변경사항 커밋
```bash
git add .
git commit -m "커밋 메시지"
git push origin main
```

## Darwin/macOS 시스템 명령어

### 디렉토리 탐색
```bash
ls -la          # 숨김 파일 포함 상세 목록
cd [directory]  # 디렉토리 이동
pwd            # 현재 경로 출력
```

### 파일 검색
```bash
find . -name "*.md"           # 마크다운 파일 찾기
grep -r "검색어" .             # 재귀적으로 텍스트 검색
```

### 파일 조작
```bash
cat [file]      # 파일 내용 출력
less [file]     # 페이지별로 파일 보기
head -n 20 [file]  # 파일의 첫 20줄 보기
tail -n 20 [file]  # 파일의 마지막 20줄 보기
```

## 유용한 Jekyll 명령어

### 드래프트 포함 실행
```bash
bundle exec jekyll serve --drafts
```

### 증분 빌드 (더 빠름)
```bash
bundle exec jekyll serve --incremental
```

### 미래 날짜 포스트 포함
```bash
bundle exec jekyll serve --future
```

### 상세 로그
```bash
bundle exec jekyll serve --verbose
```

### 특정 포트 지정
```bash
bundle exec jekyll serve --port 4001
```
