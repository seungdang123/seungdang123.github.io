---

title: '[TIL] [14681] 사분면 고르기, [2884] 알람 시계'
excerpt: Review backjoon algorithm.


categories:
    - boj

tags:
    - [python,til,boj,algorithm]


toc: true
toc_sticky: true


date: 2021-04-28
last_modified_at: 2021-04-28

---

**_backjoon algorithm review._**

***

# [14681] 사분면 고르기

 ![image](/assets/images/21_04_28_python/coordinate_1.png)

 ![image](/assets/images/21_04_28_python/coordinate_2.png)

 ***
**_Code_**
 ```
 a = int(input())
b = int(input())

if a == 0 or (-1000 > a and 1000 <a):
    a = int(input())
else:
    x = a
   
if b == 0 or (-1000 > b and 1000 <b):
    a = int(input())
else:
    y = b

if x > 0 and y > 0:
    print("1")

elif x < 0 and y > 0:
    print("2")

elif x < 0 and y < 0:
    print("3")

elif x > 0 and y < 0:
    print("4")
 ```

**_Result_**

 ![image](/assets/images/21_04_28_python/coordinate_3.png)

 ***


# [2884] 알람 시계

 ![image](/assets/images/21_04_28_python/alarm_1.png)
 
 ![image](/assets/images/21_04_28_python/alarm_2.png)

 ***

 **_Code_**

 ```
 h, m = input().split()

h = int(h)
m = int(m)

if m < 45 and h > 0:
    h = h-1
    m = (60 + m) - 45

elif m < 45 and h == 0:
    h = 23
    m = (60 + m) - 45

else:
    h = h
    m = m - 45


print(h, m)
 ```

**_Result_**

 ![image](/assets/images/21_04_28_python/alarm_3.png)