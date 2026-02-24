# 🍞 암기빵 샵 (Memory Bread Shop)

암기빵([Memory Bread](https://github.com/jk-hanguk/memory-bread)) 프로젝트를 위한 고품질 학습 데이터를 제공하는 공식 데이터 저장소입니다. 중학교 수준의 과학, 수학, 영어 등 다양한 '암기빵'(학습 데이터)이 진열되어 있습니다.

## 🥖 빵 코너 안내 (Directory Structure)

데이터는 과목별로 정돈된 계층형 구조로 관리됩니다.

```text
bread_corner/
├── index.json               # 🍞 빵 진열 안내판 (모든 데이터셋 목록 및 경로)
├── science/                 # 🧪 과학 섹션
│   └── chemistry/           # 화학 코너 (원소기호, 이온식, 화학식)
├── math/                    # 📐 수학 섹션
│   └── formulas.json        # 수학 공식 빵
└── english/                 # 🔤 영어 섹션
    └── words.json           # 영단어 빵
```

## ✨ 주요 특징

- **LaTeX 지원:** 수학 공식과 화학식은 `$ ... $` 문법을 사용하여 깔끔하게 렌더링됩니다.
- **표준 데이터 형식:** 암기빵 앱에서 즉시 사용 가능한 `id`, `keyword`, `description` 형식을 준수합니다.
- **계층형 관리:** 과목별, 주제별로 섹션이 나누어져 있어 확장이 용이합니다.

## 🛒 사용 방법 (Usage)

암기빵 프로젝트의 `BakeryService`에서 이 저장소의 데이터를 참조하여 내려받을 수 있습니다.

### 데이터 목록 가져오기 (GitHub API)
```text
https://api.github.com/repos/jk-hanguk/bread-shop/contents/bread_corner?ref=main
```

### 개별 빵 다운로드 (Raw URL)
```text
https://raw.githubusercontent.com/jk-hanguk/bread-shop/main/bread_corner/science/chemistry/elements.json
```

## 👨‍🍳 기여하기

새로운 빵(학습 데이터)을 굽고 싶으시다면 `bread_corner` 하위에 적절한 섹션을 만들고 `index.json`에 정보를 추가한 뒤 Pull Request를 보내주세요!

---
© 2026 jk-hanguk. All rights reserved.
