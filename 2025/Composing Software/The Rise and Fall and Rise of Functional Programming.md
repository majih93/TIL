# [The Rise and Fall and Rise of Functional Programming (Composing Software)](https://medium.com/javascript-scene/the-rise-and-fall-and-rise-of-functional-programming-composable-software-c2d91b424c8c)

람다 대수는 함수 합성에 관한 것이라고 함. 소프트웨어를 구축하기 위해서 함수를 합성하는 방식으로 생각하는 것..

이 글에서는 소프트웨어 디자인에 있어서 함수 합성이 가지는 중요성에 대해서 설명할 예정

# 람다 대수에서 중요한게 뭔데

**익명 함수**

함수는 항상 익명함수이다. -> 근데 이해가 잘 안되기는 하네 이게 무슨 상관이 있다는 것인지 잘은 모르겠음.

**람다 대수에서 함수는 오직 하나의 input만을 받는다. unary function.**

그러면 현실에서는 여러 개의 인자를 받는 함수를 쓰려면 어떻게 해야해? -> 커링이라는 n-ary function을 unary function의 연쇄호출 구조로 변경하는 방법을 사용해야 함.

두 개의 인자를 받는 함수를 하나의 인자를 받는 함수가 다른 인자를 받을 수 있는 함수를 반환하도록 하는 것.

**함수는 일급객체**

함수가 매개변수로 다른 함수의 입력으로 전달될 수 있고, 함수가 함수를 반환할 수도 있다.

# JavaScript는 함수형 컨셉을 잘 구현할 수 있는 언어

근데 언어가 이게 잘 된다고 해서 문제를 그렇게 푸는 것은 약간 좀 이상한거 아닌가? 이 언어는 이게 되니까 이걸로 풀어가 아니라, 이 문제는 이런 접근법이 더 좋은 해결책인데 이 언어는 그런 도구들을 지원하네 그렇게 풀어보자 가 되어야하는게 맞는 것 같음.

JavaScript가 웹의 급속한 발전과 함께 많은 주목을 받으면서 자연스럽게 function composition같은 개념들에 대해서도 사람들이 더 집중하기 시작했고, ES6에 화살표 함수가 등장하면서 커링, 람다 표현식 등이 더 쉬워졌음.
