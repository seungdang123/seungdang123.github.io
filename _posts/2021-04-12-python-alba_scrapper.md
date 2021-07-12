---

title: '알바천국 스크래핑'
excerpt: Scraping part-time recruitment info in python by using request & BeautifulSoup.


categories:
    - python

tags:
    - [python, request, beautifulsoup]


toc: true
toc_sticky: true


date: 2021-04-12
last_modified_at: 2021-04-12

---

**Scraping alba recruitment info in python via request & BeautifulSoup**

# \#1 First, Import request & BeautifulSoup

![image](/assets/images/21_04_12_python/py_code_1.png)

```
request & BeautifulSoup 사용할 수 있도록 각 모듈을 import 해준다.
```

***

# \#2 Writing Code
## \#1 Define "write_company" function which make csv file by using scraped info.
![image](/assets/images/21_04_12_python/py_code_2.png)

```
사이트에서 가져온 데이터를 이용하여 csv 파일을 생성하는 함수를 정의. 
```

***

## \#2 Scraping the alba site.
### \#1 Scrape Superbrand.
![image](/assets/images/21_04_12_python/py_code_3.png)

```
알바천국에 "슈퍼 브랜드"로 분류된 브랜드들의 정보를 가져옴. 
request & BeautifulSoup 이용하여 필요한 정보들을 추출, 정보들을 담고 있는 태그를 통해 값을 가져온다.
```
![image](/assets/images/21_04_12_python/mainsuperbrand.png)

<br>

![image](/assets/images/21_04_12_python/impact.png)

***

### \#2 Scrape Each of brand`s recruitments.

![image](/assets/images/21_04_12_python/py_code_4.png)

```
각 브랜드 사이트 이동하여 지역, 근무시간, 급여 등의 정보를 가져온다.
```

![image](/assets/images/21_04_12_python/goodsbox_info.png)

<br>

![image](/assets/images/21_04_12_python/nomal_info.png)

<br>

![image](/assets/images/21_04_12_python/local.png)

***

### \#3 Make a csv file.

![image](/assets/images/21_04_12_python/py_code_5.png)

```
company 딕셔너리의 요소인 jobs 리스트에 각 브랜드의 정보가 담긴 job 딕셔너리를 추가한다.
write_company 함수를 이용하여 csv 파일을 생성한다. 

# 이때 매개변수는 브랜드 명과 근무관련 정보를 담고 있는 company 이다.
```
![image](/assets/images/21_04_12_python/csv.png)

***

**Conclusion**

```
request, BeautifulSoup 통해 알바천국에 슈퍼 브랜드로 분류된 각각의 브랜드 공고 사이트에서 필요한 정보만을 추출해
csv 파일로 한눈에 보기 쉽게 정리해 볼 수 있었다.
```
