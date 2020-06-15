# WEB前端基础
## 一.软件架构、
### C/S架构
客户端/服务器端

- 优点：	
 用户体验好
- 缺点：
 	 开发，安装，部署，维护麻烦
###  B/S架构
(Browser/Server) 浏览器/服务器
只需要一个浏览器，用户用过不同的网址(URL),客户访问不同的服务器端程序

- 优缺点：

  - 优点：开发，安装，部署，维护简单

  - 缺点：如果应用过大，用户的体验可能会受到影响

    ​			对硬件要求过高

- B/S架构详解(浏览器只能解析静态资源)

  - 静态资源：使用静态网页开发技术发布的资源

    特点：所有用户访问得到的结果一样

    如：文本，图片，音频，视频，HTML，CSS，JavaScript

    如果用户请求的是静态资源，那么服务器会直接将静态资源发送给浏览器。浏览器中内置了静态资源的解析引擎，可以展示静态资源

  - 动态资源：使用动态网页及时发布的资源

    特点：所有用户访问的结果可能不一样

    如：jsp/servlet,php,asp...

    如果用户请求的是动态资源，服务器会执行动态资源，转换为静态资源再发送给浏览器

- 要学习的静态资源：

  HTML：用于搭建基础网页，展示页面的内容

  CSS：用于美化页面，布局页面

  JavaScript：控制页面的元素，让页面有一些动态的效果

## 二.HTML

- (了解)概念：Hyper Text Markup Language 超文本标记语言

  最基础的网络开发语言

  - 超文本：超文本是用超链接的方法，将各种不同空间的文字信息组织在一起的网状文本

  - 标记语言：由标签构成的语言   <标签名称>

    标记语言不是编程语言

- 快速入门：

  - 语法：后缀名   .html 或者 .htm

    - 围堵标签：有开始标签和结束标签 

      ```html
      <html>  </html> 
      ```

    - 自闭合标签：开始标签和结束标签在一起

      ```html
      <br/> 换行标签
      ```

    - 在开始标签中可以定义属性。属性是由键值对构成，值需要用引号(单双引号都可以)引起来

    - html标签不区分带小写，**(建议使用小写)**

- 标签：

  - 文件标签：构成html最基本的标签

    html：html文档的根标签

    head：头标签，用于指定html文档的一些属性。引入外部的资源(meta标签指定字符集)

    ```html
    
    ```
<meta charset="UTF-8">设置当前文字字符编码
    ```

    title：标题标签
    
    body：体标签
      
    ```html
    <header>
    <footer>
    <section>
    <aside>侧边栏
    ```
      
    !DOCTYPE：定义文档标签(!DOCTYPE html)  html5中定义该文档是html文档

  - 文本标签：和文本有关的标签
  
    ```html
    注释：<!-- 注释内容 -->
    <h1> to <h6> :1-6级标签(自带换行)
    <p>:段落标签
    <br/> :换行
    <hr/>:显示一条水平线(自闭和标签)
        属性：color(颜色) width(宽度) size(高度) align(对齐方式)
        (center居中 left左对齐 right右对齐)
    <b>:字体加粗
    <pre>:保留原有格式
    <i>:字体斜体
    <font>:字体标签(过时了)
        属性:color  size  face(字体)
        color:rgb(值1，值2，值3):值的范围在0-255
        如rgb(0,0,255)
        #值1值2值3:值的范围在00-FF 
        如#FF00FF(可以调出很多颜色)
        width:数值，单位是px(像素)
        数值%:占比相对于父元素的比例
    <center>:居中显示
    ```
  ```
  
  
  ```

- 图片标签
  
  img:展示图片(自闭合)
  
    ```html
    <img src="图片存放位置" alt="图片描述" title="介绍"/>
  title:鼠标放在图片上图片的显示
    相对路径: ./代表当前目录
    		../代表上一级目录
    ```
  
  
  
- 列表标签
  
  有序列表:
  
  ol:(order list)
  
    ```html
    <ol type="A" start="5">  大写字母，从第五个开始
        type 指定类型(disc,circle,square)
        start 指定开始位置
        
    ```
  
  li:(放在ol语句中)
  
  无序列表:ul,li 跟有序标签同用法
  
- 超链接标签
  
  a:定义一个超链接
  
    ```html
    <a href="http://www.i.com" title="网址介绍">点击</a>
    属性:href:指定访问资源的URL(统一资源定位符)
    	href可以指定当前页面位置
    
    
    <a href="地址" target="_self">点击</a>
    <a href="地址" target="_blank"></a>
    属性:target在哪个窗口打开
    	_self默认在当前页面
    	_blank新建空白页面
    ```
  
  往自己内部跳转示例:
  
    ```html
    <a href="#C1">点击</a>
    <h1>C1</h1>
    <div>这是一段文字</div>
    <h1> <a name="C1">C4</a></h1>
    <div>在也是一段文字</div>
    
    ```
  
  
  
- **div 和 span:**
  
  span:文本信息在一行展示，行内标签(内联标签)
  
  div:每一个div占一行，自动换行(块级标签)
  
  html4之前定义标题及结尾
  
    ```html
    <div id="header"><h1></h1></div>
    <div id="footer"><h1></h1></div>
    ```
  
  html5:语义化标签
  
    ```html
    <header></header>
    <footer></footer>
    ```
  
- 表格标签:table
  
  **caption:定义表格标题**
  
  **tr:定义行**
  
  **td:定义单元格**
  
  ​	**colspan:合并列**
  
  ​	**rowspan:合并列**
  
  **th:定义表头单元格**
  
    自定义列表：
  
    ​	
  
  ```html
    <dl>
    <dt>Coffee</dt>
    <dd>Black hot drink</dd>
    <dt>Milk</dt>
    <dd>White cold drink</dd>
    </dl>
    结果：
    Coffee
    Black hot drink
    Milk
    White cold drink
  ```
  
  
  
  ```html
  <tr>
  	<th>编号</th>
  	<th>姓名</th>
  	<th>成绩</th>
  </tr>
  
  <tr>
  	<td>1</td>
  	<td>张三</td>
  	<td>100</td>
  </tr>
  
  <tr>
  	<td>2</td>
  	<td>李四</td>
    	<td>60</td>
    </tr>
  ```
  
    **cellpadding:通常定义为0，内容与单元格之间的距离**
  
    **cellspacing:定义单元格之间的距离，如果指定为0，则单元格的线会合为一条**
  
    bgcolor:背景色
  
    align：对齐格式
  
    **caption：定义表格标题**
  
    thead：表示表格的头部分
  
    tbody：表示表格的体部分
  
    tfoot：表示表格的脚部分
  
- **注意：应该避免使用center，font,align,bgcolor,color使用style代替**

  ```htnl
  <html>
  内联方式
  修改背景色
  <body style="background-color:yellow">
  <h2 style="background-color:red">This is a heading</h2>
  <p style="background-color:green">This is a paragraph.</p>
  修改对齐格式
  <h1 style="text-align:center">This is a heading</h1>
  <p>The heading above is aligned to the center of this page.</p>
  修改字体，颜色，大小
  <h1 style="font-family:verdana">A heading</h1>
  <p style="font-family:arial;color:red;font-size:20px;">A paragraph.</p>
  </body>
  </html>
  ```

引用：

​	abbr:定义缩写

​	acronym:定义首字母缩写

​	address:定义地址

```html
The <abbr title="People's Republic of China">PRC</abbr> was founded in 1949.
<acronym title="World Wide Web">WWW</acronym>
```

- 类

  ```html
  <!DOCTYPE html>
  <html>
  <head>
  <style>
  .cities {
      background-color:black;
      color:white;
      margin:20px;
      padding:20px;
  } 
  </style>
  </head>
  
  <body>
  
  <div class="cities">
  <h2>London</h2>
  <p>
  London is the capital city of England. 
  It is the most populous city in the United Kingdom, 
  with a metropolitan area of over 13 million inhabitants.
  </p>
  </div> 
  
  </body>
  </html>
  ```



- 表单标签：

  表单：概念：采集用户输入的数据。用户和服务器进行交互

  使用标签：form(可以定义一个范围，范围代表采集用户数据的范围)

  **属性**：action:指定提交数据的URL

  ​				method:指定提交方式(一共7种，2种常用)

  **get：**

  - 请求参数会在地址栏中显示(会封装到请求行中)

  - 请求参数大小有限制

  - 不太安全

  **post：**

  - 请求参数不会在地址栏中显示，会封装在请求体中

  - 请求参数大小没有限制

  - 较为安全

  **注意：表单项中的数据要想被提交，必须指定其name属性**

  ```html
  <form action="http://" method="get">
      用户名：<input type="text" name="username"><br/>
      有name属性，会被提交
      密码:<input><br/>
      没有name属性，不会被提交
      <input type="submit" value="登录">
  </form>
  ```

表单项标签：

**input**：可以通过type属性值，改变元素展示的样式

​	type属性：

​		label：指定输入项的文字描述信息（label的for属性会和input的id值对应，点击label区域，会让input获取焦点）

​		text:文本输入框

​				**placeholder:给文本加默认值(灰色)**

​				**value只是加值**			

```html
<input type="username" name="username" placeholder="请输入用户名">
```

​		password：密码输入框

​		number：数字输入框，右边有上下箭头

​		**radio:**单选框

**单选框注意：**

- 要想让多个单选框实现单选效果，则多个单选框的name属性值必须相同

- 一般会给每一个单选框提供value属性，指定其被选中后提交的值

  ```html
  <input type="radio" name="gender" value="male" checked="checked">男
  checked="checked"(默认选中)/checked同
  <input type="radio" name="gender" value="famale">女
  ```

​		checkbox:复选框

​		file：文件选择框(选择上传文件)

​		hidden：隐藏域

​		按钮：

​				submit：提交表单

​				button：普通按钮

​				image：图片提交按钮

```html
<input type="image" src="图片的路径"> 
```

​				color：取色器

```html
<input type="color" name="color">(了解)
```

​				date：日期

```html
<input type="date" name="birthday">
<input type="datetime-local" name="birthday">(可以显示时间)
```

​				email：邮箱

```html
<input type="email" name="email">
```

select：下拉列表

```html
<select name="address">
	<option >-请选择-</option>
    <option value="1">北京</option>
    <option value="2">上海</option>
</select>
```

textarea：文本域

```html
<textarea cols="20" rows="5" name="text">
	cols:指定列数
    rows:默认多少行
</textarea>
```

## 三.CSS

（页面美化和布局控制）

- 概念：(Cascading Style Sheets 层叠样式表)

  层叠：多个样式可以作用在同一个html的元素上，同时生效

- 好处：

  - 功能强大

  - 将内容的展示和样式的控制分离

    *降低耦合度，解耦

    *让分工协作更容易

    *提高开发效率

- **CSS的使用：CSS与html结合方式**

  - **内联样式(不推荐使用)**

    在标签内使用style属性指定css代码

    ```html
    <div style="color:red;">hello css</div>
    ```

  - **内部样式**

    在head标签内定义style标签，style标签的标签体内容就是css的代码

    ```html
    <head>
    <style>
    	div{
    	color:blue;
    	}
    </style>
    </head>
    <body>
        <div>hello</div>
    </body>
    ```

  - **外部样式**

    定义css的资源文件

    在head标签内，定义link标签，引入外部的资源文件

    ```html
    a.css文件
    div{
    	color:green;
    }
    <link rel="stylesheet" type="text/css" href="css/a.css">
    <div>hello</div>
    <div>hello</div>
    
    <!-- 不常用写法，在head中导入-->
    <style>@import "css/a.css";</style>
    ```

    CSS注释：/*注释*/

    **注意：**

    - css作用的范围越来越大
    
  - **三种链接方式的优先级**

    内联式>嵌入式>外部式

- CSS语法

  - 格式：

    选择器{

    ​	属性名1：属性值1；

    ​	属性名2：属性值2；

    ​	...

    }

    选择器：筛选具有相似特征的元素

    **注意：**每一对属性需要分开

    - 标签选择器：标签名称{}

    - 类选择器：.类名{}

      ```html
      .abc{}
      <span class="abc"></span>
      ```

      

    - id选择器：#id名称{}

      **注意：**

      id选择器最多只能用一次，类选择器可以使用多次

      可以使用类选择器词列表方法为一个元素同时设置多个样式

      

      ```html
      .stress{
          color:red;
      }
      .bigsize{
          font-size:25px;
      }
      <p>到了<span class="stress bigsize">三年级</span>下学期时，我们班上了一节公开课...</p>
      ```

    - 子选择器：>用于选择指定标签元素的第一代子元素

      ```html
      .food>li{border:1px solid red;}
      ```

    - 后代选择器：空格  用于选择指定标签元素下的后辈元素

      ```html
      .first span{color:red;}
      ```

    - 通用选择器：*匹配html中所有标签元素

      ```html
      *{
      	color:red;
      }
      ```

    - 伪类选择器：允许给不存在的标签(标签的某种状态)设置样式

      ```html
      a::hover{
      	color:red;
      }
      <!-- 将a标签鼠标滑过的状态设置字体颜色变红-->
      ```

    - 分组选择器：为html多个标签元素设置同一个样式

      ```html
      h1,span{color:red;}
      ```

  - CSS的继承：

    ```html
    p{color:red;} 
    <!--这里的颜色适用于所有p标签中的元素,包括子元素span标签-->
    <p>1234<span>5678</span></p>
    ```

    **注意：**css有一些样式是不具有继承性的

    如：border:1px solid red;

    ```html
    <border:1px solid red;>
    <p>1234<span>5678</span></p>
    <!--这里只给p标签设置了边框像素为1、红色、实心边框线,而对元素span是没有起到作用的-->
    ```

  - **选择器的优先级：内联样式>id选择器>类选择器>标签选择器>通配符选择器**

  - 标签的权值计算规则：

    标签权值为1

    类选择器的权值为10

    ID选择器的权值最高为100

    ```html
    p{color:red;} /*权值为1*/
    p span{color:green;} /*权值为1+1=2*/
    .warning{color:white;} /*权值为10*/
    p span.warning{color:purple;} /*权值为1+1+10=12*/
    #footer .note p{color:yellow;} /*权值为100+10+1=111*/
    ```

    浏览器是根据权值来判断使用哪种CSS样式，哪种高用哪种

    **!important拥有最高权值，要写在分号之前**

    

  - 属性：

    设置字体：

    ​	font-size:设置字体大小

    ​	color:设置字体颜色

    ​	font-weight：字体粗细

    ​	font-family:设置字体(电脑要安装该字体，不然看不见)

    ​	font-style:

    ​			normal：正常字体(font-style)默认值

    ​			italic：设置字体为斜体

    ​			oblique：设置字体为倾斜

    ​	line-height:设置行间距

    font设置可以简写成一行:使用这种简写至少要指定font-size和font-family属性，其他属性未指定会自动使用默认值

    缩写时font-size与line-height中间要加/

    text-decoration：overline文本上的一条线

    ​								underline文本下的一条线

    ​								line-through穿过文本的一条线

    text-indent：为文本添加首行缩进

    ```html
    p{text-indent:2em;}
    <!--2em就是文字的2倍大小-->
    ```

    letter/word-spacing：设置字母或单词之间的间距

    text-align：设置文本对齐方式

- 元素分类

  - 块状元素：

    ```html
    <div> <p> <h1>...<h6> <ol> <ul> <dl> <table> <address> <blockquote> <form>
    ```

    **display:block 讲元素显示为块级元素**

    ```html
    a{display:block;}设置a为块级元素
    ```

    特点：①独占一行

    ​			②元素的高度、宽度、行高以及顶和底边距都可设置

    ​			③元素宽度在不设置时，和父元素宽度一致

  - 内联元素：

    ```html
    <a> <span> <br> <i> <em> <strong> <label> <q> <var> <cite> <code>
    ```

    **display:inline设置元素为内联元素**

    ```html
    div{display:inline;}
    <div>我要变成内联元素</div>
    ```

    特点：①和其他元素都在一行上

    ​			**②元素的高度、宽度以及顶部和底部边距不可设置**

    ​			③元素的宽度就是它包含的文字或者图片的宽度

  - 内联块状元素：

    ```html
    <img> <input>
    ```

    **display:inline-block**

    特点：①和其他元素都在一行上

    ​			②元素的高度、宽度、行高以及顶和底边距都可设置

    **none:隐藏元素**

- 盒子模型

  width,height指的是填充以里的内容范围

  border-left左边框 border-right右边框

  padding-left左填充 padding-right右填充

  margin-left左边界 margin-right右边界

  一个元素实际宽度 = 左边界+左边框+左填充+内容宽度+右填充+右边框+右边界

  - background-color：背景色

  - border：为盒子添加边框

    border-style：dashed(虚线) dotted(点线) solid(实线)

    border-color 可设置为十六进制颜色

    border-width：thin| medium | thick(最常用px)

  - padding为盒子设置内边距

    有顺序：上右下左

    ```html
    div{padding:10px;}全为10像素
    ```

    ```html
    div{padding:10px 20px;}上下为10px，左右为20px
    ```

  - margin：元素与其他元素之间的距离，也可分为上右下左

    margin-top:20px;

    margin-right:10px;

    margin-bottom:15px;

    margin-left:30px;

  - padding和margin的区别：padding在边框里，margin在边框外

- **CSS布局模型**：

  - 流动模型：Flow(默认的网页布局模式)

    特征：①块状元素都会在所处的包含元素内自上而下按顺序垂直延申分布，因为默认块状元素宽度都是100%

    ​			②内联元素会在所处的包含元素内从左到右水平分布

  - **浮动模型：**Float(环绕文字)

    ```html
    div{
        width:200px;
        height:200px;
        border:2px red solid;
        float:left;
    }
    
    div{
        width:200px;
        height:200px;
        border:2px red solid;
    }
    #div1{float:left;}
    #div2{float:right;}
    ```

    层模型：每个图层能够精确定位

    ①绝对定位：(position:absolute)

    ```html
    div{
    	width:20px;
    	height:200px;
    	border:2px red solid;
    	position:absolute;
    	left:100px;
    	top:50px;
    }
    ```

    如果不存在这样的包含块，则相对于body元素，既浏览器窗口

    ②相对定位：(position:relative)

    ```html
    #div{
    	width:200px;
    	height:200px;
    	border:2px red solid;
    	position:relative;
    	left:100px;
    	top:50px;
    }
    <div class="div1"></div>
    ```

    *偏移前的位置保留不动，比如在div中加span标签*

    *span标签中内容还是在div后面*

    ③固定定位：(position:fixed)

    ```html
    #div{
    	width:200px;
    	height:200px;
    	border:1px red solid;
    	position:fixed;
    	left:0px;
    }
    ```

    *拖动滚动条时位置固定不变*

  - relative与absolute组合使用

    - 参照定位的元素必须是相对定位元素的父元素

      ```html
      <div id="box1">    这是参照定位元素
      	<div id="box2">相对参照元素进行定位</div>    这是相对定位元素
      	</div>
      ```

    - 参照定位元素必须加position:relative

      ```html
      #box1{
      width:100px;
      height:100px;
      position:relative;
      }
      ```

    - 定位元素加position:absolute,就可以使用top,boottom,left,right来进行偏移定位

      ```html
      #box2{
      position:absolute;
      left:0px;
      }
      ```

  - 弹性盒模型:

    flex属性

    ```html
    <body>
        <div class="box">
            <div class="box1"></div>
            <div class="box2"></div>
            <div class="box3"></div>
        </div>
    </body>
    
    <style> 
        .box{
            height:400px;
            background:skyblue;
            display:flex;
        }
        .box1{
            width:200px;
            height:200px;
            background:red;
        }
        .box2{
            width:200px;
            height:200px;
            background:green;
        }
        .box3{
            width:200px;
            height:200px;
            background:orange;
        }
    </style>
    ```

    在父类容器中加flex

    - 设置display:flex属性可以把块级元素在一排显示
    - flex需要添加在父元素上，改变子元素的排列顺序
    - 默认从左往右以此排列，且和父元素左边没有间隙

    **justify-content**属性设置横轴排列方式

    justify-content:**flex-start**

    ​	交叉轴的起点对齐

    justify-content:**flex-end** 右对齐

    justify-content:**center**居中

    justify-content:**space-between**两端对齐，项目之间的间隔都相等

    justify-content:**space-around**每项两侧的间隔相等，所以项目之间间隔比项目与边框之间的间隔大一倍

    **align-items**属性设置纵轴排列方式

    **flex-start:默认值，左对齐**

    flex-end:与底部对齐

    center:在中间

    **baseline**:项目的第一行文字的基线对齐(文字底部对齐)

    **stretch(默认值)**:如果项目未设置高度或为auto，将占满整个容器的高度

  - flex占比(定义在子元素中)

    ①flex属性的值只能是正整数，表示占比多少

    ②给元素设置了flex之后，其宽度属性会失效

    ③设置子元素相对于父元素的占比

  - 水平居中设置

    - 行内元素

      通过父类给元素设置text-align:center来实现

      ```html
      <body>
          <div class="div1">我要居中</div>
      </body>
      
      <style>
          .div1{
              text-align:center;
          }
      </style>
      ```

    - 定宽块状元素

      通过设置左右margin值为auto实现居中

      ```html
      <!--已知宽高实现盒子水平垂直居中-->
      <style>
          .box{
              border:1px red solid;
              height:300px;
              position:relative;
          }
          .box1{
              position:absolute;
              top:50%;
              left:50%;
              margin:-100px 0px 0px -100px;
              width:200px;
              height:200px;
              border:1px red solid;
          }
      </style>
      ```

      **解释：**

      ​		①利用父元素设置相对位置，子元素设置绝对位置

      ​		②子元素设置上和左偏移的值都是50%，是元素的左上角在父元素中心点的位置

      ​		③然后再用margin给上和左都黑负的自身宽高的一般，就能达到垂直水平居中的效果

      ```html
      <!-- 不定宽高实现盒子垂直水平居中 -->
       <style>
              .box {
                  background-color: burlywood;
                  border: 1px blue solid;
                  height: 300px;
                  position: relative;
              }
      
              .box1 {
                  background-color: chartreuse;
                  border: 1px red solid;
                  position: absolute;
                  top: 50%;
                  left: 50%;
                  transform: translate(-50%,-50%);
                  /*
                  	用css3属性translate位移,给上和左都位移-50%距离，就能达到垂直水平居中的效果
                  */
              }
          </style>
      ```

  - 自适应列
  
    ```html
    <!--自适应三列-->
    <style>
        *{
            padding:0px;
            margin:0px;
        }
    .left {
    	width: 300px;
        height: 100vh;
        background-color: #aadddd;
        float: left;
                }
        .mid {
    		<!--margin-left:300px;-->
            <!--margin-right:300px;-->
            height: 100vh;
            background-color: #aa11dd;
                }
       	.right{
           width: 300px;
           height: 100vh;
           background-color: #f08844;
           float: right;
    }
    </style>
            <div class="left">left</div>
            <div class="right">right</div>
            <div class="mid">mid</div>
    注意：中间一列要放后面
    ```
  
- CSS布局：

  - 单列布局

  - 双列布局

  - 三列布局

    ```html
    .container{
      width: 1200px;
      height: 100vh;
      margin: 0 auto;
     } 
     .div1{
      width: 300px;
      height: 100vh;
      float: left;
      background-color: aquamarine;
      }
      .div2{
       width: 700px;
       height: 100vh;
       float: left;
       background-color: bisque;
       }
       .div3{
        width: 200px;
        height: 100vh;
        float: left;
        background-color:brown;
        }
    ```

- 动画：

  animation:

  ​	属性：**name 要绑定到选择器的关键字名**

  ​				**duration 动画指定需要多少毫秒完成**

  ​				**timing-function 设置动画将如何完成一个周期**

  ​							**属性：linear(匀速)**

  ​										**ease(默认，低速开始，加快，然后变慢)**

  ​										**ease-in(以低速开始)**

  ​										**ease-out(低速结束)**

  ​										**ease-in-out(低速开始和结束)**

  ​				**delay 动画启动前延迟**

  ​				**iteration-count 定义动画播放次数(infinite无限循环)**

  ​				**direction 指定是否该轮流反向播放动画**

  ​						**属性：normal(默认,正常播放)**

  ​									**reverse(反向播放)**

  ​									**alternate(正反反正)**

  ​									**alternate-reverse(反正正反)**

  ​				**fill-mode 动画不播放时的样式**

  ​						**属性：forwards (结束时的画面)**

  ```html
  <div>animation: heartbeat 0.5s linear  infinite alternate forwards;</div>
   <style>
          body {
              background-color: black;
  
          }
  
          .container{
              height: 500px;
              width: 400px;
              position: relative;
              margin: 100px auto;
              animation: heartbeat 0.5s linear infinite alternate ;
          }
  
          .heartbeat1 {
              width: 200px;
              height: 200px;
              left: 40px;
              border-radius: 50%;
              background-color: red;
              position: absolute;
          }
  
          .heartbeat2 {
              width: 200px;
              height: 200px;
              right: 40px;
              border-radius: 50%;
              background-color: red;
              position: absolute;
          }
  
          .bottom {
              width: 180px;
              height: 180px;
              top: 84px;
              left: 110px;
              position: absolute;
              background-color: red;
              transform: rotate(45deg);
          }
          @keyframes heartbeat{
              from{}
              to{
                  transform: scale(1.2);
              }
          }
      </style>
  ```

  **transform:属性：**

  **translate(x,y) 转换**

  **scale(x,y) 缩放转换**

  **rotate(angle) 旋转**

  ```html
  <!--Z字变换-->
  <style>
              .out{
                  width: 200px;
                  height: 200px;
                  margin: 100px auto;
                  position: relative;
                  background-color: chocolate;
              }
              .in{
                  width: 30px;
                  height: 30px;
                  background-color: cornflowerblue;
                  animation: rtg 2s linear  5 alternate forwards;
              }
              @keyframes rtg{
                  0%{
                      transform: translateX(0);
                  }
                  33%{
                      transform: translateX(170px);
                  }
                  66%{
                      transform: translate(0,170px);
                  }
                  100%{
                      transform: translate(170px,170px);
                  }
              }
          </style>
   <div class="out">
              <div class="in"></div>
          </div>
  ```

  **overflow:visible (默认 超出部分会呈现在元素框之外)**

  **overflow:hidden(超出部分内容不可见)**

  **overflow:scroll(超出部分会被放在滚动条中)**

  **overflow:auto (如果内容超出，则浏览器显示滚动条)**
