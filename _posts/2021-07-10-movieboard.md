---

title: '[React]React, Node, MySQL Movie Board'
excerpt: "Make a Movie Board with React, Node, MySQL."


categories:
    - react

tags:
    - [web,react,mysql,node]


toc: true
toc_sticky: true


date: 2021-07-10
last_modified_at: 2021-07-10

---

# React 이용한 Movie Board 만들기

![image](/assets/images/21_07_10_movieboard/4.png)  

![image](/assets/images/21_07_10_movieboard/5.png)

---

## 1. useState() & useEffect()

**useState() 란?**  
useState는 함수형 컴포넌트에서 상태값을 관리하게 해준다.

```
// 기본구조
const [state, setState] = useState(initialState);
```

초기값을 매개변수로 useState를 호출하면 첫 번째, 두 번째 요소에 각각 state, setState를 받을 수 있다.

```
// 사용 예
import React, { useState } from 'react'
export default function Profile () {
    const [name,setName] = useState('');
    return (
        <div>
            <p>{`name is ${name}`}</p>
            <input type='text' value={name} onChange={e=>setName(e.target.value)}></input>
        </div>
    )
}
```

**useEffect() 란?**  

어떤 Effect를 발생시키고 싶을 때 사용한다. 여기서 말하는 Effect란 명령형 함수 또는 타이머, 로깅, 변형, sideEffect 등을 발생시키는 함수등을 말한다.
useEffect에 전달된 함수는 렌더링 완료 후 실행되지만, 어떤 값이 변경됐을 경우 실행되도록 할 수도 있다.



## 2. Axios 란?

```
import axios from 'axios';
```

Axios는 브라우저, Node.js를 위한 Promise API를 활용하는 HTTP 비동기 통신 라이브러리이다.
백엔드와 프론트엔드 통신을 쉽게하기 위해 Ajax와 더불어 사용한다.

```
// GET 요청

const axios = require('axios');

// ID로 사용자 요청
axios.get('/user?ID=12345')
  // 응답(성공)
  .then(function (response) {
    console.log(response);
  })
  // 응답(실패)
  .catch(function (error) {
    console.log(error);
  })
  // 응답(항상 실행)
  .then(function () {
    // ...
  });

// POST, DELETE, PUT...
```



---

## 3. Conclusion


![image](/assets/images/21_07_10_movieboard/1.png)  

![image](/assets/images/21_07_10_movieboard/2.png)  

![image](/assets/images/21_07_10_movieboard/3.png)  

---

React, Node(express), MySQL 을 이용하여 CRUD 시스템을 구현해보았다.
React와 Hook, 주요 라이브러리 및 백엔드 관련해서 더 많은 공부가 필요하다고 느꼈다.




