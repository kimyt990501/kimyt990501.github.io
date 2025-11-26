# 프로젝트 스크린샷 가이드

이 디렉토리는 포트폴리오 프로젝트 카드의 스크린샷 이미지를 저장합니다.

## 📁 파일 위치
```
/assets/images/projects/
```

## 📝 파일 명명 규칙

각 프로젝트의 스크린샷은 다음 형식으로 저장하세요:

### 현재 프로젝트 파일명:
1. **Deciphish** → `deciphish-screenshot.png`
2. **Enterprise ERP System** → `erp-screenshot.png`
3. **Multi-Language Sign Language Translator** → `signlang-screenshot.png`

### 새 프로젝트 추가 시:
- 프로젝트명을 소문자로 변환
- 공백은 하이픈(-)으로 대체
- `-screenshot.png` 또는 `-screenshot.jpg` 추가

**예시:**
- "My Awesome Project" → `my-awesome-project-screenshot.png`
- "AI Chat Bot" → `ai-chat-bot-screenshot.png`

## 🖼️ 이미지 사양

### 권장 크기:
- **가로:** 1200px - 1600px
- **세로:** 800px - 1000px
- **비율:** 4:3 또는 16:10 (가로형 권장)

### 파일 형식:
- PNG (권장) - 투명 배경 지원
- JPG - 용량이 작음

### 파일 크기:
- 500KB ~ 2MB 권장
- 3MB 이하 유지 (페이지 로딩 속도 고려)

## ✨ 스크린샷 촬영 팁

1. **고해상도 화면에서 촬영**
   - 최소 1920x1080 해상도에서 캡처
   - 레티나/HiDPI 화면 권장

2. **핵심 기능이 보이도록**
   - 대시보드, 메인 UI, 핵심 기능 화면
   - 프로젝트의 가장 인상적인 부분

3. **깔끔한 배경**
   - 개발자 도구, 브라우저 탭 등 불필요한 요소 제거
   - 전체 화면 캡처 후 자르기

4. **일관된 스타일**
   - 모든 프로젝트 스크린샷의 톤과 스타일 통일
   - 브라우저 프레임 포함 여부 일관성 유지

## 🔧 이미지 최적화 도구

스크린샷을 추가하기 전에 최적화하세요:

- **TinyPNG** - https://tinypng.com
- **ImageOptim** (Mac) - https://imageoptim.com
- **Squoosh** - https://squoosh.app

## 📋 체크리스트

스크린샷 추가 전 확인사항:
- [ ] 파일명이 명명 규칙에 맞는가?
- [ ] 이미지 크기가 권장 사양인가?
- [ ] 파일 크기가 3MB 이하인가?
- [ ] 이미지가 최적화되었는가?
- [ ] 핵심 기능이 잘 보이는가?
- [ ] `_data/portfolio.yml`의 `screenshot` 경로가 올바른가?

## 🎨 카드 플립 효과

### 작동 방식:
- **데스크톱:** 마우스를 프로젝트 카드에 올리면 자동으로 뒤집혀서 스크린샷 표시
- **모바일/태블릿:** 카드를 탭하면 뒤집힘, 다시 탭하면 원래대로

### portfolio.yml 설정 예시:
```yaml
projects:
  - title: "Your Project"
    subtitle: "프로젝트 설명"
    # ... 다른 필드들 ...
    screenshot: "/assets/images/projects/your-project-screenshot.png"
```

## 🚀 스크린샷 추가 후

1. Git에 추가 및 커밋:
```bash
git add assets/images/projects/
git commit -m "feat: Add project screenshots for card flip effect"
git push
```

2. Jekyll 서버 재시작:
```bash
bundle exec jekyll serve
```

3. 브라우저에서 확인:
   - http://localhost:4000
   - 프로젝트 섹션으로 스크롤
   - 카드에 마우스를 올려 플립 효과 확인

## ❓ 문제 해결

### 스크린샷이 보이지 않는 경우:
1. 파일 경로가 정확한지 확인 (`/assets/images/projects/파일명.png`)
2. 파일명의 대소문자가 일치하는지 확인
3. 브라우저 캐시 삭제 후 새로고침 (Ctrl+Shift+R / Cmd+Shift+R)

### 카드가 뒤집히지 않는 경우:
1. `portfolio.yml`에 `screenshot` 필드가 있는지 확인
2. CSS가 올바르게 로드되었는지 확인
3. 브라우저 개발자 도구에서 에러 확인

## 📸 임시 플레이스홀더

스크린샷이 준비되지 않은 경우, 임시로 다음을 사용할 수 있습니다:
- https://placehold.co/1400x900/0F172A/06B6D4?text=Project+Screenshot
- 프로젝트 로고나 아이콘
- 아키텍처 다이어그램

---

**마지막 업데이트:** 2025-01-26
**관련 파일:**
- `_layouts/portfolio.html` - 프로젝트 카드 레이아웃
- `_sass/_portfolio.scss` - 카드 플립 효과 스타일
- `_data/portfolio.yml` - 프로젝트 데이터
