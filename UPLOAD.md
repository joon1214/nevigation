# 업로드 방법

이 폴더(`daewon-3d-map`)를 통째로 올리면 됩니다. 두 가지 방법 중 편한 쪽으로.

## A. 웹에서 드래그앤드롭 (git 설치 불필요)

1. https://github.com/new 접속
2. Repository name에 `daewon-3d-map` 입력, **Public** 선택
3. "Add a README file" 등 체크박스는 **모두 해제** (이미 README가 있음)
4. `Create repository` 클릭
5. 다음 화면의 **uploading an existing file** 링크 클릭
6. 이 폴더 안의 `index.html`, `README.md`, `.gitignore`를 드래그해서 넣고 `Commit changes`

> 탐색기에서 `.gitignore`가 안 보이면 보기 > 숨긴 항목 체크

## B. git으로 올리기

먼저 git 설치:

```powershell
winget install --id Git.Git -e
```

설치 후 **PowerShell 창을 새로 열고** (PATH 갱신 필요):

```powershell
cd c:\Users\User\Desktop\project\daewon-3d-map

git config --global user.name  "이름"
git config --global user.email "jaeyeong2022@gmail.com"

git init
git add .
git commit -m "충주대원고등학교 3D 배치도 + 길찾기"
git branch -M main
git remote add origin https://github.com/<본인계정>/daewon-3d-map.git
git push -u origin main
```

`push`할 때 GitHub 로그인 창이 뜨면 브라우저로 인증하면 됩니다.
(비밀번호 입력을 요구하면 계정 비밀번호가 아니라
Settings > Developer settings > Personal access tokens 에서 만든 토큰을 넣어야 합니다.)

---

## 올린 뒤: GitHub Pages로 바로 보이게 하기

저장소가 Public이면 무료로 웹에 띄울 수 있습니다.

1. 저장소 > **Settings** > 왼쪽 메뉴 **Pages**
2. Source를 `Deploy from a branch`, Branch를 `main` / `/ (root)`로 두고 Save
3. 1~2분 뒤 `https://<본인계정>.github.io/daewon-3d-map/` 에서 열립니다

파일 이름을 `index.html`로 맞춰 두었기 때문에 별도 설정 없이 바로 열립니다.
