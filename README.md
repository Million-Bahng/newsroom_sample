# 르 스페이스 시즌2 : 아이스 플래닛 — 뉴스룸 콘텐츠 샘플

현대백화점그룹 뉴스룸(H.스토리) 콘텐츠 샘플 페이지입니다.
순수 HTML + CSS + JavaScript로만 구성되어 있으며, 외부 의존성이 없는 정적 사이트입니다.

## 주요 기능

- **Before/After 비교 슬라이더** (시즌1 ↔ 시즌2)
  - 마우스 드래그 + 모바일 터치 + 키보드 ←→ 모두 지원
  - 외부 라이브러리 없음 (vanilla JS)
- **예티 캐릭터 편지지 박스** + **말풍선 코멘트** (모바일 반응형)
- **얼음 모티프 관람 안내 박스**

## 폴더 구조

```
.
├── index.html              # 메인 페이지 (모든 CSS/JS 포함)
└── images/
    ├── spotlight_banner.png   # 스포트라이트 메인 비주얼
    ├── main.jpg               # 르 스페이스 전경
    ├── set1_s1.jpg ~ set7_s2.jpg   # 7개 섹션 비교 이미지 (시즌1/시즌2)
    └── yeti/
        ├── basic.png    # 기본 표정
        ├── happy.png    # 기쁨
        ├── surprise.png # 놀람
        ├── angry.png    # 분노 (미사용)
        └── sad.png      # 슬픔 (미사용)
```

## 배포 방법 (3가지 옵션)

### 옵션 A. Vercel 드래그 드롭 (가장 빠름, 30초 — GitHub 불필요)

1. https://vercel.com/new 접속 (Vercel 계정 필요, GitHub로 1초 가입 가능)
2. 화면 가운데의 **"Deploy"** 영역에 압축 풀린 이 폴더(또는 zip)를 드래그
3. 자동으로 정적 사이트로 인식 → 30초 내에 `https://xxx.vercel.app` URL 발급

### 옵션 B. GitHub + Vercel 연동 (요청하신 방식, 자동 재배포 됨)

**1단계 — GitHub에 업로드**

1. https://github.com/new 접속
2. Repository name: `newsroom-lespace` (예시) → **Create repository**
3. 새 레포 화면에서 **"uploading an existing file"** 링크 클릭
4. 이 폴더 안의 `index.html`, `images/`, `README.md`, `.gitignore`를 모두 드래그
   - ⚠️ **폴더 자체가 아니라 폴더 "내용물"**을 올리세요. `index.html`이 레포 root에 있어야 합니다.
5. **Commit changes**

**2단계 — Vercel에 연결**

1. https://vercel.com/new 접속 → GitHub 로그인
2. 방금 만든 레포(`newsroom-lespace`) 옆 **"Import"** 클릭
3. Framework Preset은 **"Other"** (자동 감지됨), Root Directory는 그대로 둠
4. **"Deploy"** 클릭 → 약 30초 후 URL 발급

이후로는 GitHub에 푸시할 때마다 Vercel이 자동 재배포합니다.

### 옵션 C. CLI (데스크톱 환경이 있다면)

```bash
# 폴더로 이동
cd newsroom_lespace

# Git
git init
git add .
git commit -m "Initial commit: Le Space Season 2 newsroom page"
git branch -M main
git remote add origin https://github.com/[YOUR_USERNAME]/newsroom-lespace.git
git push -u origin main

# Vercel CLI (npx, 설치 불필요)
npx vercel --prod
```

## 이미지 최적화 권장

원본 이미지 일부(예: `set6_s1.jpg` 약 3MB)는 실제 뉴스룸 업로드용으로는 큰 편입니다.
실서비스용으로는 **800~1200px 폭으로 리사이징 + JPEG 품질 75~80%로 압축** (또는 WebP 변환)을 권장드립니다.
샘플 테스트 단계에서는 원본 그대로 사용해도 무관합니다.

## 라이선스 / 이용

내부 검토용 샘플 페이지입니다. 이미지 자산은 현대퓨처넷 / 르 스페이스 콘텐츠입니다.
