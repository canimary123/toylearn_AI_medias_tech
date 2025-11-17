당신은 최고 수준의 프론트엔드 개발자이자 UI/UX 디자이너입니다.

## 중요: 디자인 우선순위
이 프로젝트는 **디자인이 최우선**입니다. 기능보다 시각적 완성도가 더 중요합니다.
사용자가 첫 화면을 보고 "와, 이거 전문적이고 예쁘다"라고 느껴야 합니다.

## 기술 스택 (엄격히 준수)
- HTML5
- Bootstrap 5.3 (CDN)
- Vanilla JavaScript (jQuery 절대 금지)
- 단일 HTML 파일 (external CSS/JS 없음)

## 제공할 도구 목록
1. 비밀번호 생성기 (사이트별 규칙: 은행/SNS/쇼핑몰)
2. 이미지 변환/압축 (JPG↔PNG↔WebP)
3. 이미지 리사이즈
4. 텍스트 변환기 (대소문자, URL인코딩 등)
5. QR 코드 생성기
6. 글자수 세기
7. 유튜브 썸네일 추출
8. JSON 포맷터
9. PDF 변환 도구

---

## 🎨 디자인 시스템 (필수 준수)

### 컬러 팔레트 (정확히 이 값 사용)
```css
:root {
  /* Primary Colors */
  --primary-purple: #7C3AED;
  --primary-pink: #EC4899;
  --primary-blue: #3B82F6;
  
  /* Gradient Backgrounds */
  --bg-gradient: linear-gradient(135deg, #faf5ff 0%, #fce7f3 50%, #eff6ff 100%);
  --card-gradient: linear-gradient(135deg, #faf5ff 0%, #fce7f3 100%);
  --hero-gradient: linear-gradient(90deg, #7C3AED 0%, #EC4899 100%);
  
  /* Neutral Colors */
  --gray-50: #f9fafb;
  --gray-100: #f3f4f6;
  --gray-200: #e5e7eb;
  --gray-600: #4b5563;
  --gray-700: #374151;
  --gray-800: #1f2937;
  
  /* Semantic Colors */
  --success: #10b981;
  --warning: #f59e0b;
  --error: #ef4444;
  
  /* Shadows */
  --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1);
  --shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1);
}
```

### 타이포그래피
```css
/* 정확히 이 폰트 사용 */
@import url('https://fonts.googleapis.com/css2?family=Pretendard:wght@400;500;600;700;800&display=swap');

body {
  font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

/* 제목 스타일 */
h1 { 
  font-size: 2rem; 
  font-weight: 800; 
  background: linear-gradient(90deg, #7C3AED, #EC4899);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

h2 { font-size: 1.5rem; font-weight: 700; color: #1f2937; }
h3 { font-size: 1.25rem; font-weight: 600; color: #374151; }
```

### 카드 스타일 (필수)
```css
.tool-card {
  background: white;
  border-radius: 1rem;
  padding: 2rem;
  box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1);
  transition: all 0.3s ease;
}

.tool-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1);
}
```

### 버튼 스타일 (필수)
```css
/* Primary Button */
.btn-primary {
  background: linear-gradient(90deg, #7C3AED, #EC4899);
  color: white;
  padding: 1rem 2rem;
  border-radius: 0.75rem;
  font-weight: 700;
  border: none;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  box-shadow: 0 10px 15px -3px rgba(124, 58, 237, 0.3);
  transform: translateY(-2px);
}

/* Secondary Button */
.btn-secondary {
  background: white;
  color: #7C3AED;
  padding: 0.75rem 1.5rem;
  border-radius: 0.75rem;
  border: 2px solid #7C3AED;
  font-weight: 600;
}

.btn-secondary:hover {
  background: #faf5ff;
}
```

### 입력 필드 스타일
```css
input, textarea, select {
  border: 2px solid #e5e7eb;
  border-radius: 0.75rem;
  padding: 0.75rem 1rem;
  font-size: 1rem;
  transition: all 0.3s ease;
}

input:focus, textarea:focus, select:focus {
  outline: none;
  border-color: #7C3AED;
  box-shadow: 0 0 0 3px rgba(124, 58, 237, 0.1);
}
```

---

## 📐 레이아웃 구조 (정확히 따르기)

### 1. 헤더 (Sticky)
```html
<header style="
  position: sticky;
  top: 0;
  z-index: 1000;
  background: white;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  padding: 1rem 0;
">
  <div class="container">
    <div class="d-flex justify-content-between align-items-center">
      <!-- 로고 -->
      <div class="d-flex align-items-center gap-2">
        <span style="font-size: 1.75rem;">⚡</span>
        <h1 style="margin: 0; font-size: 1.5rem;">ToolKit Pro</h1>
      </div>
      
      <!-- 우측 정보 -->
      <div class="d-flex gap-4">
        <div class="d-flex align-items-center gap-2">
          <span style="color: #ef4444;">❤️</span>
          <span style="color: #6b7280; font-size: 0.875rem;">12,847 사용자</span>
        </div>
        <div class="d-flex align-items-center gap-2">
          <span>📤</span>
          <span style="color: #6b7280; font-size: 0.875rem;">0 공유</span>
        </div>
      </div>
    </div>
  </div>
</header>
```

### 2. 히어로 배너 (바이럴 요소)
```html
<div style="
  background: linear-gradient(90deg, #7C3AED, #EC4899);
  border-radius: 1.5rem;
  padding: 2.5rem;
  margin: 2rem 0;
  box-shadow: 0 20px 25px -5px rgba(124, 58, 237, 0.3);
">
  <div class="row align-items-center">
    <div class="col-md-8">
      <div class="d-flex align-items-center gap-2 mb-2">
        <span style="font-size: 1.5rem;">📈</span>
        <span style="color: white; font-weight: 600;">🔥 실시간 인기</span>
      </div>
      <h2 style="color: white; font-size: 2rem; margin-bottom: 0.5rem;">
        오늘만 1,247명이 사용중!
      </h2>
      <p style="color: rgba(255,255,255,0.9);">
        친구에게 공유하고 프리미엄 기능 무료로 받기
      </p>
    </div>
    <div class="col-md-4 text-end">
      <button class="btn-secondary" style="background: white; color: #7C3AED;">
        지금 공유하기 →
      </button>
    </div>
  </div>
</div>
```

### 3. 도구 탭 네비게이션
```html
<div class="d-flex gap-3 mb-4 overflow-auto">
  <!-- 활성 탭 -->
  <button style="
    background: white;
    color: #7C3AED;
    padding: 0.75rem 1.5rem;
    border-radius: 0.75rem;
    border: none;
    font-weight: 600;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    white-space: nowrap;
  ">
    🔒 비밀번호 생성기
    <span style="
      background: #ef4444;
      color: white;
      padding: 0.125rem 0.5rem;
      border-radius: 1rem;
      font-size: 0.75rem;
      margin-left: 0.5rem;
    ">HOT</span>
  </button>
  
  <!-- 비활성 탭 -->
  <button style="
    background: rgba(255,255,255,0.6);
    color: #6b7280;
    padding: 0.75rem 1.5rem;
    border-radius: 0.75rem;
    border: none;
    font-weight: 600;
    white-space: nowrap;
  ">
    🖼️ 이미지 변환
  </button>
</div>
```

### 4. 광고 영역 (AdSense 위치)
```html
<div style="
  background: #f3f4f6;
  border: 2px dashed #d1d5db;
  border-radius: 1rem;
  padding: 4rem 2rem;
  text-align: center;
  margin: 2rem 0;
">
  <p style="color: #9ca3af; margin: 0;">Google AdSense 광고 영역</p>
</div>
```

### 5. 메인 도구 카드
```html
<div style="
  background: white;
  border-radius: 1.5rem;
  padding: 3rem;
  box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1);
">
  <h2 style="font-size: 1.75rem; font-weight: 700; margin-bottom: 2rem;">
    🔒 최강 비밀번호 생성기
  </h2>
  
  <!-- 도구 내용 -->
</div>
```

### 6. 입력/결과 영역
```html
<!-- 옵션 선택 -->
<div class="mb-4">
  <label style="
    display: block;
    font-size: 0.875rem;
    font-weight: 600;
    color: #374151;
    margin-bottom: 0.75rem;
  ">사이트 종류 선택</label>
  
  <div class="row g-3">
    <div class="col-6 col-md-3">
      <button style="
        width: 100%;
        padding: 1rem;
        background: #faf5ff;
        color: #7C3AED;
        border: none;
        border-radius: 0.75rem;
        font-weight: 600;
        transition: all 0.3s ease;
      " onmouseover="this.style.background='#f3e8ff'">
        🌐 일반
      </button>
    </div>
    <!-- 나머지 버튼들... -->
  </div>
</div>

<!-- 결과 표시 -->
<div style="
  background: linear-gradient(135deg, #faf5ff, #fce7f3);
  border-radius: 1rem;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
">
  <div class="d-flex justify-content-between align-items-center mb-3">
    <span style="font-size: 0.875rem; font-weight: 600; color: #374151;">
      생성된 비밀번호
    </span>
    <span style="font-size: 0.875rem; font-weight: 700; color: #10b981;">
      보안 강도: 95%
    </span>
  </div>
  
  <div class="d-flex gap-3">
    <input type="text" value="P@ssw0rd123!@#" readonly style="
      flex: 1;
      background: white;
      padding: 1rem;
      border-radius: 0.75rem;
      border: 2px solid #e9d5ff;
      font-family: 'Courier New', monospace;
      font-size: 1.125rem;
    ">
    <button style="
      background: #7C3AED;
      color: white;
      padding: 1rem;
      border: none;
      border-radius: 0.75rem;
      transition: all 0.3s ease;
    ">
      📋
    </button>
  </div>
</div>

<!-- 강도 바 -->
<div style="
  height: 0.75rem;
  background: #e5e7eb;
  border-radius: 9999px;
  overflow: hidden;
  margin-bottom: 1.5rem;
">
  <div style="
    height: 100%;
    width: 95%;
    background: linear-gradient(90deg, #10b981, #34d399);
    transition: width 0.5s ease;
  "></div>
</div>
```

### 7. 액션 버튼
```html
<div class="d-flex gap-3">
  <button style="
    flex: 1;
    background: linear-gradient(90deg, #7C3AED, #EC4899);
    color: white;
    padding: 1rem 2rem;
    border: none;
    border-radius: 0.75rem;
    font-weight: 700;
    font-size: 1rem;
    transition: all 0.3s ease;
  " onmouseover="this.style.boxShadow='0 10px 15px rgba(124,58,237,0.3)'">
    🔄 새로 생성하기
  </button>
  
  <button style="
    background: #3B82F6;
    color: white;
    padding: 1rem 1.5rem;
    border: none;
    border-radius: 0.75rem;
    font-weight: 700;
    transition: all 0.3s ease;
  ">
    📤 공유
  </button>
</div>
```

### 8. 바이럴 유도 섹션
```html
<div style="
  background: #fef3c7;
  border: 2px solid #fde68a;
  border-radius: 1rem;
  padding: 1.5rem;
  margin-top: 2rem;
">
  <div class="d-flex gap-3">
    <div style="font-size: 3rem;">🎁</div>
    <div style="flex: 1;">
      <h3 style="font-size: 1.125rem; font-weight: 700; margin-bottom: 0.5rem;">
        친구에게 공유하면 프리미엄 기능 무료!
      </h3>
      <p style="color: #6b7280; font-size: 0.875rem; margin-bottom: 1rem;">
        3명에게 공유하면 무제한 비밀번호 히스토리 저장 기능이 열려요
      </p>
      <div class="d-flex gap-2 align-items-center">
        <div style="width: 4rem; height: 0.5rem; background: #7C3AED; border-radius: 9999px;"></div>
        <div style="width: 4rem; height: 0.5rem; background: #d1d5db; border-radius: 9999px;"></div>
        <div style="width: 4rem; height: 0.5rem; background: #d1d5db; border-radius: 9999px;"></div>
        <span style="font-size: 0.75rem; color: #9ca3af; margin-left: 0.5rem;">0/3</span>
      </div>
    </div>
  </div>
</div>
```

### 9. 관련 도구 추천
```html
<div style="
  background: white;
  border-radius: 1.5rem;
  padding: 2rem;
  box-shadow: 0 10px 15px rgba(0,0,0,0.1);
  margin-top: 2rem;
">
  <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 1.5rem;">
    🔥 지금 핫한 도구
  </h3>
  
  <div class="row g-4">
    <div class="col-md-4">
      <div style="
        background: linear-gradient(135deg, #faf5ff, #fce7f3);
        padding: 1.5rem;
        border-radius: 1rem;
        transition: all 0.3s ease;
        cursor: pointer;
      " onmouseover="this.style.boxShadow='0 10px 15px rgba(0,0,0,0.1)'">
        <div style="font-size: 2.5rem; margin-bottom: 0.75rem;">📱</div>
        <h4 style="font-size: 1rem; font-weight: 700; margin-bottom: 0.25rem;">
          QR코드 생성기
        </h4>
        <p style="color: #6b7280; font-size: 0.875rem; margin: 0;">
          2.3k 명이 사용중
        </p>
      </div>
    </div>
    <!-- 나머지 카드들... -->
  </div>
</div>
```

### 10. 푸터 CTA
```html
<div style="
  background: linear-gradient(90deg, #3B82F6, #7C3AED);
  border-radius: 1.5rem;
  padding: 3rem;
  text-align: center;
  margin-top: 2rem;
">
  <h3 style="color: white; font-size: 1.75rem; margin-bottom: 0.75rem;">
    💎 프리미엄으로 업그레이드
  </h3>
  <p style="color: rgba(255,255,255,0.9); margin-bottom: 1.5rem;">
    광고 없이, 무제한으로 모든 도구를 사용하세요
  </p>
  <button style="
    background: white;
    color: #7C3AED;
    padding: 1rem 2.5rem;
    border: none;
    border-radius: 0.75rem;
    font-weight: 700;
    font-size: 1rem;
    transition: all 0.3s ease;
  " onmouseover="this.style.boxShadow='0 20px 25px rgba(255,255,255,0.3)'">
    월 4,900원 시작하기
  </button>
</div>
```

---

## 🎯 필수 구현 사항

### Body 기본 스타일
```css
body {
  background: linear-gradient(135deg, #faf5ff 0%, #fce7f3 50%, #eff6ff 100%);
  min-height: 100vh;
  font-family: 'Pretendard', sans-serif;
  margin: 0;
  padding: 0;
}
```

### Container
```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}
```

### 모든 전환 효과
```css
* {
  transition: all 0.3s ease;
}
```

---

## ⚠️ 절대 금지 사항
1. ❌ Bootstrap 기본 버튼 스타일 사용 금지 (.btn-primary 등)
2. ❌ 기본 회색/파란색 색상 사용 금지
3. ❌ 각진 모서리 금지 (최소 0.75rem border-radius)
4. ❌ 그림자 없는 카드 금지
5. ❌ 단색 배경 금지 (그라데이션 필수)
6. ❌ 얇은 폰트 금지 (최소 font-weight: 600)

---

## ✅ 완성 체크리스트
- [ ] 전체 배경이 보라-핑크-파랑 그라데이션
- [ ] 모든 카드에 둥근 모서리와 그림자
- [ ] 버튼에 호버 효과 (shadow + transform)
- [ ] 입력 필드 focus 시 보라색 테두리
- [ ] 강도 바가 그라데이션으로 애니메이션
- [ ] 아이콘이 이모지로 표시
- [ ] 폰트가 Pretendard
- [ ] 모든 텍스트가 깔끔하고 읽기 쉬움

---

이제 위 디자인 시스템을 **100% 정확히 따라서** 완전한 index.html 파일을 생성해주세요.
모든 9개 도구가 실제로 작동해야 하며, 디자인은 반드시 위 스타일을 사용해야 합니다.