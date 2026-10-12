# TodoFlow

## 1. 개요

본 저장소는 팀 단위 할 일(Task) 관리를 위한 웹 애플리케이션 **TodoFlow**의 소스 코드를 관리합니다.

- **주요 기능**: 할 일 등록 / 수정 / 삭제, 담당자 지정, 진행 상태 보드, 마감일 알림
- **기술 스택**: React, FastAPI, PostgreSQL, Docker
- **팀 구성**: Frontend 2명, Backend 2명

---

## 2. 브랜치 전략

### 2.1 브랜치 네이밍 규칙

형식: `category/issueNo-issueTitle`

| 구성 요소 | 설명 |
| --- | --- |
| `category` | 작업 유형 (feat, fix, docs 등) |
| `issueNo` | 연관된 이슈 번호 |
| `issueTitle` | 이슈 제목 (영문 소문자, kebab-case) |

**예시**: `feat/1-readme-document-design`

### 2.2 category 종류

| category | 용도 |
| --- | --- |
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `docs` | 문서 작성 / 수정 |
| `refactor` | 리팩터링 (기능 변화 없음) |
| `test` | 테스트 코드 |
| `chore` | 빌드 · 설정 등 기타 작업 |

---

## 3. 협업 규칙

- 작업 내용은 **`main` 브랜치에 직접 커밋/푸시하지 않고**, PR(Pull Request)을 통해 리뷰를 요청한다.
- 모든 브랜치는 `category/issueNo-issueTitle` 형식을 따른다.
- 머지가 완료된 작업 브랜치는 **삭제**한다.

---

## 4. 작업 흐름 (Workflow)

1. 이슈 생성 및 이슈 번호 확인
2. 규칙에 맞는 작업 브랜치 생성
3. 작업 후 커밋
4. 원격 저장소로 푸시
5. PR 생성 및 리뷰어에게 리뷰 요청
6. 리뷰 승인 후 `main` 브랜치로 머지
7. 머지 완료된 작업 브랜치 삭제

---

## 5. 브랜치 삭제 방법

```bash
# 로컬 브랜치 삭제
git branch -d feat/1-readme-document-design

# 원격 브랜치 삭제
git push origin --delete feat/1-readme-document-design
```