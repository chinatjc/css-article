# BEM className 命名规范

通过BEM命名规范来命名className，可以一目了然很快速地查找对应的DOM位置、状态

> BEM，其含义是  **块(Block)**  **元素(Element)**  **修饰符(modifier)**

<br>

### 连接符

```
-  中划线：在块或者元素内部，单词之间的连接符号
__ 双下划线：块与元素之间的连接符号
-- 双中划线：（块或者元素）与修饰符之间的连接符号
```
<br>

### 块(Block)
一个模块的意思，其内部单词之间用 - 来连接
```
.search-bar
```
<br>

### 元素(Element)
模块里的元素，其内部单词之间用 - 来连接，与块连接时用 __
```
.search-bar__input
.search-bar__search-button
```
<br>

### 块(Block)
块或者元素的特定状态，与块或者元素连接时用 --
```
.search-bar--hover
.search-bar__input--hover
```
<br>

### 实例
```html
<ul class="article">
    <li class="article__item">第一项
        <div class="article__product-name">我是名称</div>
        <span class="article__ming-zi-ke-yi-hen-chang">看类名</span>
        <a href="#" class="article__link">我是link</a>
    <li>
    <li class="article__item article__item--current">第二项 且 当前选择项
        <div class="article__product-name">我是名称</div>
        <a href="#" class="article__item-link">我是link</a>
    <li>
    <li class="article__item article__item--hightlight">第三项 且 特殊高亮
         <div class="article__product-name">我是名称</div>
        <a href="#" class="article__item-link">我是link</a>
    <li>
</ul>
```