# 그는 이걸 어떻게 쓰는가.

[How I use LLMs](https://www.youtube.com/watch?v=EWvNQjAaOHw)

모든 내용을 다루지는 않고 내가 흥미롭다고 느끼는 부분들만 정리해보았다.

# ChatGPT와 상호작용이 under the hood에서 어떻게 작동하는가?

우선 GPT와 같은 LLM을 여러 정보가 일종의 손실 압축된 확률 기반의 인터넷 압축파일이라고 모델링 함

GPT와 같은 모델은 크게 2개의 학습 단계가 존재

- pre-training: 인터넷을 토큰으로 분할해서 거대한 압축본으로 만드는 느낌임. 인터넷 문서 기반으로 입력된 토큰에 대해서 다음 토큰을 확률적으로 예측한다. 비싸고 오래걸림. 자주 일어나는 일이 아니다..그래서 특정 시점을 기준으로만 지식을 가지고 있음.
- post-training: zip file에 smiley face를 추가하는 느낌. 파인튜닝하는 과정으로, 이 때 질문에 대해서 응답을 제공하는 Assistant처럼 동작하도록 학습시키는 과정.

Zip 파일에는 파라미터가 들어있고, 이 파라미터는 모델의 가중치로서, 모델이 입력에 대해서 어떤 출력을 생성할지를 결정한다.

사용자와, ChatGPT 간의 상호작용은 이런 느낌임.

사용자가 우선 대화를 시작함. 이 대화는 자연어로 입력되지만 실제로는 일련의 1차원 토큰 배열로 변환되어서 LLM에 전달된다.

그러면 GPT는 이에 대해서 확률적인 처리를 통해서 일련의 토큰을 다시 반환하고, 이를 변환해서 우리에게 보여준다.

즉 대화라는 것은 일련의 token stream 혹은 context window를 같이 만들어가는 과정임.

# Thinking Models and when to use them

가장 최근의 LLM관련 연구 포인트들 중 하나가 강화학습을 통해서 LLM의 추론 능력을 향상시키는 것에 대한 것(DeepSeek가 관련해서 논문을 가장 최초로 공개했다고 하는 것 같음)

Thinking Model은 RL(강화학습)을 통해서 추가로 튜닝된 모델을 의미함.

실제로 사고과정을 많이 요구하는 작업(수학 문제 풀이, 프로그래밍 등)을 처리할 때 정확도가 올라가는 효과가 있음.

# Modalities

더 인간스러운 상호작용을 위한 방법들

- Audio Input/Audio Output

카파시는 꽤나 음성 모드를 많이 사용한다고 함.

특히 모바일 환경에서는 일일이 치고 있기 귀찮아서 음성으로 질의하는 경우가 많다고 한다.

# Custom GPTs

예를 들어서, 한국어를 특정 방식으로 번역해주는 GPT도 있고 등등 사람들이 다양한 의도를 가지고 커스터마이징(프롬프트를 통해) 한 custom GPT들을 써보는 것도 좋은 방법
