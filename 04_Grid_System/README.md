## Grid System
일정한 간격을 두면서 레이아웃을 배치.
![grid](https://user-images.githubusercontent.com/46988995/136745168-edc7c1c6-3cf3-428e-83bd-57b5d86af6eb.png)

### Properties
**container**
`grid`를 사용하게 위해 컨테이너를 정의하는 속성, 1200px크기를 12개 컬럼으로 나눈다면 아래와 같이 작성
```css
.container {
  display: grid;
  width: 1200px;
  grid-template-columns: repeat(12, 100px);
}
```

**column&row**
grid 컨테이너내에서 최소 단위 블럭 (컬럼: 행, 로우: 열)

**gutter**
grid 라인 사이의 간격
```css
.container {
  row-gap: 10px;
  column-gap: 8px;
}
```

### tailwind-css grid
그리드를 더욱 편하게 사용할 수 있는 css 프레임워크
**grid**
grid 영역에 `grid` class 부여해서 사용한다.
```html
<div class="grid grid-cols-12 grid-rows-6 gap-x-4 gap-y-4 text-2xl">
```
+ **grid :** `display: grid;`
+ **grid-cols-12:** `grid-template-columns: repeat(1, minmax(0, 1fr));`
+ **gap-x:** `column-gap`
+ **gap-y:** `row-gap`

**Responsive**
| 종단점 | min-width | css |
| ---- | ----- | ---- |
| sm | 640px | @media (min-width: 640px) { ... } |
| md | 768px | @media (min-width: 768px) { ... } |
| lg | 1024px | @media (min-width: 1024px) { ... } |
| xl | 1280px | @media (min-width: 1280px) { ... } |
| 2xl | 1536px | @media (min-width: 1536px) { ... } |
```html
<div class="main col-span-12 md:col-span-8 row-span-4">
  <main>
    <h1>Main</h1>
  </main>
</div>
```