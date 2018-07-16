# Mo-Web
总结的一套常用网页写作模板样式，包括一些布局，特效等。持续更新。

[TOC]

## 基本样式html+css

**html:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!--************************************************************************* */
    /*                                                     O - /                  */
    /*                                                        /                   */
    /*   from moban.html                                 .::::.       .::::.      */
    /*                                                  +:+ +:+      +:+  +:+     */
    /*   By: MoFeioO <mofeioo@qq.com>                  +:+   +:+    +:+    +:+    */
    /*                                                #+#     #+#  #+#      #+#   */
    /*   Created: 2018/07/07 15:25:49 by MoFeioO     #+#       #+##+#        #+#  */
    /*   Updated: 2018/07/07 15:25:49 by MoFeioO    ###         ####          ### */
    /*                                                             /              */
    /*                                                      FEI - /               */
    /* ************************************************************************* -->
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="renderer" content="webkit">
    <!-- <link rel="stylesheet" type="text/css" href="css/style.css"> -->
    <link rel="stylesheet" type="text/css" href="./css/moban.css">
    <!-- <script src="https://cdn.bootcss.com/jquery/1.10.2/jquery.min.js"></script> -->
    <title>A Web Page</title>
</head>

<body>
    <!-- header start -->
    <div class="header clearfix layout">
        <!-- header other msg -->
        <div class="msg"></div>

        <!-- function start  搜索 输入框等-->
        <div class="function"></div>
        <!-- function end  搜索 输入框等-->


        <!-- nav start -->
        <ul class="nav">
            <li>
                <a href="#">首页</a>
            </li>
           
        </ul>
        <!-- nav end -->
    </div>
    <!-- header end -->

    <!-- banner end-->
    <div class="banner">
        </div>

    </div>
    <!-- banner end -->

    <!-- main start -->
    <div class="main">
        <!-- side start -->
        <div class="sidebar"></div>
        <!-- side  end-->

        <!-- news start  -->
        <div class="news layout"></div>
        <!-- new start  -->

        <!-- case start 案例 -->
        <div class="case layout"></div>
        <!-- case end 案例 -->

    </div>
    <!-- mian end -->

    <!-- footer start -->
    <div class="footer">
      
        <!-- copyright message -->
        <p class="copyright">Copyright &copy; 20-20 All Rights Reserved. 备案号：备号</p>
    </div>
    <!-- footer end -->
</body>
<!-- <script src="script.js"></script> -->

</html>
```



**css:**


```css
/* ************************************************************************** */
/*                                                     O - /                  */
/*                                                        /                   */
/*   moban.css                                       .::::.       .::::.      */
/*                                                  +:+ +:+      +:+  +:+     */
/*   By: MoFeioO <mofeioo@qq.com>                  +:+   +:+    +:+    +:+    */
/*                                                #+#     #+#  #+#      #+#   */
/*   Created: 2018/07/16 22:20:23 by MoFeioO     #+#       #+##+#        #+#  */
/*   Updated: 2018/07/16 22:20:23 by MoFeioO    ###         ####          ### */
/*                                                             /              */
/*                                                      FEI - /               */
/* ************************************************************************** */
/* 清除浏览器默认样式 start */

html,
body,
ul,
li,
ol,
dl,
dd,
dt,
p,
h1,
h2,
h3,
h4,
h5,
h6,
form,
fieldset,
legend,
img {
    margin: 0;
    padding: 0;
}

fieldset,
img {
    border: none;
}

html,
body {
    /* height:100%; 
    */
    /*用来三栏两栏布局*/
    background-color: #f4f4f4;
    /*同一字体 */
    color: #3C3C3C;
    font: 12px/1 Tahoma, Helvetica, Arial, "\5b8b\4f53", sans-serif;
    /*同一字体 */
}

ol,
ul {
    list-style: none;
}

h1,
h2,
h3,
h4,
h5,
h6 {
    font-size: 100%;
    font-weight: normal;
}

h1 {
    font-size: 30px;
}

h2 {
    font-size: 26px;
}

h3 {
    font-size: 22px;
}

h4 {
    font-size: 18px;
}

h5 {
    font-size: 14px;
}

table {
    border-collapse: collapse;
    /* 合并边框 */
    border-spacing: 0;
    /*单元格间距 */
}

img {
    display: block;
}

a {
    color: #000;
    text-decoration: none;
}

/* 解决高度塌陷 */

.clearfix:after {
    content: ".";
    display: block;
    height: 0;
    visibility: hidden;
    clear: both;
}

/* 清除浏览器默认样式 end */

/* 布局 居中显示 */

.layout {
    width: 1200px;
    margin: 0 auto;
    /* overflow: hidden; */
}

```



## 常用属性设置

### 不同边框

```css
/* 设置不同边框 */

.setbd {
    border-width: 0px 0px 0px 0px;
    border-style: solid;
    border-color: #fff;
    border: px solid #fff;
    border-left: 0px solid #fff;
    border-top: 0px solid #fff;
    border-right: 0px solid #fff;
    border-bottom: 0px solid #fff;
}
```



### 设置背景

```css
.setbg {
    /* 背景位置 */
    background-position: center center;
    background-position-x: 0px;
    background-position-y: 0px;
    background-image: url();
    /* 背景连写 */
    background: #fff url() center center no-repeat;
}
```



### 图片文字居中

```css 

.lb_center {
    display: inline-block;
    vertical-align: middle;
    text-align: center;
    line-height: px;
}
```

### 一行等号

```css
.show_aline {
    width: px;
    /*必须有宽度 */
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
}
```



### 定位设置垂直居中

```css
/* 定位设置垂直居中 */

.b_center {
    /* 高宽随意 */
    width: 200px;
    height: 200px;
    background: indianred;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    /* 必须知道高宽 */
    width: 200px;
    height: 200px;
    position: absolute;
    left: 50%;
    top: 50%;
    margin: -100px 0 0 -100px;
    /*高一半 0 0 宽一半 */
    /* 高宽随意 */
    width: 200px;
    height: 200px;
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    margin: auto;
}
```

## 头部

### 导航

**html**

```html
  <!-- nav start -->
        <ul class="nav">
            <li>
                <a href="#">首页</a>
            </li>
            <li>
                <a href="#">首页</a>
            </li>
        </ul>
    <!-- nav end -->
```



```css
/* 导航栏设置 */

.nav {
    height: 80px;
    width: 800px;
    float: left;
}

.nav li {
    float: left;
}

.nav li a {
    /* color:; */
    display: block;
    width: 100px;
    height: 80px;
    line-height: 80px;
    text-align: center;
    font-size: 20px;
    /* background: saddlebrown; */
}

.nav li a:hover {
    color: aqua;
}

/* 导航栏结束 */
```



## Banner

### 简单无轮播

```css

/* banner区域 */

.banner {
    width: 1000px;
    /* height: 400px; */
    background: black url() no-repeat;
    margin: 0 auto;
}

/* banner区域 结束 */
```



### 背景图方式（轮播）

**html**

```html
    <!-- banner end-->
    <div class="banner">
        <div class="item">
            <ul class="clearfix">
                <li></li>
                <li></li>
                <li></li>
            </ul>
            <div class="prev"></div>
            <div class="next"></div>
        </div>
    </div>
    <!-- banner end -->
```

**css**

```css
/* banner区域 */

.banner {
    width: 1000px;
    /* height: 400px; */
    background: black url() no-repeat;
    margin: 0 auto;
}

/* 设置轮播图 */
.banner .item {
    width: 1000px;
    height: 400px;
    background: url("") no-repeat;
    background-size: 100% 100%; 
    position: relative;
}

/* 切换的小按钮 */
.banner .item ul {
    position: absolute;
    left: 50%;
    bottom: 10%;
    transform: translateX(-50%);
    /* 在父元素水平居中 */
}

/* 每个小按钮样式 */
.banner .item li {
    width: 20px;
    height: 20px;
    float: left;
    /* 背景图方式 */
    /* background: url("") left top no-repeat; */
    /* css自定义样式 */
    background-color: seashell;
    border-radius: 50%;
    margin: 0 5px;
}

/* 小按钮放上去的样式 */
.banner .item li:hover {
    /* background: url("") left top no-repeat; */
    background-color: skyblue;
}

/* 前后切换按钮 */
.prev {
    width: 30px;
    height: 70px;
    background: transparent url() center center no-repeat;
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    border-radius: 0 5px 5px 0;
}

.next {
    width: 30px;
    height: 70px;
    background: transparent url() center center no-repeat;
    position: absolute;
    top: 50%;
    right: 0;
    transform: translateY(-50%);
    border-radius: 5px 0 0 5px;
}

.prev:hover,
.next:hover {
    background-color: rgba(0, 0, 0, 0.5);
}
```



### 插入图片式（轮播）

**html**

```html
    <!-- banner end-->
    <div class="banner">
        <div class="item">
            <img src="./images/demo1.jpg" alt="轮播图">
            <img src="./images/demo1.jpg" alt="轮播图">
            <img src="./images/demo1.jpg" alt="轮播图">
            <ul class="clearfix">
                <li></li>
                <li></li>
                <li></li>
            </ul>
            <div class="prev"></div>
            <div class="next"></div>
        </div>

    </div>
    <!-- banner end -->
```

**css**

```css
/* 设置轮播图 */

.banner .item {
    width: 1000px;
    height: 400px;
    position: relative;
}

.banner .item img {
    width: 100%;
    height: 100%;
}

/* 切换的小按钮 */
.banner .item ul {
    position: absolute;
    left: 50%;
    bottom: 10%;
    transform: translateX(-50%);
    /* 在父元素水平居中 */
}

/* 每个小按钮样式 */
.banner .item li {
    width: 20px;
    height: 20px;
    float: left;
    /* 背景图方式 */
    /* background: url("") left top no-repeat; */
    /* css自定义样式 */
    background-color: seashell;
    border-radius: 50%;
    margin: 0 5px;
}

/* 小按钮放上去的样式 */

.banner .item li:hover {
    /* background: url("") left top no-repeat; */
    background-color: skyblue;
}

/* 前后切换按钮 */

.prev {
    width: 30px;
    height: 70px;
    background: transparent url() center center no-repeat;
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    border-radius: 0 5px 5px 0;
}

.next {
    width: 30px;
    height: 70px;
    background: transparent url() center center no-repeat;
    position: absolute;
    top: 50%;
    right: 0;
    transform: translateY(-50%);
    border-radius: 5px 0 0 5px;
}

.prev:hover,
.next:hover {
    background-color: rgba(0, 0, 0, 0.5);
}
/*轮播图结束*/
```



## 内容页

### 常用分块起名

```html
        <!-- side start -->
        <div class="sidebar"></div>
        <!-- side  end-->

        <!-- hot start 热点 -->
        <div class="hot layout"></div>
        <!-- hot end 热点 -->

        <!-- news start  -->
        <div class="news layout"></div>
        <!-- new start  -->

        <!-- case start 案例 -->
        <div class="case layout"></div>
        <!-- case end 案例 -->

        <!-- top start 排名 -->
        <div class="top"></div>
        <!-- top end 排名 -->

        <!-- product start 产品 -->
        <div class="product"></div>
        <!-- product end 产品 -->

        <!-- advantage start 建议 -->
        <div class="advantage"></div>
        <!-- advantage end 建议 -->

        <!-- introduction start 介绍 -->
        <div class="introduction"></div>
        <!-- introduction end 介绍 -->
```



### 版块标题

#### 简单大标题（居中）



#### 标题+图标+more



**html**	

```html
        <!-- title start -->
        <!-- 每个版块的标题 一般不用浮动 -->
        <div class="title">
            <h3>标题</h3>
            <a class="more">more</a>
        </div>
        <!-- title start -->
```

**css**

```css
/* 每个版块的标题样式 */

.title {
    height: 50px;
    /*宽碎父元素 */
}

.title h3 {
    height: 100%;
    /* 用来设置左边的小图片 */
    padding-left: 20px;
    background: url("") left center no-repeat;
}

.title a {
    font-size: 14px;
    float: right;
    color: #3C3C3C;
}

/*标题结束*/
```



#### 大标题+文字

**html**

```html
        <!-- title start -->
        <!-- 每个版块的标题 一般不用浮动 -->
        <div class="title">
            <h2>标题</h2>
            <p>文字</p>
        </div>
        <!-- title start -->
```

**css**

```css
/* 每个版块的标题样式 */

.title {
    height: 50px;
   	text-align:center;
}

.title h3 {
	color:;
    font-size:;
}

.title p{
    color:;
    font-size;
}
```
###　子版块图文展示

**html**

```html
        <!-- 案例展示  浮动布局  strat -->
        <dl>
            <dt>
                <img src="#" alt="img">
            </dt>
            <dd>
                <h4></h4>
                <p></p>
            </dd>
        </dl>
        <!-- 案例展示  浮动布局  end -->
```

**css**

```css
/* 案例item  图 文 父元素需bfc   */
/*不设置浮动就是上图下文*/
dl {
    float: left;
    width: px;
    height: px;
}

dt {
    /* float: left; */
}

dt img {
    width: px;
    height: px;
}

dd {
    /* float: right */
}

dd h4 {}

dd p {
    font-size: px;
}

/* 设置中间案例的间距 */

/* dl:nth-child(){
    margin: 0 px;
} */
```


###　友情链接等

**html**

```html
        <!-- link start 更多链接 -->
        <div class="link">
            <!--插入图片方式 -->
            <!-- <li><a href="#"><img src="#" alt=""></a></li> -->

            <!-- 背景整合方式 -->
            <li>
                <a href="#"></a>
            </li>
        </div>
        <!-- link end 更多链接 -->
```

**css**

```css

```


## 底部

### 更多链接

**html**

```html
      <!-- link  start 简单的n排链接导航-->
        <ul class="link_more clearfix">
            <li>
                <h5>标题</h5>
                <a href="#"></a>
                <a href="#"></a>
                <a href="#"></a>
            </li>
        </ul>
        <!-- link  start 简单的n排链接导航-->
```

**css**

```css
/* 底部更多链接 */
.link_more {
    float: left;
}

.link_more li {
    float: left;
    width: px;
}

.link_more h5 {
    color: ;
    margin: px 0;
}

.link_more a{
    display: block;
    font-size: px;
    color: ;
    margin-bottom: px;

}
/* 底部更多链接结束 */
```




## 边侧快捷按钮

**html**

```html
        <div class="side_btn">
            <a class="erweima" href="">
                <img src="./images/erweima.jpg" alt="二维码">
            </a>
            <a class="totop" href="#"></a>
        </div>
```

**css**

```css
/* 右侧的的小功能模块 如回顶部 */

.side_btn {
    position: fixed;
    right: 5%;
    bottom: 10%;
    border: 1px solid grey;
    border-radius: 2px;
}

.side_btn a {
    display: block;
}

/* 二维码按钮*/

.erweima {
    background: url("../images/ew_icon1.png") center center no-repeat;
    width: 50px;
    height: 50px;
    position: relative;
    overflow: hidden;
    border-bottom: 1px solid grey;
}

.erweima:hover {
    overflow: unset;
    background-image: url("../images/ew_icon2.png");
}

/* 二维码图片 */

.erweima img {
    position: absolute;
    left: -101px;
    top: 50%;
    width: 100px;
    height: 100px;
    transform: translateY(-50%);
}

/* 回到顶部 */

.totop {
    background: url("../images/up1.png") center center no-repeat;
    width: 50px;
    height: 50px;
}

.totop:hover {
    background-image: url("../images/up2.png");
}

/* 右侧按钮区域结束 */
```
