# StoryWeave 설치 안내 (Windows)

StoryWeave는 Windows 10/11 64비트용입니다. 인터넷 없이도 집필할 수 있고, 작품은 내 PC에만 저장됩니다.

## 처음 설치

1. [Releases](https://github.com/godgyu77/StoryWeave-Releases/releases)에서 최신 버전의 `StoryWeave-<버전>-windows-amd64.zip`을 받습니다.
2. 압축을 원하는 곳(예: `내 문서\StoryWeave`)에 풉니다. 프로그램 폴더는 **쓰기 가능한 곳**이어야 업데이트를 받을 수 있습니다. `C:\Program Files` 같은 곳은 피해 주세요.
3. `StoryWeave 시작.cmd`를 두 번 눌러 실행합니다. 잠시 뒤 브라우저에 StoryWeave가 열립니다.
4. 끝낼 때는 검은 창을 닫습니다. 저장한 원고는 그대로 남습니다.

- 작품은 `내 문서\StoryWeaveData`에 저장됩니다. 프로그램 폴더를 옮기거나 지워도 작품은 남습니다.
- 처음 실행할 때 Windows SmartScreen이 "알 수 없는 게시자"라고 경고할 수 있습니다. 받은 파일이 맞는지 아래 "파일 확인"으로 확인한 뒤 실행해 주세요.

## 파일 확인 (선택)

PowerShell에서 받은 파일의 SHA-256을 확인할 수 있습니다.

```powershell
Get-FileHash .\StoryWeave-v0.2.0-windows-amd64.exe -Algorithm SHA256
```

결과가 릴리스의 `storyweave-update.json`에 적힌 `sha256`과 같아야 합니다. 프로그램은 업데이트할 때 이 확인과 전자서명 확인을 직접 합니다.

## 업데이트

업데이트 기능이 들어간 버전부터는 **설정 → 프로그램 정보 → 업데이트 확인**에서 받습니다. 자세한 내용은 [README.md](README.md)를 보세요.

- 설치하기 전에 원고를 저장해 주세요. 저장하지 않은 글이 있으면 프로그램이 먼저 물어봅니다.
- AI 작업이 진행 중이면 끝난 뒤에 설치할 수 있습니다.
- 설치하면 StoryWeave가 닫혔다가 새 버전으로 다시 열립니다. 새 검은 창이 뜰 수 있습니다.

## 직접 되돌리기

업데이트 뒤에 문제가 있으면 이전 버전으로 돌아갈 수 있습니다.

1. StoryWeave를 끕니다(검은 창 닫기).
2. 프로그램 폴더의 `app\.storyweave-update\backup` 안에 있는 이전 프로그램 파일(예: `storyweave-v0.1.0.exe`)을 복사합니다.
3. `app\storyweave.exe` 자리에 붙여넣고 이름을 `storyweave.exe`로 바꿉니다.
4. `StoryWeave 시작.cmd`로 다시 실행합니다.

작품과 설정은 데이터 폴더에 따로 있어 되돌려도 그대로입니다.
