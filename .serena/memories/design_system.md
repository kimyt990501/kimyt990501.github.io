# Portfolio Design System

## Theme System - Night/Day Mode Toggle

### 테마 전환
- **기본 모드**: Night Mode (다크 테마)
- **대체 모드**: Day Mode (라이트 테마)
- **토글 버튼**: 우측 상단 고정 원형 버튼
- **저장**: localStorage에 사용자 선택 저장
- **전환 효과**: 0.3s 부드러운 transition

## Color Palette - Night Mode (Default)

### Night Mode Colors
**Accent Colors:**
- Primary: `#60A5FA` (소프트 블루)
- Secondary: `#3B82F6` (모던 블루)
- Bright: `#BFDBFE` (밝은 블루)
- Dark: `#2563EB` (다크 블루)

**Background Colors:**
- Primary: `#0F172A` (다크 네이비)
- Secondary: `#1E293B` (카드 배경)
- Card: `#1E293B`

**Text Colors:**
- Primary: `#F8FAFC` (흰색에 가까운 밝은 회색)
- Secondary: `#E2E8F0` (밝은 회색)
- Muted: `#94A3B8` (중간 회색)

## Color Palette - Day Mode (Light)

### Day Mode Colors
**Accent Colors:**
- Primary: `#4B5563` (진한 회색)
- Secondary: `#374151` (더 진한 회색)
- Bright: `#6B7280` (중간 회색)
- Dark: `#1F2937` (거의 검정)

**Background Colors:**
- Primary: `#F5F3EE` (아이보리)
- Secondary: `#FFFFFF` (순백)
- Card: `#FFFFFF`
- Card Hover: `#F9F7F4` (밝은 아이보리)

**Text Colors:**
- Primary: `#1F2937` (거의 검정)
- Secondary: `#374151` (진한 회색)
- Muted: `#6B7280` (중간 회색)

### Text Colors
- **Primary Text**: `#F8FAFC` (매우 밝은 회색 - 본문, 더 높은 가독성)
- **Secondary Text**: `#E2E8F0` (밝은 회색 - 부가 설명)
- **Muted Text**: `#94A3B8` (흐릿한 회색 - 라벨)
- **Accent Text**: `#60A5FA` (소프트 블루 - 강조)

### Gradients
- **Primary Gradient**: `linear-gradient(135deg, #60A5FA 0%, #3B82F6 100%)`
- **Dark Gradient**: `linear-gradient(180deg, #0F172A 0%, #020617 100%)`
- **Card Gradient**: `linear-gradient(135deg, #1E293B 0%, #334155 100%)`

### Shadows
- **Small**: `0 2px 8px rgba(0, 0, 0, 0.4)`
- **Medium**: `0 4px 16px rgba(0, 0, 0, 0.5)`
- **Large**: `0 8px 32px rgba(0, 0, 0, 0.6)`
- **Extra Large**: `0 16px 48px rgba(0, 0, 0, 0.7)`
- **Accent Shadow**: `0 8px 32px rgba(96, 165, 250, 0.3)`

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
- **깔끔하고 전문적인**: 소프트 블루 컬러로 가독성 높고 세련된 느낌
- **높은 가독성**: 밝고 선명한 블루 톤으로 텍스트와 강조 요소가 명확하게 구분됨
- **일관성**: 모든 링크, 버튼, 강조 요소가 동일한 색상 팔레트 사용
- **포트폴리오 최적화**: 튀지 않으면서도 전문적인 인상을 주는 색상 선택

### Responsive Breakpoints
- **Desktop**: 1400px+ (2열 그리드, 가로 카드)
- **Tablet**: 969px - 1399px (1열 그리드, 가로 카드)
- **Mobile**: 968px 이하 (1열 그리드, 세로 카드)

## Key Design Decisions

1. **색상 변경 이유**: 기존 슬레이트 블루(#64748B)가 가독성이 낮음 → 소프트 블루(#60A5FA)로 변경하여 깔끔하고 가독성 높은 포트폴리오 디자인 구현
2. **카드 레이아웃**: 세로에서 가로로 변경하여 한 눈에 정보 파악 가능, 더 넓고 짧은 카드
3. **전역 링크 색상 통일**: 모든 링크를 슬레이트 블루로 강제하여 일관성 확보
4. **프로필 이미지**: `/assets/profile.jpeg` 사용

## File Locations

- **Design Tokens**: `_sass/_portfolio.scss` (line 4-41)
- **Color Overrides**: Throughout `_sass/_portfolio.scss`
- **Global Links**: `_sass/_portfolio.scss` (line 138-153)
- **Project Card Layout**: `_sass/_portfolio.scss` (line 591-700)
- **Hero Section**: `_sass/_portfolio.scss` (line 280-454)
