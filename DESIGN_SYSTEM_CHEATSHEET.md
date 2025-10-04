# 🚀 Design System Cheat Sheet

> 빠른 참조를 위한 디자인 시스템 치트시트

## 🎨 색상 - 한눈에 보기

```css
/* Primary */
--color-primary: #FF385C;           /* 주요 액션 */
--color-secondary: #00D9FF;         /* 보조 액션 */
--color-accent: #A855F7;            /* 강조 */

/* Dark */
--color-dark: #0F0F23;              /* 배경 */
--color-dark-secondary: #1A1A2E;    /* 섹션 */

/* Light */
--color-light: #FFFFFF;             /* 텍스트 */
--color-gray-300: #D4D4D4;          /* 보조 텍스트 */

/* Gradient */
--gradient-primary: linear-gradient(135deg, #FF385C 0%, #A855F7 100%);
```

---

## 📏 간격 - 8px 시스템

| 변수 | 값 | 용도 |
|------|-----|------|
| `xs` | 8px | 작은 패딩 |
| `sm` | 16px | 기본 패딩 |
| `md` | 24px | 컴포넌트 간격 |
| `lg` | 32px | 섹션 내부 |
| `xl` | 48px | 섹션 간격 |
| `2xl` | 64px | 큰 섹션 |
| `3xl` | 96px | 페이지 패딩 |
| `4xl` | 128px | 히어로 섹션 |

**빠른 사용:**
```css
padding: var(--spacing-lg);
margin: var(--spacing-xl) 0;
gap: var(--spacing-md);
```

---

## 🔤 타이포그래피 스케일

| 크기 | 값 | 용도 |
|------|-----|------|
| `xs` | 12px | 캡션 |
| `sm` | 14px | 작은 텍스트 |
| `base` | 16px | 본문 |
| `lg` | 18px | 큰 본문 |
| `xl` | 20px | 소제목 |
| `2xl` | 24px | H3 |
| `3xl` | 30px | H3 |
| `4xl` | 36px | H2 |
| `5xl` | 48px | H1 |
| `6xl` | 60px | 히어로 |
| `7xl` | 72px | 대형 |

**빠른 헤딩 스타일:**
```css
h1 { font-size: var(--font-size-6xl); font-weight: 900; }
h2 { font-size: var(--font-size-5xl); font-weight: 700; }
h3 { font-size: var(--font-size-4xl); font-weight: 700; }
```

---

## 🎭 자주 쓰는 패턴

### 그라디언트 텍스트
```css
.gradient-text {
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
```

### 카드 호버 효과
```css
.card {
  transition: var(--transition-base);
}
.card:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-xl);
}
```

### 중앙 정렬
```css
.center {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### 풀스크린 히어로
```css
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

---

## 📱 반응형 브레이크포인트

```css
/* 모바일 기본 */
/* 스타일 작성 */

/* 태블릿 (768px+) */
@media (min-width: 768px) { }

/* 데스크톱 (1024px+) */
@media (min-width: 1024px) { }

/* 대형 (1280px+) */
@media (min-width: 1280px) { }
```

---

## 🔘 버튼 템플릿

```css
/* Primary */
.btn-primary {
  padding: 1rem 2rem;
  background: var(--gradient-primary);
  color: white;
  border: none;
  border-radius: var(--radius-lg);
  transition: var(--transition-base);
}

/* Secondary */
.btn-secondary {
  padding: 1rem 2rem;
  background: transparent;
  color: var(--color-light);
  border: 2px solid var(--color-light);
  border-radius: var(--radius-lg);
}
```

---

## 💳 카드 템플릿

```css
.card {
  padding: var(--spacing-xl);
  background: rgba(255, 255, 255, 0.05);
  border-radius: var(--radius-xl);
  border: 1px solid rgba(255, 255, 255, 0.1);
}
```

---

## 🎬 애니메이션 속도

```css
--transition-fast: 150ms;   /* 버튼 호버 */
--transition-base: 300ms;   /* 일반 효과 */
--transition-slow: 500ms;   /* 페이드 */
```

---

## 🌗 그림자 레벨

```css
--shadow-sm: ...;   /* 텍스트 필드 */
--shadow-md: ...;   /* 버튼, 카드 */
--shadow-lg: ...;   /* 드롭다운 */
--shadow-xl: ...;   /* 모달 */
--shadow-2xl: ...;  /* 호버 상태 */
```

---

## 📐 Border Radius

```css
--radius-sm: 6px;    /* 작은 요소 */
--radius-md: 8px;    /* 기본 */
--radius-lg: 12px;   /* 버튼 */
--radius-xl: 16px;   /* 카드 */
--radius-2xl: 24px;  /* 대형 */
--radius-full: 9999px; /* 원형 */
```

---

## ⚡ 빠른 스타트 템플릿

### 섹션 구조
```html
<section class="section">
  <div class="container">
    <div class="section-header">
      <span class="section-label">라벨</span>
      <h2 class="section-title">제목</h2>
    </div>
    <!-- 콘텐츠 -->
  </div>
</section>
```

### 그리드 레이아웃
```html
<div class="grid">
  <div class="card">카드 1</div>
  <div class="card">카드 2</div>
  <div class="card">카드 3</div>
</div>
```

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--spacing-lg);
}
```

---

## 🎯 자주 쓰는 조합

### 섹션 레이블
```css
.section-label {
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

### 입력 필드
```css
.input {
  width: 100%;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: var(--radius-lg);
  color: var(--color-light);
}

.input:focus {
  border-color: var(--color-primary);
  box-shadow: 0 0 0 3px rgba(255, 56, 92, 0.1);
}
```

---

## 📋 체크리스트

새 컴포넌트 만들 때:

- [ ] CSS 변수 사용 (`var(--color-primary)`)
- [ ] 간격은 8px 시스템 (`var(--spacing-*)`)
- [ ] 트랜지션 추가 (`transition: var(--transition-base)`)
- [ ] 호버 상태 정의
- [ ] 포커스 스타일 추가
- [ ] 반응형 확인 (모바일/태블릿/데스크톱)
- [ ] 접근성 검증 (색상 대비 4.5:1)

---

## 🔗 빠른 링크

- [전체 문서](DESIGN_SYSTEM.md)
- [이미지 가이드](IMAGES_GUIDE.md)
- [프로젝트 README](README.md)
- [라이브 데모](https://dami-shin-01.github.io/251005_landing_test/)

---

**Tip**: 이 파일을 프린트하거나 북마크하여 개발할 때 빠르게 참조하세요!

