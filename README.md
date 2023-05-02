# git-conventions
Git conventions for clean code

## How to use Repo
1. Issue를 생성합니다.
2. Issue에 대응하는 branch를 **branch 규칙**에 따라 생성합니다.
3. Issue와 관련된 feature의 개발이 완료되면 **commit 규칙**에 따라 커밋합니다.
4. Branch를 병합하기 위한 PR을 요청합니다.
5. Merge 후 해당 브랜치를 제거합니다.
6. Issue를 종료합니다.

## Branch Naming Convention

| 이름 | 규칙 | 설명 | 분기점 | 병합점 |
|---|---|---|---|---|
| Master | `main` | 배포 가능한 최종 상태의 브랜치 | - | Develop |
| Develop | `develop` | 기능 개발을 위한 분기 및 병합 지점으로 사용하는 브랜치 | Master | Release |
| Release | `release/v<release-version>` | 배포를 위한 마무리 작업 브랜치 | Develop | Master |
| Hotfix | `hotfix/v<hotfix-version>` | 배포 버전에서 발생한 버그 긴급 수정 작업 브랜치 | Master | Master, Develop |
| Feature | `feature/<feature-name>` | 기능 개발 브랜치 | Develop | Develop |
| Refactoring | `refactor/<feature-name>` | 리팩토링 브랜치 | Develop | Develop |

## Pull Request Convention
- Pull request template에 따라 내용을 작성합니다.
```
## What is this PR?
- contents

## Changes
- contents

## Test Checklist - to Reviers
- [ ] checklist
```

## Commit Naming Convention
| 이름 | 규칙 | 설명 |
|---|---|---|
| feat | `feat: <contents> (#<issue-number>)` | 새로운 기능에 대한 커밋 |
| fix | `fix: <contents> (#<issue-number>)` | build 빌드 관련 파일 수정에 대한 커밋 |
| build | `build: <contents> (#<issue-number>)` | 빌드 관련 파일 수정에 대한 커밋 |
| chore | `chore: <contents> (#<issue-number>)` | 그 외 자잘한 수정에 대한 커밋(기타 변경) |
| ci | `ci: <contents> (#<issue-number>)` | CI 관련 설정 수정에 대한 커밋 |
| docs | `docs: <contents> (#<issue-number>)` | 문서 수정에 대한 커밋 |
| style | `style: <contents> (#<issue-number>)` | 코드 스타일 혹은 포맷 등에 관한 커밋 |
| refactor | `refactor: <contents> (#<issue-number>)` | 코드 리팩토링에 대한 커밋 |
| test | `test: <contents> (#<issue-number>)` | 테스트 코드 수정에 대한 커밋 |

### 커밋 메시지 예시
- Issue를 종료하는 경우 커밋명 footer에 `close` 태그를 사용한다.
```
feat: 관심지역 알림 ON/OFF 기능 추가 (#123)

시군구의 알림을 각각 ON/OFF 할 수 있도록 기능을 추가함
 - opnion0055: 구분 코드

해결: close #123
```
