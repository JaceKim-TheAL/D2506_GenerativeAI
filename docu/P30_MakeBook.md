# 챗GPT와 스테이블 디퓨전으로 책만들기

- 챗GPT와 스테이블 디퓨전을 활용하여 책을 젝작하는 생성형 인공지능 앱 만들기
- 두 모델을 사용하여 글을 생성하고 책에서 사용할 이미지를 만덜어내는 과정을 학습한다.
- 특히 이번에는 두개의 모델을 사용하여 보다 창의적인 형태의 인공지능 앱을 제작

### 1. 이미지 생성AI
생성형 AI 중 이미지 생성 인공지능(AI)에 대해 알아보고 오픈소스로 가장 많이 이용되고 있는 모델인 스테이블(Stable Diffusion)에 대해 알아보기

### 이미지 생성AI
- 인공지능을 사용하여 새로운 이미지를 만들어 내는 기술
- 인공지능이 사용자가 입력한 텍스트 설명을 분석하고 이해하여 그 내용에 맞는 이미지를 생성
- 이 기술은 머신러닝과 적대적 생성 신경망(GANs, Generative Adverarial Networks), 트랜스포머(Transformer) 같은 딥러닝 알고리즘을 사용하여 작동

---

# 스테이블 디퓨전 API

### 이미지 생성 AI 서비스
- 달리(DALL-E), 미드저니(Midjourney), 드림스튜디오(DreamStudio), 파이어플라이(Firefly), 노벨AI(NovelAI), 스테이블 디퓨전(Stable Diffusion)
<br/>

### 스테이블 디퓨전(Stable Diffusion)
- Stability AI에서 오픈소스 라이선스로 배포한 이미지 생성 인공지능 모델
- 특히 오픈소스 모델이면서도 낮은 성능의 PC에서도 잘 작동되는 스테이블 디퓨전이 등장하며 이미지 생성 AI의 시대를 열게 되었다
- 스테이블 디튜전 사용방법 <br/>
  ❶ 깃허브에 올라와 있는 stable-diffusion 모델을 복잡한 과정을 거처 직접 설치하여 사용하는 방법 <br/>
  ❷ 허깅페이스에서 Diffusers 프레임워크를 설치해 사용하는 방법 <br/>
  ❸ 노드 방식으로 여러 모델을 조합해 사용하는 comfyUI를 설치해 사용하는 방법 <br/>
  ❹ 가장 많은 사람이 사용하는 방식인 Stable Diffusion web UI를 설치해 사용하는 방법 <br/>

  
### 1. Stable Diffusion API 가입 및 API 키 발급

1️⃣ Stable Diffusion API 접속 : https://stablediffusionapi.com/ <br/>

2️⃣ Sign Up with Google <br/>

3️⃣ API 키 생성  <br/>

4️⃣ Pricing <br/>
<br/>


### 2. Stable Diffusion API

1️⃣ Stable Diffusion API :   <br/>
  - 프롬프트로부터 이미지를 생성하는 Text to Image,   <br/>
  - 이미지와 프롬프트로부터 이미지를 생성하는 Image to Image, <br/>
  - 이미지와 마스크 이미지로부터 부분적인 이미지를 생성하는 Inainting  <br/>
  이 있다.  <br/>

2️⃣ Community Models API V4 <br/>
  - Community Models API V4는 위의 Stable Diffusion API 와 같은 기능을 가지고 있지만, <br/>
    여러 이미지 생성 모델을 자유롭게 사용할 수 있다. <br/>
  - 유저들이 자신들이 원하는 스타일의 이미지를 학습시킨 생성 모델을 이용할 수 있고 <br/>
  - 로라(LoRA)라는 기법을 이용한 모델을 추가로 이용하여 이미지에 다른 스타일을 입히는 방법도 있다. <br/>
    
3️⃣ ControlNet <br/>
  - ControlNet은 이미지를 생성하는 과정에서 좀 세부적으로 제어할 수 있는 기능이다. <br/>
  - 공간의 깊이나 이미지의 외곽선 특징, 인간의 잣 등 특징을 남겨 입력한 이미지의 특징을 최대한 살린 이미지를 생성할 수 있다. <br/>

4️⃣ Text to Video <br/>
  - Text to Video는 프롬프트로부터 비디오를 생성한다. <br/>
  - 현재 생성 AI 인공지능은 이미지를 넘어 영상을 생성하는 데 많은 노력을 기울리고 있다. <br/>
  - 아직은 생성된  영상이 부자연스럽지만 관련 연구가 활발히 이루이지고 있다. <br/>
  
5️⃣ Image Editing <br/>
  - Image Editing에는 이미지를 편집하는 여러 기능이 모여 있다. <br/>
  - 인물을 제외한 배경을 삭제하는 Remove Backgroud, <br/>
  - 이미지를 고해상도로 바꿔주는 Super Resolution, <br/>
  - 이미지의 보이지 않는 외곽 부분을 더 확장시켜 생성하는 Outpainting 등 <br/>
  - 세부적인 기능을 사용할 수 있다.  <br/>
  
6️⃣ Text to 3D <br/>
  - Text to 3D는 프롬프트나 이미지를 입력하여 3D 이미지(Object)를 생성하는 기능이다. <br/>
  - 아직까지는 생성된 3D 이미지에 어색한 부분이 있기는 하지만 빠르게 발전 중인 분야이다. <br/> 
<br/>

### 3. 플레이그라운드

1️⃣ 스테이블 디퓨전 <br/>
  -  sDXL 모델을 사용해 이미지를 출력하는 스테이블 디튜전의 Playground 기본 인터페이스 <br/>
  ① Select API Endpoint : <br/>
  ② Prompt : <br/>
  ③ Negative prompt <br/> 
  ④ Enhance Prompt <br/>
  ⑤ GEnerate : <br/>

2️⃣ Community Model <br/>
  - Community Model은 다른 유저가 학습시킨 모델을 이용할 수 있는 기능이다. <br/>
  - 스테이블 디퓨전과 마찬가지로 Select API Endpoint를 설정하고 Model ID에서 다른 유저의 모델을 선택한다. <br/>
  - 그 밖의 다른 기능은 모두 동일


---

# 스테이블 디퓨전 API와 그라디오로 책 생성 프로그램 제작

##### `TAP1.` 삽화 생성
  - 기본적인 텍스트 입력으로 이미지를 생성 <br/>
  - 소설 내용에 어울리는 프롬프트를 작성할 수 있도록 한다면 보다 편리한 기능이 될 수 있다. <br/>
  🏠 소설 내용에 어울리는 프롬프트를 생성하는 기능과 프롬프트 기반으로 이미지를 생성하는 앱을 제작 <br/>
  <br/>
    
##### `TAP2.` 이미지 편집
  - 생성된 이미지의 많은 부분을 변경해야 할 수 있다. <br/>
  - 수정할 부분을 선택한 후에 어떻게 편집할지 텍스트 입력만으로도 바꿀 수 있다면 편리한 편집 기능이 될 수 있다. <br/>
  🏠 수정할 부분을 선택한 후에 프롬프트 기반으로 이미지를 편집하는 앱을 제작 <br/>
  <br/>


