# GitHub Branch 사용 가이드

Git 브랜치를 사용하면 메인 코드베이스에 영향을 주지 않고 새로운 기능을 개발하거나 버그를 수정할 수 있습니다. 이 가이드에서는 터미널을 사용하여 GitHub 브랜치를 관리하는 기본적인 방법을 설명합니다.

## 브랜치 생성 및 전환

새 브랜치를 생성하고 전환하려면:

```bash
git checkout -b 브랜치이름
```

예: `git checkout -b feature/login-page`

## 브랜치 목록 확인

모든 로컬 브랜치를 확인하려면:

```bash
git branch
```

원격 브랜치를 포함한 모든 브랜치를 확인하려면:

```bash
git branch -a
```

## 브랜치 전환

기존 브랜치로 전환하려면:

```bash
git checkout 브랜치이름
```

## 변경사항 커밋

1. 변경된 파일을 스테이징:

   ```bash
   git add .
   ```

2. 변경사항 커밋:
   ```bash
   git commit -m "커밋 메시지"
   ```

## 브랜치 푸시

로컬 브랜치를 GitHub에 푸시:

```bash
git push -u origin 브랜치이름
```

## 브랜치 병합

1. 메인 브랜치로 전환:

   ```bash
   git checkout main
   ```

2. 브랜치 병합:
   ```bash
   git merge 브랜치이름
   ```

## 브랜치 삭제

로컬 브랜치 삭제:

```bash
git branch -d 브랜치이름
```

원격 브랜치 삭제:

```bash
git push origin --delete 브랜치이름
```

## 팁

- 브랜치 이름은 작업 내용을 명확히 나타내도록 지정하세요 (예: `feature/user-authentication`, `bugfix/header-overflow`).
- 정기적으로 `git pull`을 실행하여 원격 저장소의 변경사항을 동기화하세요.
- 병합 전 항상 변경사항을 검토하고 테스트하세요.
