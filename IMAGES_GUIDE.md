# 🖼️ 이미지 파일 저장 가이드

## 📁 이미지 폴더 구조

```
assets/
├── images/
│   ├── portfolio/        # 포트폴리오 프로젝트 이미지
│   │   ├── webapp-1.jpg
│   │   ├── website-1.jpg
│   │   └── platform-1.jpg
│   └── profile/          # 프로필 이미지
│       └── profile.jpg
└── icons/                # 아이콘 파일
    └── logo.svg
```

## 🎨 권장 이미지 규격

### 포트폴리오 이미지
- **해상도**: 1200 x 800px (3:2 비율)
- **포맷**: JPG, PNG, WebP
- **용량**: 각 이미지 최대 500KB 권장
- **최적화**: TinyPNG, ImageOptim 등으로 압축 필수

### 프로필 이미지
- **해상도**: 400 x 400px (정사각형)
- **포맷**: JPG, PNG
- **용량**: 최대 200KB 권장

## 📝 이미지 추가 방법

### 1. 포트폴리오 프로젝트 이미지 추가

1. `assets/images/portfolio/` 폴더에 이미지 저장
2. `index.html`에서 placeholder 이미지 URL을 실제 경로로 변경:

```html
<!-- 변경 전 -->
<img src="https://via.placeholder.com/600x400/1a1a2e/ffffff?text=Project+1" alt="Project 1">

<!-- 변경 후 -->
<img src="assets/images/portfolio/webapp-1.jpg" alt="웹 애플리케이션 프로젝트">
```

### 2. 프로필 이미지 추가 (선택사항)

About 섹션에 프로필 이미지를 추가하려면:

1. `assets/images/profile/` 폴더에 이미지 저장
2. `index.html`의 About 섹션에 이미지 태그 추가:

```html
<div class="about-content">
    <div class="about-image" data-aos="fade-right">
        <img src="assets/images/profile/profile.jpg" alt="프로필">
    </div>
    <div class="about-text" data-aos="fade-left">
        <!-- 기존 텍스트 -->
    </div>
</div>
```

## 🔄 이미지 최적화 도구

### 온라인 도구
- [TinyPNG](https://tinypng.com/) - PNG/JPG 압축
- [Squoosh](https://squoosh.app/) - 다양한 포맷 지원
- [SVGOMG](https://jakearchibald.github.io/svgomg/) - SVG 최적화

### CLI 도구
```bash
# ImageMagick으로 일괄 리사이즈
magick mogrify -resize 1200x800 -quality 85 *.jpg

# WebP 변환
cwebp input.jpg -q 80 -o output.webp
```

## 🎭 Placeholder 이미지 유지

개발 중에는 현재의 placeholder 이미지를 유지해도 됩니다:
- 빠른 프로토타이핑 가능
- 실제 이미지 없이도 레이아웃 테스트 가능
- 나중에 실제 이미지로 교체 가능

## 📌 주의사항

1. **파일명**: 영문, 소문자, 하이픈 사용 권장
   - ✅ `project-ecommerce.jpg`
   - ❌ `프로젝트 1.jpg`

2. **용량 관리**: 전체 이미지 합계 5MB 이하 권장

3. **저작권**: 사용 권한이 있는 이미지만 업로드

4. **Alt 텍스트**: 접근성을 위해 항상 alt 속성 작성

## 🚀 이미지 추가 후

이미지를 추가한 후:

```bash
git add assets/images/
git commit -m "Add portfolio images"
git push origin master
```

GitHub Pages에서 자동으로 반영됩니다!

