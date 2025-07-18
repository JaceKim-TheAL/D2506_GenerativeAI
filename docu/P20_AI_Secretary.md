# 음성인식 AI비서

### STT(Sppech to Text) 서비스
사람이 말한 음성성을 인식해서 글자로 바꿔주는 기술 <br/>

▶️ 주요특징 <br/>
- 실시간 음성 인식: 회의, 전화, 방송 등에서 바로 텍스트로 변환
- 화자 분리: 누가 말했는지 구분 가능 (예: 상담원 vs 고객)
- 키워드 추출: 특정 단어나 금지어 자동 감지
- 활용 분야: 콜센터, 회의록 자동화, 자막 생성, 음성 명령 인터페이스 등
<br/>

▶️ 서비스종류 <br/>
1. 클로바노트, NAVER ClovaNote 
- 회의, 강의, 상담 등의 다양한 상황에 맞도록 편리하게 사용할 수 있는 서비스
- 녹음한 내용을 텍스트로 변환
- 핵심 내용만 요약해 요점만 정리
- 홈페이지 : https://clovanote.naver.com/
<br/>

2. 다글로 
- 영상 파일 업로드 뿐만 아니라 유튜브 링크를 붙여 넣으면 영상의 음성을 원고로 생성
- 녹음환경에 따른 발화자의 수를 인식하고 발화자별로 음성인식 결과를 분리
- 텍스트 내용을 요약한 요약문도 사용 가능
- API 형태로 사용가능
- 무료버전 : 매월20시간 정도 사용 가능
- 홈페이지 : https://daglo.ai/
<br/>

3. 구글받아쓰기
- 구글 문서에도 음성 입력이 있음
- 문장의 길이가 긴 경우에는 적합하지 않고
- 짧은 메모나 회의 안건, 회의 요약과 같은 간단한 문서를 만들때 적합
<br/>

---

### TTS(Text to Speech) 서비스
입력된 텍스트를 사람처럼 말하는 음성으로 바꿔주는 기술 <br/>

▶️ 주요특징 <br/>
- 자연스러운 음성 합성: 딥러닝 기반으로 실제 사람 목소리처럼 들림
- 다국어 지원: 다양한 언어와 억양 제공
- 감정 표현 가능: 기쁨, 슬픔, 분노 등 감정 조절
- 활용 분야: 오디오북, 내비게이션, 음성 비서, 교육 콘텐츠, 접근성 지원 등
<br/>

▶️ 서비스종류 <br/>
1. NAVER ClovaVoice, 클로바보이스
2. 온에어 스튜디오
3. 타입캐스트
<br/>


🔁 STT vs TTS 비교

| 항목 | STT (Speech-to-Text) | TTS (Text-to-Speech) | 
|-----|----------------------|----------------------|
| 변환 방향 | 음성 → 텍스트         | 텍스트 → 음성 | 
| 주요 기술 | 음성 인식, 자연어 처리 | 음성 합성, 딥러닝 | 
| 활용 예시 | 회의록 작성, 자막 생성 | 오디오북, 음성 안내, 챗봇 | 
| 대표 서비스 | Google STT, 네이버 CLOVA STT | Google TTS, Microsoft Azure TTS 등 | 

<br/>

---

### 음성 변환 기술 구현

1. STT

▶️ 위스퍼(Whisper)
- 2022년 OpenAI에서 공개한 인공지능 모델
- OpenAI에서 개발한 오픈소스 음성 인식(STT, Speech-to-Text) 모델
- 다양한 언어와 억양을 인식할 수 있도록 6만 시간 이상의 다국어 음성 데이터로 학습된 Transformer 기반 모델
<br/>

🧠 Whisper의 특징
- 다국어 지원: 한국어, 영어, 일본어 등 수십 개 언어 인식 가능
- 멀티태스킹: 음성 인식뿐 아니라 언어 감지, 음성 번역까지 가능
- 높은 정확도: 잡음이 있는 환경에서도 비교적 정확한 인식
- 오픈소스: 누구나 자유롭게 설치하고 사용할 수 있음
- 모델 크기 다양: tiny, base, small, medium, large 등 성능과 속도에 따라 선택 가능
<br/>

⚙️ 설치 및 사용 예시 (Python)

```shell
pip install git+https://github.com/openai/whisper.git
```
<br/>

```python
import whisper

model = whisper.load_model("base")  # 또는 "small", "medium", "large"
result = model.transcribe("audio.mp3", language="ko")
print(result["text"])
```

<br/>

🚀 활용 예시
- 유튜브 영상 자막 자동 생성
- 회의 녹음 자동 받아쓰기
- 다국어 음성 번역
- 음성 기반 챗봇 입력 처리
<br/>

🔗 더 알아보기
- [Whisper GitHub 저장소](https://github.com/openai/whisper): 설치법, 모델 구조, 예제 코드 등
- [Whisper 사용법 블로그 가이드](https://toby2718.com/whisper-openai/): Windows에서 쉽게 사용하는 방법 정리
<br/>

