# 0724

깃허브연습

GitHub에서 팀(또는 Collaborator)을 초대한 **다음 단계**는 다음과 같은 흐름으로 이어집니다:

---

## ✅ 1. **상대방이 초대 수락**

- 상대방은 이메일 또는 GitHub 알림에서 초대를 확인하고 수락해야 합니다.
- 수락 전에는 리포지토리나 조직에 접근할 수 없습니다.

> 👉 수락 여부는:
> Organization → People → 상태(Status)에 `Pending Invitation` 으로 표시됩니다.

---

## ✅ 2. **리포지토리 접근 권한 확인**

초대가 수락되면:

- 개인 리포에 초대한 경우: 해당 리포지토리에 자동으로 접근 가능
- Organization의 팀인 경우: 권한 부여된 리포지토리 목록에 따라 접근 가능

---

## ✅ 3. **협업 시작 – 보통은 다음과 같은 작업을 합니다**

| 작업           | 설명                                                            |
| -------------- | --------------------------------------------------------------- |
| ✅ 클론        | 리포지토리 로컬로 복사: `git clone URL`                         |
| ✅ 브랜치 생성 | 새로운 작업을 위해 브랜치 만듦: `git checkout -b feature/login` |
| ✅ 코드 작업   | 기능 개발, 수정 등                                              |
| ✅ 커밋 & 푸시 | `git commit -m "로그인 기능"` → `git push origin feature/login` |
| ✅ PR 생성     | GitHub에서 Pull Request 열기 (코드 리뷰 받기)                   |
| ✅ 리뷰 & 머지 | 리뷰 후 merge / 수정 요청 가능                                  |

---

## 🧩 그 외 협업 팁

- **README.md** 잘 작성해두기 (설치 방법, 개발 가이드 등)
- **Issues**로 작업 내용 정리 & 할당
- **Projects** 또는 **Projects Beta**로 칸반보드 사용 가능 (Trello처럼)
- **Wiki**로 문서화도 가능

---

## 💬 예시 흐름 (협업 시작 후)

```bash
git clone https://github.com/잭/project.git
cd project
git checkout -b feature/login
# 코드 작성
git add .
git commit -m "로그인 페이지 추가"
git push origin feature/login
```

그 다음 GitHub에서 PR(Pull Request) 열고 팀원이 코드 리뷰 후 머지합니다.

---

GitHub에서의 \*\*브랜치(branch)\*\*는 코드의 **별도 작업 공간**입니다. 여러 명이 동시에 개발하거나 기능을 나눠 작업할 때 아주 유용합니다. 아래에 브랜치의 개념부터 GitHub에서 어떻게 쓰는지까지 정리해드릴게요.

---

## 🧠 1. 브랜치란?

- 기본 브랜치는 `main` 또는 `master`입니다.
- 브랜치를 새로 만들어서 실험하거나 기능 추가한 뒤, 검토 후 `main`에 합칩니다 (merge).
- 충돌 없이 병합하려면 잘게 쪼개서 작업하는 게 핵심입니다.

---

## 🛠️ 2. GitHub에서 브랜치 사용 흐름

### ✅ 새 브랜치 만들기

```bash
git checkout -b feature/login
```

> `feature/login`이라는 새 브랜치를 만들고 그 브랜치로 이동

---

### ✅ 작업 후 GitHub에 푸시

```bash
git add .
git commit -m "로그인 기능 추가"
git push origin feature/login
```

> 원격 GitHub에도 해당 브랜치가 생성됩니다

---

### ✅ GitHub에서 Pull Request(PR) 생성

1. GitHub 리포지토리 접속
2. 자동으로 `Compare & pull request` 버튼 뜸
3. PR 제목, 설명 작성 → 리뷰 요청 → Merge

---

### ✅ 브랜치 병합 (Merge)

- PR을 통해 `main` 브랜치로 병합 (팀원 승인/리뷰 가능)
- 병합 후 브랜치는 필요 시 삭제 가능

---

## 📘 GitHub 브랜치 화면 위치

- 리포지토리 페이지 > 상단에서 `main ▼` 드롭다운 클릭하면 브랜치 확인/전환 가능
- `Branches` 탭 클릭하면 전체 브랜치 목록 확인 가능

---

## 🧩 브랜치 작명 예시 (규칙화)

| 유형      | 작명 예시            |
| --------- | -------------------- |
| 기능 추가 | `feature/login-page` |
| 버그 수정 | `fix/login-error`    |
| 문서 작업 | `docs/readme-update` |
| 실험용    | `test/api-response`  |

---

## 📝 브랜치 관련 주요 명령어 요약

| 명령어                            | 설명                    |
| --------------------------------- | ----------------------- |
| `git branch`                      | 현재 브랜치 목록 보기   |
| `git branch <name>`               | 브랜치 만들기           |
| `git checkout <name>`             | 브랜치 이동             |
| `git checkout -b <name>`          | 만들고 이동까지 한 번에 |
| `git push origin <name>`          | 원격으로 브랜치 푸시    |
| `git branch -d <name>`            | 로컬 브랜치 삭제        |
| `git push origin --delete <name>` | 원격 브랜치 삭제        |

---
