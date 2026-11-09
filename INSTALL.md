# StoryWeave 설치 안내 (Windows, 베타)

StoryWeave 베타는 Windows 10/11 64비트용 실행 파일 하나입니다. 인터넷 없이도 집필할 수 있고, 작품은 내 PC에만 저장됩니다.

> 첫 공개 배포는 베타입니다. 정식판 안내는 정식판을 낼 때 따로 적습니다.

## 처음 설치 (또는 베타 0.1.7·0.1.8에서 옮겨 올 때)

1. [Releases](https://github.com/godgyu77/StoryWeave-Releases/releases)에서 최신 베타(Pre-release)의 `StoryWeave-<버전>-windows-amd64.exe`를 받습니다.
2. 실행 파일을 **쓰기 가능한 폴더**에 둡니다(예: `내 문서\StoryWeave`). `C:\Program Files` 같은 곳은 피해 주세요. 업데이트 파일이 실행 파일 옆 숨김 폴더 `.storyweave-update`에 생깁니다.
3. 두 번 눌러 실행합니다. 화면 오른쪽 아래 알림 영역에 StoryWeave 아이콘이 생기고 브라우저가 열립니다.

- 작품은 `%LOCALAPPDATA%\StoryWeaveBeta`에 저장됩니다. 베타 0.1.7·0.1.8과 같은 폴더라서, 새 실행 파일로 바꿔도 쓰던 작품이 그대로 열립니다.
- ChatGPT 로그인도 0.1.7·0.1.8과 같은 곳(`%AppData%\StoryWeaveBeta`)에 있어 다시 로그인하지 않아도 됩니다.
- 예전 실행 파일(`StoryWeave-Beta-v0.1.8.exe` 등)은 지우지 말고 보관해 두면, 문제가 있을 때 그것으로 다시 열 수 있습니다. 두 개를 동시에 실행하지는 마세요.
- 처음 실행할 때 Windows SmartScreen이 "알 수 없는 게시자"라고 경고할 수 있습니다. 아래 "파일 확인"으로 받은 파일이 맞는지 확인한 뒤 실행해 주세요. 앱 안에서 받은 업데이트는 이 경고가 다시 뜨지 않습니다.

## 파일 확인 (선택)

PowerShell에서 받은 파일의 SHA-256을 확인할 수 있습니다.

```powershell
Get-FileHash .\StoryWeave-v0.1.9-beta.1-windows-amd64.exe -Algorithm SHA256
```

결과가 같은 릴리스의 `storyweave-update.json`에 적힌 `sha256`과 같아야 합니다. 프로그램은 업데이트할 때 이 확인과 전자서명 확인을 직접 합니다.

## 업데이트

업데이트 기능이 들어간 베타부터는 **설정 → 프로그램 정보 → 업데이트 확인**에서 받습니다. 자세한 내용은 [README.md](README.md)를 보세요.

- 저장하지 않은 원고가 열린 탭에 있으면 설치 버튼이 잠깁니다. 저장하거나 버린 뒤 설치하세요.
- AI 작업이 진행 중이거나 ChatGPT 로그인 중이면 끝난 뒤에 설치할 수 있습니다.
- 설치하면 StoryWeave가 잠시 닫혔다가 새 버전으로 다시 열립니다. 브라우저 화면에 "새로 고침" 안내가 나오면 눌러 주세요.
- 새 버전이 제대로 시작되지 않으면 원래 버전으로 자동으로 되돌립니다.

## 직접 되돌리기

업데이트 뒤에 문제가 있거나 "되돌리지 못했습니다" 안내가 나오면 이전 버전으로 돌아갈 수 있습니다.

1. 알림 영역의 StoryWeave 아이콘에서 끝내기를 누릅니다.
2. 실행 파일이 있는 폴더의 숨김 폴더 `.storyweave-update\backup` 안에서 이전 프로그램 파일(예: `StoryWeave-v0.1.9-beta.1.exe`처럼 버전이 붙은 파일)을 찾습니다. 탐색기에서 "숨긴 항목"을 켜야 보입니다.
3. 그 파일을 원래 실행 파일 자리에 복사해 원래 이름으로 바꿉니다.
4. 다시 실행합니다.

작품과 설정은 `%LOCALAPPDATA%\StoryWeaveBeta`에 따로 있어 되돌려도 그대로입니다.
