# [AI Agents, Clearly Explained](https://www.youtube.com/watch?v=FwOTs4UxQS4)

자 일단 우리가 이미 친숙한 개념인 LLM부터 시작해보자.

LLM은 그 자체만으로는 2가지 한계가 존재함.

- 훈련되지 않은 데이터는 모른다.(특정 고객의 DB 등)
- passive하게 동작함. 우리가 프롬프트를 입력해야지만 처리해서 출력값을 준다.

자 이걸 감안하고 `AI Workflow`라는 개념에 대해서 살펴보자.

만약에 LLM에 지시를 이런식으로 내린다면 어떨까??

내가 물어볼때마다, 내 개인 구글 캘린더에서 일정을 가져와서 참고해서 답변을 보내줘.

그러면 손쉽게 원래 훈련된 데이터는 아닌 나의 개인 일정에 대한 정보를 제공해줄 수 있을 것이다.

근데 만약에 내가 그날 날씨 예보가 어떤지 알고 싶다면..?

그러면 답변하는데 실패하겠지 왜? 날씨에 대한 정보가 없으니까... 내가 사전에 입력한, `predefined`된 path만 통해서 답변을 도출하기 때문에 캘린더 정보 외에 정보를 참고해서 답변을 줄 수 없음.

ai workflows can only follow predefined paths set by humans

근데 그러면 이런 질문 할 수 있겠지? 날씨도 조회해오라고 하면 되지!

그러면 당연히 내가 원하는 답변을 받을 수 있겠지만, 문제는 본질적으로 `the human is the decision maker`라는 점. 어떤 단계를 거쳐서 답변을 도출할지 인간이 미리 설정(결정)해서 이에 대한 처리를 기계가 수행하는, 기존 시스템보다야 약간 더 동적이긴 하지만 여전히 `에이전트`적인 동작이라고 보기는 힘들다. 자율성이 없다고 생각되기는 해.

참고로 RAG도 여기저기서 화려하게 표현되기는 하는데, 그냥 `type of ai workflow`임. `lookup something`해서 문제 처리해라 이거지뭐.

인간이 정의한 경로를 통해서 작업을 처리하면 `ai workflow`임.

여기에 추가로, 사전에 정의된 flow에 의해서 원하는 결과가 나오지 않았을 때 이를 인간이 manual하게 수정해서 피드백을 돌려야한다는 점.

# AI Agent 의 등장..

어떤 작업을 처리하기 위해서 인간이 하는 일을 생각해보자.

1. `Reason` - 어떤 프로세스를 통해서 어떤 점들을 고려해서 일을 처리할지 추론해야함.
2. `Act(using tools)` - 결정된 프로세스의 각 단계를 처리할 수 있는 도구를 활용해서 작업을 처리해야 함.

이 과정에서는 인간이 지속적으로 의사결정을 한다.

- 어떤 과정을 통해서 일을 처리할지
- 각 과정을 어떤 도구를 통해서 처리할지.

이 의사결정을 `Agent`가 해야지 `AI Agent`지.

주어진 작업이 있을 때, 일단 작업을 어떻게 처리하는지 좋을지 인간이 미리 결정해주는것이 아니라, AI Agent 가 추론을 통해서 작업 단계를 생성하는 것.

그리고 Agent는 본인이 추론해낸 작업과정을 기반으로 각 과정에 적합한 도구를 선택해서 Act할 수 있어야 한다.

이 구조 때문에 가장 많이 사용되는 ai agent configuration 방식이 ReAct Framework임. `Reason` + `Act`

그리고 AI Agent의 또 하나의 특장점은 `ability to iterate`

사람이 의사결정을 할 때는 결과를 수정하기 위해서 다시 프롬프트를 작성하거나 해서 시스템을 돌렸어야 하는데, AI Agent는 생성된 결과를 별도의 특정작업 특화 LLM에 넣어서 돌려서 개선하는 작업을 몇 번 돌린다던지 하는 식으로 iteration을 하는게 가능하다.

심지어 이 필요여부와 어떤 도구가 필요한지를 AI가 판단해서 자율적으로 처리하는게 AI Agent 개념.

# 정리하자면

1단계 LLM: LLM에 인풋 제공하고 아웃풋 받음.
2단계 AI Workflow: LLM에 인풋과 predefined process path를 제공해서 여러 단계를 걸쳐서 원하는 작업을 처리한 아웃풋을 받음. 인간이 의사결정 판단 주체
3단계 AI Agent: AI Agent가 주어진 인풋을 처리하기 위한 작업과 필요한 도구를 추론해서 처리함. Reasoning -> Act -> (필요시) Iteration 이 과정을 알아서 하는 것.

# [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)

앤트로픽에서 올려준 글을 보면, 사람들마다 `agent`라는 것을 조금씩 다르게 이해한다고 함.

앤트로픽에서는 `workflow`와 `agent`로 구분짓는다고...

workflow - Workflows are systems where LLMs and tools are orchestrated through predefined code paths.

agent - on the other hand, are systems where LLMs dynamically direct their own processes and tool usage, maintaining control over how they accomplish tasks.
