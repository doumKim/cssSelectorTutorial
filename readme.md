# CSS Selector

#### index.html

```html
<div class="wrap">
	<h1>CSS practice!</h1>
	<div class="box box1"></div>
	<div class="box box2"></div>
	<div class="box box3"></div>
	<div class="box box4"></div>
	<p>Hello css!</p>
	<form>
		<input type="text" name="userName" placeholder="이름을 입력하세요" />
	</form>
</div>
```

- \+ selector<br />
  \+ 선택자는 앞의 요소 바로 뒤에 위치하는 요소에 스타일을 적용할 때 사용하면 좋다.

```css
.box {
	background-color: cadetblue;
	width: 100px;
	height: 100px;
}

.box + .box {
	margin-top: 20px;
}

.box1 {
	background-color: chocolate;
}

.box2 {
	background-color: yellowgreen;
}

.box3 {
	background-color: gold;
}

.box4 {
	background-color: silver;
}
```

<style>
  img{display:block;width:300px;margin:0 auto; }
</style>

![](./img/plusSelector.jpg)

- \~ selector<br />
  \~ 선택자는 앞의 요소 다음에 나오는 특정 요소들에 모두에게 스타일을 적용할 수 있다.

```css
h1 ~ .box {
	width: 200px;
}
```

![](./img/anf.png)

- \[attribute = value] selector<br />
  \[] 선택자는 요소의 속성과 값을 이용해 스타일을 적용할 수 있다.

```css
input[name='userName'] {
	width: 300px;
}
```

![](./img/input.png)

- nth-of-type(n) selector<br />
  nth-of-type(n) 선택자는 태그 타입의 n번째 요소에 스타일을 적용할 수 있다.

```html
<div>
	<p>I live in Duckburg.</p>
	<h2>My name is Donald</h2>
	<p>My best friend is Mickey.</p>
	<p>I will not be styled.</p>
</div>
```

```css
div p:nth-of-type(2) {
	background: red;
}
```

![](./img/nthoftype.jpg)
