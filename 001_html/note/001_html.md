## 笔记：

#### 常用的浏览器

1. IE、火狐（Firefox）、谷歌（Chrome）、Safari和Opera等。


#### 浏览器内核（理解）

1. 浏览器内核又可以分成两部分：渲染引擎 和 JS 引擎。

2. 渲染引擎 它负责取得网页的内容（HTML、XML、图像等等）、整理讯息（例如加入 CSS 等），以及计算网页的显示方式，然后会输出至显示器或打印机。浏览器的内核的不同对于网页的语法解释会有不同，所以渲染的效果也不相同。

3. JS 引擎 则是解析 Javascript 语言，执行 javascript语言来实现网页的动态效果。

4. 最开始渲染引擎和 JS 引擎并没有区分的很明确，后来 JS 引擎越来越独立，内核就倾向于只指渲染引擎。常见的浏览器内核可以分这四种：Trident、Gecko、Blink、Webkit。

```
> Trident(IE内核)

代表： IE、傲游、世界之窗浏览器、Avant、腾讯TT、猎豹安全浏览器、360极速浏览器、百度浏览器等。

> Gecko(firefox) 

Gecko(Firefox 内核)： Mozilla FireFox(火狐浏览器) 

> webkit(Safari)  

 代表浏览器：傲游浏览器3、 Apple Safari (Win/Mac/iPhone/iPad)、Symbian手机浏览器、Android 默认浏览器。

> Chromium/Blink(chrome) 

大部分国产浏览器最新版都采用Blink内核。二次开发

> Presto(Opera) 
```

#### Web 标准的好处
1. 让Web的发展前景更广阔 
2. 内容能被更广泛的设备访问 
3. 更容易被搜寻引擎搜索 
4. 降低网站流量费用 
5. 使网站更易于维护 
6. 提高页面浏览速度



#### HTML

* HTML 指的是超文本标记语言 (Hyper Text Markup Language)
* HTML 不是一种编程语言，而是一种标记语言 (markup language)
* 标记语言是一套标记标签 (markup tag)

> 总结：HTML 作用就是用标记标签来描述网页，把网页内容在浏览器中展示出来。

```
HTML标签  -- 根标签
head标签  -- 文档的头部
title标签 -- 文档的标题
body标签  -- 文档的主体 
```
```
HTML标签分类
1. 双标签 <html></html>
2. 单标签 <br />
```
```
HTML标签关系
1. 嵌套关系 <head><title></title></head>
2. 并列关系 
	<head></head>
	<body></body>
```

```
文档类型<!DOCTYPE>
<!DOCTYPE html> 
<!DOCTYPE> 标签位于文档的最前面，用于向浏览器说明当前文档使用哪种 HTML 或 XHTML 标准规范，必需在开头处使用<!DOCTYPE>标签为所有的XHTML文档指定XHTML版本和类型，只有这样浏览器才能按指定的文档类型进行解析。

注意：  一些老网站可能用的还是老版本的文档类型比如 XHTML之类的，但是我们学的是HTML5,而且HTML5的文档类型兼容很好(向下兼容的原则)
```
```
字符集
<meta charset="UTF-8" />
utf-8是目前最常用的字符集编码方式，常用的字符集编码方式还有gbk和gb2312。
gb2312 简单中文  包括6763个汉字
BIG5   繁体中文 港澳台等用
GBK包含全部中文字符    是GB2312的扩展，加入对繁体字的支持，兼容GB2312
UTF-8则包含全世界所有国家需要用到的字符
```

#### HTML标签的语义化
1. 方便代码的阅读和维护
2. 同时让浏览器或是网络爬虫可以很好地解析，从而更好分析其中的内容 
3. 使用语义化标签会具有更好地搜索引擎优化 

#### HTML常用标签
##### 排版标签
###### 标题标签

```
 <h1>、<h2>、<h3>、<h4>、<h5>和<h6>
```

###### 段落标签
```
<p>文本</p>
```
###### 水平线标签
```
<hr />
```
###### 换行标签
```
<br />
```
###### div span标签
```
<div></div> <span></span>
```
##### 文本格式化标签

|标签（后面的语义更强烈）|显示效果|
|:--: |:--:|
|`<b></b>和<strong></strong>` | 粗体 显示 |
|`<i></i>和<em></em>` | 斜体 显示 |
|`<s></s>和<del></del>` | 加删除线 显示 |
| `<u></u>和<del></del>` | 加下划线 显示 |

##### 标签属性
```
<标签名 属性1="属性值1" 属性2="属性值2" …> 内容 </标签名>

1.标签可以拥有多个属性，必须写在开始标签中，位于标签名后面。
2.属性之间不分先后顺序，标签名与属性、属性与属性之间均以空格分开。
3.任何标签的属性都有默认值，省略该属性则取默认值。
采取  键值对 的格式   key="value"  的格式  
```
##### 图像标签img
```
<img src="图像URL" />
```

|属性|属性值|描述|
|:--:|:--:|:--:|
|src|URL|图像的路径|
|alt|文本|图像不能显示时的替换文本|
|title|文本|鼠标悬停时显示的内容|
|width|像素|设置图像的宽度|
|height|像素|设置图像的高度|
|border|数字|设置图像边框额宽度|

##### 链接标签
```
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>

href：用于指定链接目标的url地址，当为标签应用href属性时，它就具有了超链接的功能。 

target：用于指定链接页面的打开方式，其取值有_self和_blank两种，其中_self为默认值，_blank为在新窗口中打开方式。

如果当时没有确定链接目标时，通常将链接标签的href属性值定义为“#”(即href="#")，表示该链接暂时为一个空链接。
```

##### 锚点定位 
通过创建锚点链接，用户能够快速定位到目标内容。
创建锚点链接分为两步：
```
1.使用<a href="#id名">链接文本</a>创建链接文本（被点击的）
  <a href="#two">   

2.使用相应的id名标注跳转目标的位置。
  <h3 id="two">第2集</h3> 
```

##### base 标签
```
base 写到  <head>  </head>  之间
把所有的连接 都默认添加 target="_blank"
```

##### 特殊字符标签 
|特殊字符|描述|字符代码|
|:--:|:--:|:--:|
|&nbsp;|空格符|`&nbsp;`|
|&lt;|小于号|`&lt;`|
|&gt;|大于号|`&gt;`|
|&amp;|和号|`&amp;`|
|&yen;|人民币|`&yen;`|
|&copy;|版权|`&copy;`|
|&reg;|注册商标|`&reg;`|
|&deg;|摄氏度|`&deg;`|
|&plusmn;|正负号|`&plusmn;`|
|&times;|乘号|`&times;`|
|&divide;|除号|`&divide;`|
|&sup2;|上标2|`&sup2;`|
|&sup3;|上标3|`&sup3;`|

##### 注释标签
```
 <!-- 注释语句 -->
```

#### 路径
```
1. 相对路径
* 图像文件和HTML文件位于同一文件夹：只需输入图像文件的名称即可，如<img src="logo.gif" >。
* 图像文件位于HTML文件的下一级文件夹：输入文件夹名和文件名，之间用“/”隔开，如<img src="img/img01/logo.gif" >。
* 图像文件位于HTML文件的上一级文件夹：在文件名之前加入“../” ，如果是上两级，则需要使用 “../ ../”，以此类推，如<img src="../logo.gif" >。


2. 绝对路径
```

#### 列表标签
##### 无序列表ul
```
<ul>
  <li>列表项1</li>
  <li>列表项2</li>
  <li>列表项3</li>
  ......
</ul>

注意：
1. <ul></ul>中只能嵌套<li></li>
2. <li>与</li>之间相当于一个容器，可以容纳所有元素。
```

##### 有序列表 ol 
```
<ol>
  <li>列表项1</li>
  <li>列表项2</li>
  <li>列表项3</li>
  ......
</ol>
```

##### 自定义列表
```
<dl>
  <dt>名词1</dt>
  <dd>名词1解释1</dd>
  <dd>名词1解释2</dd>
  ...
  <dt>名词2</dt>
  <dd>名词2解释1</dd>
  <dd>名词2解释2</dd>
  ...
</dl>
```


### 笔记
#### 表格 table
##### 创建表格
```
<table>
  <tr>
    <td>单元格内的文字</td>
    ...
  </tr>
  ...
</table>
```
```
1.table用于定义一个表格。
2.tr 用于定义表格中的一行
3.td 用于定义表格中的单元格
注意：
<tr></tr>中只能嵌套<td></td>
<td></td>标签，他就像一个容器，可以容纳所有的元素
```
##### 表格属性
|属性名|含义|常用属性值|
|:--:|:--:|:--:|
|border|设置表格边框|像素值|
|cellspacing|设置单元格与单元格边框之间的空白间距|像素值|
|cellspadding|设置单元格内容与单元格边框之间的空白间距|像素值|
|width|设置表格宽度|像素值|
|height|设置表格高度|像素值|
|align|设置表格在网页中的水平对齐方式|left、right、center|
三参为0    border  cellpadding  cellspacing  为  0

##### 表头标签
```
<th></th>
```

##### 表格结构
```
<thead></thead>:定义表格头部
<tbody></tbody>:定义表格主体
```

##### 表格标题
```
caption 定义表格标题
<table>
	<caption>我是表格标题</caption>
</table>
```

##### 合并单元格
```
跨行合并：rowspan   跨列合并：colspan

合并的顺序：先上后下，先左后右
```

#### 表单标签
<table align="center">
    <tr>
    	<th>属性</th>	
        <th>属性值</th>	
        <th>描述</th>	
    </tr>
    <tr>
    	<td rowspan="9">type</td>
        <td>text</td>
        <td>单行文本输入框</td>
    </tr>
    <tr>
    	<td>password</td>
        <td>密码输入框</td>
    </tr>
    <tr>
    	<td>radio</td>
        <td>单选按钮</td>
    </tr>
    <tr>
    	<td>checkbox</td>
        <td>复选框</td>
    </tr>
    <tr>
    	<td>button</td>
        <td>普通按钮</td>
    </tr>
    <tr>
    	<td>submit</td>
        <td>提交按钮</td>
    </tr>
    <tr>
    	<td>reset</td>
        <td>重置按钮</td>
    </tr>
    <tr>
    	<td>image</td>
        <td>图像形式的提交按钮</td>
    </tr>
    <tr>
    	<td>file</td>
        <td>文件域</td>
    </tr>
    <tr>
    	<td>name</td>
        <td>用户自定义</td>
        <td>控件名称</td>
    </tr>
    <tr>
    	<td>value</td>
        <td>用户自定义</td>
        <td>input控件的默认文本值</td>
    </tr>
    <tr>
    	<td>checked</td>
        <td>checked</td>
        <td>定义选择控件默认被选中的项</td>
    </tr>
    <tr>
    	<td>maxlength</td>
        <td>正整数</td>
        <td>控件允许输入的最多字符数</td>
    </tr>
</table>



##### label标签

```
<label for="male">Male</label>
<input id="male" type="radio" name="sex"  value="male">
```

##### textarea控件（文本域）
```
<textarea cols="每行中的字符数" rows="显示的行数">
  文本内容 不支持富文本
</textarea>
```

##### 下拉菜单
```
<select>
  <option value="" selected="selected">选项1</option>
  <option value="">选项2</option>
  <option value="">选项3</option>
  ...
</select>
```

##### 表单域
```
<form action="url地址" method="提交方式" name="表单名称">
  各种表单控件
</form>

1. Action
在表单收集到信息后，需要将信息传递给服务器进行处理，action属性用于指定接收并处理表单数据的服务器程序的url地址。
2. method
用于设置表单数据的提交方式，其取值为get或post。
3. name
用于指定表单的名称，以区分同一个页面中的多个表单。
```

### 查文档

经常查阅文档是一个非常好的学习习惯。

W3C :  http://www.w3school.com.cn/

MDN: https://developer.mozilla.org/zh-CN/