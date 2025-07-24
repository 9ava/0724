# 0724
깃허브연습

GitHub에서 팀(또는 Collaborator)을 초대한 **다음 단계**는 다음과 같은 흐름으로 이어집니다:

---

## ✅ 1. **상대방이 초대 수락**

* 상대방은 이메일 또는 GitHub 알림에서 초대를 확인하고 수락해야 합니다.
* 수락 전에는 리포지토리나 조직에 접근할 수 없습니다.

> 👉 수락 여부는:
> Organization → People → 상태(Status)에 `Pending Invitation` 으로 표시됩니다.

---

## ✅ 2. **리포지토리 접근 권한 확인**

초대가 수락되면:

* 개인 리포에 초대한 경우: 해당 리포지토리에 자동으로 접근 가능
* Organization의 팀인 경우: 권한 부여된 리포지토리 목록에 따라 접근 가능

---

## ✅ 3. **협업 시작 – 보통은 다음과 같은 작업을 합니다**

| 작업        | 설명                                                         |
| --------- | ---------------------------------------------------------- |
| ✅ 클론      | 리포지토리 로컬로 복사: `git clone URL`                              |
| ✅ 브랜치 생성  | 새로운 작업을 위해 브랜치 만듦: `git checkout -b feature/login`         |
| ✅ 코드 작업   | 기능 개발, 수정 등                                                |
| ✅ 커밋 & 푸시 | `git commit -m "로그인 기능"` → `git push origin feature/login` |
| ✅ PR 생성   | GitHub에서 Pull Request 열기 (코드 리뷰 받기)                        |
| ✅ 리뷰 & 머지 | 리뷰 후 merge / 수정 요청 가능                                      |

---

## 🧩 그 외 협업 팁

* **README.md** 잘 작성해두기 (설치 방법, 개발 가이드 등)
* **Issues**로 작업 내용 정리 & 할당
* **Projects** 또는 **Projects Beta**로 칸반보드 사용 가능 (Trello처럼)
* **Wiki**로 문서화도 가능

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

원하시면 협업 규칙을 `.md`로 정리하거나, PR 템플릿 설정하는 방법도 알려드릴게요.
