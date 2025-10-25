# 🚀 띠별 돈 운세 채널 완전 자동화 패키지

## 📋 목차
1. [시스템 개요](#시스템-개요)
2. [빠른 시작](#빠른-시작)
3. [파일 설명](#파일-설명)
4. [설치 가이드](#설치-가이드)
5. [사용 방법](#사용-방법)
6. [자동화 설정](#자동화-설정)
7. [문제 해결](#문제-해결)

---

## 시스템 개요

### 🎯 목표
**매일 12개 쇼츠 + 월간 12개 롱폼** 자동 생성 및 업로드

### 📊 예상 성과
- **월 360개 쇼츠** (12띠 × 30일)
- **월 12개 롱폼** (12띠 월간 운세)
- **타겟**: 전 국민 (띠별 8.3%)
- **검색 키워드**: 쥐띠 운세, 용띠 재물운 등 (월 수만 건)

### 🛠️ 기술 스택
- **프론트엔드**: React (웹앱)
- **백엔드**: Python 3.11+
- **TTS**: Edge TTS (무료) 또는 타입캐스트
- **영상**: FFmpeg + Pillow
- **트렌드**: Google Trends API (pytrends)
- **업로드**: YouTube Data API v3

---

## 빠른 시작

### ⚡ 30초 안에 시작하기

```bash
# 1. 웹앱 실행 (대본 생성)
open zodiac-fortune-app.html

# 2. Python 스크립트 실행 (자동화)
python3 master_automation.py
```

### 🎬 첫 영상 만들기 (5분)

1. **웹앱에서 띠 선택**
   - `zodiac-fortune-app.html` 열기
   - 생년월일 입력 or 띠 직접 선택
   - "운세 생성" 클릭
   
2. **대본 복사**
   - 생성된 대본 복사 버튼 클릭
   
3. **TTS 생성**
   - VREW 또는 타입캐스트에 붙여넣기
   - AI 음성 자동 생성
   
4. **썸네일 만들기**
   - 캔바 → "유튜브 쇼츠" 템플릿
   - 띠 이모지 + 오늘 날짜
   
5. **업로드**
   - 유튜브 스튜디오 → 쇼츠 업로드

---

## 파일 설명

### 📱 웹앱 (브라우저에서 실행)

| 파일 | 용도 | 특징 |
|------|------|------|
| `zodiac-fortune-app.html` | 띠별 운세 생성기 | 단일 띠 선택, 예쁜 UI |
| `bulk-generator.html` | 12띠 한방 생성기 | 클릭 한 번에 12개 |

**사용법**: 파일을 더블클릭하면 브라우저에서 실행

### 🐍 Python 스크립트 (자동화용)

| 파일 | 용도 | 필수 여부 |
|------|------|----------|
| `trends_fortune_generator.py` | 트렌드 키워드 연동 대본 | ⭐ 핵심 |
| `auto_tts_generator.py` | TTS 자동 생성 | 선택 |
| `youtube_uploader.py` | 유튜브 자동 업로드 | 선택 |
| `longform_fortune_generator.py` | 월간/주간 롱폼 | 선택 |
| `master_automation.py` | 통합 자동화 | ⭐ 최종 |

### 📊 데이터 파일

| 파일 | 용도 |
|------|------|
| `fortune-templates.json` | 12띠 문장 템플릿 |

---

## 설치 가이드

### 1️⃣ 기본 설치 (필수)

```bash
# Python 라이브러리
pip install pytrends --break-system-packages
pip install edge-tts --break-system-packages
pip install Pillow --break-system-packages

# FFmpeg (영상 생성)
# Mac
brew install ffmpeg

# Ubuntu/Debian
sudo apt install ffmpeg

# Windows
# https://ffmpeg.org/download.html 에서 다운로드
```

### 2️⃣ 고급 설치 (선택)

```bash
# Google Cloud TTS (더 자연스러운 음성)
pip install google-cloud-texttospeech --break-system-packages

# YouTube API (자동 업로드)
pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib --break-system-packages
```

### 3️⃣ API 키 설정 (선택)

#### Google Trends (무료)
- 별도 설정 불필요
- pytrends가 자동으로 처리

#### YouTube API (무료 할당량 있음)
1. https://console.cloud.google.com 접속
2. 새 프로젝트 생성
3. YouTube Data API v3 활성화
4. OAuth 2.0 클라이언트 ID 생성
5. `client_secrets.json` 다운로드

---

## 사용 방법

### 🎯 시나리오 1: 수동 제작 (초보자)

**매일 10분 투자로 12개 쇼츠 제작**

```bash
# 1. 웹에서 대본 생성
open bulk-generator.html
# → "12띠 전체 생성" 클릭
# → TXT 다운로드

# 2. VREW에서 일괄 TTS 생성
# - 대본 12개 복사
# - VREW에 붙여넣기
# - AI 음성 자동 적용
# - MP3 일괄 다운로드

# 3. 캔바에서 썸네일 12개 제작
# - 템플릿 하나 만들고 복제
# - 띠만 바꾸기

# 4. 유튜브 스튜디오에서 예약 업로드
# - 오전 7시: 쥐·소·호랑이·토끼띠
# - 낮 12시: 용·뱀·말·양띠
# - 저녁 6시: 원숭이·닭·개·돼지띠
```

### 🤖 시나리오 2: 반자동 (중급자)

**Python 스크립트로 대본+TTS 자동 생성**

```bash
# 1. 트렌드 연동 대본 생성
python3 trends_fortune_generator.py
# → fortune_trends_20251025.json 생성

# 2. TTS 자동 생성
python3 auto_tts_generator.py
# → tts_edge/*.mp3 12개 생성

# 3. 영상 수동 편집 (VREW, 프리미어)

# 4. 유튜브 업로드 (수동)
```

### 🚀 시나리오 3: 완전 자동 (고급자)

**하루 한 번 실행으로 모든 작업 완료**

```bash
# 마스터 스크립트 실행
python3 master_automation.py

# 또는 GitHub Actions로 매일 자동 실행
# (.github/workflows/daily-fortune.yml 설정)
```

---

## 자동화 설정

### 📅 매일 자동 실행 (GitHub Actions)

**`.github/workflows/daily-fortune.yml`**

```yaml
name: Daily Fortune Automation

on:
  schedule:
    - cron: '0 22 * * *'  # 매일 오전 7시 KST
  workflow_dispatch:

jobs:
  generate-and-upload:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Setup Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'
      
      - name: Install dependencies
        run: |
          pip install pytrends edge-tts Pillow
          sudo apt-get install -y ffmpeg
      
      - name: Run automation
        run: python master_automation.py
      
      - name: Upload artifacts
        uses: actions/upload-artifact@v3
        with:
          name: daily-shorts
          path: outputs/shorts/
```

### ⏰ 업로드 시간 최적화

**권장 업로드 스케줄**

| 시간대 | 띠 | 타겟 |
|--------|-----|------|
| 07:00-09:00 | 쥐·소·호랑이·토끼 | 출근길 |
| 12:00-14:00 | 용·뱀·말·양 | 점심시간 |
| 18:00-20:00 | 원숭이·닭·개·돼지 | 퇴근길 |

---

## 문제 해결

### ❓ 자주 묻는 질문

**Q: pytrends 설치가 안 됩니다**
```bash
# --break-system-packages 옵션 추가
pip install pytrends --break-system-packages

# 또는 가상환경 사용
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install pytrends
```

**Q: Edge TTS 음성이 로봇 같아요**
- 타입캐스트, VREW 등 유료 TTS 권장
- Google Cloud TTS도 고려 (월 100만 글자 무료)

**Q: 영상 화질이 낮아요**
- FFmpeg 설정 수정:
```python
# master_automation.py에서
'-c:v', 'libx264',
'-preset', 'slow',  # 추가
'-crf', '18',  # 추가 (낮을수록 고화질)
```

**Q: 유튜브 업로드 실패**
- YouTube API 할당량 확인 (일 10,000 units)
- OAuth 인증 재설정
- client_secrets.json 경로 확인

### 🐛 일반적인 오류

**ModuleNotFoundError**
```bash
# 필요한 라이브러리 전부 설치
pip install pytrends edge-tts Pillow google-api-python-client --break-system-packages
```

**Permission Denied**
```bash
# 실행 권한 추가
chmod +x *.py
```

**FFmpeg not found**
```bash
# 설치 확인
ffmpeg -version

# 없으면 설치
# Mac: brew install ffmpeg
# Ubuntu: sudo apt install ffmpeg
```

---

## 📊 성과 측정

### 예상 채널 성장 (월간)

| 지표 | 1개월 | 3개월 | 6개월 |
|------|-------|-------|-------|
| 쇼츠 수 | 360 | 1,080 | 2,160 |
| 조회수 | 10만 | 50만 | 200만 |
| 구독자 | 1,000 | 5,000 | 20,000 |
| 수익 | $100 | $500 | $2,000 |

*실제 성과는 콘텐츠 품질, 일관성에 따라 달라집니다*

---

## 🎯 다음 단계

### 1주차
- [ ] 웹앱으로 대본 생성 테스트
- [ ] VREW로 TTS 테스트
- [ ] 첫 쇼츠 1개 업로드

### 2주차  
- [ ] Python 스크립트 설치
- [ ] 12띠 전체 대본 자동 생성
- [ ] 일주일간 매일 12개 업로드

### 3주차
- [ ] TTS 자동화 테스트
- [ ] 썸네일 템플릿 확정
- [ ] 업로드 스케줄 최적화

### 4주차
- [ ] 완전 자동화 설정
- [ ] GitHub Actions 또는 크론잡
- [ ] 월간 롱폼 제작 시작

---

## 📞 지원

**문제가 있나요?**
- 이 README를 먼저 확인
- 각 스크립트 파일의 주석 참고
- 오류 메시지를 복사해서 ChatGPT/Claude에 질문

**더 개선하고 싶다면?**
- 템플릿 문장 추가/수정
- 썸네일 디자인 고도화
- 롱폼 콘텐츠 다양화

---

## 📝 라이선스

본 프로젝트는 교육/학습 목적으로 제공됩니다.
- 상업적 이용 가능
- 수정 및 재배포 자유
- 저작권은 각자 콘텐츠에 귀속

**주의사항**
- 운세 콘텐츠는 오락/교양 목적
- 투자 자문이 아님을 명시 필수
- 유튜브 커뮤니티 가이드 준수

---

## 🙏 크레딧

**사용된 오픈소스**
- lunar-javascript (MIT)
- pytrends (Apache 2.0)
- Edge TTS (MIT)
- FFmpeg (GPL/LGPL)

**추천 도구**
- VREW (무료 TTS)
- 타입캐스트 (프리미엄 TTS)
- 캔바 (썸네일 제작)

---

**🎉 성공적인 채널 운영을 응원합니다!**

마지막 업데이트: 2025년 10월 25일
