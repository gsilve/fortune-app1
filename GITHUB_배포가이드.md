# 🚀 GitHub Pages 배포 완벽 가이드

초보자도 따라할 수 있는 단계별 설명

---

## 📌 시작하기 전에

### 준비물
- [ ] fortune-app.zip 다운로드 완료
- [ ] fortune-app 폴더 압축 해제
- [ ] 인터넷 연결
- [ ] 이메일 주소

### 예상 소요 시간
- GitHub 가입: 5분
- 저장소 생성: 2분
- 파일 업로드: 5분
- Pages 활성화: 3분
- **총 15분**

---

## STEP 1: GitHub 계정 만들기

### 이미 GitHub 계정이 있으면 → STEP 2로!

### 계정 생성 (5분)

```
1. 브라우저에서 https://github.com 접속

2. 우측 상단 "Sign up" 클릭

3. 이메일 입력
   예: moneyfortune2025@gmail.com

4. 비밀번호 만들기
   (영문+숫자+특수문자 조합, 8자 이상)

5. 사용자명(Username) 입력
   추천:
   - moneyfortune
   - donbyul-fortune  
   - fortune12zodiac
   
   ⚠️ 중요: 이 이름이 URL에 들어감!
   https://사용자명.github.io

6. 이메일 인증 코드 입력
   (이메일 확인)

7. 인증 문제 풀기
   (로봇 아님 확인)

8. "Create account" 클릭

9. 무료 플랜 선택
   (Free 선택)

10. 완료! ✅
```

---

## STEP 2: 저장소(Repository) 만들기

### 2-1. 새 저장소 생성

```
1. GitHub 메인 페이지
   (로그인 후 화면)

2. 우측 상단 "+" 버튼 클릭

3. "New repository" 선택
```

### 2-2. 저장소 설정

```
Repository name 입력란:
┌─────────────────────┐
│ fortune-app         │ ← 정확히 이렇게!
└─────────────────────┘

Description (설명) 입력란:
┌─────────────────────────────────┐
│ 12띠 금전운 자동 생성 도구       │
└─────────────────────────────────┘
(선택사항, 안 써도 됨)

Public / Private 선택:
⦿ Public ✅ (이것 선택!)
○ Private

⚠️ 중요: Public으로 해야 무료!

Initialize this repository:
□ Add a README file (체크 X)
□ Add .gitignore (체크 X)  
□ Choose a license (선택 X)

⚠️ 중요: 아무것도 체크 안 함!
```

### 2-3. 저장소 생성

```
하단 녹색 버튼
"Create repository" 클릭!

→ 빈 저장소 페이지로 이동됨
```

---

## STEP 3: 파일 업로드

### 3-1. 파일 준비

```
1. fortune-app.zip 압축 해제
   (더블클릭 또는 우클릭 → 압축 풀기)

2. fortune-app 폴더 열기

3. 폴더 안의 모든 파일 확인
   (21개 파일 있어야 함)
```

### 3-2. 업로드 방법 A: 드래그 앤 드롭 (추천!)

```
1. GitHub 저장소 페이지에서
   "uploading an existing file" 링크 클릭
   
   또는
   
   페이지 중앙에 있는 안내 확인:
   "Drag and drop files here..."

2. fortune-app 폴더 열기
   (Windows 탐색기 / Mac Finder)

3. 모든 파일 선택
   - Windows: Ctrl + A
   - Mac: Cmd + A

4. 선택한 파일들을 GitHub 페이지로 드래그!
   
5. 파일이 업로드되면 하단으로 스크롤

6. "Commit changes" 입력란:
   ┌─────────────────────────┐
   │ Add fortune-app files   │
   └─────────────────────────┘
   (자동 입력되어 있음, 그대로 두면 됨)

7. 녹색 버튼 "Commit changes" 클릭!

8. 업로드 완료! (1-2분 소요)
```

### 3-3. 업로드 방법 B: Upload files 버튼

```
1. 저장소 페이지 상단
   "Add file" 버튼 클릭

2. 드롭다운에서
   "Upload files" 선택

3. "choose your files" 클릭
   또는 파일 드래그

4. fortune-app 폴더 안의
   모든 파일 선택

5. "Open" 클릭

6. 파일 업로드 확인 후
   하단 "Commit changes" 클릭

7. 완료!
```

### 3-4. 업로드 확인

```
저장소 페이지에서 확인:

파일 목록이 보여야 함:
- index.html
- slide-format-generator.html
- title-generator.html
- fortune-templates.json
- ...등 21개 파일

⚠️ 주의: 
폴더 안에 폴더가 있으면 안 됨!
fortune-app/fortune-app/index.html ❌
fortune-app/index.html ✅
```

---

## STEP 4: GitHub Pages 활성화

### 4-1. Settings 메뉴로 이동

```
저장소 페이지 상단 탭:
Code  Issues  Pull requests  Settings
                              ↑ 클릭!
```

### 4-2. Pages 설정

```
왼쪽 사이드바 (스크롤 내려서 찾기):

General
Access
...
Pages ← 클릭!
```

### 4-3. Source 설정

```
Build and deployment 섹션:

Source: 
┌──────────────────┐
│ Deploy from a   │
│ branch    ▼      │
└──────────────────┘

Branch:
┌──────────────┬────┐
│ main    ▼    │ / (root) ▼ │
└──────────────┴────┘

"Save" 버튼 클릭!
```

### 4-4. 배포 대기 (1-5분)

```
상단에 파란색 박스 나타남:
"GitHub Pages source saved."

페이지 새로고침 (F5)

1-5분 후 다시 확인하면
초록색 박스로 변경:

┌────────────────────────────────┐
│ ✅ Your site is live at        │
│ https://사용자명.github.io/    │
│ fortune-app/                   │
└────────────────────────────────┘

이 URL이 당신의 웹앱 주소!
```

---

## STEP 5: 접속 및 테스트

### 5-1. URL 접속

```
브라우저 새 탭에서:
https://사용자명.github.io/fortune-app/

예시:
https://moneyfortune.github.io/fortune-app/
```

### 5-2. 메인 페이지 확인

```
index.html 페이지가 열려야 함:

┌────────────────────────────┐
│ 💰 띠별 운세 자동 생성     │
│                            │
│ [띠별 운세 생성]           │
│ [12띠 한방 생성]           │
│ [썸네일 생성]              │
│ ...                        │
└────────────────────────────┘

모든 카드가 잘 보이면 성공!
```

### 5-3. 각 도구 테스트

```
클릭해서 확인:

✅ 띠별 운세 생성
   → zodiac-fortune-app.html 열림
   
✅ 12띠 슬라이드 생성
   → slide-format-generator.html 열림
   
✅ 영상 제목 생성
   → title-generator.html 열림
   
✅ 썸네일 생성
   → thumbnail-auto-generator.html 열림
   
✅ 채널 정보
   → channel-info-generator.html 열림

모두 작동하면 완벽! 🎉
```

---

## 🎁 보너스: 모바일 앱처럼 사용

### iPhone (Safari)

```
1. Safari에서 URL 접속
   https://사용자명.github.io/fortune-app/

2. 하단 중앙 공유 버튼 터치
   (사각형에 위쪽 화살표 ⬆️)

3. 스크롤해서 "홈 화면에 추가" 찾기

4. 이름 입력:
   ┌─────────────────┐
   │ 돈별운세 제작   │
   └─────────────────┘

5. "추가" 터치

6. 홈 화면에 아이콘 생성! 📱
   → 앱처럼 터치해서 실행
```

### Android (Chrome)

```
1. Chrome에서 URL 접속

2. 우측 상단 메뉴(⋮) 터치

3. "홈 화면에 추가" 선택

4. 이름 입력:
   ┌─────────────────┐
   │ 돈별운세 제작   │
   └─────────────────┘

5. "추가" 터치

6. 자동 설치 확인 → "추가"

7. 홈 화면에 아이콘 생성! 📱
```

---

## 🔧 문제 해결 (Troubleshooting)

### Q1: 404 오류가 나요

```
원인: Pages가 아직 배포 안 됨

해결:
1. 5분 더 기다리기
2. Settings → Pages 다시 확인
3. Branch가 "main"인지 확인
4. URL 정확히 입력했는지 확인
   (fortune-app 맞는지)
```

### Q2: 페이지가 비어있어요

```
원인: 파일이 잘못된 위치에

해결:
1. 저장소 메인 페이지에서
   index.html이 보이는지 확인
   
2. fortune-app/fortune-app/index.html
   이런 구조면 잘못됨
   
3. 파일 다시 업로드:
   - 기존 파일 전부 삭제
   - fortune-app 폴더 "안의" 파일만 업로드
```

### Q3: CSS가 안 먹혀요

```
원인: 경로 문제

해결:
1. 브라우저 새로고침 (Ctrl+F5)
2. 캐시 삭제
3. 시크릿 모드로 테스트
```

### Q4: 폴더 구조가 이상해요

```
잘못된 구조:
fortune-app/
└─ fortune-app/
   └─ index.html

올바른 구조:
fortune-app/
├─ index.html
├─ slide-format-generator.html
└─ ...

해결:
압축 풀 때 폴더 하나만 나오게!
```

---

## ✅ 최종 체크리스트

배포 완료 확인:

- [ ] GitHub 저장소 생성됨
- [ ] 21개 파일 모두 업로드됨
- [ ] Pages 활성화 완료
- [ ] URL 접속 가능
- [ ] index.html 정상 표시
- [ ] 모든 도구 작동 확인
- [ ] 모바일에서도 테스트

모두 체크되면 완벽! 🎉

---

## 🎯 다음 단계

### 1. URL 북마크
```
브라우저 북마크 추가
→ 즐겨찾기 바에 고정
```

### 2. 모바일 앱 추가
```
iPhone/Android 홈 화면에 추가
→ 앱처럼 빠르게 접속
```

### 3. 사용 시작!
```
매일 새벽 접속:
1. slide-format-generator.html
   → 대본 생성
   
2. title-generator.html
   → 제목 생성
   
3. VREW에서 영상 제작
   
4. 유튜브 업로드!
```

---

## 📌 중요한 URL 정리

### 당신의 웹앱 주소:
```
https://[사용자명].github.io/fortune-app/

예시:
https://moneyfortune.github.io/fortune-app/
```

### GitHub 저장소:
```
https://github.com/[사용자명]/fortune-app

예시:
https://github.com/moneyfortune/fortune-app
```

### Settings (수정할 때):
```
https://github.com/[사용자명]/fortune-app/settings/pages
```

---

## 💡 Pro Tips

### 파일 수정하려면:
```
1. GitHub 저장소 접속
2. 수정할 파일 클릭
3. 연필 아이콘(✏️) 클릭
4. 수정
5. "Commit changes" 클릭
6. 자동 재배포 (1-2분)
```

### URL 공유:
```
팀원이나 다른 사람과 공유 가능!
누구나 접속해서 사용 가능
(Public 저장소니까)
```

### 나중에 업데이트:
```
1. fortune-app 파일 수정
2. GitHub에 다시 업로드
3. 자동 반영 (1-2분)
```

---

## 🎉 축하합니다!

GitHub Pages 배포 완료! 🚀

이제 어디서든 URL로 접속해서
운세 콘텐츠를 만들 수 있습니다!

---

생성일: 2025-10-25
버전: 1.0 (초보자용)
