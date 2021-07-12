---

title: '"Call by Value" vs "Call by Reference"'
excerpt: What is difference between "Call by Value" and "Call by Reference".


categories:
    - cpp

tags:
    - [c, cpp]


toc: true
toc_sticky: true


date: 2021-03-31
last_modified_at: 2021-03-31

---

**Let's check what is difference between "Call by Value" and "Call by Reference" ?**

<br>

# \#1 Call by Value


<br>

![image](/assets/images/21_03_30_clang/call_by_value.png)
<br><br>

```

1. 입력받은 a, b 값은 swap 함수 매개변수인 x, y 에 넘겨진다.

2. x에는 a, y에는 b 값이 담기고 swap 함수 실행한다.

```

<br>

***

<br>

![image](/assets/images/21_03_30_clang/call_by_value_result.png)

    위의 결과를 보면 의도했던 바와 다르게 a, b값이 바뀌지 않은 상태로 출력되었다.

<br>

***
<br>

## 1-1. Why didn't it work?

swap(a,b)에 의해 a, b 값이 매개변수로 각각 x, y에 전달된다. 이후 정의해 놓은 swap 함수에 의해 x와 y의 값은 바뀌게 되어 x=3, b=2 의 값을 가지게 되지만 a, b의 값은 어떠한 영향도 받지 않으므로 아무런 변화없이 기존의 값을 출력하게 된다.
<br>

***

<br>

# \#2. Call by Reference

<br>

![image](/assets/images/21_03_30_clang/call_by_reference.png)

<br>

```

1. 입력받은 a, b의 주소값이 swap 함수 매개변수인 x, y 에 넘겨진다.

2. 이후 정의된 swap 함수를 실행하게되면 위의 코드와는 다르게 swap 함수 내의 *x, *y 값 뿐만 아니라 a, b값에도 영향을 주기 때문에 의도했던대로 a, b 값이 바뀌어서 출력된 것을 확인 할 수 있다.

```

<br>

***

<br>

![image](/assets/images/21_03_30_clang/call_by_reference_result.png)

