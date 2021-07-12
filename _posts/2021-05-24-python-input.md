---

title: '[TIL] input vs sys.stdin.readline'
excerpt: "What is difference input and sys.stdin.readline?"


categories:
    - python

tags:
    - [python,til]


toc: true
toc_sticky: true


date: 2021-05-24
last_modified_at: 2021-05-24

---
# input vs sys.stdin.readline

![image](/assets/images/21_05_24_python/1.png)

알고리즘 문제를 풀 때 input 으로 입력을 받으면 시간초과로 인해 오답 처리가 되지만 sys.stdin.readline 으로 입력을 받으면 시간 안에 채점이 되어 정답으로 인정되는 상황이 자주 발생한다. 

input 과 sys.stdin.readline 의 차이는 무엇일까?

---


# 차이점


1) input 함수는 **파라미터로 프롬프트 메세지**를 받을 수 있는데 이 경우 입력받기 전 프롬프트 메세지를 출력하게 된다. 이러한 점은 약간의 부하로 작용할 수 있다. 하지만 sys.stdin.readline 은 프롬프트 메세지를 파라미터로 받지 않는다.

2) input 함수는 입력받은 값의 **개행 문자를 삭제**시켜서 리턴한다. 하지만 sys.stdin.readline 은 개행 문자를 포함한 값을 리턴한다. input 에는 삭제과정이 포함 sys.stdin.readline 에는 삭제과정이 포함되지 않는 것이다.

---

# 결론

input 함수는 sys.stdin.readline() 과 비교해서 **프롬프트 메세지를 출력**하고, **개행문자를 삭제**하는 과정이 포함되어 있기 때문에 느리다.

따라서 알고리즘 문제를 풀 때는 input 보다 sys.stdin.readline 을 활용하여 입력을 받는 것이 효율적이다.

---

![image](/assets/images/21_05_24_python/3.png)

![image](/assets/images/21_05_24_python/2.png)