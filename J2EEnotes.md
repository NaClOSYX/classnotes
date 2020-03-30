# 视频笔记

## HTML5

**HTML**是<u>*htyper text markup language*</u> 的缩写，即超文本标记语言。

**HTML基础模板**

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
	</head>
	<body>
		
	</body>
</html>
```

**`<!DOCEYPE HTML>`**

> `<!DOCTYPE> `声明必须位于 HTML5 文档中的第一行，也就是位于`<html>` 标签之前。该标签告知浏览器文档所使用的 HTML 规范。
>
> doctype 声明不属于 HTML 标签；它是一条指令，告诉浏览器编写页面所用的标记的版本。

### 标签

* 标签是由一对尖括号包裹的单词构成 例如: `<html>` 
* 标签不区分大小写，`<html>` 和 `<HTML>` 是一样的
* 标签分为两部分: 开始标签`<a>` 和 结束标签`</a>`. 两个标签之间的部分 我们叫做标签体
* 有些标签功能比较简单，使用一个标签即可.这种标签叫做自闭和标签.例如: `<br/><hr/><input/><img/>`
* 标签可以嵌套.但是不能交叉嵌套. `<a><b></a></b>`这样就不对
* 标签的属性通常是以键值对形式出现的. 例如 name="nick"
* 标签的属性只能出现在**开始标签**或**自闭和标签**中
* 标签的属性名字全部小写，属性值必须使用双引号或单引号包裹，例如`name="nick"`
* 如果属性值和属性名完全一样，直接写属性名即可，例如`readonly`

#### 常用标签

> `<html>`：定义 HTML 文档。

* 此元素可告知浏览器其自身是一个 HTML 文档。
* `<html> `与 `</html>` 标签限定了文档的开始点和结束点，在它们之间是文档的头部和主体。

> `<head>`：定义关于文档的信息。

* `<head>`元素是所有头部元素的容器。
* `<head>`元素必须包含文档的标题，可以包含脚本、样式、meta 信息以及其他更多的信息。

> `<title>`：定义文档的标题。

* 浏览器会以特殊的方式来使用标题，并且通常把它放置在浏览器窗口的标题栏或状态栏上。同样，当把文档加入用户的链接列表或者收藏夹或书签列表时，标题将成为该文档链接的默认名称。

> `<meta>`：定义关于 HTML 文档的元信息。

* 属性`content` 定义与`http-equiv`或`name`属性相关的元信息，是必要的属性。

* 属性`http-equiv `把`content`属性值关联到http头部。
  * Content-Type（浏览器接受的文档类型，一般是text/html）
  * refresh（网页刷新，以秒为单位）
  * expires（设定网页到期时间，一旦过期，必须到服务器上重传）
* 属性`name` 把`content`属性关联到一个名称。
  * keywords（搜索关键字，用于搜索引擎抓取信息的显示）
  * description（搜索到网站后显示的网页内容简描述）
  * author（站点制作者信息）
  *  generator（用以说明生成工具）

> `<base>`：定义页面中所有链接的默认地址或默认目标。

* 通常情况下，浏览器会从当前文档的 URL 中提取相应的元素来填写相对 URL 中的空白。

* 使用`<base>`标签可以改变这一点。浏览器随后将不再使用当前文档的 URL，而使用指定的基本 URL 来解析所有的相对 URL。
* `href='URL'`：规定页面中所有相对链接的基准 URL。

> `<link>`：定义文档与外部资源的关系。

> `<style>`：定义文档的样式信息。

> `<script>`：定义客户端脚本。

> `<body>`：定义文档的主体。

> `<div>`：定义文档中的节。

* 定义文档中的分区或节。

* 把文档分割为独立的、不同的部分。它可以用作严格的组织工具，并且不使用任何格式与其关联。

  ```html
  <div style="color:#00FF00">
    <h3>This is a header</h3>
    <p>This is a paragraph.</p>
  </div>
  ```

> `<a>`：定义超链接标签。

* `href`超链接地址。可以是Web上任意资源，包括图片，网页，样式，脚本文件等。`href="#“`时，表示被链接页面就是当前页面。

  ```html
  # 跳转网页
  <a href="">a</a>
  ```

* `target`文档打开时要显示的目标位置。属性值一般有：blank（新窗口中打开）、self（默认，在超链接所在的容器中打开）、parent（在超链接的父容器中打开）、top（整个容器中打开）、name（框架名称）。

* `name`锚记名称。作用：跳转到文档的某个地方。返回首页。

  ```html
  # 跳转锚记书签名称
  <a name="top"><h3>Top！</h3></a>
  <div style="height：800px"></div>
  <a href="#top">top</a>
  ```

> `<img>`：定义图像。

* `src`图片地址。

* `title`鼠标悬浮在图片上的文字。

* `alt`图片找不到时要替换的文字。如果图片资源使用的是外网资源，则不会显示要替换的文字。如果使用的是本网站的资源（相对路径给出），则找不到图片时会显示替换的文字，并保留图片设置的宽高结构。

* `align`图片周围文字的垂直对齐情况。常用的属性值有：top（与图片的顶部对齐）、middle（与图片的中部对齐）、bottom（默认，与图片的底部对齐）。

* `width`图片的宽

* `height`图片的高 (宽高两个属性只用一个会自动等比缩放)。

  ```html
  <img src="http://images.cnblogs.com/cnblogs_com/suoning/845162/o_ns.png" alt="图片加载失败。。。" title="The knife girl, kiss"/>
  ```

##### 基本标签
> `<h1>~<h6>`：定义HTML标题。

* `<h1>`定义最大的标题。`<h6>`定义最小的标题。

* <h1>h1</h1><h2>h2</h2><h3>h3</h3><h4>h4</h4><h5>h5</h5><h6>h6</h6>

> `<b>`定义粗体字。

> `<strong>`定义强调文本。

> `<em>`定义强调文本。

> `<i>`定义斜体字。

> `<u>`定义下划线文本。

> `<sup>`定义上标文本。

> `<sub>`定义下标文本。

> `<strike>`定义加删除线文本。

> `<p>`：定义段落

> `<span>`：定义文档中的节。

> `<br>`：定义一个简单的换行符。

* `<br>`是空标签，建议使用`<br/>`。

> `<hr>`：定义水平分割线。

* 在HTML页面中创建一条水平线。

* 水平分割线可以在视觉上将文档分割成各个部分。

* `<hr>`是空标签，建议使用`<hr/>`。

* <hr/>

> `<!--..-->`：定义注释。

##### 列表标签

> `<ul>`：定义无序列表。

> `<ol>`：定义有序列表。

> `<li>`：定义列表的项目。

* type指明项目的类型，属性值有：A，a，I，i，1，disc（实心圆），square（实心正方形），circle（空心圆）。
* value表示序号值从几开始。

```html
<ul>
   <li>Coffee</li>
   <li>Tea</li>
   <li>Milk</li>
</ul>
<ol>
   <li>Coffee</li>
   <li>Tea</li>
   <li>Milk</li>
</ol>
```

> `dl`定义定义列表。

> `dt`定义定义列表中的项目。

> `dd`定义定义列表中项目的描述。

```html
<dl>
   <dt>计算机</dt>
   <dd>用来计算的仪器 ... ...</dd>
   <dt>显示器</dt>
   <dd>以视觉方式显示信息的装置 ... ...</dd>
</dl>
```

##### 表格标签

> `<table>`：定义表格。

* > `<caption>`定义表格标题。

* > `<tr>`定义表格中的行。

* > `<th>`定义表格中的表头单元格。

* > `<td>`定义表格中的单元。

* > `<thead>`定义表格中的表头内容。

* > `<tbody>`定义表格中的主体内容。

* > `<tfoot>`定义表格中的表注内容（脚注）。

```html
<table>
    <caption>xxxxxxxxxx</caption>
    <thead>
            <tr>
                <th>序号</th>
                <th>姓名</th>
                <th>年龄</th>
                <th>女神</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th>1.</th>
                <td>nick</td>
                <td>18</td>
                <td>可可西</td>
            </tr>
            <tr>
                <th>2.</th>
                <td>jenny</td>
                <td>21</td>
                <td>nick!!!</td>
            </tr>
        </tbody>

</table>
```

<table>
    <caption>xxxxxxxxxx</caption>
    <thead>
            <tr>
                <th>序号</th>
                <th>姓名</th>
                <th>年龄</th>
                <th>女神</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th>1.</th>
                <td>nick</td>
                <td>18</td>
                <td>可可西</td>
            </tr>
            <tr>
                <th>2.</th>
                <td>jenny</td>
                <td>21</td>
                <td>nick!!!</td>
            </tr>
        </tbody>
</table>
##### 表单标签


> `<form>`：定义供用户输入的 HTML 表单。

* HTML 表单用于接收不同类型的用户输入，用户提交表单时向服务器传输数据，从而实现用户与Web服务器的交互。表单标签, 要提交的所有内容都应该在该标签中。

* `action`表单要提交的地址，用于处理表单的内容（一般是提交字典到后台的一个接口，这个接口是java写成的，提交到这个接口后后台就知道如何处理这些数据了）。

* `method` 提交的方法，默认是get方式提交。

  * `get`
    1. 提交的键值对.放在地址栏中url后面。
    2. 安全性相对较差。
    3. 对提交内容的长度有限制。
  * `post`
    1. 提交的键值对不在地址栏。
    2. 安全性相对较高。
    3. 对提交内容的长度理论上无限制。

  ```html\
  <form action="https://www.baidu.com/s">
  	<input type="text" name="wd">
  	<input type="submit" value="百度一下">
  </form>
  ```

> `<input>`：定义输入控件。

* `type`
  * `text`文本框
    * `autocomplete`（自动完成输入的内容，要求表单元素要有name属性才有自动完成的效果，off表示自动完成不可用，on表示自动完成可用）
    * `disabled`（设置获取控件的状态，默认是false即可用，等于true时不可用，不能输入内容）
    
  * `password`密码框（以下属性text和password共有）
    
    * `value`（设置默认值）
    
    * `size`（指定表单元素的初始宽度。当type为text或password时，表单元素的大小以字符为单位，对于其他元素，宽度以像素为单位）。
    * `maxlength`（type为text或password时，表示输入的最大字符数），有利于防止sql的注入攻击。
    * `readonly` 只读。
    * `placeholder` 框内预置内容(灰色)，写上内容时才消失。
    
  * `radio`单选按钮
    * name（将name的值设置为相同值，才表示一组数据，才能实现单选功能）
    * value（必须要写，提交到服务器的key值，实际开发过程中value一般是编号）
    * checked（是否被选中的状态）
    
  * `checkbox`复选框
    * name（名字一定要一样一样的，才表示是一组数据，添加到同一value值列表提交到服务器）
    * value（必须要写，提交到服务器的key值，实际开发过程中value一般是编号）
    * checked（是否被选中的状态
    
  * `submit`提交按钮。用于提交表单。
  
  * `reset` 重置按钮。清空表单的输入，恢复到表单默认的状态。
  
  * `button`普通按钮。一般结合javascript使用。
  
  * `image`图片按钮，用来提交表单，与submit是一样的效果。
    
    * src（图片路径）
    
  * `date`日期选择器，用来选择日期。
  
  * `color`颜色选择器，用来选择颜色。
  
  * `range`范围选择器，用来选择范围
  
    * `min`（最小值）
    * `max`（最大值）
  
  * `email`邮件输入框
  
    * 提交的时候会进行邮件格式校验
  
  * `url`地址输入框
  
    * 提交的时候会进行地址格式校验
  
  * `file`文件域，上传文件（不同的浏览器表现形式不同）
  
    * `multiple="multiple"`（可以选择多个文件）
  
  * `hidden`隐藏字段
    
    * value（隐藏的内容）

> `<textarea>`定义多行的文本输入控件。

* 默认表现形式是可以输入很多行文本的文本框。
* name （表单提交项的key）
* cols（设置文本域宽度）
* rows（设置文本域高度，即行数）

> `<label>`：

* 把元素与文本结合起来

* 不只是选中复选框才能选中并打钩，要求点击对应的文字也能选中该复选框。
  这种情况下要用到<label>标签的for属性（设置或获取给定标签对象指定到的对象，值=另一个元素的id号即可）

  ```html
  <label for="name">姓名</label>
  <input id="name" type="text">
  ```

> `<select>`：定义选择列表（下拉列表）。

* 使用时要结合`<option>`子标签一起使用。
* name（表单提交项的key）
* size（选项个数）
* multiple（多选）

> `<option>` 定义选择列表中的选项。

* value（表单提交项的值）

*  selected（selected下拉选默认被选中）

  ```html
  <select>
    <option value ="volvo">Volvo</option>
    <option value ="saab">Saab</option>
    <option value="opel">Opel</option>
    <option value="audi">Audi</option>
  </select>
  ```

### 特殊符号

>HTML 中的预留字符必须被替换为字符实体。
>
>一些在键盘上找不到的字符也可以使用字符实体来替换。
>
>实体名称对大小写敏感！

```tml
&nbsp;  空格
&copy;  版权符号 ©
&gt;    大于号 >
&lt;    小于号 <
&quot;  双引号 "
&apos;  单引号 '
```

## CSS

CSS是*Cascading Style Sheets*的缩写，即层叠样式表

对网页中的元素进行精确控制 

网页表现与内容分离的样式设计语言

### 写法格式

* 外链样式：通过加载后缀名为.css的文件载入使用，写在`<head>`标签中。影响引入该文件的页面所有内容。

  1. 链接式

     ```html
     <link type="text/css" rel="styleSheet"  href="CSS文件路径" />
     ```

  2. 导入式

     ```html
     <style type="text/css">
       @import url("css文件路径");
     </style>
     ```

* 页内样式：在本页面内书写该样式，尽量写在`<head>`标签中。只影响本页面。

  ```html
  <style type="text/css">
      ...
  </style>
  ```

* 行内样式：写在HTML标签内部。只影响本标签。

  ```html
  <标签 style="..."></标签>
  ```

### CSS选择器

| 选择器            | 例子            | 例子描述                                   |
| ----------------- | --------------- | ------------------------------------------ |
| .class            | .intro          | 选择 `class="intro" `的所有元素。          |
| #id               | \#firstname     | 选择 `id="firstname" `的所有元素。         |
| *                 | *               | 选择所有元素。                             |
| element           | p               | 选择所有 `<p>` 元素。                      |
| element,element   | div,p           | 选择所有` <div>` 元素和所有 `<p> `元素。   |
| element element   | div p           | 选择 `<div> `元素内部的所有` <p>` 元素。   |
| element>element   | div>p           | 选择父元素为 <div> 元素的所有 <p> 元素。   |
| element+element   | div+p           | 选择紧接在 <div> 元素之后的所有 <p> 元素。 |
| [attribute]       | [target]        | 选择带有 target 属性所有元素。             |
| [attribute=value] | [target=_blank] | 选择 target="_blank" 的所有元素。          |

#### 基础选择器

1. 标签选择器

   * 选择标签的名字，比如：ul、li、lable、dt、input…

   * 标签选择器，选择的是页面上的所有这种类型的标签，所有经常描述“共性”，无法描述某一元素的“个性”的。

     ```html
     <p>我是一个段落标签</p>
     ```

     ```css
     <style type="text/css">
     	p{
     	}
     </style>
     ```

2. id选择器

   * id选择器的选择符是“#”。

   * 任何HTML标签都有id属性。表示这个标签的唯一标识。

     * 这个标签的名字可以任意取，但是
       1. 只能有字母、数字、下划线。 
       2. 必须以字母开头。 
       3. 不能和标签同名，比如id不能叫做：body、ul、img、a......

   * 一个HTML页面，不能出现相同的id，哪怕他们不是一个类型的标签。

     ```html
     <p>我是段落1</p>
     <p id="para2">我是段落2</p>
     ```

     ```css
     <style type="text/css">
     	#para2{
     	}
     </style>
     ```

3. 类选择器

   * .就是类的符号。

   * 所谓的类就是class属性，class属性和id十分相似，任何的标签都可以携带class属性。

   * class属性可以重复，比如，页面上可能有很多标签同一个class；

     ```html
     <h3 class="special">我是一个h3啊</h3>
     <p class="special">我是一个段落啊</p>
     ```

   * 同一个标签，可能同时属于多个类，用空格隔开：

     ```html
     <h3 class="special importance">我是一个h3啊2</h3>
     ```

     ```html
     <h3 class="special">我是一个h3啊2</h3>
     <p class="special">我是一个段落啊2</p>
     ```

     ```css
     <style type="text/css">
     	.special{
     	}
     </style>
     ```

#### 高级选择器

1. 后代选择器

   * 选择一个标签的所有后代。

   * 空格就表示后代，.div1 p就是.div1的后代所有p。

     ```html
     <div class="div1">
     	<ul>
     		<li>
     			<p>段落</p>
     			<p>段落</p>
     			<p>段落</p>
     		</li>
     	</ul>
     </div>
     ```

     ```css
     <style type="text/css">
     	.div1 p{
     	}
     </style>
     ```

     ```css
     <style type="text/css">
     	.div1 ul li p{
     	}
     </style>
     ```

2.  儿子选择器

   * 选择一个标签的儿子（下一级标签）。

   * `>`表示儿子，div1>p就是.div1的下一级儿子p。

     ```html
     <div>
     	<p>我是div的儿子</p>
     </div>
     ```

     ```css
     <style type="text/css">
     	div>p{
     	}
     </style>
     ```

3.  下一个兄弟选择器

   *  选择一个标签的下一个兄弟（平级的下一个标签）。

   * `+`表示下一个兄弟

     ```html
     <h3>我是一个标题</h3>
     <p>我是一个段落</p>
     ```

     ```css
     <style type="text/css">
     	h3+p{
     	}
     </style>
     ```

4.  交集选择器

   * 选择的同时满足n个条件的标签

   * 交集选择器可以连续交

     ```css
     <style type="text/css">
     	h3.special{
     	}
     </style>
     ```

5.  并集选择器

   *  选择分别满足几个条件的标签

   * 用逗号隔开表示交集。

     ```css
     <style type="text/css">
     	h3,li{
     	}
     </style>
     ```

6. 通配符

   * 选择所有元素

   * 用 `*`表示

     ```css
     *{
     }
     ```

### 常用属性



## JS

## JSP

### JSP九大内置对象

- pageContext
- request
- response
- session
- application
- config
- out
- page
- exception



# 课堂笔记

## 第一次课

Java EE

1. 课程介绍

   * 第一部分：Java高级编程

     * String与日期类使用
     *  Java 集合框架
     * Java数据库JDBC编程
   * 第二部分：JSP开发技术
     * HTML5, JavaScript,CSS
     * JSP, Servlet,JavaBean, Filter
   * 第三部分：Java开源框架
     * Hibernate 持久层框架
     * Spring & SpringMVC

2. 该如何学习？、

   结合项目，多写代码，设计系统架构等

   读程序（强调软件开发规范，阿里软件开发规范）；写程序；持续思考（效率，并发性，……，更好的规范）

   Web前端；JSP；开源部分；

3. 开发环境

   * JDK版本
     * JDK1.8
   * Eclipse
     * Version：2019-2（4.1.14.0）
     * Eclipse for JavaEE
     * 开发JSP支持Web开发
   * 数据库
     * MySql 5.5,5.6,...8.5
     * Oracle 

4. Eclipse开发Web项目

   Html5 编辑器 ---- HBuilder

   Web服务器 Tomcat 9.0 下载压缩版，解压之后就可以使用呢

## 第二次课

**常用工具类的使用**

1. String与StringBuffer

   * String类的使用

     1. 如何构建String类

        ```java
        String s1="Java";
        String s2=new String("Java");
        String s3=s1
        ```

        * 类：用来描述现实世界中的实体，将具有相同属性及操作的一组实体抽象成类（面向对象编程）

        * 对象：本质上对象就是变量；

          * 值类型：int,double boolean,char,... `int x=10; int y=x;y=80;`

          * 引用类型：Integer,Double,Boolean,Long,...,数组，系统类，自定义类;

            ​     			   `int[] arr=new int[10];arr[5]=100;`

            ​                   `Student s1=new Student();`

        * 实例：JVM 堆区域 开辟空间，存储对象所引用内存，对象属性存储地址，方法入口地址，所占用空间我们称为实例。

          * "Java"---> 字符串常量实例

          * `new String("Java");`

          * e.g.:

            ```java
            int[] arr=new int[10];
            int[] arr2=arr;
            arr2[0]=34;
            arr[0]=?;
            ```

        2. 串比较

           * e.g.:

             ```java
             String uname=txtUName.getText();
             if("admin".equals(uname)){//uname==null?
                 ...
             }
             ```

        3. 串分割

           ```java
           String s="Java,C#,Python,PHP,Scala";
           String[] arr=s.split(",");
           for(String t:arr){
               System.out.println(t);
           }
           ```

        4. 查找

           ```java
           String s="Java,C#,Python,PHP,Scala,Java";
           int x=s.indexOf("Java");//如果没有找到返回-1
           String sub=s.substring(5);//"C#,Python,PHP,Scala,Java
           String sub=s.substring(5,7);//
           String sub=s.substring("Java".length());//",C#,Python,PHP,Scala,Java"
           		sub.indexOf("Java");
           ```

           > ==补充实验一：使用字符串查找函数，统计字符串中某个字符串出现的次数==

        5. StringBuffer 缓冲区字符串

           * String为final类

             e.g:

             ```java
             final class A{//不可派生子类
                 ...
             }
             class MyString extends String{...} Math
             ```

             ```java
             class A{
                 public final void fun(){...}//子类不能覆盖或重写父类中的final函数
             }
             ```

             ```java
             public static final double PI=3.1415926; 
             ```

             ```java
             StringBuffer sb3=new StringBuffer("Java");
             String s=sb3.toString();
             ```

2. 日期类与日历类

   1. Date日期类、

      ```java
      Date date=new Date();
      System.out.println(date);
      ```

      * 格式化日期类(DateFormat)

        ```java
        SimpleDateFormat df=new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        System.out.println(df.format(date));
        ```

      * 串转变日期（解析）

        ```
        String s1="2020-01-01";
        SimpleDateFormat df=new SimpleDateFormat("yyyy-MM-dd");
        Date date1=df.parse(s1);
        ```

      > ==补充实验二：如何自定义格式化类 MyDateFormat?==
      >
      > ```java
      > public class MyDateFormat{
      >     String format="yyyy-MMM-dd";
      >     public MyDateFormat(String format){
      >         this.format=format;
      >     }
      >     public String format(Date date){
      >         return ...
      >     }
      >     public Date prase(String dateString) throws MyDateFormatException{
      >         return ...
      >     }
      > }
      > ```
      >
      > 

   2. 日历类

      ```java
      @Test
      public void test4() {
          Calendar cal=Calendar.getInstance();
          int year=cal.get(Calendar.YEAR);
          System.out.println(year);
      }    @Test
      public void test5() {
          Calendar cal=Calendar.getInstance();
          cal.set(Calendar.YEAR,2021);
          cal.set(Calendar.MONTH,2);
          cal.set(Calendar.DAY_OF_MONTH,9);
          System.out.println(cal.get(Calendar.WEEK_OF_MONTH));
      }
      ```


## 第三/四次课

1. 复习

   * 日期和日历类

   * `Calendar cal=Calendar.getInstance();`

     ```java
     public class MyCalendar {
         private static MyCalendar cal = null;
     
         public static MyCalendar getInstance() {
             if (cal == null)
                 cal= new MyCalendar();
             return cal;
         }
         
         @Test
         public void MyCalendarTest() {
             //单例模式
             MyCalendar cal1 = MyCalendar.getInstance();
             MyCalendar cal2 = MyCalendar.getInstance();
             System.out.println(cal1==cal2);//true
         }
     }
     ```

   * set(part,value)

2. Java集合框架

   1. 数据存储结构

      * 缓存中存储  数据结构=内存数据结构+算法

      * 持久化存储  文件；数据库技术

      * 几种主要形式

        * 顺序存储：数据在内存中是按照某种顺序存储。元素存储空间上是连续的。

          * ```java
            int[] x = new int[100]; //开辟100*4空间，
            x[10] = 45
            ```

          * 不利于元素增加，删除，移动等操作

          * ArrayList 动态改变存储空间，顺序存储结构；看成一个动态数组

            * ```java
              ArrayList list = new ArrayList();
              list.add(元素)；
              ```

        * 链式存储

          * LinkedLIst

        * 哈希存储

          * 每个元素存储位置由"元素值+Hash算法"来确定。
          * HashSet 元素值相同，存储空间相同，值不同则存储空间不同；没有重复值。

        * Map存储

          * 元素由key+value构成，存储位置由Key决定；查找元素值依据Key；key与value构成Map。

      * 集合框架：由系列接口与类构成Java集合

        * ```mermaid
          graph TB
          A[Colletion]-->B[Set]
          A-->C[List]
          B-->D[HashSet]
          B-->E[TreeSet]
          C-->F[LinkedList]
          C-->G[ArrayList]
          ```

        * 增加、移除、查找等基本操作

   2. HashSet

      * `HashSet hs = new HashSet();`//集合可以存储任意实例，任意元素实例
      * 实际编程中，集合用来存储某一种数据类型
      * `HashSet<Student> hs = new HashSet();`

   3. ArrayList

      * 动态数组，顺序存储，可以按照索引访问元素

      * ```java
        //速度对比
        @Test
        public void test2() {
            HashSet<Integer> hs=new HashSet<Integer>();
            long l1=System.currentTimeMillis();
            for (int i=1;i<=1000000;i++){
                hs.add(new Integer(i));
            }
            long l2=System.currentTimeMillis();
            System.out.println(l2-l1);
        
            ArrayList<Integer> list =new ArrayList<Integer>();
            long l3=System.currentTimeMillis();
            for (int i=1;i<=1000000;i++){
                list.add(new Integer(i));
            }
            long l4=System.currentTimeMillis();
            System.out.println(l4-l3);
        }
        
        ```

      * e.g.:

      * ```java
        HashSet<Integer> hs=new HashSet<Integer>();
        hs.add(1);,...hs.add(1000);
        hs.remove(100);//移除值为100这个Interger元素，无法按照索引移除元素
        
        List<Integer> ls=new ArrayList<Integer>();
        ls.add(1);,...ls.add(1000);
        ls.remove(1);//移除第二个元素，按索引移除
        ls.remove(new Integer(1));
        //
        for(int i=0;i<10000;i++)
            ls.remove(i);//移动次数多
        ```

   4. TreeSet：有序平衡二叉树（存储结构）

      * 按照某种指定排序算法对元素进行排序；

      * `TreeSet<Integer> ts=new TreeSet<Integer>();//如果没有指定算法，按照默认排序算法`

      * ```java
        public class MyCmp implements Comparator<Student> {
            public int compare(Student s1, Student s2) {
                int diffScore=s2.getScore()-s1.getScore();
                if(diffScore==0)
                    return -s1.getName().compareTo(s2.getName());
                return diffScore;
            }
        }
        ```

      * `````java
        //匿名类
        TreeSet<Student> ts=new TreeSet<Student>(new Comparator<Student>() {
            public int compare(Student s1, Student s2) {
                int diffScore=s2.getScore()-s1.getScore();
                if(diffScore==0)
                    return -s1.getName().compareTo(s2.getName());
                return diffScore;
            }
        });
        ```

      * ```java
        //让学生类变成可以比较
        public class Student implements Comparable<Student> {
            ...
            public int compareTo(Student s) {
                int diffScore=s.getScore()-this.getScore();
                if(diffScore==0)
                    return -this.getName().compareTo(s.getName());
                return diffScore;
            }
            ...
        }
        ```

      * 

   5. LinkedList：双向循环链表形式存储元素

   6. HashMap集合

      * 每个元素由key与value构成，依据key确定存储位置，查找元素的值，key---Map---value

      * ```java
        Map<Integer,Student> hm=new HashMap<Integer, Student>();
        ```

      * HTML5 (key,value)///(email,name)

      * ```java
                Map<Integer,String> hm=new HashMap<Integer, String>();
                hm.put(new Integer(1),"zhang");
                hm.put(new Integer(2),"li");
                hm.put(new Integer(3),"wang");
                hm.put(new Integer(2),"lou");
                /*首先找出key集合，迭代keys，依据每个key,查找元素的value*/
                Set<Integer> keys=hm.keySet();
                Iterator<Integer> it = keys.iterator();
                while (it.hasNext()){
                    Integer key=it.next();
                    String value=hm.get(key);
                    System.out.println(key+"  "+value);
                }
        ```

   7. TreeMap

      * 每个元素由key与value构成，依据key确定存储位置，查找元素的值；基于key平衡二叉树结构

   8. 栈、队列、向量

      * Stack,Queue,Vector;

      * ```java
        public List<Student> queryAllStudents(){
            List<Student> slist=new ArrayList<Student>;
            ...
            slist.add(s); //JDBC操作
            return slist;
        }
        ```

      Java JDBC操作

      1. 安装MySQL 5.5,5.6,...,8.5
      2. 复习基本sql


## 第五次课

1. MySQL编程基本步骤（SQLServer,Oracle等）

   1. 加载驱动（数据库访问驱动程序jar形式）

      mysql-connector-java

      ```java
      String driver="com.mysql.jdbc.Driver";
      Class.forName(driver);//加载驱动程序
      ```

   2. 创建连接Connection

      JDBC：Sun制定的一套开发数据库的统一规范，接口，各个数据库开发者（公司）；基于JDBC规范实现

      ```java
      String url="jdbc:mysql://localhost:3306/j2eeclass";
      String dbuser="root";
      String dbpwd="root";
      Connection conn= DriverManager.getConnection(url,dbuser,dbpwd);
      ```

   3. 发送SQL命令，执行SQL命令

      ```java
      Statement cmd=conn.createStatement();
      String sql = "select * from test";
      ```

   4. 执行SQL命令，返回结果集ResultSet

      ```java
      ResultSet rs = cmd.executeQuery(sql);
      ```

   5. 读取结果集中的数据

      ```java
      while (rs.next()) {
          int id = rs.getInt(1);
          String name = rs.getString(2);
          String password = rs.getString(3);
          System.out.println(id + name + password);
      }
      ```

   6. 关闭连接

      ```java
      conn.close();
      ```

2. 执行insert,update,delete,create等cuid语句，写数据库或更新数据库

   ```java
   String sql = "delete from test where id = 1";
   int x=cmd.executeUpdate(sql);
   ```

3. 带参数SQL语句

   ```java
   public int addUser(int id,String name,String password) throws Exception {
       String driver="com.mysql.jdbc.Driver";
       Class.forName(driver);//加载驱动程序
       String url="jdbc:mysql://localhost:3306/j2eeclass";
       String dbuser="root";
       String dbpwd="root";
       Connection conn= DriverManager.getConnection(url,dbuser,dbpwd);
       Statement cmd=conn.createStatement();
       String sql="insert into test values("+"id"+","+name+","+password+")";
       int x=cmd.executeUpdate(sql);
       conn.close();
       return x;
   }
   ```

   ```java
   public int addUser(int id,String name,String password) throws Exception {
       String driver="com.mysql.jdbc.Driver";
       Class.forName(driver);//加载驱动程序
       String url="jdbc:mysql://localhost:3306/j2eeclass";
       String dbuser="root";
       String dbpwd="root";
       Connection conn= DriverManager.getConnection(url,dbuser,dbpwd);
       String sql="insert into test values(?,?,?)";
       PreparedStatement pcmd=conn.prepareStatement(sql);
       pcmd.setInt(1,id);
       pcmd.setString(1,name);
       pcmd.setString(1,password);
       int x=pcmd.executeUpdate();
       conn.close();
       return x;
   }
   ```

   * 批量导入，使用带参数SQL语句效率更高；
   * 可读性高；
   * 提高安全性，SQL注入
     * `String sql="select count(*) from users where uid='@uid' and upwd='@upwd'";//1`
     * `String sql="select count(*) from users where uid='admin' or '1'='1' and upwd='@upwd'";//1`
   * 

4. 数据库编程分层设计

   * CustomerDao 数据库访问类Bean，包含对于表Customers的相关操作

   * Customer 实体类：映射数据库中某个表Customer ，Entity

     * ```sql
       create table customers(
       	cid varchar(20) not null primary key,
           cname varchar(30),
           cphone varchar(30)
       )
       ```

     * ```java
       public class Customer(){
           private String id,name,phone;
           //构造函数
           //getter-setter函数
       }
       ```

       

     * 

   * ss

   

5. sa




