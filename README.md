# 개발자 포트폴리오 랜딩페이지

야놀자 그룹의 디자인 시스템을 참고하여 제작된 전문 개발자 포트폴리오 랜딩페이지입니다.

## 🌐 라이브 데모

**GitHub Pages**: https://dami-shin-01.github.io/251005_landing_test/

**GitHub Repository**: https://github.com/Dami-Shin-01/251005_landing_test

## 📚 디자인 시스템

이 프로젝트의 디자인 시스템은 재사용 가능하도록 문서화되어 있습니다:

- **[📖 Design System 전체 문서](DESIGN_SYSTEM.md)** - 색상, 타이포그래피, 간격 등 모든 디자인 토큰
- **[⚡ Cheat Sheet](DESIGN_SYSTEM_CHEATSHEET.md)** - 빠른 참조용 치트시트

다른 프로젝트에도 자유롭게 적용할 수 있습니다!

## 🎨 핵심 디자인 토큰

### 색상
- **Primary**: #FF385C (핑크) - 주요 액션
- **Secondary**: #00D9FF (사이안) - 보조 액션
- **Accent**: #A855F7 (퍼플) - 강조
- **Background**: #0F0F23, #1A1A2E (다크)

### 폰트
- **영문**: Inter (Google Fonts)
- **한글**: Noto Sans KR (Google Fonts)

**💡 전체 디자인 시스템은 [DESIGN_SYSTEM.md](DESIGN_SYSTEM.md)에서 확인하세요!**

## 📋 주요 섹션

1. **Hero Section** - 메인 비주얼 및 CTA
2. **About Section** - 개발자 소개 및 통계
3. **Services Section** - 제공 서비스 (Web Application, Web Site, Platform Development)
4. **Portfolio Section** - 프로젝트 포트폴리오 그리드
5. **Achievements Section** - 성과 및 실적
6. **Contact Section** - 연락처

## 🚀 기술 스택

- HTML5
- CSS3 (CSS Variables, Flexbox, Grid)
- Vanilla JavaScript (ES6+)
- AOS (Animate On Scroll Library)

## 📱 반응형 디자인

- Desktop (1280px+)
- Tablet (768px ~ 1024px)
- Mobile (< 768px)

## ✨ 주요 기능

- ✅ 스크롤 애니메이션
- ✅ 숫자 카운터 애니메이션
- ✅ 네비게이션 바 자동 숨김/표시
- ✅ 모바일 햄버거 메뉴
- ✅ 스크롤 진행 표시줄
- ✅ 카드 틸트 효과
- ✅ 레이지 로딩
- ✅ 스무스 스크롤

## 📦 설치 및 실행

1. 레포지토리 클론
```bash
git clone <repository-url>
```

2. 프로젝트 폴더로 이동
```bash
cd 251005_landing_test
```

3. 로컬 서버로 실행
```bash
# Python 3
python -m http.server 8000

# Node.js (http-server)
npx http-server

# VS Code Live Server 확장 프로그램 사용
```

4. 브라우저에서 열기
```
http://localhost:8000
```

## 📂 프로젝트 구조

```
251005_landing_test/
├── index.html              # 메인 HTML 파일
├── css/
│   ├── variables.css       # CSS 변수 및 디자인 시스템
│   ├── style.css          # 메인 스타일시트
│   └── responsive.css     # 반응형 스타일
├── js/
│   ├── main.js            # 메인 JavaScript
│   ├── animations.js      # 애니메이션 로직
│   └── utils.js           # 유틸리티 함수
├── assets/
│   ├── images/
│   │   ├── portfolio/     # 포트폴리오 프로젝트 이미지
│   │   └── profile/       # 프로필 이미지
│   └── icons/             # 아이콘 파일
├── IMAGES_GUIDE.md        # 이미지 추가 가이드
└── README.md              # 프로젝트 문서
```

## 🖼️ 이미지 추가하기

포트폴리오 이미지를 추가하려면:

1. `assets/images/portfolio/` 폴더에 이미지 파일 저장
2. `index.html`에서 placeholder 이미지 URL을 실제 경로로 변경

자세한 내용은 [IMAGES_GUIDE.md](IMAGES_GUIDE.md)를 참고하세요.

**권장 이미지 규격:**
- 포트폴리오: 1200 x 800px (3:2 비율)
- 프로필: 400 x 400px (정사각형)
- 포맷: JPG, PNG, WebP
- 용량: 각 이미지 최대 500KB

## 🎯 커스터마이징

### 색상 변경
`css/variables.css` 파일에서 CSS 변수를 수정하세요.

```css
:root {
    --color-primary: #FF385C;
    --color-secondary: #00D9FF;
    /* ... */
}
```

### 콘텐츠 수정
`index.html` 파일에서 텍스트, 이미지, 링크를 수정하세요.

### 애니메이션 조정
`js/animations.js` 파일에서 애니메이션 효과를 커스터마이징하세요.

## 🌐 브라우저 지원

- Chrome (최신)
- Firefox (최신)
- Safari (최신)
- Edge (최신)

## 📄 라이선스

MIT License

## 👤 제작자

Web Designer Portfolio Project

## 📞 문의

프로젝트에 대한 문의사항이 있으시면 이슈를 등록해주세요.

---

Made with ❤️ using Yanolja Design System

