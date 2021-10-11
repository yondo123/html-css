## HTML Basic
### Structure
**DOCTYPE**
HTML으로 작성되었다는 것을 표시한다. 표준 규격에 맞게 출력할 수 있도록 하려면 `DOCTYPE`을 반드시 기술한다.
```html
<!DOCTYPE html>
```

**head**
`head`내부에는 메타데이터 등을 작성한다.

**body**
`body`내부에는 브라우저 화면에 출력할 내용들을 작성한다.

### Meta
**Encoding**
HTML 파일의 인코딩 종류를 명시한다.
```html
<meta charset='UTF-8' />
```

**Viewport**
모바일 장치에 따른 화면 크기에 맞춰 웹 페이지를 출력한다.
```html
<meta name="viewport" content="width=device-width, initial-scale=1" />
```

### Tag
시작 태그와 종료 태그로 콘텐츠를 감싸서 콘텐츠의 내용을 작성한다.
```html
<tag></tag>
```
**중첩**
태그 내에 태그를 삽입할 수 있다. (부모태그 > 자식태그)
```html
<div><h1>제목</h1></div>
```

**속성**
속성을 사용해 다양한 정보를 추가할 수 있다. 일반적으로 값을 따옴표로 감싸서 사용한다.
```html
<html lang="ko"></html>
```

**빈 태그**
컨텐츠를 꼭 넣지 않고 사용할 수 있는 빈 요소 태그들도 있다.
```html
<img src="image.png" alt="sample"/>
```

### Semantic Tag
**section**
컨텐츠의 그룹을 명시한다. (시각적인 기준으로 나누는 것이 아닌, 비슷한 내용 기준으로 나눈다.)

**nav**
다른 페이지 이동 또는 페이지 내부 요소로의 링크를 모을 때 사용한다.

**aside**
부가 정보라는 것을 명시, 사이드바의 정보나 광고 내용에도 사용한다.

**body**
`sectionng root`라고도 불리며 페이지 전체의 콘텐츠임을 명시한다.

**main**
문서의 핵심적인 내용임을 명시, 하나의 html에서는 한 개의 `main`만을 허용한다.

**article**
하나의 완전한 콘텐츠임을 명시한다. 주로 블로그 또는 뉴스의 기사 등에 사용한다.  
(특정 브라우저에서는 `article`내용을 추출해 쉽게 사용자에게 보여주는 기능이 있다.)
```html
<article>
    <h2>Title</h2>
    <p>Content.</p>
</article>
```
**header**
해당 섹션의 상단임을 명시한다.
**footer**
해당 섹션의 하단임을 명시한다.

### Elements
**h1~h6**
제목임을 명시한다.
```html
<h2>Title.</h2>
```

**div/span**
```html
<div class="blue-text">
    <p>Blue</p>
</div>
<span class="unspread">
    <p>more..</p>
</span>
```
특별한 의미를 가지지 않고, 스타일링을 위해 그룹으로 묶을 때 주로 사용한다.

**p**
```html
<p>The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham.</p>
```
문단을 명시한다.

**br**
줄바꿈을 넣을 때 사용하는 빈요소
```html
<br />
```

**anchor**
링크를 설정한다. 
링크 이동, `href`속성에 이동하고자 하는 주소 입력 (절대경, 상대경로)
- 섹션 이동
    ```html
    <a href="#section">link</a>
    ```
    
- 메일 쓰기
    ```html
    <a href="mailto:myname@gmail.com">write mail..</a>
    ```
- target
    새로운 탭으로 페이지 이동
    ```html
    <a href="www.naver.com" target="_blank">go to naver.com</a>
    ```

**img**
이미지 출력을 위해 사용한다.
- src : 이미지 파일 경로
- alt : 대체 텍스트 경로
    ```html
    <img src="/resource/SAMPLE.png" alt="blog-title" />
    ```

**table**
표를 구성할 때 사용한다.
- tr : table내의 하나의 행
- th : 제목
- td : 내용
```html
<table>
    <tr>
        <th></th>
        <td></td>
    </tr>
</table>
```

**ol/ul**
리스트 형식의 정보임을 명시한다. 리스트의 각 항목은 반드시 `<li>`태그로 마크업한다.  
순서에 정보가 있다면 ol, 순서가 중요하지 않다면 ul을 사용한다.
```html
<ul>
    <li></li>
    <li></li>
    <li></li>
<ul>
```