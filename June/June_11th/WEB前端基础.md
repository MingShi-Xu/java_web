# WEB前端基础
## 一、WEB概述、
### 1.软件架构、
#### C/S架构
客户端/服务器端

- 优点：	
 用户体验好
- 缺点：
 	 开发，安装，部署，维护麻烦
####  B/S架构
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

### 2.HTML

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

    title：标题标签

    body：体标签

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
  
  
  
- 图片标签
  
  img:展示图片(自闭合)
  
    ```html
    <img src="图片存放位置" alt="图片描述"/>
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
    <a href="http://www.i.com">点击</a>
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
      用户名：<input name="username"><br/>
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
<input type="image" sec="图片的路径"> 
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

### 3.CSS

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

- CSS语法

  - 格式：

    选择器{

    ​	属性名1：属性值1；

    ​	属性名2：属性值2；

    ​	...

    }

    选择器：筛选具有相似特征的元素

    **注意：**每一对属性需要分开

  - 属性：

    

