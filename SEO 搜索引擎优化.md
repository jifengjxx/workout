> 参考链接
>
> http://uxc.360.cn/archives/984.html
>
> http://seokol.com/shuo/80.html

# # 简介

SEO（Search Engine Optimization），就是传说中的搜索引擎优化，是指为了增加网页在搜索引擎自然搜索结果中的收录数量以及提升排序位置而做的优化行为。这是一门说来简单，但操作起来复杂的技术，只可意会，不可言传。作为一名前端工程师，不需要精通SEO，但必须要了解它。SEO有一条不变的准则就是它永远都在变，因为没有一成不变的优化方案可供大家套用。但我们仍然可以发现一些基础的或是被人们公认的规律来进行网站的SEO。更重要的是我们要有自己的实践，不断发现适合自己行之有效的SEO方法。

从宏观的角度来说，我认为SEO有三条最重要的规律，那就是原创的内容、高质量的外部链接和持之以恒适度的优化。

前端是构建网站中很重要的一个环节，本篇重点从前端的角度来讲解一下SEO的实施方法。前端的工作主要是负责页面的HTML+CSS+JS，优化好这几个方面会为SEO工作打好一个坚实的基础。突出重要内容可以让搜索引擎判断当前页面的重点是什么，提升网站访问速度可以让搜索引擎的蜘蛛顺利、快速、大量的抓取网页内容，所以以下我就着重以突出重要内容和提升网站速度为主来总结一下。

# # 实现

## 1. 网站链接规范

**1.1. 整站URL需统一**

避免出现同一个页面多个链接的形式出现。

```javascript
http://www.xxx.com/
http://www.xxx.com
http://www.xxx.com/index.html
```

这个3个链接搜索殷勤会认为是3个不同的页面，避免这种情况的出现，全站中使用这3种链接中的一个。

**1.2. URL中的链接符只用使用 “-” or “_” 两种**

URL中连接符不能使用“-”、“_”两种之外的符号。因为这可能导致搜索引擎无法正确识别链接。



**1.3. Tag页URL中包含关键词（可以为拼音）**

URL中出现页面关键字利于搜索引擎识别页面主体内容。该关键字可以为中文，也可以为拼音。



**1.4. 控制网站目录层次少于3层**

目录太深的链接，搜索引擎可能抓取不到，尽量将网站结构控制在3层目录以内。



## 2. HTML 源码规范

**2.1. meta信息完善（包含title、keyword、description），突出重要内容**

标准的html头部应该包含title、keyword、description这3个meta信息。这些meta信息是SEO优化必要的基础。

虽然现在搜索对这三项的权重慢慢减小，但还是希望能够合理的写好他们，只写有用的东西，不要在这里写小说，要表达重点。

title：只强调重点即可，重要关键词出现不要超过2次，而且要靠前，每个页面title要有所不同。

keywords：列举出几个重要关键词即可，也不可过分堆砌。

description：把网页内容高度概括到这里，长度要合理，不可过分堆砌关键词，每个页面description要有所不同。



**2.2. 合理使用H1-H6标签**

在页面内合理应用H1-H6标签，能够让页面内容主次结构分明，利于搜索引擎识别页面内容偏重。



**2.3. 整站优先使用伪静态**

伪静态链接能够避免出现重复无效的动态链接。更利于整站链接规范。

如果是动态网页，可以开启伪静态功能，让蜘蛛“误以为”这是静态网页，因为静态网页比较合蜘蛛的胃口，如果url中带有关键词效果更好。

动态地址：
http://www.360.cn/index.php

伪静态地址：
http://www.360.cn/index.html



**2.4. img标签需完善alt属性**

搜索引擎还不能有效的识别出图片的内容，给img添加alt属性就相当于告知搜索引擎图片的内容。从而获取较好的图片排名。



**2.5. 重要内容靠前**

重要的内容html代码放在前面，放在左边。搜索引擎爬虫是从左往右，从上到下进行抓取的，利用布局来实现重要的代码在上面



**2.6. 页面主体内容需静态化到html中**

页面主体内容请静态化到html源码中，不然搜索引擎很可能抓取不到。



**2.7. 页面源代码控制在200K以内**

超过200K的内容将不被百度搜索引擎抓取。



**2.8. 语义化书写HTML代码，符合W3C标准**

对于搜索引擎来说，最直接面对的就是网页HTML代码，如果代码写的语义化，搜索引擎就会很容易的读懂该网页要表达的意思。例如文本模块要有大标题，合理利用h1-h6，列表形式的代码使用ul或ol，重要的文字使用strong等等。总之就是要充分利用各种HTML标签完成他们本职的工作，当然要兼容IE、火狐、Chrome等主流浏览器。
我们来看看著名的禅意花园网站（<http://www.csszengarden.com/>），在没有样式的情况下，代码非常语义化，看起来很工整，加载不同的样式之后可以随心所欲的改变页面外观。



**2.9. 尽量不使用iframe框架**

搜索引擎不会抓取到iframe里的内容，重要内容不要放在框架中。



**2.10. 需要强调的地方可以加上title属性**



**2.11. 提升网站速度**

尽量外链CSS和JS，保证网页代码的整洁，也有利于日后维护。

```html
<link rel="stylesheet" href="css/index.css">
<script src="js/main.js"></script>
```

这样的好处是可以把内容、表现和行为分离开，保证代码整洁的同时也方便维护。



**2.12. CSS放在文件头部，JS放在文件尾部，可使用工具对CSS和JS文件进行压缩，CSS Sprites**

减少HTTP请求。利用CSS Sprites技术可以把网页用到的切片合成到一张图上，这样做既减少了HTTP请求数，又使得样式图片一次加载，避免网页“白”的尴尬。



**2.13. 压缩、格式化代码**

可以在上线前，使用一些工具，把HTML、CSS和JS都压缩、格式化一下，可以减少页面大小。



**2.14. 注释的东西能去掉应该去掉，对搜索引擎更加友好**



## 3. CSS 规范

**3.1. 慎重使用CSS隐藏**

慎重使用 “display：none;  text-indent: -9999px” 等CSS隐藏。过度使用可能会被搜索引擎识别为作弊。



**3.2. 页面文字勿过度使用黑体、粗体、斜体**

过度的使用黑体、粗体、斜体可能会被搜索引擎识别为作弊。



**3.3. 禁用透明色和底色加关键词**

使用颜色作弊的手法来提高关键词密度或者布局和页面不相关的关键词都是作弊行为。



**3.4. 利用CSS截取字符**

如果文字长度过长，可以用样式截取，设置高度，超出的部分隐藏即可。这样做的好处是让文字完整呈现给搜索引擎，同时在表现上也保证了美观。



**3.5. 为图片设置高度和宽度，可提高页面的加载速度。**



**3.6. 重要的地方可以保留文字，有些地方必须用图，但是蜘蛛不会爬img，这时应该设置文本，再用缩进隐藏的方法去掉文字，例如logo的优化就是这样做的。注意隐藏不能用display：none，蜘蛛不会检索display：none的内容，应用这个方法的标签一般是logo，标题等重要信息**



## 4. js 规范

**4.1. 减少http的请求，使页面更快加载**



**4.2. 尽量少的使用JS后加载**

Google对JS抓取支持较好，ajax内容也能够抓取。但是现在国内搜索引擎大多不会抓取JS中的内容。重要链接静态化到html源码中。



# # robots

## 1. robots.txt是什么？

http://www.robotstxt.org/robotstxt.html

搜索引擎通过一种程序robot（又称spider），自动访问互联网上的网页并获取网页信息。

您可以在您的网站中创建一个纯文本文件robots.txt，在这个文件中声明该网站中不想被robot访问的部分，这样，该网站的部分或全部内容就可以不被搜索引擎收录了，或者指定搜索引擎只收录指定的内容。

Robots协议（也称为爬虫协议、机器人协议、蜘蛛程序等）的全称

是“网络爬虫排除标准”（Robots ExclusionProtocol），

网站通过Robots协议告诉搜索引擎哪些页面可以抓取，哪些页面不能抓取。

 

robots.txt文件是一个文本文件。

robots.txt是一个协议，而不是一个命令。

robots.txt是搜索引擎中访问网站的时候要查看的第一个文件。

robots.txt文件告诉蜘蛛程序在服务器上什么文件是可以被查看的。

 

Robots协议是国际互联网界通行的道德规范，基于以下原则建立：

  1、搜索技术应服务于人类，同时尊重信息提供者的意愿，并维护其隐私权；

  2、网站有义务保护其使用者的个人信息和隐私不被侵犯。

 ## 2. robots.txt文件放在哪里?

robots.txt文件应该放在网站根目录下。举例来说，当robots访问一个网站（比如http://www.abc.com）时，首先会检查该网站中是否存在http://www.abc.com/robots.txt这个文件，如果机器人找到这个文件，它就会根据这个文件的内容，来确定它访问权限的范围。

## 3. robots.txt文件的格式

"robots.txt"文件包含一条或更多的记录，这些记录通过空行分开（以CR,CR/NL, or NL作为结束符），每一条记录的格式如下所示：

"*<field>:<optionalspace><value><optionalspace>*"。

在该文件中可以使用#进行注解，具体使用方法和UNIX中的惯例一样。该文件中的记录通常以一行或多行User-agent开始，后面加上若干Disallow行,详细情况如下：

**User-agent: **
该项的值用于描述搜索引擎robot的名字，在"robots.txt"文件中，如果有多条User-agent记录说明有多个robot会受到该协议的限制，对该文件来说，至少要有一条User-agent记录。如果该项的值设为`*`，则该协议对任何机器人均有效，在"robots.txt"文件中，"User-agent：*" 这样的记录只能有一条。

**Disallow :**
该项的值用于描述不希望被访问到的一个URL，这个URL可以是一条完整的路径，也可以是部分的，任何以Disallow 开头的URL均不会被robot访问到。例如"Disallow: /help"对/help.html 和/help/index.html都不允许搜索引擎访问，而"Disallow: /help/"则允许robot访问/help.html，而不能访问/help/index.html。
任何一条Disallow记录为空，说明该网站的所有部分都允许被访问，在"/robots.txt"文件中，至少要有一条Disallow记录。如果"/robots.txt"是一个空文件，则对于所有的搜索引擎robot，该网站都是开放的。

## 4. robots.txt文件用法举例

例1.  禁止所有搜索引擎访问网站的任何部分

```
User-agent: * 
Disallow: /
```

例2. 允许所有的robot访问(或者也可以建一个空文件 "/robots.txt" file)

```
User-agent:* 
Disallow: 
```

例3. 禁止某个搜索引擎的访问

```
User-agent: baiduspider
Disallow: /
```

例4.  允许某个搜索引擎的访问

```
User-agent: Google
Disallow:

User-agent: *
Disallow: /
```

例5. 一个简单例子，在这个例子中，该网站有三个目录对搜索引擎的访问做了限制，即搜索引擎不会访问这三个目录。需要注意的是对每一个目录必须分开声明，而不要写成 "Disallow: /cgi-bin/ /tmp/"。

User-agent:后的* 具有特殊的含义，代表"any robot"，所以在该文件中不能有"Disallow: /tmp/*" or "Disallow: *.gif"这样的记录出现.

```
User-agent: *
Disallow: /cgi-bin/
Disallow: /tmp/
Disallow: /~joe/
```

> 提示：请注意，仅当您的网站包含不希望被搜索引擎收录的内容时，才需要使用robots.txt文件。如果您希望搜索引擎收录网站上所有内容，请勿建立robots.txt文件或者创建一个内容为空的robots.txt文件。

























