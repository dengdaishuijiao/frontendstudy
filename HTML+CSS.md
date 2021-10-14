# 前端笔记

## 1HTML基础

### 1.1基础显示

#### 1.1.1 文字显示

标题显示为:h1-h6标签

```html
<h1>
    这是最大的标题
</h1>
<h6>
    这是最小的标题
</h6>
```

段落使用p标签，p标签包围的内容就是一个段落。br标签可以换行，注意br标签是单独出现，之后内容会从下一行显示。

```html
<p>
    这句话形成一个段落。这是第一段。
</p>
<p>
    这是第二段。
</p>
```

强调显示，使用标签让标签包围的内容显示效果不同。

1. em标签为斜体
2. strong标签为加粗

现在使用更多的强调。

1. i标签，斜体。常用外国文字，分类名称，技术术语。
2. b标签，粗体。关键字，产品名称
3. u标签，下划线。专有名词。

无序列表和有序列表使用ul和ol标签。其中每一条内容使用li标签。

```html
 <ul>
    <li>cat nip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
  </ul>
  <p>Top 3 things cats hate:</p>
  <ol>
    <li>flea treatment</li>
    <li>thunder</li>
    <li>other cats</li>
  </ol>
<dl>
    <dt>名词1</dt>
    <dd>名词1解释1</dd>
    <dd>名词1解释2</dd>
</dl>
```

#### 1.1.2 其他显示

超链接 使用a标签。

图片使用img标签，并且只有一个，并不是一对。

```html
<a href="https://www.w3school.com.cn">w3c学习HTML基础</a>
<img src="w3school.jpg" width="104" height="142" border="1" title="w3c网站" alt = "w3school网址" />
<!--
也可以将两个标签同时使用，起到点击图片进行页面切换效果。
-->
<a href="https://www.w3school.com.cn"><img src="w3school.jpg" width="104" height="142" /></a>
```

a标签可以添加title属性，当你将鼠标移动到超链接上时可以显示出额外的文字。

超链接的地址不仅仅可以是网址，也可以是你本地页面。需要注意的是当你跳转本地页面时注意需要注意路径

1. 指向当前目录，href="index.html"
2. 指向子目录，需要带上文件夹，如href="project/index.html"
3. 指向上级目录，..表示上级目录，如href="../project/index.html"

超链接到页面的片段。在需要跳转的标签添加id属性，并且在a标签添加制定。

```html
<h2 id="Mail">
    邮箱
</h2>
<a href="#Mail">跳转到邮箱</a>
```



#### 1.1.3 转义字符

| 原意字符 | 等价字符引用 |
| -------- | ------------ |
| <        | &lt          |
| >        | &gt          |
| "        | &quot        |
| '        | %apos        |
| &        | &amp         |

注意等价字符后需要;来进行转义。转义字符就是为了让浏览器知道我们输入的文本仅仅是用做文本显示而不是代码的一部分。

```html
<p>
    HTML中使用&lt;p&gt;来定义段落元素
</p>
```



#### 1.1.4文字排版

表格显示

table 标签 tr是一行，td一个单元格。

### 1.2 输入

#### 1.2.1 input标签

```html
<input type="text" placeholder="cat photo URL" required>
<!--
type为输入框类型，placeholder为默认内容，required要求输入框内为必填项.-->
<input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked> Indoor

```

input标签常见属性。

1. id,用于区分每个input标签，类似变量名。
2. type类型，text为文本框，radio为单选框。checkbox为复选框。
3. 单选框和复选框，可以修改 value值来决定选择后的参数。name为这个参数传入的变量名。

type属性值

| 属性值   | 描述                               |
| -------- | ---------------------------------- |
| button   | 定义可点击按钮                     |
| checkbox | 定义复选框                         |
| file     | 定义输入字段和浏览按钮，供文件上传 |
| hidden   | 定义隐层的输入字段                 |
| image    | 定义图像形式的提交按钮             |
| password | 定义密码字段                       |
| radio    | 定义单选字段                       |
| reset    | 定义重置按钮。会重置表单内所有数据 |
| submit   | 定义提交按钮，发送表单数据到后端   |
| text     | 定义单行的输入字段。默认宽度为20   |

select标签

下拉列表。

```html
籍贯<select>
    <option>北京</option>
    <option>上海</option>
    <option>河北</option>
</select>
```



textarea文本域

```html
今日反馈<textarea rows="5" cols="10">
</textarea>
```



## 2CSS基础

### 2.1选择器

#### 2.1.1 标签选择器

html标签名的选择器。快速修改同类标签。但是同类标签无法做区别。

#### 2.2.2 类选择器

单独选择一个或某几个标签进行修改。

不能使用原有的标签名作为类名。

| 头                       | header            |
| ------------------------ | ----------------- |
| 内容                     | content/container |
| 尾                       | footer            |
| 导航                     | nav               |
| 侧栏                     | sidebar           |
| 栏目                     | column            |
| 页面外围控制整体布局宽度 | wrapper           |
| 左中右                   | left right center |
| 登录条                   | loginbar          |
| 标志                     | logo              |
| 广告                     | banner            |
| 页面主题                 | main              |
| 热点                     | hot               |
| 新闻                     | news              |
| 下载                     | download          |
| 子导航                   | subnav            |
| 搜索                     | search            |
| 友情链接                 | friendlink        |

一个标签可以使用多个类名，他们之间用空格隔开。

#### 2.2.3 id选择器

通过id属性值进行修改

#### 2.2.4通配符选择器

使用“*”定义，它表示所有标签。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>css案例</title>
    <style>
        .box {
            width: 200px;
            height: 200px;
        }
        .red {
            background-color: red;
        }
        .green {
            background-color: green;
        }
        .font35 {
            font-size: 35px;
        }
        /* id选择器，结构通过id调用，只能调用一次。 */
        #pink {
            color: pink;
        }
        * {
            color: indigo;
        }

    </style>
</head>
<body>
    <div class="box red font35">红色</div>
    <div class="box green">绿色</div>
    <div class="box red" id="pink">红色</div>
    <P>我的</P>
    <span>我的</span>

</body>
</html>
```

### 2.2字体属性

字体font-family

字体大小font-size，单位px

字体粗细font-weight，默认normal,bold粗体，bolder特粗，lighter细体。也可以用数字100-900。

其中400=normal ，700=bold.

文字样式，font-style，normal默认，italic斜体

字体复合属性，font:font-style font-weight font-size/line-height font-family

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>字体显示</title>
    <style>
        h2 {
            font-family:"微软雅黑";
            font-weight: 400;
        }
        body {
            font-size: 16px;
            font-family: 'Times New Roman', Times, serif;
        }
        .bold {
            font-weight: 900;
        }
        div {
            font-style: italic;
            font-weight: 700;
            font-size: 16px;
            font-family: 'Microsoft yahei';
        }
        /* 复合代码 */
        /* font: font-style font-weight font-size/line-height font-family 
        顺序十分重要,font-size和font-family属性不可省略*/
        span {
            font: italic 400 16px 'Microsoft yahei';
        }
    </style>
</head>
<body>
    <h2>十二月历</h2>
    <p>年轻时候</p>
    <p class="bold">以为坚持是永不动摇</p>
    <p>到这个年纪明白了</p>
    <p>坚持就是犹疑着</p>
    <p>退缩着心猿意马着</p>
    <p>一步三停着</p>
    <p>还在往前走</p>

    <div>三生三世十里桃花，一心一意百行代码</div>
    <span>三生三世十里桃花，一心一意百行代码</span>

</body>
</html>
```

### 2.3文本属性

定义文本外观，如颜色，对齐文本，文本缩进，行间距。

文本颜色color

文本对齐text-align

装饰文本text-decoration

文本缩进，文本第一行首行缩进。text-indent

行间距line-height。行间距包含上间距，文本高度，下间距。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>文本属性</title>
    <style>
        div {
            /* 可以是预定义颜色，十六进制#FFFFFF，或者RGB代码 */
            color: lawngreen;
            /* 对齐方式 */
            text-align: left;
            /* none 默认 underline 下划线 overline 上划线 line-through删除线 */
            text-decoration: line-through;
            /* 首行缩进 text-indent  单位：px，em（几个字）*/
        }
        a {
            text-decoration: none;
        }
        p {
            text-indent: 2em;
            /* 行间距 line-height */
            line-height: 2em;
        }
    </style>
</head>
<body>
    <div>颜色配置</div>
    <a href="#">超链接</a>
    <p>打开北京、上海与广州的地图，你会看见三张纵横交错的线路网格，这代表了中国最成熟的三套城市轨道交通。</p>
    <p>新的赛季由湖人和篮网开启，不知道赛季的最后一场，是否同样能由他们结局。作为夺冠呼声最高的两支球队，即便只是一场无关胜负的季前赛，即便六大超巨有五位都没有上场，但篮网和湖人的名号，就足以吸引所有人的目光。</p>
    <p>如果从最终结果来看，湖人惨败，你会担心紫金军团今夏的疯狂引援是否徒有虚名，甚至担心于，湖人和篮网之间的差距，是否真有外界传的那么接近。但事实上，比赛的进程已经达到了一场季前赛的价值，26分的分差不能说明太多问题，万里长征，湖人才刚刚开始热身而已。</p>
</body>
</html>
```

### 2.4 CSS引入方式

css样式表可以分为三种。

1. 行内式。修改简单功能。直接在标签内添加style属性。

2. 外部式。创建css文件，在html文件内引用。link标签。

3. 内部式。放在style标签内，之前使用的。可以控制整个页面。

   

### 2.5 emmet语法

用于快捷生成代码结构语法。

#### 快速生成html标签

1. div*5，生成五个div标签
2. ul>li，直接生成ul和一个li标签。>可以生成父子级标签如：div>span等
3. "."快速生成class属性的div，"#"生成id属性的div
4. p.one,快速生成class属性的p标签。
5. 自增富豪“$”快速生成递增class值的标签。如：.demo$*5,生成五个div标签，class值从demo1到demo5.
6. {}快速生成标签内容。如：p{这是一个段落}会自动形成p标签及其内容。

#### 快速生成CSS标签

1. 首字母缩写，如text-align:center 可以缩写成tac。

### 2.6 CSS复合选择器

复合选择器是建立在基础选择器之上的，就是对基本选择器进行选择。

常用的复合选择器包括，后代选择器，子选择器，并集选择器，伪类选择器。

使用选择器的目的是为了修改特定内容，而不影响其他内容。选择器的目的是选择。

#### 2.6.1 后代选择器

后代选择器又称包含选择器。选择父元素中子元素修改其内容。

后代选择器，父元素 子元素｛样式｝

后代选择器的子元素不仅仅可以是儿子，也可以是孙子等等后代，只要子元素包含在父元素内即可

#### 2.6.2 子选择器

只能选择最近一级子元素，可理解为亲儿子元素。

使用父元素>子元素{样式声明}格式。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS选择器</title>
    <style>
        /* 想要将ol里所有标签颜色改为蓝色，但是不修改ul里面的 */
        /* 后代选择器，父元素 子元素｛样式｝ */
        /* 后代选择器的子元素不仅仅可以是儿子，也可以是孙子等等后代，只要子元素包含在父元素内即可 */
        ol li {
            color: blue;
        }

        ul a {
            color: yellowgreen;
            text-decoration: none;
        }

        .end li {
            color: pink;
        }
	
        .nav>a {
            color: greenyellow;
            text-align: center;
        }
    </style>
</head>

<body>
    <ul>
        <li>我是ul的孩子</li>
        <li>我是ul的孩子</li>
        <li>我是ul的孩子</li>
        <li>我是ul的孩子</li>
        <li><a href="#">我是ul的孙子</a></li>
    </ul>
    <ol>
        <li>我是ol的孩子</li>
        <li>我是ol的孩子</li>
        <li>我是ol的孩子</li>
        <li>我是ol的孩子</li>
        <li>我是ol的孩子</li>
        <li>我是ol的孩子</li>
    </ol>
    <ul class="end">
        <li>我是ul的孩子</li>
        <li>我是ul的孩子</li>
        <li>我是ul的孩子</li>
        <li>我是ul的孩子</li>
        <li><a href="#">我是ul的孙子</a></li>
    </ul>
    <div class="nav">
        <a href="#">这是div标签的儿子</a>
        <p>
            <a href="#">这是div标签的孙子</a> <br>
            这也是div标签的儿子
        </p>
    </div>

</body>

</html>
```



#### 2.6.3 并集选择器

并集选择器可以选择多组标签，同时为它们定义相同的样式。

使用“,”连接各部分内容，其他选择器可以是并集选择器的一个部分。

#### 2.6.4 伪类选择器

用于向某些选择器添加效果。

##### 2.6.4.1 链接伪类选择器

| 代码      | 含义                       |
| --------- | -------------------------- |
| a:link    | 所有未被访问的连接         |
| a:visited | 所有已被访问的连接         |
| a:hover   | 鼠标指针指向位于上方的连接 |
| a:active  | 鼠标按下时的连接           |

注意事项

1. 为了确保生效，使用lvha顺序，即link,visited,hover,active。声明格式。

2. 即使规定了body的样式，也需要单独对a标签进行样式规定。

3. 常用的方式是规定a的样式和a:hover的样式。

   

##### 2.6.4.2 focus伪类选择器

一般常见于input标签，主要针对表单内元素。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>伪类选择器</title>
    <style>
        /* 未访问的连接 */
        a:link {
            color: black;
            text-decoration: none;
            font-size: large;
        }

        a:visited {
            color: red;
        }

        a:hover {
            color: black;
        }

        a:active {
            color: skyblue;
        }

        input:focus {
            background-color: pink;
            color: red;
        }
    </style>
</head>

<body>
    <a href="http:www.baidu.com" target="_blank">小猪佩奇</a>
    <input type="text">
    <input type="text">
    <input type="text">
</body>

</html>
```

### 2.7 CSS元素显示模式

html元素可以分为块元素和行内元素。

块元素主要有：

1. h1-h6
2. p
3. div
4. ul
5. ol
6. li

独占一行，可以设置宽度高度，内外边距。宽度默认是父级元素宽度。

块级元素可以看做是一个容器或者盒子，里面放块级元素或者行内元素。

文字类的元素内不能再使用块级元素。类似p div /div /p这样使用

行内元素有：

1. a
2. strong
3. b
4. span

一行可以使用多个。不能直接设置高度宽度，默认都是内容的大小。

行内元素内只能使用文本或者其他行内元素。

a标签里可以使用块级元素。

行内块元素

1. img
2. input
3. td

同时具有块元素和行内元素的特点

一行可以显示多个，默认宽度就是本身内容宽度，高度，行高及内外边距可以像块元素一样控制。

总结

| 元素模式   | 元素排列       | 设置样式           | 默认宽度   | 包含               |
| ---------- | -------------- | ------------------ | ---------- | ------------------ |
| 块级元素   | 一行只能放一个 | 可以设置宽度高度   | 容器的100% | 任何标签           |
| 行内元素   | 一行可以放多个 | 不可以设置         | 内容宽度   | 文本或其他行内元素 |
| 行内块元素 | 一行可以放多个 | 可以设置宽度和高度 | 内容宽度   |                    |

#### 2.7.1 元素显示模式切换

一个模式的元素需要另外一种元素的特性。

```HTML
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>侧边栏</title>
    <style>
        a {
            display: block; /*将a标签通过切换变为块元素，可以设置高度和宽度*/
            height: 40px;
            width: 230px;
            background-color: gray;
            font-size: 14px;
            color: white;
            text-align: center;
            text-decoration: none;
            line-height: 40px;
        }

        a:hover {
            background-color: #ff6700;
        }
    </style>
</head>

<body>
    <a href="#">手机 电话卡</a>
    <a href="#">电视 盒子</a>
    <a href="#">笔记本 平板</a>
    <a href="#">出行 穿戴</a>
    <a href="#">智能 路由器</a>
    <a href="#">健康 儿童</a>
    <a href="#">耳机 音响</a>

</body>

</html>
```

### 2.8 CSS背景

#### 2.8.1 背景颜色

background-color,默认为trasparent(透明的)

#### 2.8.2 背景图片

background-image，比img标签便于控制位置，所以网页中小的图片可以直接使用背景图片方式，即使这个背景图片上没有内容。

#### 2.8.3 背景平铺

background-repeat，repeat平铺，no-repeat不平铺，repeat-x沿x轴平铺，repeat-y沿y轴平铺

#### 2.8.4 背景位置

background-position x y;可以是具体数值，也可以是方位如left，center。

数值和方位可以混合使用，这样使用x,y顺序是固定的。

#### 2.8.5 背景图像固定（背景附着）

background-attachment，scroll滚动的，fixed固定的

background：背景颜色 背景图片地址 背景屏幕 图像滚动 位置 一般使用这个顺序。

#### 2.8.6 背景色半透明

background:rgba(r,g,b,a).其中a为透明度0-1之间，1为不透明。

| 属性                  | 作用           | 值                                   |
| --------------------- | -------------- | ------------------------------------ |
| background-color      | 背景颜色       | 预定义颜色/十六进制/RGB代码          |
| background-image      | 背景图片       | url(图片路径)                        |
| background-repeat     | 是否平铺       | repeat/no-repeat/repeat-x/repeat/y   |
| background-position   | 背景位置       | length/positon,顺序为x，y            |
| background-attachment | 背景附着       | scroll/fixed（背景不随页面滚动）     |
| background：          | 背景简写       | 颜色 地址 平铺 滚动 位置             |
| background：rgba()    | 背景颜色半透明 | r g b a，a为透明度0-1之间，1为不透明 |

## 3 CSS三大特性

css三大特性：层叠性，继承性，优先级。

### 3.1层叠性

相同选择器给设置相同的样式，此时一个样式会覆盖另一个样式，解决冲突问题。

后面的会覆盖前面的

### 3.2 继承性

子标签会继承父标签的某些样式，如文本颜色和字号。

主要继承的样式为：text-,font-,line-，以及color属性。

### 3.3 优先级

不同类选择器优先级id>(伪)类>标签，即无论代码先后，id选择器有最高优先级。

| 选择器               | 权重    |
| -------------------- | ------- |
| 继承或 *             | 0,0,0,0 |
| 元素选择器           | 0,0,0,1 |
| 类选择器，伪类选择器 | 0,0,1,0 |
| id选择器             | 0,1,0,0 |
| 行内样式 style=“”    | 1,0,0,0 |
| !important           | 无穷大  |



使用复合选择器要考虑权重叠加问题

## 4 盒子模型

### 4.1 盒子模型基础

页面布局三个核心内容，盒子模型，浮动和定位。

#### 4.1.1盒子模型与网页布局

网页是由一个个盒子构成的，设置好盒子的样式和位置，再将内容放入盒子中。

一个盒子包含边框，外边距，内边距，和实际内容。

border边框，content内容，padding内边距，margin外边距

##### 4.1.1.1 border边框

| 属性         | 作用             |
| ------------ | ---------------- |
| border-width | 边框粗细，单位px |
| border-style | 边框样式         |
| border-color | 边框颜色         |

边框样式

| 属性   | 作用                             |
| ------ | -------------------------------- |
| none   | 无边框                           |
| hidden | 隐藏边框                         |
| dashed | 虚线                             |
| dotted | 点线                             |
| solid  | 实线                             |
| double | 双线边框，间隔等于border-width值 |

边框简写 border:px solid red。通用顺序，但是没有规定顺序。

border-top之规定上边框。

##### 4.1.1.2 padding内边距

| 属性           | 作用     |
| -------------- | -------- |
| padding-left   | 左内边距 |
| padding-right  | 右内边距 |
| padding-top    | 上内边距 |
| padding-bottom | 下内边距 |

padding简写模式

| 值的个数                    | 意思                                                      |
| --------------------------- | --------------------------------------------------------- |
| padding:5px;                | 上下左右都是5像素内边距                                   |
| padding:5px 10px;           | 上下5像素，左右10像素                                     |
| padding:5px 10px 20px;      | 上内边距5像素，左右10像素，下20像素                       |
| padding:5px 10px 20px 30px; | 上内边距5像素，右内边距10像素，下20像素，左30像素，顺时针 |

##### 4.1.1.3 不撑开盒子情况

当宽度或高度没有指定时，添加内边距不会对盒子的宽度或高度造成影响。

##### 4.1.1.4 margin外边距

margin和padding使用方式一致。

**外边距典型应用，让块级盒子水平居中。**

需要满足两个条件：

1. 盒子必须设置了宽度
2. 盒子左右边距设置为auto

**如何让行内块元素水平居中**

给父元素添加text-align:center

##### 4.1.1.5外边距合并问题

**嵌套块元素垂直外边距塌陷**

对于两个嵌套关系（父子）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素外边距值会变大。

解决方案：

1. 可以为父元素定义上边框
2. 可以为父元素定义内边距
3. 可以为父元素添加overflow:hidden

**清除内外边距**

```html
*{
	padding:0;
	margin:0;
	/*通配符清除默认内外边距*/
}
```

对行内元素设置外边距时，尽量只设置左右外边距。因为行内元素无法设置高度，容易引起问题。

### 4.2 泛指的盒子模型

之前的盒子模型都是矩形的，现在接触一些盒子模型的其他样式。

#### 4.2.1 圆角边框

border-radius：length

length单位是px，当length值为高度一半时，这是一个圆角矩形（左右两侧是圆弧）

#### 4.2.2 盒子阴影

CSS3中新增了盒子阴影，使用box-shadow

| 值       | 描述                           |
| -------- | ------------------------------ |
| h-shadow | 必须，水平阴影的位置，允许负值 |
| v-shadow | 必须，垂直阴影位置，允许负值   |
| blur     | 可选，模糊距离                 |
| spread   | 可选，阴影尺寸                 |
| color    | 可选，阴影颜色                 |
| inset    | 可选，将外部阴影改为内部阴影   |

语法：**box-shadow: h-shadow v-shadow blur spread color inset**

#### 4.2.3 文字阴影

| 值       | 描述                           |
| -------- | ------------------------------ |
| h-shadow | 必须，水平阴影的位置，允许负值 |
| v-shadow | 必须，垂直阴影位置，允许负值   |
| blur     | 可选，模糊距离                 |
| color    | 可选，阴影颜色                 |

语法：**text-shadow:h-shadow v-shadow blur color**

## 5 CSS浮动

### 5.1 传统网页布局的三种方式

传统网页布局的本质就是用CSS来摆放盒子。把盒子放在相应的位置。

1. 普通流/标准流
2. 浮动
3. 定位

实际开发中是三种方式混合使用。

**多个盒子纵向排列使用标准流，横向排列使用浮动。**

#### 5.1.1标准流

就是标签按照默认方式排列。

块级元素会独占一行，从上到下顺序排列，常用：div,hr,p,h1-h6,ul,ol,dl,form,table

行内元素会按照顺序从左到右排列，碰到父元素边缘自动换行。常用：span,a,i,em

#### 5.1.2 浮动

浮动可以让多个块级元素一行内显示

float属性用于创建浮动框，将其移动到一边，知道左边缘或右边缘踧踖包含块或另一个浮动框的边缘。

### 5.2 浮动的特性

#### 5.2.1浮动元素脱离标准流

脱离标准普通流的控制（浮）移动到指定位置（动），浮动的盒子不在保留原先的位置。

#### 5.2.2 浮动元素会一行显示并且顶部对齐

当一行装不下时，会自动到下一行对齐。

#### 5.2.3 浮动元素具有行内块特性

给行级元素添加浮动属性后，行级元素会有行内块元素特性（比如设置宽度）。

**综合以上内容，我们可以知道，浮动元素和标准流父级元素搭配使用**



### 5.3 清除浮动

当一个父盒子里面子盒子大小，多少不是确定值时，如果父盒子不设定高度更加合适。

但是由于脱标后，子盒子不占用空间，所以当父盒子里所有子盒子都是浮动的话，父盒子高度为0.

![](C:\Users\zong\Pictures\Saved Pictures\清除浮动.png)

#### 5.3.1 清除浮动本质

清除浮动之后，父级元素就会根据浮动的子盒子自动检测高度。父级元素有了高度就不会影响下面的标准流

选择器{clear:属性}

| 属性  | 描述             |
| ----- | ---------------- |
| left  | 清除左侧浮动影响 |
| right | 清除右侧浮动影响 |
| both  | 清除左右浮动影响 |

#### 5.3.2 清除浮动方法

1. 额外标签法
2. 父级添加overflow属性
3. 父级添加after伪元素
4. 父级添加双伪元素

##### 5.3.2.1 额外标签法

添加新标签，新标签添加样式clear:both.

优点：通俗易懂，书写方便

缺点：新增很多无意义标签，结构化差

##### 5.3.2.2 父级元素添加overflow

优点：代码简洁

缺点：无法显示溢出的部分

##### 5.3.2.3 after伪元素法

是额外标签法的升级版

优点：没有增加标签，结构简单

缺点：照顾低版本浏览器

##### 5.3.2.4双伪元素

优点：代码比after简洁

缺点:照顾低版本浏览器

```html	
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>清除浮动</title>
    <style>
        /* after伪元素 */
        /* .clearfix:after {
            content: "";
            display: block;
            height: 0;
            clear: both;
            visibility: hidden;
        }

        .clearfix {
            *zoom: 1;
        } */
        /* 双伪元素 */
        /* .clearfix:before,
        .clearfix:after {
            content: "";
            display: table;
        }

        .clearfix:after {
            clear: both;
        }

        .clearfix {
            *zoom: 1;
        } */

        .box {
            /* 父级元素overflow */
            /* overflow: hidden; */
            width: 1200px;
            background-color: skyblue;
            border: 1px solid pink;
            margin: 50px auto 0;
        }

        .box .one {
            float: left;
            width: 200px;
            height: 200px;
            background-color: purple;
        }

        .box .two {
            float: left;
            width: 200px;
            height: 200px;
            background-color: red;
        }

        .footer {
            height: 200px;
            background-color: black;
            margin: 0 auto;
        }

        /* 标签法 */
        /* 在浮动元素后添加一个新的div标签，新的标签使用clear */
        /* .clear {
            clear: both;
        } */
    </style>
</head>

<body>
    <div class="box clearfix">
        <div class="one">第一</div>
        <div class="two">第二</div>
        <!-- <div class="clear"></div> -->
    </div>
    <div class="footer"></div>
</body>

</html>
```

#### 5.3.3 总结

清除浮动：

1. 父元素没高度
2. 子盒子浮动
3. 影响后面布局

三个条件都满足，就需要清除浮动

有四种方法清除浮动

## 5.4 案例总结

#### 5.4.1CSS书写顺序

1. 布局定位属性：display/position/float/clear/visibility/overflow
2. 自身属性:width/height/margin/padding/border/background
3. 文本属性:color/font/text-decoration/text-align/vertical-align/white-space/break-word
4. 其他属性:content/cursor/border-radius/box-shadow/text-shadow

#### 5.4.2 整体布局思路

1. 确认核心区域
2. 分析页面行模块，及其每个行模块内列模块
3. 确定每个列模块大小，之后确定位置。

开发中更常用li+a做导航栏

**代码在04布局案例实践**

## 6 CSS定位

一些无法用标准流和浮动无法快速实现，可以需要定位实现。比如：将一个盒子固定显示在屏幕右下角，无论如何滚动都在右下角。

浮动和定位的区别：

1. 浮动可以让多个块级盒子无缝隙排列显示，常用于横向排列。
2. 定位是让盒子自由的在某个盒子内移动位置或固定屏幕的某个位置，并且可以压住其他盒子。

### 6.1 定位组成

将盒子定在某一个位置，所以定位也是在摆放盒子，按照定位的方式移动盒子。

定位=定位模式+偏移

#### 6.1.1 定位模式

使用position属性

| 值       | 语义     |
| -------- | -------- |
| static   | 静态定位 |
| relative | 相对定位 |
| absolute | 绝对定位 |
| fixed    | 固定定位 |

#### 6.1.2 边偏移

使定位的盒子移动到最终位置，有top,bottom,left,right四个属性。

四个属性分别代表盒子移动的像素距离。

### 6.2 相对定位relative

静态定位是默认定位模式，无定位的意思。按照标准流的特性摆放，没有边偏移。

相对定位是元素在移动位置的时候，是相对于它有来的位置来说的。

```css
选择器{position:relative;}
```

1. 相对定位的边偏移是根据原来它所处的位置定位，即top，表示比原来的上边移动多少距离。
2. 这个使用相对定位的盒子原来在标准流的位置继续占有，后面的盒子仍然以标准流的方式对待它（不脱标）。

相对定位最典型的应用是辅助绝对定位的。

### 6.3 绝对定位absolute

绝对定位是元素在移动位置的时候相对它祖先元素来说的。

若没有祖先元素或祖先元素没有定位，则以浏览器为准定位。

绝对定位不再占有原来的位置（脱标）

### 6.4 子绝父相

子元素使用绝对定位来实现自己位置的“自由”移动，父元素为了辅助子元素来使用相对定位。

### 6.5 固定定位fixed

特点：

1. 以浏览器可视窗口为参照点移动元素。
2. 不在占有原先位置，也是脱离标准流的。

### 6.6 粘性定位

相对定位和固定定位的结合。

特点：

1. 以浏览器的可视窗口为参照点移动元素
2. 粘性定位占有原先的位置
3. 必须添加top,left,right,bottom其中一个才生效
4. 兼容性差，有其他的实现方法

### 6.7 总结

| 定位模式         | 是否脱标 | 移动位置               |
| ---------------- | -------- | ---------------------- |
| static静态定位   | 否       | 不移动                 |
| relative相对定位 | 否       | 相对于自身原来位置移动 |
| absolute绝对定位 | 是       | 带有定位的父级元素     |
| fixed固定定位    | 是       | 浏览器可视区域         |
| sticky粘性定位   | 否       | 浏览器可视区域         |

### 6.8 定位扩展

#### 6.8.1 显示的优先级

z-index，显示的优先级。

数值越大，优先级越高，没有单位。

#### 6.8.2 绝对定位盒子居中

用绝对定位到50%，盒子左上角在居中处。再通过margin移动盒子位置

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>盒子居中</title>
    <style>
        .box {
            position: absolute;
            left: 50%;
            margin-left: -100px;
            top: 50%;
            margin-top: -100px;
            /* 使盒子居中，用绝对定位到50%，盒子左上角在居中处。再通过margin移动盒子位置 */
            width: 200px;
            height: 200px;
            background-color: skyblue;
            /* margin: auto; */
            /* 在不使用定位时，盒子可以通过marginauto来实现居中 */
        }
    </style>
</head>

<body>
    <div class="box"></div>
</body>

</html>
```

#### 6.8.3 定位的特殊性

1. 当行内元素使用定位后，可以给行内元素直接赋予高度和宽度。
2. 当块元素使用定位后，如果不给宽度或者高度，默认是内容的大小。
3. 脱标的盒子是不会触发外边距塌陷。

#### 6.8.4 绝对定位（固定定位）会压住盒子

浮动元素不会压住后面标准流的文字。



## 7 显示与隐藏

### 7.1 display

设置display:none 可以让盒子隐藏，并且不再占有位置。

### 7.2visibility

| 属性     | 效果                                                 |
| -------- | ---------------------------------------------------- |
| inherit  | 继承上个父级对象的可见性                             |
| visible  | 可见的                                               |
| hidden   | 隐藏的                                               |
| collapse | 隐藏表格的行或者列，如对其他对象使用效果等同于hidden |

依旧占有位置

### 7.3 overflow

如果内容溢出一个元素的框（超过高度或者宽度）时，overflow决定对其隐藏还是显示。

| 属性    | 效果                                             |
| ------- | ------------------------------------------------ |
| visible | 不剪切也不增加滚动条。                           |
| auto    | 在需要时剪切内筒并添加滚动条。body和textarea默认 |
| hidden  | 不显示超出的内容                                 |
| scroll  | 总是显示滚动条                                   |

