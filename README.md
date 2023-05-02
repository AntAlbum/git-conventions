# git-conventions
Git conventions for clean code

## How to use Repo
1. 레포지토리를 fork합니다.
2. 규칙에 따라 브랜치 이름을 정하고 해당 브랜치로 체크아웃합니다.
3. 단위별로 코드가 완성되면 코드를 커밋합니다. 이때 **commint 규칙**을 지켜 커밋합니다.
4. 원본 저장소에 pull request를 보냅니다.
5. 다른 사람들의 PR을 보고 자유롭게 코드리뷰를 합니다.

## Branch Naming Convention

| 이름 | 규칙 | 설명 | 분기점 | 병합점 |
|---|---|---|---|---|
| Master | `main` | 배포 가능한 최종 상태의 브랜치 | - | Develop |
| Develop | `develop` | 기능 개발을 위한 분기 및 병합 지점으로 사용하는 브랜치 | Master | Release |
| Release | `release/v<release-version>` | 배포를 위한 마무리 작업 브랜치 | Develop | Master |
| Hotfix | `hotfix/v<hotfix-version>` | 배포 버전에서 발생한 버그 긴급 수정 작업 브랜치 | Master | Master, Develop |
| Feature | `feature/<feature-name>` | 기능 개발 브랜치 | Develop | Develop |
| Refactoring | `refactor/<feature-name>` | 리팩토링 브랜치 | Develop | Develop |

## Commit Naming Convention
| 이름 | 설명 |
|---|---|
| feat | 새로운 기능에 대한 커밋 |
| fix | build 빌드 관련 파일 수정에 대한 커밋 |
| build | 빌드 관련 파일 수정에 대한 커밋 |
| chore | 그 외 자잘한 수정에 대한 커밋(rlxk qusrud) |
| ci | CI 관련 설정 수정에 대한 커밋 |
| docs | 문서 수정에 대한 커밋 |
| style | 코드 스타일 혹은 포맷 등에 관한 커밋 |
| refactor | 코드 리팩토링에 대한 커밋 |
| test | 테스트 코드 수정에 대한 커밋 |

### 커밋 메시지 예시
```
feat: 관심지역 알림 ON/OFF 기능 추가(#123)

시군구의 알림을 각각 ON/OFF 할 수 있도록 기능을 추가함
 - opnion0055: 구분 코드

해결: close #123
```
