# 빅테크에서 어떤 것을 보려고 하는지?

feature 개발 자체를 할 줄 아는가를 보는게 아님.

feature 개발은 다들 하는데, 다음 요소들을 고려하고 이해해서 개발하는지가 포인트

- 기본 원리를 이해하고 있는가?
- 현대적인 개발 이론에 대해서 충분히 알고 있는가?
- 설계 능력(디자인 시스템)
- 애자일하게 일해본 경험
- feature개발 관련해서 고려해야되는 변수들이나, 백단에 엮여서 돌아가는 다양한 이론들에 대해서 이해하고 있는지?
- 리팩토링은 너무 당연한 것... 숨쉬듯이 매일매일 코드베이스를 수정해가면서 처리한다.
- 폭 넓은 지식을 갖추면서 동시에 트렌드를 따라가는 노력이 필요하다.
- 백엔드
  - 비동기 트래픽 처리 (큐 기반 처리 등 시스템 간 통신을 비동기적으로 다룰 수 있는 방법들에 대한 이해가 필요)
  - 백엔드는 깊이 있게, 프론트엔드는 폭넓게 다양한 아키텍처 개념들의 장단점 같은 것들을 잘 숙지하는 것이 중요하다.

폭넓게 다루고 사고해야 하며, 왜라는 질문에 대답할 수 있어야 한다.

- 타성과 관성에 젖어서 하던대로 하는게 아니라 명확한 기술적/상황적 이유에 대해서 이해하고 기술을 사용해야 한다.

# CS지식이 언제 쓸모가 있는지?

CS지식이 쓸모가 생기는 상황은 문제 상황이다.

연차가 늘어갈수록 문제를 digging할 때 CS 지식이 도움이 된다. 아니면 깊이 있는 대답을 제공하기 어려움.

고연차에게 기대하는 것

- CS등 기반 지식과 경험이 풍부해서 타인에게 인사이트를 제공할 수 있고
- 문제를 해결하는 능력

고연차와 저연차의 피쳐 처내는 속도 자체는 크게 차이나지 않는다. 그러면 왜 연봉 차이나?
-> 저연차가 모르는 CS관련된 지식과 경험을 토대로 문제 풀고 애들 잘 알려주고 이끌어가면서 성과 내라고...

반대로 말하면? feature 치는 능력만 가지고 고연차가 되었다? 약간 포프 채널에서 이야기했던 전문 주니어 같은 느낌인데, 굳이 돈을 줄 필요가 없음.

문제를 해결하는 사람이 되어야 하는데, 문제를 해결하는 과정에서 CS지식은 반드시 필요하다.(+ 기타 등등 깊고 넓은 지식과 경험..)

# 모르는 키워드

- KETAMA Hash 알고리즘 -> 구글에서 사용하는 알고리즘인데, 이런 것들에 대한 이해가 있는지 기본적으로 고려한다고 함.

# golang으로 한 번 그냥 프로젝트나 갈겨볼까 심심한데?

golang awesome으로 검색하면 깃허브에 golang으로 할만한 다양한 기능들을 모아둔 repo가 있다고 한다. 그걸 보면서 공부하고 체험해보는 것도 도움이 될 듯. (꿀팁!!!)

다른 언어들도 awesome으로 검색하면 이것저것 많이 나온다.

# Golang, Scala, Swift, Rust

다양한 언어를 다뤄보는 것을 추천하심..ㅋㅋㅋㅋㅋ 아니 이게 뭐 되나?

아니지 그래도 뭐 도전적으로 해보는거지.(문제를 해결하는 사람...)

# 개발자가 인프라쪽도 알아야 하는지??

Docker, Dockerizing, Kubernetes를 다루는 것은 숨쉬듯이 할 수 있어야 한다.

일반적으로 배포를 할 때 필요한 것과, Docker를 활용해서 배포하는 것의 차이, 각 상황이 어떤 특징들이 일반적으로 있는지(일반적 배포는 모놀리식, 도커는 MSA로 많이 한다 등...)

가급적 인프라는 클라우드 인프라를 잘 알 수 있도록 노력하자.

- 원리
- 네트워크 이론(개발자들이 잘 모르는 경우가 많음)
- Docker
- Cloud
- Kubernetes(운영 측면에서 필요한 쿠버네티스 이론보다, 개발과 배포 측면에서 필요한 쿠버네티스 이론들이 있음. 운영 측면에서 개발자가 깊게 갈 필요는 없다.)
