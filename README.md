# 🧑‍💻 Sparta Git Cowork — I6팀 팀원 소개 페이지

> 스파르타코딩클럽 Git 협업 온보딩 과제 — I6팀

---

## 📌 프로젝트 소개

팀원 각자가 **브랜치를 생성 → JSON 파일 작성 → PR 제출**하는 Git 협업 플로우를 직접 경험하는 온보딩 프로젝트입니다.  
완성된 팀원 정보는 `team-portfolio.html` 페이지에서 카드 형태로 자동 렌더링됩니다.

---

## 🗂 프로젝트 구조

```
sparta-git-cowork-I6/
├── team-portfolio.html     # 팀원 목록 페이지 (카드 UI)
├── members/                # 팀원 정보 JSON 파일 디렉토리
│   ├── members.json        # 팀원 슬러그 목록 (렌더링 순서 관리)
│   ├── bw.json             # 이병우
│   ├── dh.json             # 이동희
│   ├── js.json             # 김준성
│   ├── jy.json             # 이지영
│   └── sk.json             # 고수경
└── image/                  # 프로필 이미지 파일 디렉토리
```

---

## 👥 팀원 소개

| ID | 이름  | 기술 스택 | MBTI |
|----|-----|-----------|------|
| bw | 이병우 | Java, Spring Boot, MySQL, Python | ISTJ |
| dh | 이동희 | 학습 중 | INTP |
| js | 김준성 | Java, Spring Boot, Docker, AWS, Python | INFJ |
| jy | 이지영 | 백엔드, DB, Git | - |
| sk | 고수경 | C#, MySQL, C++, Redis, Unity | INFP |

---

## 🚀 시작하기

### 1. 저장소 클론 및 브랜치 생성

```bash
# 저장소 클론
git clone https://github.com/20LDH/sparta-git-cowork-I6.git
cd sparta-git-cowork-I6

# 새 브랜치 생성 (본인 ID로)
git checkout -b feat/<your-id>
```

### 2. 팀원 JSON 파일 작성

`members/` 디렉토리에 `본인아이디.json` 파일을 생성합니다.

```json
{
  "id": "your-id",
  "name": "홍길동",
  "role": "백엔드 개발자",
  "bio": "한 줄 자기소개",
  "image": "image/your-id.png",
  "skills": ["Java", "Spring Boot", "MySQL"]
}
```

### 3. members.json에 본인 파일명 추가

```json
{
  "members": [
    "bw", "dh", "js", "jy", "sk",
    "your-id"
  ]
}
```

> ⚠️ 기존 슬러그는 그대로 유지하고, 본인 ID만 추가하세요.

### 4. 프로필 이미지 추가 (선택)

```
image/your-id.png  또는  image/your-id.jpg
```

### 5. 커밋 & 푸시

```bash
git add members/your-id.json members/members.json
git add image/your-id.png   # 이미지가 있는 경우

git commit -m "feat: 홍길동 팀원 정보 추가"
git push origin feat/your-id
```

### 6. Pull Request 생성

- **PR 제목:** `feat: [본인 이름] 팀원 정보 추가`
- **PR 설명:** 간단한 자기소개 작성
- 팀원 리뷰 후 `main` 브랜치에 머지

---

## 🖥 로컬 실행 방법

`fetch()`를 사용하기 때문에 `file://` 프로토콜에서는 동작하지 않습니다.  
반드시 **Live Server** (VS Code 확장) 또는 로컬 HTTP 서버를 사용해주세요.

```bash
# VS Code Live Server 설치 후
# team-portfolio.html 우클릭 → "Open with Live Server"
```

---

## ✅ 협업 규칙

| 항목 | 규칙 |
|------|------|
| 브랜치명 | `feat/<본인ID>` |
| 커밋 메시지 | `feat: [이름] 팀원 정보 추가` |
| JSON 파일명 | `본인아이디.json` (소문자) |
| 이미지 경로 | `image/본인아이디.png` |
| PR | 최소 1명 이상 리뷰 후 머지 |

---

## ⚠️ 주의사항

- `members.json`에서 기존 슬러그를 **삭제하거나 수정하지 마세요**
- JSON 문법 오류가 없는지 꼭 확인해주세요 ([JSONLint](https://jsonlint.com) 활용)
- 충돌 발생 시 `members.json`만 주의해서 resolve하면 됩니다

---

## 📬 문의

프로젝트 관련 문의는 [Issues](https://github.com/20LDH/sparta-git-cowork-I6/issues)에 남겨주세요.