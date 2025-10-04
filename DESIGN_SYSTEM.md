# 🎨 Design System Documentation

> 야놀자 그룹 디자인 시스템을 기반으로 한 재사용 가능한 디자인 시스템

## 목차
1. [색상 시스템](#색상-시스템)
2. [타이포그래피](#타이포그래피)
3. [간격 시스템](#간격-시스템)
4. [Border Radius](#border-radius)
5. [그림자](#그림자)
6. [그라디언트](#그라디언트)
7. [애니메이션](#애니메이션)
8. [컴포넌트](#컴포넌트)
9. [레이아웃](#레이아웃)
10. [반응형 디자인](#반응형-디자인)

---

## 색상 시스템

### Primary Colors (주요 색상)

```css
--color-primary: #FF385C;        /* 핑크 - 주요 액션 */
--color-primary-dark: #E31C5F;   /* 다크 핑크 - 호버 상태 */
--color-primary-light: #FF5A7E;  /* 라이트 핑크 - 백그라운드 */
```

**사용 예시:**
- 주요 CTA 버튼
- 중요한 링크
- 액센트 요소
- 그라디언트 텍스트

### Secondary Colors (보조 색상)

```css
--color-secondary: #00D9FF;      /* 사이안 - 보조 액션 */
--color-accent: #A855F7;         /* 퍼플 - 강조 */
```

**사용 예시:**
- 보조 버튼
- 아이콘
- 그라디언트 배경
- 데코레이션 요소

### Dark Shades (다크 색상)

```css
--color-dark: #0F0F23;           /* 메인 다크 */
--color-dark-secondary: #1A1A2E; /* 섹션 배경 */
--color-dark-tertiary: #16213E;  /* 카드 배경 */
```

**사용 예시:**
- 페이지 배경
- 섹션 구분
- 카드/컨테이너 배경
- 다크 테마

### Light & Gray Scale

```css
--color-light: #FFFFFF;          /* 순수 화이트 */
--color-gray-100: #F7F7F7;       /* 가장 밝은 그레이 */
--color-gray-200: #E5E5E5;
--color-gray-300: #D4D4D4;
--color-gray-400: #A3A3A3;
--color-gray-500: #737373;       /* 중간 그레이 */
--color-gray-600: #525252;
--color-gray-700: #404040;
--color-gray-800: #262626;
--color-gray-900: #171717;       /* 가장 어두운 그레이 */
```

**사용 예시:**
- 텍스트 (gray-300 ~ gray-900)
- 보더 (gray-200 ~ gray-400)
- 배경 (gray-100 ~ gray-200)
- 비활성 요소 (gray-400 ~ gray-500)

### Color Usage Guide

| 용도 | 색상 | 예시 |
|-----|------|------|
| 주요 텍스트 | `--color-light` | 헤딩, 본문 (다크 배경) |
| 보조 텍스트 | `--color-gray-300` | 설명, 캡션 |
| 주요 액션 | `--color-primary` | 버튼, 링크 |
| 보조 액션 | `--color-secondary` | 보조 버튼 |
| 성공 | `--color-accent` | 성공 메시지 |
| 배경 (다크) | `--color-dark` | 페이지 배경 |
| 섹션 배경 | `--color-dark-secondary` | 교차 섹션 |

---

## 그라디언트

### Primary Gradient

```css
--gradient-primary: linear-gradient(135deg, #FF385C 0%, #A855F7 100%);
```

**사용 예시:**
```css
.gradient-text {
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.gradient-button {
  background: var(--gradient-primary);
  color: white;
}
```

### Secondary Gradient

```css
--gradient-secondary: linear-gradient(135deg, #00D9FF 0%, #0EA5E9 100%);
```

### Dark Gradient

```css
--gradient-dark: linear-gradient(180deg, #0F0F23 0%, #1A1A2E 100%);
```

---

## 타이포그래피

### Font Families

```css
--font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-korean: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

**사용법:**
```css
body {
  font-family: var(--font-primary), var(--font-korean);
}
```

### Font Sizes

| 변수 | 크기 | 용도 |
|------|------|------|
| `--font-size-xs` | 0.75rem (12px) | 캡션, 라벨 |
| `--font-size-sm` | 0.875rem (14px) | 작은 텍스트 |
| `--font-size-base` | 1rem (16px) | 본문 텍스트 |
| `--font-size-lg` | 1.125rem (18px) | 부제목 |
| `--font-size-xl` | 1.25rem (20px) | 소제목 |
| `--font-size-2xl` | 1.5rem (24px) | 섹션 라벨 |
| `--font-size-3xl` | 1.875rem (30px) | H3 |
| `--font-size-4xl` | 2.25rem (36px) | H2 |
| `--font-size-5xl` | 3rem (48px) | H1 |
| `--font-size-6xl` | 3.75rem (60px) | 히어로 타이틀 |
| `--font-size-7xl` | 4.5rem (72px) | 대형 디스플레이 |

### Font Weights

```css
--font-weight-light: 300;    /* 가벼운 텍스트 */
--font-weight-normal: 400;   /* 일반 텍스트 */
--font-weight-medium: 500;   /* 중간 강조 */
--font-weight-bold: 700;     /* 강한 강조 */
--font-weight-black: 900;    /* 헤딩, 숫자 */
```

### Line Heights

```css
--line-height-tight: 1.2;    /* 헤딩 */
--line-height-normal: 1.5;   /* 본문 */
--line-height-relaxed: 1.75; /* 긴 텍스트 */
```

### Typography Scale 사용 예시

```css
/* 헤딩 */
h1 {
  font-size: var(--font-size-6xl);
  font-weight: var(--font-weight-black);
  line-height: var(--line-height-tight);
}

h2 {
  font-size: var(--font-size-5xl);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
}

h3 {
  font-size: var(--font-size-4xl);
  font-weight: var(--font-weight-bold);
}

/* 본문 */
p {
  font-size: var(--font-size-base);
  line-height: var(--line-height-relaxed);
}

/* 작은 텍스트 */
small {
  font-size: var(--font-size-sm);
}
```

---

## 간격 시스템

8px 기반의 일관된 간격 시스템을 사용합니다.

```css
--spacing-xs: 0.5rem;   /* 8px */
--spacing-sm: 1rem;     /* 16px */
--spacing-md: 1.5rem;   /* 24px */
--spacing-lg: 2rem;     /* 32px */
--spacing-xl: 3rem;     /* 48px */
--spacing-2xl: 4rem;    /* 64px */
--spacing-3xl: 6rem;    /* 96px */
--spacing-4xl: 8rem;    /* 128px */
```

### 간격 사용 가이드

| 용도 | 권장 간격 |
|------|----------|
| 컴포넌트 내부 패딩 (작음) | `--spacing-xs`, `--spacing-sm` |
| 컴포넌트 내부 패딩 (일반) | `--spacing-md`, `--spacing-lg` |
| 컴포넌트 간 여백 | `--spacing-lg`, `--spacing-xl` |
| 섹션 간 여백 | `--spacing-2xl`, `--spacing-3xl` |
| 페이지 패딩 | `--spacing-3xl`, `--spacing-4xl` |

### 사용 예시

```css
/* 카드 패딩 */
.card {
  padding: var(--spacing-lg);
}

/* 섹션 간격 */
section {
  padding: var(--spacing-4xl) 0;
}

/* 버튼 간격 */
.button-group {
  gap: var(--spacing-md);
}
```

---

## Border Radius

```css
--radius-sm: 0.375rem;   /* 6px - 작은 요소 */
--radius-md: 0.5rem;     /* 8px - 일반 */
--radius-lg: 0.75rem;    /* 12px - 버튼, 인풋 */
--radius-xl: 1rem;       /* 16px - 카드 */
--radius-2xl: 1.5rem;    /* 24px - 대형 카드 */
--radius-full: 9999px;   /* 완전 둥근 모양 */
```

### 사용 예시

```css
/* 버튼 */
.btn {
  border-radius: var(--radius-lg);
}

/* 카드 */
.card {
  border-radius: var(--radius-xl);
}

/* 뱃지 */
.badge {
  border-radius: var(--radius-full);
}

/* 이미지 */
.profile-image {
  border-radius: var(--radius-full);
}
```

---

## 그림자

```css
--shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
--shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
--shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
--shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
--shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
```

### 그림자 사용 가이드

| 용도 | 그림자 |
|------|--------|
| 텍스트 필드, 작은 요소 | `--shadow-sm` |
| 버튼, 카드 (기본) | `--shadow-md` |
| 드롭다운, 툴팁 | `--shadow-lg` |
| 모달, 팝업 | `--shadow-xl` |
| 대형 요소 (호버) | `--shadow-2xl` |

### 사용 예시

```css
/* 카드 */
.card {
  box-shadow: var(--shadow-md);
}

/* 호버 효과 */
.card:hover {
  box-shadow: var(--shadow-xl);
  transform: translateY(-4px);
}

/* 모달 */
.modal {
  box-shadow: var(--shadow-2xl);
}
```

---

## 애니메이션

### Transitions

```css
--transition-fast: 150ms ease-in-out;   /* 빠른 인터랙션 */
--transition-base: 300ms ease-in-out;   /* 기본 */
--transition-slow: 500ms ease-in-out;   /* 부드러운 효과 */
```

### 사용 예시

```css
/* 버튼 호버 */
.btn {
  transition: all var(--transition-base);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

/* 메뉴 토글 */
.nav-menu {
  transition: all var(--transition-fast);
}

/* 페이드 효과 */
.fade-element {
  transition: opacity var(--transition-slow);
}
```

### 주요 애니메이션 효과

#### 1. Float Animation (부동 효과)

```css
@keyframes float {
  0%, 100% { 
    transform: translate(0, 0); 
  }
  50% { 
    transform: translate(30px, 30px); 
  }
}

.floating-element {
  animation: float 8s ease-in-out infinite;
}
```

#### 2. Scroll Animation (스크롤 인디케이터)

```css
@keyframes scroll {
  0% { 
    opacity: 1; 
    transform: translateX(-50%) translateY(0); 
  }
  100% { 
    opacity: 0; 
    transform: translateX(-50%) translateY(15px); 
  }
}

.scroll-indicator::before {
  animation: scroll 2s infinite;
}
```

#### 3. Gradient Animation

```css
@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.gradient-text {
  background: linear-gradient(90deg, #FF385C, #A855F7, #00D9FF);
  background-size: 300% 300%;
  animation: gradient 8s ease infinite;
}
```

---

## 컴포넌트

### 버튼

#### Primary Button

```css
.btn-primary {
  padding: 1rem 2rem;
  background: var(--gradient-primary);
  color: var(--color-light);
  border: none;
  border-radius: var(--radius-lg);
  font-weight: var(--font-weight-medium);
  transition: var(--transition-base);
  cursor: pointer;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 30px rgba(255, 56, 92, 0.3);
}
```

**HTML 사용 예시:**
```html
<button class="btn btn-primary">클릭하기</button>
```

#### Secondary Button

```css
.btn-secondary {
  padding: 1rem 2rem;
  background: transparent;
  color: var(--color-light);
  border: 2px solid var(--color-light);
  border-radius: var(--radius-lg);
  font-weight: var(--font-weight-medium);
  transition: var(--transition-base);
}

.btn-secondary:hover {
  background: var(--color-light);
  color: var(--color-dark);
}
```

### 카드

```css
.card {
  padding: var(--spacing-xl);
  background: rgba(255, 255, 255, 0.05);
  border-radius: var(--radius-xl);
  border: 1px solid rgba(255, 255, 255, 0.1);
  transition: var(--transition-base);
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-xl);
  border-color: var(--color-primary);
}
```

**HTML 사용 예시:**
```html
<div class="card">
  <h3>카드 제목</h3>
  <p>카드 내용...</p>
</div>
```

### 입력 필드

```css
.form-input {
  width: 100%;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: var(--radius-lg);
  color: var(--color-light);
  font-family: inherit;
  font-size: var(--font-size-base);
  transition: var(--transition-fast);
}

.form-input:focus {
  outline: none;
  border-color: var(--color-primary);
  box-shadow: 0 0 0 3px rgba(255, 56, 92, 0.1);
}
```

### 배지

```css
.badge {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: rgba(255, 56, 92, 0.1);
  color: var(--color-primary);
  border-radius: var(--radius-full);
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-medium);
  text-transform: uppercase;
  letter-spacing: 1px;
}
```

---

## 레이아웃

### Container

```css
--container-max-width: 1280px;
--container-padding: 1.5rem;

.container {
  max-width: var(--container-max-width);
  margin: 0 auto;
  padding: 0 var(--container-padding);
}
```

### Grid System

```css
/* 자동 반응형 그리드 */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--spacing-lg);
}

/* 고정 컬럼 그리드 */
.grid-2 { grid-template-columns: repeat(2, 1fr); }
.grid-3 { grid-template-columns: repeat(3, 1fr); }
.grid-4 { grid-template-columns: repeat(4, 1fr); }
```

### Flexbox Utilities

```css
.flex {
  display: flex;
}

.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.flex-between {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.flex-col {
  display: flex;
  flex-direction: column;
}
```

---

## 반응형 디자인

### Breakpoints

```css
--breakpoint-sm: 640px;   /* 모바일 가로 */
--breakpoint-md: 768px;   /* 태블릿 */
--breakpoint-lg: 1024px;  /* 데스크톱 */
--breakpoint-xl: 1280px;  /* 대형 데스크톱 */
--breakpoint-2xl: 1536px; /* 초대형 데스크톱 */
```

### 미디어 쿼리 사용법

```css
/* Mobile First 접근 방식 */

/* 기본 (모바일) 스타일 */
.element {
  font-size: 1rem;
  padding: 1rem;
}

/* 태블릿 (768px 이상) */
@media (min-width: 768px) {
  .element {
    font-size: 1.125rem;
    padding: 1.5rem;
  }
}

/* 데스크톱 (1024px 이상) */
@media (min-width: 1024px) {
  .element {
    font-size: 1.25rem;
    padding: 2rem;
  }
}
```

### 반응형 타이포그래피

```css
/* 모바일 */
h1 {
  font-size: var(--font-size-4xl); /* 36px */
}

/* 태블릿 */
@media (min-width: 768px) {
  h1 {
    font-size: var(--font-size-5xl); /* 48px */
  }
}

/* 데스크톱 */
@media (min-width: 1024px) {
  h1 {
    font-size: var(--font-size-6xl); /* 60px */
  }
}
```

### 반응형 그리드

```css
.services-grid {
  display: grid;
  gap: var(--spacing-lg);
}

/* 모바일: 1열 */
.services-grid {
  grid-template-columns: 1fr;
}

/* 태블릿: 2열 */
@media (min-width: 768px) {
  .services-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* 데스크톱: 3열 */
@media (min-width: 1024px) {
  .services-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

---

## Z-Index Scale

```css
--z-dropdown: 1000;
--z-sticky: 1020;
--z-fixed: 1030;
--z-modal-backdrop: 1040;
--z-modal: 1050;
--z-popover: 1060;
--z-tooltip: 1070;
```

### 사용 예시

```css
.navbar {
  z-index: var(--z-fixed);
}

.modal-backdrop {
  z-index: var(--z-modal-backdrop);
}

.modal {
  z-index: var(--z-modal);
}
```

---

## 접근성 가이드

### 색상 대비

- **텍스트와 배경 대비비**: 최소 4.5:1 (WCAG AA)
- **큰 텍스트 대비비**: 최소 3:1
- **그래픽 요소**: 최소 3:1

### Focus States

```css
/* 모든 인터랙티브 요소에 포커스 스타일 추가 */
button:focus,
a:focus,
input:focus {
  outline: 2px solid var(--color-primary);
  outline-offset: 2px;
}

/* 또는 커스텀 포커스 링 */
.custom-focus:focus {
  box-shadow: 0 0 0 3px rgba(255, 56, 92, 0.3);
}
```

### 터치 타겟

```css
/* 모바일 터치 타겟 최소 크기: 44px x 44px */
.btn-mobile {
  min-height: 44px;
  min-width: 44px;
  padding: 0.75rem 1.5rem;
}
```

---

## 다크 테마 (선택사항)

```css
[data-theme="dark"] {
  --color-background: var(--color-dark);
  --color-surface: var(--color-dark-secondary);
  --color-text-primary: var(--color-light);
  --color-text-secondary: var(--color-gray-300);
}
```

---

## 실제 적용 예시

### 새 프로젝트에 적용하기

1. **CSS 변수 파일 생성**
```css
/* variables.css */
:root {
  /* 이 문서의 모든 CSS 변수 복사 */
}
```

2. **HTML에서 불러오기**
```html
<link rel="stylesheet" href="variables.css">
<link rel="stylesheet" href="main.css">
```

3. **사용하기**
```css
/* main.css */
.my-button {
  background: var(--color-primary);
  padding: var(--spacing-md);
  border-radius: var(--radius-lg);
  transition: var(--transition-base);
}
```

### 커스터마이징

디자인 시스템을 프로젝트에 맞게 수정:

```css
:root {
  /* 기본 색상 오버라이드 */
  --color-primary: #YOUR_COLOR;
  --color-secondary: #YOUR_COLOR;
  
  /* 간격 조정 */
  --spacing-lg: 2.5rem; /* 기본 2rem에서 증가 */
}
```

---

## 체크리스트

새 프로젝트에 디자인 시스템을 적용할 때:

- [ ] CSS 변수 파일 생성 및 연결
- [ ] 컨테이너 max-width 확인
- [ ] 반응형 브레이크포인트 설정
- [ ] 폰트 로드 (Inter, Noto Sans KR)
- [ ] 버튼 컴포넌트 생성
- [ ] 카드 컴포넌트 생성
- [ ] 그리드 시스템 설정
- [ ] 접근성 검증 (색상 대비, 포커스 상태)
- [ ] 모바일 터치 타겟 크기 확인

---

## 참고 자료

- **원본 프로젝트**: [251005_landing_test](https://github.com/Dami-Shin-01/251005_landing_test)
- **라이브 데모**: https://dami-shin-01.github.io/251005_landing_test/
- **영감**: [야놀자 그룹](https://www.yanoljagroup.com/ko)

---

**버전**: 1.0.0  
**최종 업데이트**: 2025년 10월 4일  
**라이선스**: MIT

이 디자인 시스템은 자유롭게 사용, 수정, 배포할 수 있습니다.

