# 엄태욱T 국어 컨설팅 랜딩페이지

엄태욱T 국어 역량 진단 & 학습 로드맵 1:1 컨설팅 안내 페이지입니다.

## 📁 파일 구성

```
release/
├── index.html              # 메인 랜딩페이지 (강사 사진·미디어 썸네일·책 표지 모두 base64 인라인)
├── og-image.png            # 카카오톡/페이스북/트위터 미리보기 이미지 (1200×630)
├── apple-touch-icon.png    # iOS 홈 화면 아이콘 (180×180)
├── favicon-16.png          # 브라우저 탭 아이콘
├── favicon-32.png          # 브라우저 탭 아이콘 (HiDPI)
├── poster-A4.pdf           # A4 인쇄용 포스터
└── README.md               # 이 파일
```

> **자체 실행 안내:** `index.html` 한 파일만 더블클릭해도 모든 이미지가 정상 표시됩니다(base64 인라인). 단, 카카오톡/페이스북 미리보기를 위해서는 GitHub Pages 또는 일반 웹서버에 업로드해야 합니다.

## 🚀 GitHub Pages 배포 방법

### 1) 새 저장소 생성

GitHub에서 새 public 저장소를 만듭니다. 예: `eum-consulting`

### 2) 파일 업로드

`release/` 폴더 안의 모든 파일을 저장소 루트에 업로드합니다.

```bash
git init
git add index.html og-image.png favicon-*.png apple-touch-icon.png poster-A4.pdf README.md
git commit -m "Initial release: 엄태욱T 컨설팅 랜딩페이지 v1.0"
git branch -M main
git remote add origin https://github.com/[YOUR_USERNAME]/eum-consulting.git
git push -u origin main
```

### 3) GitHub Pages 활성화

저장소 **Settings → Pages**에서:
- Source: `Deploy from a branch`
- Branch: `main` / `/ (root)`
- Save

5~10분 후 `https://[YOUR_USERNAME].github.io/eum-consulting/`에서 페이지가 활성화됩니다.

### 4) 메타태그 URL 수정 ⚠️ **꼭 필요**

`index.html`의 `<head>` 섹션에서 아래 두 줄을 실제 배포 URL로 교체하세요:

```html
<meta property="og:url" content="https://studytouch23-dev.github.io/eum-consulting/">
<meta property="og:image" content="https://studytouch23-dev.github.io/eum-consulting/og-image.png">
<meta name="twitter:image" content="https://studytouch23-dev.github.io/eum-consulting/og-image.png">
```

> ⚠️ **카카오톡 미리보기는 절대 URL이 필요합니다.** 상대 경로(`./og-image.png`)는 카카오톡에서 작동하지 않습니다.

## 🔗 신청 링크

현재 페이지의 CTA 버튼은 모두 `naver.me/FLEe6b4F`로 연결되어 있습니다.

변경하려면 `index.html`에서 다음을 검색해 교체하세요:

```
https://naver.me/FLEe6b4F
```

## 📤 카카오톡 미리보기 캐시

카카오톡은 한 번 URL을 본 후 미리보기를 캐싱합니다. OG 이미지를 변경한 경우 캐시를 갱신해야 합니다:

1. https://developers.kakao.com/tool/clear/og 접속
2. 페이지 URL 입력
3. "초기화" 버튼 클릭

페이스북도 동일한 도구가 있습니다: https://developers.facebook.com/tools/debug/

## 🎨 디자인 정보

- **Primary**: `#6F48E9` (스터디피크 보라)
- **Accent**: `#FF8A3D` (엄제자 특전 오렌지)
- **Background**: `#1a1a1a` (검정), `#F7F5FF` (연보라)
- **Font**: Pretendard Variable (CDN 로딩)

## 📝 컨텐츠 업데이트

페이지 내용을 수정하려면 `index.html`을 직접 편집하면 됩니다. 주요 섹션:

| 섹션 | 위치 (검색 키워드) |
|------|--------------------|
| Hero 타이틀 | `엄태욱T 국어 역량 진단` |
| 학부모 고민 3가지 | `quote-line` 또는 `quote-card` |
| 컨설팅 3단계 | `step-card` |
| 강사 프로필 | `instructor-grid` |
| 미디어 출연 4채널 | `media-grid` |
| 책 소개 | `book-card` |
| 가격 박스 | `price-card` |
| 최종 CTA | `cta-section` |

## 📊 추적·분석

Google Analytics 등을 붙이려면 `<head>` 끝에 추적 스크립트를 추가하세요. 현재 별도 추적 코드는 들어 있지 않습니다.

---

**제작:** StudyPeak · (주)엄티처
**버전:** v1.0 (2026.05)
**문의:** [카카오톡 채널 @엄태욱T]
