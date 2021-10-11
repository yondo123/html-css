## BasicSize
`max-width`를 적극 활용하자.
```css
body {
	margin : 0 auto;
	max-width : 960px;
	width : 90%;
}
```
## 가변 그리드 (Fluid Grid)
### 개념
그리드는 격자나 눈금 등 구역을 나누는 단위를 의미, 웹 페이지 상에선 가로 크기 또는 세로 크기, 여백 등 웹 사이트의 구조 설계를 나타내는 단위로 사용

### 공식
$${가로너비\over 부모박스의 너비} \ast 100$$
만약, 300px 크기의 박스를 960px 너비를 감싸고있다면 해당 박스의 그리드 값은 `(300 / 960) * 100 = 31.25%`이다.

### 최상위 요소
그럼 최상위 요소는 어떤 기준으로 잡아야할까? 정답은 `없다`이다. 말 그대로 웹 사이트의 구조를 미리 정의해 최상위 요소는 임의의 크기로 잡아야한다.

## 가변 마진 & 패딩
### 가변 마진
$${가로너비\over 부모박스의 너비} \ast 100$$
가변 그리드와 공식은  똑같다.
```css
body {
    box-sizing: border-box;
    margin: 0 auto;
    max-width: 960px;
    width: 90%;
}

#wrap {
    height: 500px;
    background-color: #2d3436;
}

#wrap div {
    display: inline-block;
    /* 200/960*100=20.833333 */
    width: 20.833333%;
    height: 100%;
}

.red {
    background-color: #d63031;
}

.yellow {
    /* 560/960*100=58.333333 */
    margin-left: 58.333333%;
    background-color: #fdcb6e;
}
```

### 가변 패딩
가변 패딩은 너비 값에 포함이된다. → 가장 상위의 박스 크기를 기준으로 삼아야한다.
$${패딩 값\over 최상위 박스의 너비} \ast 100$$

**일반적인 패딩**
```css
body{
    margin: 0 auto;
    max-width: 960px;
    width: 90%;
}

#text-wrap {
    height: 100vh;
    background-color: #636e72;
}

#text {
    /* 40/960*100=4.166667 */
    color: #ecf0f1;
    padding: 40px 4.166667%;
}
```

**박스 유지형 패딩(특정 너비를 유지해야할 때)**
패딩의 좌우합 (예 50px → 100px)을 해당 가로 너비에서 빼준뒤 최상위 너비 값을 나누고 100 곱하면된다.
```css
/* (해당 박스의 너비 - 패딩 적용 값) / 최상위 박스의 너비 * 100 */
#text {
    /* (600-100) / 960 * 100=52.083333 */
    width: 52.083333%;
    /* 50/960 * 100=5.208333 */
    padding: 50px 5.208333%;
    padding: 40px 4.166667%;
    margin: 0 auto;
}
```