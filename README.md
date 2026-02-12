# 📦 LiveOrals 상세페이지 이미지 뷰어

상세페이지 이미지를 GitHub Pages로 배포해서 웹에서 바로 확인할 수 있는 뷰어입니다.

## 🚀 처음 세팅 (1회만)

### 1. GitHub에서 새 레포 생성
- https://github.com/new 접속
- Repository name: `product-pages`
- **Public** 선택 (GitHub Pages 무료 사용을 위해)
- Create repository 클릭

### 2. 로컬에서 연결
```bash
cd product-pages
git init
git remote add origin https://github.com/Livedent/product-pages.git
git branch -M main
git add .
git commit -m "초기 세팅"
git push -u origin main
```

### 3. GitHub Pages 활성화
1. 레포 → **Settings** 탭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. Source → **Deploy from a branch** 선택
4. Branch → **main** / **(root)** 선택
5. **Save** 클릭

### 4. 접속 확인 (1~2분 후)
```
https://livedent.github.io/product-pages/
```

---

## 📝 이미지 업데이트 방법

### Step 1: images/ 폴더에 이미지 넣기
```
product-pages/
├── images/
│   ├── 01_hero.jpg
│   ├── 02_feature.png
│   └── 03_detail.jpg
└── index.html
```

### Step 2: index.html에서 파일명 수정
`index.html` 파일을 열고 상단의 `IMAGE_FILES` 배열을 수정:
```javascript
const IMAGE_FILES = [
    '01_hero.jpg',
    '02_feature.png',
    '03_detail.jpg',
];
```

### Step 3: GitHub에 올리기
```bash
git add .
git commit -m "상세페이지 이미지 업데이트"
git push
```

### Step 4: 웹에서 확인
```
https://livedent.github.io/product-pages/
```
(push 후 1~2분 소요)

---

## 🔧 기능
- **너비 조절**: 슬라이더로 미리보기 너비 조절 가능
- **플랫폼 프리셋**: 모바일(420px) / PC(860px) 전환
- **이미지 목록**: 왼쪽 사이드바에서 이미지 클릭 시 해당 위치로 스크롤