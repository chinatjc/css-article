# className在css、js之间如何解藕

```html
<style>
	.comment {
		color: red;
	}
</style>

<p class="comment">这是一段评论</p>

<script>
	document.querySelector('.comment').innerHTML = 11111;
</script>
```

> 针对以上这段代码，dom的className被样式和脚本同时使用，如果要修改dom的className，需要同时维护样式和脚本两套代码，费时费力，胆战心惊，很容易导致bug产生。

<br>

### 使用 rel 属性

通过 rel 属性来确定要查找的dom，从而使得className和js之间成功解藕

```html
<style>
	.comment {
		color: red;
	}
</style>

<p class="comment" rel="js-comment">这是一段评论</p>

<script>
	document.querySelector('[rel="js-comment"]').innerHTML = 11111;
</script>
```