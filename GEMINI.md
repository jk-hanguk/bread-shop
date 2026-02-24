# 🍞 암기빵 샵 가이드 (GEMINI.md)

이 문서는 **암기빵 샵** 저장소의 데이터 구성 원칙과 개발 가이드를 정의합니다.

## 🥐 프로젝트 정체성 (Identity)

- **목적:** 암기빵(`memory-bread`) 프로젝트의 학습 데이터 제공소.
- **컨셉:** 베이커리 (빵 코너, 섹션, 빵 굽기 등).

## 🛠️ 데이터 구성 규칙 (Coding Rules)

### 1. JSON 파일 구조 (Data Model)
모든 학습 데이터는 반드시 아래 형식을 준수해야 합니다.
```json
[
  {
    "id": "chem_001",
    "keyword": "$H_2O$",
    "description": "물 (가장 기본적인 용매, 생명 유지 필수)"
  }
]
```
- `id`: 고유 식별자 (예: `chem_001`, `math_025` 등).
- `keyword`: 암기할 대상 (LaTeX `$ ... $` 권장).
- `description`: 암기 대상의 의미와 상세 설명 (괄호 등을 활용).

### 2. LaTeX 사용 원칙 (LaTeX Rules)
- 화학식($H_2O$, $Na^+$), 수학 공식($a^2 + b^2 = c^2$) 등은 반드시 `$ ... $`로 감싸서 LaTeX 문법을 적용합니다.
- 복잡한 수식의 경우 가독성을 고려하여 작성합니다.

### 3. 디렉토리 구조 (Directory Convention)
- 모든 데이터는 `bread_corner/` 디렉토리 하위에 위치합니다.
- 과목별(`science/`, `math/`, `english/`)로 섹션을 나누어 계층 구조를 유지합니다.

## 🍞 워크플로우 (Workflow)

1.  **신규 빵 굽기 (데이터 추가):** `bread_corner` 하위의 적절한 경로에 새로운 JSON 파일을 생성합니다.
2.  **메뉴판 업데이트 (index.json):** `bread_corner/index.json`에 새로 생성한 파일의 `id`, `name`, `path` 정보를 추가합니다.
3.  **진열하기 (Push):** 모든 변경 사항을 `main` 브랜치에 커밋하고 푸시합니다.

## 🥖 커밋 메시지 컨벤션 (Commit Convention)

- `feat: [bread_name] 빵 추가` (예: `feat: 중학 기하 공식 빵 추가`)
- `fix: [bread_name] 빵 레시피 수정` (예: `fix: 원소기호 LaTeX 오타 수정`)
- `docs: 설명서 업데이트` (README, GEMINI 수정 시)

---
준비된 데이터를 정성껏 구워 암기빵 사용자들에게 행복한 학습 경험을 제공합시다! 🍞🧤
