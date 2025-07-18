# 챗GPT
> 


▶️ GPT : Chat Generative Pre-trained Transformer, 사전 훈련된 생성형 변환기
▶️ Transformer란 대규모 언어모델(LLM)

▶️ 언어모델(LM) : 인간의 언어 패턴을 이해하고 구조 및 관계를 학습한 후 이를 바탕으로 언어를 생성하도록 훈련된 인공지능 모델 <br/>

▶️ 대규모 언어모델(LLM) : 대용량의 언어모델, 종류에는 GPT, BERT, LlaMA, Claude, PaLM 등이 있음 <br/>

▶️ 트랜스포머(Transformer) : 현재 가장 활발하게 사용되는 딥러닝 아키텍처 중 하나 <br/>
<br/>

*️⃣※ 2017년 구글에서 『Attention is all you need』라는 제목의 논문 발표 <br/>
이 논문의 핵심은 `어텐션 메커니즘(Attention Mechanism)`으로, 이는 모델이 입력된 텍스트의 각 부분을 독립적으로 고려하고 중요한 부분에 더 많은 `주의(Attention)`를 기울이게 하는 기능을 한다. <br/>
이 메커니즘 덕분에 모델은 문장의 전체적인 맥락을 더 잘 이해하여 더욱 정확하고 자연스러운 언어를 생성할 수 있다. <br/>


▶️ GPT : Chat Generative Pre-trained Transformer, 사전 훈련된 생성형 변환기 <br/>
이전에 문장에서 쓰인 단어들을 바탕으로 다음에 올 단어를 예측해 생성하고 생성된 단어를 다시 문장에 포함시켜 그 다음에 올 단어를 예측하는 방법을 반복한다. <br/>
이러한 과정을 거치기 때문에 문장을 자연스럽게 생성하는 데 강점을 가진다.  <br/>

#️⃣ GPT 시리즈 : OpenAI에서 개발한 GPT는 계속 발전 중 <br/>
- GPT는 버전이 올라갈수록 매개변수의 개수가 증가
- 매개변수란, 신경망 모델을 학습할때 사용되는 내부변수
- GPT-3부터 인간과 가까운 언어를 구사하게 되었다는 평을 받았고, GPT-3.5부터 RLHF(인간 피드백형 강화학습)을 적용하여 사람들의 니즈를 충족시켜 주는 방향으로 발전시켜왔다. 이때부터 챗GPT라고 부름
- GPT-4는 비약적으로 많은 매개변수를 이용하며, 이미지를 이해(사진을 보고 물건의 사용법을 알려주거나, 요리재료를 보고 음식을 추천하는 등 다양한 분야에 사용) <br/>
간단한 명령으로 이미지를 생성하거나 음성을 입력받아 음성으로 대답해주는 서비스를 추가했으며, 이러한 기능을 특정한 목적에 맞춰 구성할 수 있도록 GPTs라는 서비스를 추가했다.


▶️ 챗GPT 웹서비스 알아보기
- ❶ 프롬프트 입력
- ❷ 프롬프트 보내기
- ❸ GPT 버전 설정 (GPT-3.5, GPT-4)
- ❹ 슬라이드 접기/펼치기
- ❺ 새 채팅 세션 생성
- ❻ 이전 채팅 리스트
- ❼ GPT Plus
- ❽ 도움말

<!-- ♠️ ♣️ ♥️ ♦️ -->
♣️ 챗GPT Plan 차이(요금제) <br/>

| 기능 | Free | Plue |
|------|------|------|
| 모델    | GPT-3.5       | GPT-4 |
| 응답속도 | 상대적으로 느림 | 상대적으로 빠름 |
| 사용량에 따른 접속 제한 | 있음 | 없음 |
| 입력 토큰 제한 | 4096 | 8192 |
| Beta 체험   | 불가능 | 가능  |
| Plugin 추가 | 불가능 | 가능  |
| 이미지 인식/생성 | 불가능 | 가능  |
| GPTs 생성/사용  | 불가능 | 가능  |


♥️ 참조 : https://platform.openai.com/docs/quickstart?api-mode=responses

