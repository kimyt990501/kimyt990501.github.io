# Portfolio Design System

## Color Palette - Professional Slate Blue Theme

### Primary Colors
- **Accent Primary**: `#64748B` (슬레이트 블루)
  - 용도: 버튼, 링크, 주요 강조 요소
- **Accent Secondary**: `#475569` (진한 슬레이트)
  - 용도: 그라데이션, 호버 상태, 방문한 링크
- **Accent Bright**: `#CBD5E1` (밝은 슬레이트)
  - 용도: Hero subtitle, 호버 상태, 강조 텍스트
- **Accent Dark**: `#334155` (다크 슬레이트)
  - 용도: 어두운 배경 요소

### Background Colors
- **Primary BG**: `#0F172A` (다크 네이비)
- **Secondary BG**: `#1E293B` (카드 배경)
- **Tertiary BG**: `#334155` (호버 배경)
- **Card BG**: `#1E293B`
- **Card Hover BG**: `#334155`

### Text Colors
- **Primary Text**: `#F1F5F9` (밝은 회색 - 본문)
- **Secondary Text**: `#CBD5E1` (중간 회색 - 부가 설명)
- **Muted Text**: `#94A3B8` (흐릿한 회색 - 라벨)
- **Accent Text**: `#64748B` (슬레이트 블루 - 강조)

### Gradients
- **Primary Gradient**: `linear-gradient(135deg, #64748B 0%, #475569 100%)`
- **Dark Gradient**: `linear-gradient(180deg, #0F172A 0%, #020617 100%)`
- **Card Gradient**: `linear-gradient(135deg, #1E293B 0%, #334155 100%)`

### Shadows
- **Small**: `0 2px 8px rgba(0, 0, 0, 0.4)`
- **Medium**: `0 4px 16px rgba(0, 0, 0, 0.5)`
- **Large**: `0 8px 32px rgba(0, 0, 0, 0.6)`
- **Extra Large**: `0 16px 48px rgba(0, 0, 0, 0.7)`
- **Accent Shadow**: `0 8px 32px rgba(100, 116, 139, 0.3)`

## Layout Structure

### Project Cards - Horizontal Layout
- **Grid**: 1열 (전체 너비 사용)
- **카드 구조**: 가로 레이아웃 (왼쪽: 이미지 320px, 오른쪽: 컨텐츠)
- **최소 높이**: 420px (데스크톱), 550px (모바일)
- **이미지 크기**: 320px × 전체 높이 (데스크톱), 100% × 200px (모바일)
- **반응형**: 968px 이하에서 세로 레이아웃으로 전환

### Card Flip Effect
- **3D 플립**: hover 시 rotateY(180deg)
- **앞면**: 프로젝트 상세 정보
- **뒷면**: 스크린샷 또는 플레이스홀더
- **Perspective**: 1500px
- **Transition**: 0.8s ease

## Typography

### Font Family
- Primary: 'Gowun Dodum' (한글 최적화)
- Fallback: System fonts

### Hero Section
- **Name**: clamp(2.5rem, 6vw, 4rem), 900 weight
- **Subtitle**: clamp(1.5rem, 3.5vw, 2.25rem), 800 weight, accent-bright color
- **Title**: clamp(1.3rem, 2.5vw, 1.8rem), 600 weight
- **Description Primary**: clamp(1.1rem, 2.2vw, 1.3rem), 600 weight, accent-primary color
- **Description Secondary**: clamp(0.95rem, 1.8vw, 1.05rem), 400 weight, muted color

### Section Titles
- **Title**: clamp(2.5rem, 5vw, 3.5rem), 800 weight
- **Subtitle**: 1.15rem, 400 weight, secondary text color

### Project Cards
- **Title**: 1.65rem, 800 weight
- **Subtitle**: 1rem, 600 weight, accent-primary color
- **Body Text**: 0.9-0.95rem, 400-500 weight

## Design Philosophy

### Theme Characteristics
- **차분하고 전문적인**: 슬레이트 블루 컬러로 미니멀하고 고급스러운 느낌
- **AI 템플릿 느낌 제거**: 청록색(Cyan) 제거, 슬레이트 계열로 통일
- **일관성**: 모든 링크, 버튼, 강조 요소가 동일한 색상 팔레트 사용
- **가독성**: 어두운 배경에 밝은 텍스트, 충분한 대비

### Responsive Breakpoints
- **Desktop**: 1400px+ (2열 그리드, 가로 카드)
- **Tablet**: 969px - 1399px (1열 그리드, 가로 카드)
- **Mobile**: 968px 이하 (1열 그리드, 세로 카드)

## Key Design Decisions

1. **색상 변경 이유**: 기존 청록색(#06B6D4)이 너무 AI 템플릿 느낌 → 슬레이트 블루(#64748B)로 변경하여 전문적이고 차별화된 느낌
2. **카드 레이아웃**: 세로에서 가로로 변경하여 한 눈에 정보 파악 가능, 더 넓고 짧은 카드
3. **전역 링크 색상 통일**: 모든 링크를 슬레이트 블루로 강제하여 일관성 확보
4. **프로필 이미지**: `/assets/profile.jpeg` 사용

## File Locations

- **Design Tokens**: `_sass/_portfolio.scss` (line 4-41)
- **Color Overrides**: Throughout `_sass/_portfolio.scss`
- **Global Links**: `_sass/_portfolio.scss` (line 138-153)
- **Project Card Layout**: `_sass/_portfolio.scss` (line 591-700)
- **Hero Section**: `_sass/_portfolio.scss` (line 280-454)
