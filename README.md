# TALA AI — Frontend

> **Traffic Accident Legal Advisor, based on AI**
> 교통사고 상황을 입력하면 관련 법령을 근거로 과실과 대응 방법을 안내하는 AI 법률 조언 서비스

**🏆 IBM 겨울 해커톤 우승작** (2025년 2월) · 팀 **한문철TV**

이 저장소는 TALA AI의 **프론트엔드**입니다. 프론트엔드는 [Rehgud](https://github.com/Rehgud)가 전담해 개발했습니다.
백엔드·모델은 팀 조직 [TALA-AI](https://github.com/TALA-AI)에 있습니다.

## 구성

| 경로 | 내용 |
|---|---|
| `index.html`, `css/`, `js/main.js` | 서비스 소개 랜딩 페이지. 스크롤에 따라 캔버스 영상 프레임이 재생되는 인터랙션 |
| `videos/picdiet1~3/` | 스크롤 애니메이션용 이미지 프레임 |
| `streamlit/app.py` | Streamlit 기반 AI 챗봇 화면 (랜딩 페이지에 iframe으로 삽입) |
| `images/`, `tala_ai.pdf` | 로고 및 발표 자료 |

## 실행

```bash
# 랜딩 페이지: index.html을 브라우저로 열기 (또는 간단한 정적 서버)
python3 -m http.server 8000

# 챗봇 화면
cd streamlit
pip install -r requirements.txt
streamlit run app.py
```

> 챗봇이 연결되는 백엔드(FastAPI + watsonx.ai)는 별도 저장소에 있습니다.
> `index.html`의 iframe 주소는 해커톤 당시 서버를 가리키므로, 직접 실행할 때는 본인 Streamlit 주소로 바꿔야 합니다.
