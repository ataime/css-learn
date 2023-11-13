### CSS 文档

https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout

### css 动画演示

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        body {
            width: 100vw;
            height: 100vh;
            background: #34495e;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        main {
            width: 100px;
            height: 100px;
            background: white;
            /*使用关键帧*/
            animation-name: hd;
            animation-duration: 10s;
        }

        /* 定义关键帧 */
        @keyframes hd {
            from {
                background: white;
            }

            10% {
                transform: scale(2);
            }

            to {
                background: red;
            }
        }
    </style>
</head>

<body>
    <main></main>
</body>

</html>
```

演示：
![演示动画](css1.gif)

```
<main> 标签用于表示文档的主要内容，通常用于包裹整个页面的主要内容部分，比如文章内容、新闻列表、主要功能区等。一个 HTML 文档中应该只有一个 <main> 标签，用于标识整个页面的主要内容区域。
<main> 标签，用于标识整个页面的主要内容区域。
<section> 标签用于将文档分成各个节（section），通常用于组织相关的内容块。一个 <section> 可以包含任意数量的其他 HTML 元素，用于表示页面中的一个独立的部分或区块，比如文章中的各个章节、页面中的不同功能模块等。
<article>：用于表示页面中独立的、完整的、可以独立分配或重用的内容，比如一篇文章、一篇博客、一条新闻等。
<aside>：用于表示页面的侧边栏内容，通常包含与主要内容相关但不是主要内容的信息，比如侧边栏导航、广告、引用等。
<header>：用于表示页面或区块的头部，通常包含导航链接、页面标题、LOGO 等内容。
<footer>：用于表示页面或区块的底部，通常包含版权信息、联系方式、页面链接等内容。
<nav>：用于表示页面的导航链接，通常包含页面的主要导航菜单。
<div>：用于将文档分组，通常用于包裹一组相关的元素，比如一个功能模块、一个部分内容等。<div> 是最通用的块级容器，没有特定的含义，主要用于样式和脚本的操作。
<h1> - <h6>：用于表示标题，<h1> 表示最高级标题，<h6> 表示最低级标题。
<p>：用于表示段落。
<ul> 和 <ol>：分别用于表示无序列表和有序列表。
<li>：用于表示列表中的每一项。
<table>：用于表示表格。
<tr>：用于表示表格中的行。
<td>：用于表示表格中的单元格。
<form>：用于表示表单。
<input>：用于表示表单中的输入字段。
<select> 和 <option>：分别用于表示下拉列表和下拉列表中的选项。
<iframe>：用于嵌入另一个 HTML 页面。
<figure> 和 <figcaption>：用于表示文档中的图像、图表、照片等。
```

```
<body>
    <header>
        <!-- 页面头部内容 -->
    </header>
    <main>
        <!-- 页面的主要内容 -->
        <section>
            <!-- 主要内容的一个部分 -->
        </section>
        <section>
            <!-- 主要内容的另一个部分 -->
        </section>
    </main>
    <footer>
        <!-- 页面底部内容 -->
    </footer>
</body>
```

### CSS 中 display 属性有多个可能的取值，每个取值都会影响元素的表现方式。以下是 display 属性的全部可能取值及其说明：

```
display: block  元素会作为块级元素显示，会独占一行，可以设置宽度、高度、内外边距等。
display: inline  元素会作为行内元素显示，不会独占一行，宽度和高度由内容决定。
display: inline-block  元素会作为行内块元素显示，结合了行内元素和块级元素的特性，可以设置宽度、高度、内外边距等。
display: none  元素会被隐藏，不会在页面上显示，并且不占据空间。
display: flex  使用弹性盒子布局，可以实现灵活的布局。
display: grid 使用网格布局，可以实现复杂的多列布局。
display: table  元素会作为表格显示，类似于 HTML 表格元素。
display: inline-table  元素会作为内联表格显示，类似于 HTML 表格元素，但在行内显示。
display: table-row  元素会作为表格的行显示。
display: table-cell  元素会作为表格的单元格显示。
display: list-item  元素会作为列表项显示，类似于 HTML 中的列表元素。
display: inline-flex  元素会以行内元素的方式显示弹性盒子。
display: inline-grid  元素会以行内元素的方式显示网格布局。
display: inherit  继承父元素的 display 属性。
display: initial  设置元素为它的初始值。
display: unset  重置为元素的自然值。
```

当元素的 position 属性设置为 absolute 时，元素的位置会相对于最近的已定位祖先元素进行定位 （相对父元素定位时，要给父元素设置 position:relative），如果没有已定位的祖先元素，那么它的位置会相对于最初的包含块（通常是文档的最外层容器）进行定位。元素设置为 absolute 后会脱离文档流，让出文档流空间占用，不再影响其他元素的位置。

当元素的 position 属性设置为 relative 时，元素的位置会相对于它在文档流中的正常位置进行定位，不会脱离文档流，仍然保留文档流位置空白，元素相对于原始位置定位。可以通过设置 top、right、bottom、left 属性来改变元素的位置，但是不会影响其他元素的位置。

### 当使用 CSS 中的弹性盒子（Flexbox）布局时，可以使用以下属性来控制弹性盒子的布局和排列方式：

```
display: flex | inline-flex;

用途: 定义一个块级或行内的弹性容器。
flex-direction: row | row-reverse | column | column-reverse;

用途: 定义主轴的方向，决定项目的排列方向。
flex-wrap: nowrap | wrap | wrap-reverse;

用途: 定义项目在容器中是否换行。
flex-flow: <flex-direction> || <flex-wrap>;

用途: 是flex-direction和flex-wrap的简写属性，用于同时设置弹性盒子的方向和是否换行。
justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;

用途: 定义项目在主轴上的对齐方式。
align-items: flex-start | flex-end | center | baseline | stretch;

用途: 定义项目在交叉轴上的对齐方式。
align-content: flex-start | flex-end | center | space-between | space-around | stretch;

用途: 定义多根轴线的对齐方式，如果只有一根轴线，该属性不起作用。
order: <integer>;

用途: 定义项目的排列顺序，数值越小，排列越靠前。
flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ];

用途: 是flex-grow、flex-shrink和flex-basis的简写属性。
align-self: auto | flex-start | flex-end | center | baseline | stretch;

用途: 控制单个项目在交叉轴上的对齐方式，覆盖align-items属性。
```

### CSS 的 Grid 布局是一种二维的布局系统，可以用来创建复杂的网格布局。以下是 CSS Grid 布局中常用的属性及其说明：

```
display : grid | inline-grid
用途: 定义一个块级或行内的网格容器。

grid-template-rows, grid-template-columns, grid-template-areas
用途: 分别定义网格的行、列和区域的模板。可以使用长度值、百分比、fr单位、auto等定义单元格的大小，也可以使用repeat()、minmax()等函数进行复杂的布局定义。

grid-template
用途: grid-template-rows、grid-template-columns和grid-template-areas的简写属性，用于同时定义网格的行、列和区域。

grid-column-gap, grid-row-gap, grid-gap
用途: 分别定义列间隔、行间隔以及同时定义列和行的间隔。

justify-items: start | end | center | stretch
用途: 定义网格项目在单元格中的水平对齐方式。

align-items: start | end | center | stretch
用途: 定义网格项目在单元格中的垂直对齐方式。

justify-content: start | end | center | stretch | space-around | space-between | space-evenly
用途: 定义网格容器中所有网格项目在主轴上的对齐方式。

align-content: start | end | center | stretch | space-around | space-between | space-evenly
用途: 定义网格容器中所有网格项目在交叉轴上的对齐方式。

grid-auto-rows, grid-auto-columns, grid-auto-flow
用途: 分别定义未在模板中显式定义的行高、列宽以及自动布局流程。

grid
用途: grid-template-rows、grid-template-columns、grid-template-areas、grid-auto-rows、grid-auto-columns和grid-auto-flow的简写属性，用于同时定义网格的行、列、区域和自动布局。
```
