* PhtotShop快捷键
ctrl + n 新建
ctrl + o 打开
v 移动
u 矩形工具
ctrl + left-mouse 选择图层
alt + 方向键（复制单个图片）/ctrl + j （复制图层）
ctrl + t 变形
ctrl + "+" 放大
ctrl + g 分组
ctrl + shift + n 新建图层
alt + del 前景色
ctrl + del 背景色
ctrl + alt + z 后退多步
ctrl + r 标尺
ctrl + h 隐藏辅助线
shift + alt 等比缩放
g 渐变
ctrl+j / alt 复制图案
alt + v + e 新建参考线
alt + shift 画正圆
ctrl + d 取消虚线框
ctrl + alt + c 调画布大小
调背景 -- 图层蒙版
b 画笔工具
x 前景色和后景色切换
ctrl+shift + i 反选
s 仿制图章
ctrl + u 调整色相
ctrl + m 调曲线
钢笔工具：
p 抠图
摁住alt 点中间原点一下，去除一侧轴线
摁ctrl 调轴线，归位
ctrl + 回车  路径改选区
ctrl + j 复制选区
ctrl + shift + alt + e 合并图层
ctrl + shift + alt + t 复制旋转
ctrl + e 向下合层
选择工具：a
套索工具：L
魔棒工具：W
历史纪录画笔：Y
吸管工具：I
裁剪工具：C
ctrl + shift + alt + s   :储存为web 格式
橡皮擦： E
修补工具： J
直接拖走
剪贴蒙版 ：上色，上图。例如：画一个矩形，填充，把一张图片做成剪贴蒙版，图片自动填充进矩形中，可随意拖动。
图层蒙版 ： （画笔）前景色和背景色，相同则显示，相反则隐藏。例如：黑色隐藏，白色显示。***选在蒙版上操作。
ctrl + shift + t :按角度旋转
关闭ps界面：ctrl + w
取消当前命令：Esc
工具选项版：Enter
选项版调整：Shift+Tab

页面：自适应。
（宽度width、字号font-size、行高line-height、边距margin,psdding 不用px做单位了）

自适应布局： 目标元素 /（除以）  上下文元素（父级）= 百分比   （包括宽度、字号......）
ctrl+F 在sublime代码中搜素同一个名称

单位：em 相对单位        默认网页字号 16px = 1em  例如：在body里设置的字号是多少（eg：12px），默认1em = 12px
                                                                                        在body里设置的字号是多少（eg：80%），默认1em = 80%*16px=12.8px 

字号：自身的字号除以父级的字号
行高：行高/字号（自身的行高除以自身的字号）
line-height:20   （不写单位，代表20倍于字号）  
边距：自身的边距除以父级的宽度。

弹性图片：max-width:100%;


/* 媒体查询 断点从大到小写 */
@media screen and (min-width: 1200px){
    body{background-color:green;}
}
@media screen and (min-width: 992px) and (max-width:1200px){
    body{background-color:lightblue;}
}
@media screen and (min-width: 768px) and (max-width: 992px){
    body{background-color: lightgreen;}
}
@media screen and (max-width: 768px){
    body{background-color:pink;}
}


display:none;   隐藏                      display:block;   显示




实现图片效果：

nav ul{display:table-row;/* 转换成表格的行 */}
select{display:none;}
@media screen and (max-width: 768px){
    article>a{
        display: block;
        text-align: center;
        margin-bottom: 10%;
    }
    aside,article{
        float: none;
        width: 94%;
        margin: 0 auto;
    }
    nav{
        background:none;
    }
    nav ul{
        display: none;
    }
    select{display:block;}
}
动画：
@keyframes name{
    from{transform:rotate(0deg);}
    to{transform:rotate(360deg);}
}
引用:animation:name 5s;
@keyframe  规定动画
animation  所有动画属性的简写属性，除了animation-state属性
animation-name 规定@keyframes动画的名称
animation-duration 规定动画完成一个周期所花费的秒或毫秒，默认是0
animation-timing-function 规定动画的速度曲线，默认是ease
animation-delay 规定动画何时开始 默认是0
animation-iteration-count 规定动画被播放的次数，默认是1
animation-iteration-count:n\infinite
n定义动画播放次数的数值    infinite规定动画应该无限次播放
animation-direction 规定动画是否在下一周期逆向地播放，默认是normal
normal默认值，动画应该正常播放   alternate动画应该轮流反向播放
animation-play-state 规定动画是否正在运行或暂停，默认是running
pused  规定动画已暂停
animation-fill-mode:none\forward\backwards\both;
none 不改变默认行为
forwards 当动画完成后，保持最后一个属性值（在最后一个关键帧中定义）
backwards 在animation-delay所指定的一段时间内，在动画显示之前，应用开始属性值
缩写从名字开始往下排，有就写，没有不写。
animation: round  5s linear 1s infinite;/*（规则） 名字，运行时间，曲线，延迟时间，状态 */
表格：(tr代表行   td代表列)
    <table>(表格)
        <tr>（行）
            <td>（列）
            </td>
        </tr>
        <tr>（行）
            <td>（列）
            </td>
        </tr>
    </table>
例如：
nav{
    width: 960px;
    margin-left: -10px;
    background:linear-gradient(#fff,#e3e3e3);
    display: table;/* 转换成表格，可自适应宽度 */
}
nav ul{display:table-row;/* 转换成表格的行 */}
nav ul li{
    display:table-cell;
    text-align: center;/* 转换成表格的列 */
}
响应式：
@font-face规则：
@font-face{
    font-family:myFirstFont;
    src:url(‘Sanantion’)
前端页面（三部分）： 
            1，结构层
            Html代码
             2，表示层
            css层叠样式表
             3，行为层
            Js脚本
body里写结构（html）
style里写样式（css）,在head里，最好写在title下面
sublime 快捷键
所有的html代码都在body里写
ctrl + n : 新建
ctrl + o : 打开
Tab : 显示闭合标签
！+ Tab : 初始化代码
W3C掌握：
<article> : 定义文章
<aside> : (侧边栏）定义页面内容之外的内容
<body> : 定义文档的主体
<footer> : 定义section或page的页脚
<header> : 定义section或page的页脚
<section> : 定义section  (section 部分)
<nav> : 定义导航链接
<div> : 定义文档中的节 （盒子）
写完标签 + Tab :自动加上尖括号
简化写法：.wrap+header+.main + footer
.+ 自定义名字（加.会自动附上名字）
下一级用>    同级用+     ^返回上一层
css层叠样式表
    1 内部样式
    2 外部样式
    3 内联样式 （行内样式）
<img>引入图片
ctrl + F3 :同一个全选中
ctrl + <或> : 选中部分上移或下移
ctrl + [或]  :左移或右移
ctrl + 滚轮 : 放大或缩小
标签 div{样式}:表示标签下面的所有div都用这个样式。
border-top:4px solid white;
/* 上边框：4像素   实线  白色*/
margin: 0 auto; : 水平居中
float:left; :向左浮动
background-image : 背景图
background-repeat:no-repeat; :背景不重复
background-position:50% 29%;  :背景图位置
background-position:center center;  : 背景图居中
background-size:100px 50px;  : 背景图尺寸(按照容器的宽高而定)
background-size:cover; : 将背景图像扩展至足够大，以使背景图像完全覆盖背景区域。背景图像的某些部分也许无法显示在背景定位区域中。
background-size:contain; :按照容器的宽高(等比放大)
快捷提示 ：Tab
不怎么替换的图 : 用背景图  例如logo 或者 购物车、登录的小图标
可更换的图 ：用插图img  例如轮播图、新闻图
选择器   class选择器（.xxx） 标签选择器（xxx） 后代选择器E F
文字：
font-size:38px;  :字体大小（字号）
color：#fff;  : 颜色
font-family:"微软雅黑"; ：字体
font-family:"微软雅黑","备用字体";
font-family:"Agency FB","微软雅黑",Sans-serif;  :后备机制，显示"Agency FB"，若没有，则显示"微软雅黑"，若还没有，则显示无衬线的默认字体。
css中五种通用字体类型：Serif 有衬线的字体
               Sans-serif 无衬线的字体
h标签：（标题）
font-weight: normal;  //字体加粗:正常
font-weight: bold;    //定义粗体字符
font-weight: bolder;  //定义更粗的字体
font-weight: lighter; //定义更细的字符
100 200 300 400 500 600 700 800 900   定义由粗到细的字符。400等同于normal，而700等同于bolder.
h1  必须有一个
h1  尽量一个页面只能有一个
h3  页面中的栏目标题尽量用h3
overflow:hidden;/*溢出:隐藏*/     加在父级上可以清浮动
margin-top:77px;/*上边距:77px*/
<br/>  强制换行
p标签
line-height:30px;  //行高 固定高度（px）或倍数（3）
text-align:center;/*文本居中*/  left/center/right
<i><!-- 倾斜 --></i><b><!-- 加粗 --></b>
PC端：文字最小是12px，默认是16px
font-weight: normal;/*字体加粗:正常*/
text-indent:30px;/*首行缩进*/
给标签一个名字，用名字找到对象写样式
ctrl+Y  :反撤销（撤销多了反撤回来）
padding-top:24px;/*内边距的上边距，盒子会被撑大，要在宽高上减去相应的值*/
background-repeat:repeat重复/no-repeat不重复/repeat-x水平重复/repeat-y垂直重复
.clear{clear:both;}<!-- 清除浮动对下级的影响---清浮动 -->
<div class="clear"></div><!-- 在最后一个浮动元素后加空标签 -->
.clearfix:before,
.clearfix:after {
content: "";
display: block;
clear: both;
visibility: hidden;
line-height: 0;
height: 0;
font-size:0;
}
.clearfix { *zoom:1;}
:after  选择器在被选元素的内容后面插入内容
使用content属性来制定要插入的内容

初始化
html, body, div, span, applet, object, iframe,
    h1, h2, h3, h4, h5, h6, p, blockquote, pre,
    a, abbr, acronym, address, big, cite, code,
    del, dfn, em, font, img, ins, kbd, q, s, samp,
    small, strike, strong, sub, sup, tt, var,
    dl, dt, dd, ol, ul, li,
    fieldset, form, label, legend,
    table, caption, tbody, tfoot, thead, tr, th, td {
        margin: 0;
        padding: 0;
        border: 0;
        outline: 0;
        font-weight: inherit;
        font-style: inherit;
        font-size: 100%;
        font-family: inherit;
        vertical-align: baseline;
    }
    .clearfix:before,
    .clearfix:after {
                        content: "";
                        display: block;
                        clear: both;
                        visibility: hidden;
                        line-height: 0;
                        height: 0;
                        font-size:0;
}
.clearfix { *zoom:1;}
position:relative  /*相对定位*/以其自身位置为参照。
position:absolute/*绝对定位*/
position:fixed   /*固定定位*/
z-index:5;    设置元素的堆叠顺序，数值大的在数值小的前面(覆盖)
相对定位 保留原来位置
绝对定位  不保留原来位置
background-origin 属性规定background-position属性相对于什么位置来定位
padding-box:背景图像相对于内边距框来定位
border-box：背景图像相对于边框盒来定位
content-box：背景图像相对于内容框来定位
verticle-align:2px;竖直方向。
cusor  属性规定要显示光标的位置
pointer 光标呈现为指示链接的指针（一只手）
default 默认光标（通常是一个箭头）
move 十字箭头
表单：
input{outline:0;} 去掉默认的边（光标经过变色）
input:focus{border:1px solid red;}让光标经过时的边变红色
vertical-align 属性 设置元素的垂直对齐方式
alt+shift +2/3/4   再开几个页面
 



 

 
<meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no"/>
    <title>OSCARS</title>
    <link rel="stylesheet" type="text/css" href="css/index.css">



@keyframes warning{
    0%{text-shadow: 0 0 0 red;}
    25%{text-shadow: 0 0 20px red;}
    50%{text-shadow: 0 0 0px blue;}
    75%{text-shadow: 0 0 20px blue;}
    100%{text-shadow: 0 0 0px blue;}
}
@-webkit-keyframes warning{
    0%{text-shadow: 0 0 0 red;}
    25%{text-shadow: 0 0 20px red;}
    50%{text-shadow: 0 0 0px blue;}
    75%{text-shadow: 0 0 20px blue;}
    100%{text-shadow: 0 0 0px blue;}
}
@-o-keyframes warning{
    0%{text-shadow: 0 0 0 red;}
    25%{text-shadow: 0 0 20px red;}
    50%{text-shadow: 0 0 0px blue;}
    75%{text-shadow: 0 0 20px blue;}
    100%{text-shadow: 0 0 0px blue;}
}
@-moz-keyframes warning{
    0%{text-shadow: 0 0 0 red;}
    25%{text-shadow: 0 0 20px red;}
    50%{text-shadow: 0 0 0px blue;}
    75%{text-shadow: 0 0 20px blue;}
    100%{text-shadow: 0 0 0px blue;}
}


nav ul li a:hover{
    animation: warning 2s linear 0s infinite;
    -webkit-animation: warning 2s linear 0s infinite;
    -o-animation: warning 2s linear 0s infinite;
    -moz-animation: warning 2s linear 0s infinite;
}
雪碧图
雪碧图：  节省带宽          通过可视窗口调背景图（雪碧图）位置。
总结：

快捷键：ctrl + F 在代码里寻找目标位置
             alt + F3 将代码里所有与鼠标选中相同的元素都选中，可用于同时替换。
1，盒子模型
margin  border   padding   content（正文）
2，定位
  （1） 相对定位   相对于自己原位置
  （2） 绝对定位   a,最近   b,祖先   c,已定位
  （3） 固定定位
3，浮动
    一旦浮动了就要再其父级清浮动（因为其脱离了普通文档流）
（1）文字环绕  将图片浮动（左浮）
 清浮动：a,    空标签      在html的最后一个浮动的div后面加 <div class="clear">
                                    在css加 .clear{clear:both;}
              b,    overflow    
              c,    clearfix
4，选择器
    class    类选择器
    >    子集选择器
    空格     后代选择器  
    ,    群组选择器
    +    相邻兄弟选择器
    # id选择器
    nth-child()
5，自适应布局
        所有固定值（固定布局）替换为百分比（自适应布局）
        目标元素 / 上下文元素 = 百分比
6，响应式（响应式网站）
        技术，媒体查询
        768    992    1200
        三个区间： （1）~768px    手机端    (2) 768~992px   pad竖屏 (3)992~1200px   pad横屏    (4)1200~    pc端        【注意断点页面：768 992 1200】
        固定布局也可以做成响应式，但自适应比固定布局更好更方便实现响应式
        但凡固定布局，轻易不要给宽度，尽量元素包裹（代码里只有最大的宽给百分比，其他给px，在媒体查询里给百分比）
7，过渡
        开始和结束，必须有触发点，过渡写在开始
        transition: all 0.5s linear 0s;
        transition: 名字  执行时间  运动曲线  延迟 ；                  /* transform  2D(不要混)*/
8，动画
        不需要触发
        有开始和结束
 @-moz-keyframes round{
    0%{transform: rotate(0deg);}
    25%{transform: rotate(-20deg);}
    50%{transform: rotate(0deg);}
    75%{transform: rotate(20deg);}
    100%{transform: rotate(0deg);}
}
@keyframes round2{
    0%{transform: rotate(0deg);}
    25%{transform: rotate(20deg);}
    50%{transform: rotate(0deg);}
    75%{transform: rotate(-20deg);}
    100%{transform: rotate(0deg);}
}
@-webkit-keyframes round2{
    0%{transform: rotate(0deg);}
    25%{transform: rotate(20deg);}
    50%{transform: rotate(0deg);}
    75%{transform: rotate(-20deg);}
    100%{transform: rotate(0deg);}
}
@-o-keyframes round2{
     0%{transform: rotate(0deg);}
    25%{transform: rotate(20deg);}
    50%{transform: rotate(0deg);}
    75%{transform: rotate(-20deg);}
    100%{transform: rotate(0deg);}
}
@-moz-keyframes round2{
    0%{transform: rotate(0deg);}
    25%{transform: rotate(20deg);}
    50%{transform: rotate(0deg);}
    75%{transform: rotate(-20deg);}
    100%{transform: rotate(0deg);}
}
规则：
    animation:round2 1s linear 0s 4;        animation:    自定义名字  执行时间  运动曲线  延迟  是否循环或重复；
    -webkit-animation:round2 1s linear 0s 4;
    -o-animation:round2 1s linear 0s 4;
    -moz-animation:round2 1s linear 0s 4;
9，table   
        当找不到规律时选用（不用浮动，给ul宽）
        div {display: table;    /* 转换成表格，可自适应宽度 */}
        ul{display:table-row;    /* 转换成表格的行 */}
        li{display:table-cell;text-align: center;}    /* 转换成表格的列，并居中 */
10，背景渐变
        （1）线性渐变
               background: linear-gradient(#222,#121212);
        （2）镜像渐变
11,雪碧图
          


12,rem
rem 是相对单位，相对于整个body    用于web  app










pc端兼容
注意：IE10及以上注释法失效
css hack主要有三种：IE条件注释法、CSS属性前缀法、选择器前缀法。

IE条件注释法：
        <!--[if lt IE 8]>
        <link rel="stylesheet" href="iehack.css" />
        <![endif]-->
CSS属性前缀法：
body{
    background-color: lightpink;
    background-color: lightblue\0/;        /* \0/ie8专属hack */
    background-color: lightblue\9;        /* \9 ie6/ie7/ie8/ie9/ie10都生效 */
    background-color: lightblue\0;        /* ie8及以上 */
    background-color: lightblue\9\0;    /* ie9/ie10 */
    _background-color: lightblue;        /* ie6 */
    *background-color: lightblue;        /* ie6/ie7 */
}
提升优先级（比id都厉害）：
div{
    width: 300px;
    height: 300px;
    margin: 0 auto;
    background:red !important;   /*!important  提升优先级  但这样放一起ie6不认*/
    background: blue;
}
/*!important  提升优先级  但这样分开放ie6认*/
div{
    width: 300px;
    height: 300px;
    margin: 0 auto;
    background:red !important;/* ie6  ie7&ff */
}
div{
    width: 300px;
    height: 300px;
    margin: 0 auto;
    background: blue;
}

选择器前缀法
body{
    background-color:lightgreen;
}
*html body{        *   前缀只对ie6生效
background-color: red;
}
*+html body{      *+   前缀只对ie7生效
    background-color: pink;
}

/* 选择器前缀 */
*html     *前缀只对IE6生效
*+html     *+前缀只对IE7生效
@media \0screen {body { background: red; }}    /* 只对IE8有效 */
@media \0screen\,screen\9{body { background: blue; }}    /* 只对IE6/7/8有效 */
@media screen\0 {body { background: green; }}     /* 只对IE8/9/10有效 */
@media screen and (min-width:0\0) {body { background: gray; }}     /* 只对IE9/10有效 */
@media screen and (-ms-high-contrast: active), (-ms-high-contrast: none) {body      { background: orange; }}    /*  只对IE10 IE11有效等等 */



H5标签ie8 不识别问题
1.css：article,aside,dialog,footer,header,section,footer,nav,figure,menu{display:block;}
2.Head下面添加：
<!--[if lt IE 9]>
<script>
   (function() {
     if (!
     /*@cc_on!@*/
     0) return;
     var e = "abbr, article, aside, audio, canvas, datalist, details, dialog, eventsource, figure, footer, header, hgroup, mark, menu, meter, nav, output, progress, section, time, video".split(', ');
     var i= e.length;
     while (i--){
         document.createElement(e[i])
     }
})()
</script>
<![endif]-->

老师：
CSS hack主要有三种：IE条件注释法、CSS属性前缀法、选择器前缀法。
<!--  lt是小于 gt是大于 lte是小于等于 gte是不小于 !是不等于 -->
<!--[if IE]>
    你想要执行的代码
<![endif]--> 
<!--[if lt IE 8]>
    你想要执行的代码
<![endif]--> 
<!--[if ! IE 8]>
    你想要执行的代码
<![endif]--> 
²例：  <!--[if ! IE 8]>
        <link rel="stylesheet" href="iehack.css" />
        <![endif]--> 
²<metahttp-equivmetahttp-equiv="x-ua-compatible"content="IE=7"/>
注意： ie10及以上注释法失效。
把这段代码放到<head>里面，在IE8里面的页面解析起来就跟IE7一模一样的了，
²Css属性前缀法
“-″减号是IE6专有的hack
“*″减号是IE6 /IE7的hack
“\9″ IE6/IE7/IE8/IE9/IE10都生效
“\0″ IE8/IE9/IE10都生效，是IE8/9/10的hack
“\9\0″ 只对IE9/IE10生效，是IE9/10的hack
!important   提升优先级
²选择器前缀
*html *前缀只对IE6生效
*+html *+前缀只对IE7生效
@media screen\9{...}只对IE6/7生效
@media \0screen {body { background: red; }}只对IE8有效
@media \0screen\,screen\9{body { background: blue; }}只对IE6/7/8有效
@media screen\0 {body { background: green; }} 只对IE8/9/10有效
@media screen and (min-width:0\0) {body { background: gray; }} 只对IE9/10有效
@media screen and (-ms-high-contrast: active), (-ms-high-contrast: none) {body      { background: orange; }} 只对IE10 IE11有效等等
IE6bug汇总
双边距：一个div盒子如果设置了margin，并且该div设置了float浮动，那么在IE6下便会产生双边距问题：如果设置 float:left 那么左边距会是原来margin的两倍；如果是float:right，那么右边距会是原来margin的两倍。      解决办法：_display: inline
3像素：3像素bug是IE6的一个著名的bug，当浮动元素与非浮动元素相邻时，这个3像素的Bug就会  出现。 在浮动元素上加上_margin-right:-3px;
微型高度这个BUG的产生原因很简单，IE不允许元件的高度小于字体的高度，所以，下面的fix是设置上字体大小。解决方案一{font-size:0px;} 解决方案二{overflow:hidden;}(最佳)
绝对定位：在IE6下面 position:absolute的绝对定位层前面紧邻的那个层如果有用到“float” css浮动属性会导致这个绝对定位层无法显示解决办法就是在这个绝对定位浮动层前面插入一个清除浮动的层（或者空div）
Png透明：img和background都有不同的解决办法但是不能同时兼容因此引入一个js来解决，
!–[if IE 6]><script type=”text/javascript” src=”js/DD_belatedPNG_0.0.8a-min01.js”></script>
       <script type=”text/javascript”>
       DD_belatedPNG.fix(‘选择器名称  , 应用类型（属性名称或者是元素名称）’);
       </script>
       <![endif]–>
IE6不识别最大最小宽高的问题。
max-width:1000px;
_width:expression((document.documentElement.clientWidth||document.body.clientWidth)<1000?"1000px":"");
overflow:hidden;
min-width:1000px;
       _width:expression((document.documentElement.clientWidth||document.body.clientWidth)>1000?"1  000px":"");
max-width:620px;
       min-width:1px;
       _width:expression(this.scrollWidth > 620 ? "620px":(this.scrollWidth < 1? "1px":"auto"));
max-height:1000px;
       _height:expression((document.documentElement.clientHeight||document.body.clientHeight)<1000?" 1000px":"");
       overflow:hidden;
min-height:1000px;
       _height:expression((document.documentElement.clientHeight||document.body.clientHeight)>1000?" 1000px":"");
Max-Height:620px;
       Min-Height:40px;
       _height:expression(this.scrollHeight > 620 ? "620px":(this.scrollHeight < 40 ? "40px":"auto"));
360浏览器
<meta name="renderer" content="webkit">
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">

<!-- E=edge：保持使用最高级别模式显示内容；

chrome=1：谷歌的外挂插件Google Chrome Frame（谷歌内嵌浏览器框架GCF），使用IE浏览网页时实际上是使用Chrome浏览器内核渲染，最低支持IE6，但前提是客户端已经安装GCF。 -->
Chrome谷歌浏览器下不支持css字体小于12px的解决办法
-webkit-transform : scale()        eg:transform:scale(0.8,0.8); 10号字体【但是包括装它的盒子整体都会变大小，所以要另加标签写。例如span】
@media screen and (-webkit-min-device-pixel-ratio:0) {   }chrome /safari
 @media screen and (-moz-images-in-menus:0) {   }ff   或者css后缀！important
@media all and (min-width: 0px){  \0}opera
H5标签ie8 不识别问题
css：article,aside,dialog,footer,header,section,footer,nav,figure,menu{display:block;}
Head下面添加：
<!--[if lt IE 9]>
<script>
   (function() {
     if (!
     /*@cc_on!@*/
     0) return;
     var e = "abbr, article, aside, audio, canvas, datalist, details, dialog, eventsource, figure, footer, header, hgroup, mark, menu, meter, nav, output, progress, section, time, video".split(', ');
     var i= e.length;
     while (i--){
         document.createElement(e[i])
     }
})()
</script>
<![endif]-->



 第十三节：移动端兼容
2     fixed元素无法点击
场景：父元素设置position: fixed;
子元素设置position: absolute;
此时，如果父元素/子元素还设置了overflow: hidden 则出现“父元素遮挡该子元素“的bug。
视觉(view)层并没有出现遮挡，只是无法触发绑定在该子元素上的事件。可理解为：「看到点不到」。
补充： 页面往下滚动，触发position: fixed;的特性时，才会出现这个bug，在最顶不会出现。
解决办法： 把父元素和子元素的overflow: hidden去掉。
2     场景：<video>标签的父元素(祖辈元素)设置transform样式后，<video>标签会脱离文档流。
解决方案：不使用transform属性。translate用top、margin等属性替代。<video>总是在前
2     textarea这个标签，具有默认样式
-webkit-appearance: none;? ?通过这个属性可以取消；
2     拨打手机直接如下
<a href="tel:15677776767">点击拨打15677776767</a>
     <a href="tel:4008106999,1034">400-810-6999 转 1034</a>
2     圆角bug/：某些Android手机圆角失效
background-clip: padding-box;
2     通过transform进行skew变形，rotate旋转会造成出现锯齿现象
-webkit-transform: rotate(-4deg) skew(10deg) translateZ(0);
       transform: rotate(-4deg) skew(10deg) translateZ(0);
       outline: 1px solid rgba(255,255,255,0)
2     个人建议有些动画用transition来做尽量不要用animation(常用循环动画)
必要时还要打开其渲染3d功能。在全局样式中进行设置如下样式：
-webkit-transform-style:preserve-3d;
-webkit-backface-visibility:hidden;
-webkit-transform:translate3d(0,0,0)

jQuery

ctrl+shift+d  复制当前行到下一行
ctrl+上下键  交换上下行内容
img是行元素，图片四周会出现白边，加display:block;可以去掉白边。
检查每一步是否生效：alert(检查)；
cursor:pointer;  链接鼠标经过变手，可点击
阻止a的跳转：在点击事件的最后面加上    return false(return false后面的东西全都不会生效)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery</title>
    <style type="text/css">
        .box{
            width: 200px;
            height: 200px;
            background-color:blue;
            transition: all 2s;
        }
    </style>
</head>
<body>
    <!-- 动画库  Animate.css -->
    <!-- jquery使用
    1.下载（固定同一个版本）min.js (压缩版)        .js (非压缩版)
    2.引入到html文件    使用script(src属性    写路径)标签 位置:bdy内部最后面
    3.使用     在script标签中使用 但这个标签和引入标签不相同 -->
    <!-- <input type="" name=""> -->
    <div class="box"></div>
    <input type="button" class="button" value="按钮">
    <input type="button2" class="button2" value="按钮2">
    <script src="js/jquery-3.2.1.min.js"></script>
    <script>
        // js代码    jquer 1.选择器    2.方法(.xxx())    3.事件 .事件名(function(){})
        
        // $('css选择器')
        // 点击button 让box变色
        // 1.找到button
        // 2.给button绑定点击事件        .click(function()){要做的事}
        // 3.找到box  变色

       js代码：严格区分大小写        非js语法要用""或''包裹(字符串)        数字可以直接写
        属性选择器：例如：input[type=button]
        选择器  xxx:eq(n)   选择所有xxx中下标为n的那个(下标从0开始)
        选择器  xxx:first    选择xxx中的第一个
        .css( )    改变样式
        .attr( )    改变或者获取属性    .attr('属性名'，'属性值')
        $(this)    触发事件的这个元素   例如：
    <img src="images/gracetan_01.jpg">
    <input type="button" class="button" value="1" title="images/gracetan_01.jpg">
    <input type="button" class="button" value="2" title="images/gracetan_02.jpg">
    <input type="button" class="button" value="3" title="images/gracetan_03.jpg">
    <input type="button" class="button" value="4" title="images/gracetan_04.jpg">
    <input type="button" class="button" value="5" title="images/gracetan_05.jpg">    
    <script src="js/jquery-3.2.1.min.js"></script>
    <script>
        $(".button").click(function(){
            $("img").attr("src",$(this).attr("title"))
        })
检查
$(".button").click(function(){
            // $("img").attr("src",$(this).attr("title"))
            alert($(this).attr("title"))
        })

或者

        $(".button").click(function(){
            $(".box").css({"width":"300px","height":"300px"})
        })
        $(".button2").click(function(){
            $(".box").css({"width":"200px","height":"200px"})
        })
        $(".button1").click(function(){
            $("img").attr("src","images/gracetan_01.jpg")
        })
    </script>
</body>
</html>



变量    存储值的容器
1.声明： var 名（驼峰命名法，由两个单词组成的话，第二个单词的首字母大写。只能由字母和下划线组成）
2.存储：用赋值（=）操作    变量=值
3.使用：直接用变量名    不加引号  






js2

calc 计算
.next( )  同级的下一个兄弟（挨着）

阻止跳转

js中阻止默认行为（超链接跳转，按钮提交）









检测：
console.log(xxx)  控制台输出


mouseenter 移入选中或其子元素只能触发一次 与hover类似
mouseover 移入选中或其子元素 能重复触发（一般不用）
.toggleClass('class名')    点一下添加class，再点一下删除class

js1







jq    动画       
所有动画都可以加回调(可以有先后顺序)   .动画名（500，function( ){回调：动画执行完之后做的事}）
淡入fadeIn     淡出fadeOut        切换fadetoggle
上卷slideUp      下拉slideDown    切换slidetoggle
消失 hide      出现show     切换toggle

show( )   hide( )    可以加毫秒值或者‘slow’或着'fast'

.animate({样式的改变}，500，function( ){回调})   自定义动画
改变的样式要是数值的改变

.animate()方法允许我们在任意的数值的CSS属性上创建动画。唯一必要的属性就是一组CSS属性键值对。这组属性和用于设置.css()方法的属性键值对类似，除了属性范围做了更多限制。

所有用于动画的属性必须是数字的，除非另有说明；这些属性如果不是数字的将不能使用基本的jQuery功能。（例如，width, height或者left可以执行动画，但是background-color不能，除非使用jQuery.Color()插件。）属性值的单位像素（px）,除非另有说明。单位em 和 %需要指定使用。

回调，如下：先变宽然后变色，有先后顺序



鼠标移动事件    .mousemove(function( ){ })

可反复触发






DOM操作
dom：文档对象模型
















例如：





表单（获取）：



  就是拿到选中的值





,keydown 键盘按下        .keyup键盘弹起        .keypress按键盘
event.which    获取所按键盘的code码   13代表回车





滚动条事件：


滚动条事件    窗口 $(window).scroll( )





                       
xx.length  不加括号
只要是JQ的动画，都能用stop( )去停掉




jQuery 总结：

选择器    事件    方法    动画

选择器 :1.css选择器    
            2.遍历查找   :eq(ind)    :not    :lt(ind)    :gt(ind)    :first    :last   
            3.表单选择器 :text    :button    ...

事件：    click    hover    mouseenter    mouseleave    focus    blur    change    scroll    .ready    .keydown    .keyup    .keypress    .on(可以绑定多个事件)    .one（只能执行一次）     .trigger
事件对象    event    鼠标坐标 event.pageX    event.pageY    阻止跳转    event.preventDefault   获取键盘code码 event.which   13回车
方法     1.改变样式    .css    .width    .height    .addClass    .removeClass    .toggleClass      
            2.改变属性    .attr     .prop(获取checkbox radio 是否被选中) 
            3.查找    .parent    .parents    .sibling    .find    .children    .next    .before    .first    .last    .not    .eq    .each      
            4.dom操作    .append    .appendTo    .prepend    .prependTo    .after    .insertAfter    .before    .insertBefore    .remove    .empty    .clone    .text    .val
            5.  .index    $(this)    .length    .offset    .scrollTop
动画：   动画可以使用回调 .xxx(事件,function( ){回调}) 
.show    .hide    .toggle    .fadeIn    .fadeOut    .fadeToggle       .slideToggle    .slideUp    .slideDown    .animate    .stop

数据交互：    ajax


Flexbox






网页制作强大工具：

flexbox 布局
jQuery 插件
swiper 插件

swiper 点击或触摸停止自动播放，点击或触摸恢复
autoplayDisableOnInteraction: false,
原生  js





js语言严格区分大小写
1.变量    存储数据的容器
变量声明提升：使用var声明变量时，会将此变量的声明提升到当前作用域的最顶端。
命名：语义化 ， 开头必须以字母、下划线、$开头 ； 由数字、字母、下划线组成，不能以关键字和保留字命名。通常使用驼峰命名法（第二个单词首字母大写）
使用：var（声明） xx(变量名) = 数据；
同一个变量只能声明一次，再次使用的时候不用声明，修改时直接再次赋值（=）
标识符：js语言中可以自定义命名的    变量    函数名    参数名
变量名不能使用 name 命名（不能单单写name,可组合）
2.数据类型   数字（number） 字符串（string） 布尔（boolean）  null   undefined    对象（object）
数字    1，2，3，4
字符串    '1','2','3'
布尔    true   false
eg:    var bool = true
数据类型检测    typeof  x(数据)    返回数据类型（string,number）
console.log(typeof  '1')
3.数据类型转换
a.字符串转化为数字    Numer( )    parseFloat( )    parseInt( )
    Numer( )  先整体看括号内的值是否能直接转化为数字，能就转化，不能转化为Nan   eg:  var str1 = Number('2')
     parseFloat( )    parseInt( ) 先看最前面一位是否能转化为数字，能则继续查看，直到不能是把所有能转化的整数转化，如果第一位不能转化为数字，则转化成NaN
b.布尔值转化为数字    Number( )    true---1    false---0
c.数字，布尔转化成字符串        String( ) 
d.隐式转换   
    1.加号    +    当加号左右只要出现字符串，会把其他类型的数据转化为字符串后再相连
    2. /  *  -  %   以上符号出现时，会直接把左右两侧的数据用Number（）方法转化为数字，再运算 
    3. if语句会直接把( )里面的东西转化为布尔值 再判断
    e.数字，字符串转化为布尔值 Boolean（）
    只有数字 0     字符串 ''     null    undefined    NaN    可以转化为false
    null    undefined（声明了变量但没有给变量赋值，使用这个变量会变成undefined）
    js 数据类型有两种  值  引用类型
     
    运算符    +  -  /  *  %
    +    加法、字符串拼接
    >  <   >=   <=   ==   !=   ===   !==   !   ||   &&
    ==和===        ==比较的是值是否相等    ===比较的是值和数据类型是否都相等
       如果 || 左面的值不是undefined，就不会执行后面的
     如果 && 左面的值不是undefined，就不会执行后面的
       ++   --   +=   -=   *=   /=   %=


三目运算符
运算符的优先级

语句






.text( ) 获取文本节点，框外面的
.val( )  获取属性值，包括用户输入进框的内容
js原生   循环           函数    
  
声明多个变量可以使用     var a,b,c







函数：语句块
创建    function声明    函数名（首字母不能大写）     （参数：辅助语句）    {语句的集合}
函数声明时不执行，函数调用的时候执行内部的语句
调用函数    函数名（）


参数    形参（函数声明的时候小括号内部）
           实参（调用函数时小括号内传入的）


形参相当于在函数内部声明了变量并且没有赋值，当调用函数时传了实参的话相当于给形参赋值

只有函数有作用域    声明在作用域内的变量或者函数，其他不相关的作用域内是不能访问的，只有子级作用域可以访问或修改，父级作用域也不能访问子级作用域。
最大作用域下创建的，全局变量
全局变量越多，越会污染全局环境



匿名函数：  如： xxx.click(function( ){ })

函数的返回值：在函数最后加上return

                      return    还有跳出函数的作用


   
对象    内置对象（数组）    自定义对象    浏览器对象
对象    属性和方法 

 
       





内置对象：数组
                (数组    日期    正则表达式    数字    数学    字符串    布尔)
数组(array)    :    数据的集合
属性    ：length数组的长度
            var num = arr.lengrh





方法：
.push( )    向数组最后面添加一个或多个元素，并返回新数组的长度
.pop( )    删除数组中的最后一项，并返回删除的元素
.unshift( )    想数组的最前面添加一个或多个元素，并返回新数组的长度
.shift( )    删除数组中的第一项，并返回被删除的元素
.concat( )    合并两个或多个数组（有先后顺序）


.reverse( )    （翻转）颠倒数组的顺序
.join("x" )    将数组使用连接符x拼接成字符串并返回，原数组并不会改变


.slice(a,b)    数组的截取    从a开始（包括a）截取到b（不包括b），返回截取的数组


从第一个开始到结束

.splice(a,b,c )   
     a添加或删除的位置,b删除的个数,c添加的元素，返回一个数组，内部放的是被删除的元素    
.indexOf( )    检测数组中是否存在a这个元素，如果存在返回第一个存在的索引
                    不存在返回 -1
sort    filter    find    map
sort    数组排序    直接使用.sort( )会将数字和字符串的首位字符顺序排序


冒泡排序    快速排序    二分法

filter    过滤/筛选    .filter(function(item,index,array){  })
        item    数组中的每一项
        index   数组中每一项的索引值
        array    原数组


find( )    返回符合条件的第一个元素，不符合返回undefined


map    映射
数学对象    Math

ceil    上进
round    四舍五入
更改属性：attr    prop 
过10毫秒执行一次fun1方法（自动点）



日期对象    Date：（获取input输入框中的值，val( )    别老忘）
创建本地当前日期对象：    var    date = new    Date(    )
var    time    =    Date(    )    获取当前时间
方法：
.getFullYear( )    获取当前的年份
var    year = date.getFullYear
.getMonth( )    获取月份（0-11）
var month =date.getMonth( ) +1
.getDate( )    号
var    hao = date.getDate( )
.getDay( )    星期（0-6）
var day = date.getDay( )
.getHours( )
var hour = date.getHours( )
.getMinutes( )
var minute = date.getMinutes
.getSeconds( )
var second =date.getSeconds( )
.getMilliseconds( ) 毫秒数
.getTime( )    格林威治时间    从1970.1.1到现在的毫秒数，永远不会重复的数值

计时器    方法：    setInterval    clearInterval    setTimeout    clearTimeout
setInterval (函数名，毫秒数)    每过这个毫秒数之后就会执行一次前面的函数

setTimeout(函数名，毫秒数)    延迟这个毫秒数之后，执行一次前面的函数

















function time(){
            var date = new     Date()
            var hour = date.getHours()    
            var minute = date.getMinutes()
            var second = date.getSeconds()
            var nowTime = hour*3600 + minute*60 + second
            var secondDeg = (360/60)*second
            var minuteDeg = (360/60/60)*minute
            var hourDeg = (360/60/60/12)*hour
         $(".hero-second").css("transform","rotate("+ secondDeg +"deg)")
         $(".hero-minute").css("transform","rotate("+ minute +"deg)")
         $(".hero-hour").css("transform","rotate("+ hour +"deg)")
        }
        time()  
        setInterval(time , 500)
内置对象    正则表达式（RegExp）

用来检测文本的规则    （eg：登录注册输入时候弹出警告框）
创建    var  变量 = / 规则 /

检测


规则




只要不是特殊规则，//里面写什么就检测什么


\转义符






\w    一位数字或字母或下划线
\W    \以为非\w




false




得到焦点消失，失去焦点显示


模拟trigger
报错信息整理





错误时候输出试试    console.log( )        alert( )


表单验证
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>yuku-load</title>
    <style type="text/css">
        .bg{
            width: 760px;
            height: 419px;
            margin: 0 auto;
            margin-top: 50px;
            background:url("images/youku.jpg") right bottom no-repeat;
            position: relative;
        }
        .register{
            position: absolute;
            right:32px;
            top: 0;
        }
        h1{
            margin-top: 30px;
            font-size: 18px;
            color: #fff;
            font-weight:400;
        }
        #warn{
            display: block;
            height: 20px;
            font-size: 12px;
            color: red;
        }
        input{
            display: block;
            width: 316px;
            font-size: 14px;
            padding: 10px 0px;
            margin-top: 20px;
            text-indent:8px;
        }
        #phone{
            margin-top:5px;
        }
        #v_container{
            float: right;
        }
        .check #code_input{
            width: 176px;
            float: left;
        }
        #v_container{
            margin-top: 20px;
        }
        #my_button{
            width: 320px;
            font-size: 14px;
            line-height: 40px;
            background-color: #35b5ff;
            border: 0;
            color: #fff;
            margin-top: 20px;
        }
        /* WebKit browsers */
        input:focus::-webkit-input-placeholder { color:transparent; }
        /* Mozilla Firefox 4 to 18 */
        input:focus:-moz-placeholder { color:transparent; }
        /* Mozilla Firefox 19+ */
        input:focus::-moz-placeholder { color:transparent; }
        /* Internet Explorer 10+ */
        input:focus:-ms-input-placeholder { color:transparent; }
    </style>
</head>
<body>
    <div class="bg">
        <div class="register">
            <h1>手机注册</h1>
            <span id="warn"></span>
            <input id="phone" type="text" placeholder="手机号码">
            <input id="password" type="password" placeholder="密码(6-16位字母、数字和符号)">
            <input id="passwordAgain" type="password" placeholder="确认密码">
            <div class="check">
                <!-- <input id="checknum" type="text" placeholder="验证码"> -->
                <div id="v_container" style="width:130px;height: 40px;"></div>
                <input type="text" id="code_input" value="" placeholder="验证码"/>
            </div>
            <button id="my_button">注册</button>
        </div>
    </div>
    <script src="js/jquery-3.2.1.min.js"></script>
    <script src="js/gVerify.js"></script>
    <script>
        //手机号码检测
        var phone = /^((13[0-9])|(14[5,7])|(15[0,1,2,3,5,6,7,8,9])|(17[3,6,7,8])|(18[0-9]))\d{8}$/;
        $("#phone").blur(function(){
            var myphone = $(this).val()
            if(!phone.test(myphone)){
                $("#warn").text("请输入正确的手机号码")
            }
        })
        //密码检测    
        var password1 = / /    
        var password2 = /\(|\)|'|"/
        var password3 = /^([a-zA-Z]{6,16}|[0-9]{6,16}|\W{6,16})$/
        $("#password").blur(function(){
            var mypassword = $(this).val()
            if(mypassword.length === 0){
                $("#warn").text("请输入密码")
            }else if(mypassword.length < 6 || mypassword.length > 16){
                $("#warn").text("密码位数必须在6-16位之间")
            }else{//长度在6-16之间
                if(password1.test(mypassword)){
                $("#warn").text("密码不能有空格，请更换")
                }else if(password2.test(mypassword)){
                $("#warn").text("密码不支持小括号、引号，请更换")
                }else if(password3.test(mypassword)){
                $("#warn").text("密码不能为纯数字、纯字母或纯字符")
                }else{
                $("#warn").text("")
                }
            }
        })
        //确认密码检测    
        $("#passwordAgain").blur(function(){
            var password = $("#password").val()
            var mypasswordAgain = $("#passwordAgain").val()
            if(password != mypasswordAgain){
                $("#warn").text("两次输入密码不一致")
            }else{
                $("#warn").text("")
            }
        })
        //验证码检测
        var verifyCode = new GVerify("v_container");
        document.getElementById("my_button").onclick = function(){
            var res = verifyCode.validate(document.getElementById("code_input").value);
            var myphone = $("#phone").val()
            var mypassword = $("#password").val()
            var mypasswordAgain = $("#passwordAgain").val()
            if(!phone.test(myphone)){
                $("#phone").trigger("blur")
            }else if((mypassword.length === 0) ||(mypassword.length < 6 || mypassword.length > 16) ||(password1.test(mypassword))|| (password2.test(mypassword))||(password3.test(mypassword))){
                $("#password").trigger("blur")     //虚拟trigger
            }else if(password != mypasswordAgain){
                $("#passwordAgain").trigger("blur")
            }else if(res){
                alert("注册成功，请登录");
            }else{
                alert("验证码错误");
            }
        }
    </script>
</body>
</html>
对象  字符串对象
内置对象(对象{ })

创建    var arr = [1,2,3]    var math = Math( )    var date  = new Date( )   
对象{
    属性
    方法
} 
字符串对象
属性 length    字符串的长度
方法    .tirm( )    去掉字符串左右的空白符，并返回新的字符串

s

indexOf() 方法可返回某个指定的字符串值在字符串中首次出现的位置

.replace(正则，新的字符)    符合正则的，被新的字符替换掉







判断字符串内所有字符是否都相等



for循环遍历，拿到每一个字符
另一个方法




创建带变量的正则表达式（拆成字符串拼接）
将原来的正则双斜杠里面的值完全看成一个字符串 如果带变量用 + 拼接








Dom
获取操作    document对象（处理html的各种标签）
方法    .getElementById('id名')    通过id名获取标签
eg:    document.getElementById('box')
             对象              方法                    参数






可简化





数组不能绑定事件












return document.querySelectorAll( )    获得的都放在了数组里。























属性    获取 .     设置 .完再赋值
方法     （）
 

函数不能放在事件里面，不然每执行一次事件函数都执行一次，耗内存

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<style type="text/css">
    *{margin: 0;padding: 0;}
    body{
        background-color: #ccc;
    }
    .warp{
        width:  calc(5 * 101px - 1px);
        padding: 10px;
        background-color: #fff;
        margin: 0 auto;
        margin-top: 100px;
    }
    .list{
        width:calc(5 * 100px - 1px);
        list-style: none;
        overflow: hidden;
        border-bottom: 1px solid #ccc;
        
    }
    ul.list li{
        float: left;
        padding: 10px;
    }
    ul.list li a{
        display: block;
        width: 77px;
        border-right: 1px solid #ccc;
        color: #000;
        font-size: 16px;
        line-height: 20px;
        text-align: center;
        text-decoration: none;
    }
    ul.list li a:hover{
        color:red;
    }
    ul.list li:last-child a{
        border-right: none;
    }
    .warp>.line{
        width:80px;
        height: 3px;
        position: relative;
        background-color:red;
        top: -3px;
        left:0px;
        transition: all .2s;
    }
    .warp>.tabs{
        padding-top: 10px;
    }
    .warp>.tabs>.tab{
        width: 100%;
        height: 400px;
        font-size: 46px;
        display: none;
        text-align: center;
        line-height: 400px;    
        background-color:teal;
    }
    .warp>.tabs>.tab:first-child{
        display: block;
    }
    .list li .active{
        color: red;
    }
</style>
<body>
    <div class="warp">
        <ul class="list">
            <li><a href="#">拉拉裤</a></li>
            <li><a href="#">男装</a></li>
            <li><a href="#">大家电</a></li>
            <li><a href="#">手机通讯</a></li>
            <li><a href="#">吸顶灯</a></li>
        </ul>
        <div class="line"></div>
        <div class="tabs">
            <div class="tab">
                <h2>拉拉裤</h2>
            </div>
            <div class="tab">
                <h2>男装</h2>
            </div>
            <div class="tab active">
                <h2>大家电</h2>
            </div>
            <div class="tab">
                <h2>手机通讯</h2>
            </div>
            <div class="tab">
                <h2>吸顶灯</h2>
            </div>
        </div>
    </div>
    <script>
        function getElements(selector){
            return document.querySelectorAll(selector)
        }
        var aArr = getElements('ul li a')
        var tabArr = getElements('.tabs .tab')
        console.log(aArr)
        for(var i = 0;i<aArr.length;i++){
            aArr[i].index = i
            aArr[i].onmouseenter = function(event){
                event.preventDefault()
                var j = this.index
                // console.log(j)
                for(var t = 0;t<tabArr.length;t++){
                    if(j == t){
                        tabArr[t].style.display = 'block'
                    }else{
                        tabArr[t].style.display = 'none'
                        }
                    }
                    if(j == 0){
                            getElements('.line')[0].style.left = 0
                    }else if(j ==aArr.length - 1 ){
                        getElements('.line')[0].style.left = j*100+22+'px'
                    }
                    else{
                            getElements('.line')[0].style.left = j*100-5+'px'
                    }
                }
            }
            function addClass(ele,className){
                var oldClass = ' '+ele.className+' '
                // var newClass = oldClass+' '+className
                if(oldClass.indexOf(' '+className+' ' )==-1){
                    var newClass = oldClass+className
                    ele.className = newClass.trim()
                    
                }else{
                    var newClass = oldClass
                    ele.className = newClass
                }
            }
            function removeClass(ele,className){
                var oldClass = ' '+ele.className+' '
                while(oldClass.indexOf(' '+className+' ')!==-1){
                    oldClass = oldClass.replace(' '+className+' ',' ')
                }
                ele.className = oldClass.trim()
            }
            addClass(aArr[0],'active')
            removeClass(tabArr[2],'active')
            console.log(aArr[0],tabArr[2])
    </script>
</body>
</html>
flexbox弹性盒子
给父级    display:flex;
flex-direction : row/row-reverse/column/column-reverse/space-between/space-around/normal/center/flex-start/flex-end




















DOM     增删改查
         //创建标签
        //document.createElement('标签名')
        //创建一个空标签
        var a = document.createElement('a')
        //给标签设置属性
        a.setAttribute('href','#')
        a.setAttribute('title','123')
        //向标签内部添加文字 (innerText)或 元素(innerHTML)
        a.innerText = '456'//属性修改---赋值操作
        a.innerHTML = '<span>12345</span>'//危险操作
        console.log(a)
        //dom元素a.appendChild(dom 元素b)    向a内部最后面添加b
        document.getElementsByTagName('div')[0].appendChild(a)
        //父级dom元素a.insertBefore(要添加的dom元素b，参照物dom元素c)
        //将b 添加到a的内部c的前面
        document.getElementsByTagName('body')[0].insertBefore(a,document.getElementsByTagName('div')[0])
        //父级dom元素a.removeChild(dom元素b)
        //从父级a中删除子集b
        document.getElementsByTagName('body')[0].removeChild(a)
        //克隆    
        //dom元素 .cloneNode()    克隆标签包括开始标签内部的属性 不包括尖括号之间的内容 空标签
        //dom元素 .cloneNode(true) 完全克隆一个dom元素
        
        var a1 = a.cloneNode(true)
        console.log(a1)









事件委托

将子级事件委托给祖先级（祖先级必须是不会改变的，要一直存在的）
找到真正触发事件的元素，判断这个元素什么时候执行操作
event    事件对象    使用event时要在事件函数写上一个参数  event(兼容)
event.target    属性    获取触发事件的真正元素




三目运算符


原生的事件

onclick    onmouseenter    onmouseleave    onmouseover    onmouseout    onblur    onfocus       onscroll    onchange表单    onload文档加载    oninput表单    onmousemove

 





onload 比jq的ready文档加载的东西多

原生的滚动条事件    窗口的滚动条    可以绑定在    window    document    和body标签上
某个标签的滚动调绑定在该标签上







滚动条兼容






注意跟onblur区分开
获取文本    innerText

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>search</title>
    <style type="text/css">
        li{cursor:pointer;}
    </style>
</head>
<body>
    <input type="text" id = "txt" name="">
    <button id = 'search'>搜索</button>
    <button id = 'all'>全部</button>
    <ul>
        <li>张三</li>
        <li>李四</li>
        <li>王五</li>
        <li>赵六</li>
        <li>郑七</li>
    </ul>
    <script>
            var liArr = document.querySelectorAll('ul>li')
        document.getElementById('search').onclick = function(){
            var val = document.getElementById('txt').value
            if(val.trim()!==''){
                for(var i = 0;i<liArr.length;i++){    
                    var text = liArr[i].innerText
                    if(text.indexOf(val)!= -1){
                        liArr[i].style.display = 'block'
                    }else{
                        liArr[i].style.display = 'none'
                    }
                }
            }else{
                alert('搜索内容不能为空')
            }
        }
        document.getElementById('all').onclick = function(){
            for(var i = 0;i<liArr.length;i++){
            liArr[i].style.display = 'block'
            }
        }
        //自动搜索
        var timer = null
        document.getElementById('txt').oninput = function(){
            clearTimeout()
            timer = setTimeout(function(){
                var val = document.getElementById('txt').value
            if(val.trim()!==''){
                for(var i = 0;i<liArr.length;i++){    
                    var text = liArr[i].innerText
                    if(text.indexOf(val)!= -1){
                        liArr[i].style.display = 'block'
                    }else{
                        liArr[i].style.display = 'none'
                    }
                }
            }else{
                alert('搜索内容不能为空')
            }
        },3000)
        }
    </script>
</body>
</html>
原生事件对象
事件对象    
event（写在事件函数的参数内 写成任意变量都可以 但是都是event的简写）
方法    
event.preventDefault()    阻止事件默认触发的事
event.stopPropagation    阻止事件冒泡（非ie）
event.cancelBubble = true    阻止事件冒泡（ie）
属性    
event.target    触发时间的真正元素
event.keyCode    键盘码
event.type    事件类型
event.clientX     event.clientY     获取事件出发时鼠标的位置    鼠标相对于浏览器窗口的坐标
event.screenX     event.screenY     获取事件出发时鼠标的位置    鼠标相对于屏幕的坐标
浏览器
window    浏览器对象
所有创建在全局下的变量    都是属于window的属性    window.变量名 window可省略
所有创建在全局下的function    都是属于window的方法    window.函数名( )    window可省略

window    方法
alert( )    浏览器警告弹窗
confirm( )    点击确定按钮返回true，点击取消按钮返回false
prompt( )    点击确定返回输入的内容，点击取消返回null
计时器方法
setInterval( )    clearInterval( )    setTimeout( )    clearTimeout( )
清除计时器    使用clear清除set的返回值  
set内部的函数怎么传参数    setInterval('fun(a)',1000)
open(地址，新网页的名字)    打开一个新网页  
close( )  
网页名字作用：不会每次都打开一个新的，会把之前的覆盖掉




排序：

冒泡
<script>
        var numArr = [11,4,7,9,23,45,67,2,43,25]
        for(var j=0;j<numArr.length - 1 ;j++){
                for(var i = 0;i<numArr.length - j- 1;i++){
                if(numArr[i]>numArr[i+1]){
                    var bigNum = numArr[i]
                    numArr[i] = numArr[i+1]
                    numArr[i+1]= bigNum
                }
            }
        }
        console.log(numArr)
    </script>








整屏











var subtotal = getEle(".subtotal").innerText.replace(/[^\d.]/g,'')
购物车
function getEle(selector){
    return document.querySelector(selector)
}
function getEles(selector){
    return document.querySelectorAll(selector)
}
//checkAll 全选按钮
var checkAll = getEles('.checkAll')
//check 所有按钮
var check = getEles('input[type = checkbox]')
//shop 店铺按钮
var shop = getEles('.shop')
//goods 商品按钮
var goods = getEles('.goods')
//加减按钮
var counts = getEles('.goodson .amount')
//点击删除
var dele =getEles('.del')
//改变全部checkbox的状态（点击全选或者店铺按钮）
//var active = this.checked
function allChange(checkboxObjs,active){
    for(var i = 0;i<checkboxObjs.length;i++){
        checkboxObjs[i].checked = active
    }
}
//计算总数量函数
function numberAll(allNum){
    var result = 0
    for(var i =0;i<allNum.length;i++){
        if(allNum[i].checked==true){
            var num2 = allNum[i].parentNode.querySelector('.amount .number').value
            result = result + Number(num2)
        }
    }
    return result
}
//计算总价函数
function countAll(allGoods){
    var result = 0
    for(var i =0;i<allGoods.length;i++){
        if(allGoods[i].checked==true){
            var num1=allGoods[i].parentNode.parentNode.querySelector('.name .subtotal').innerText.replace(/[^\d.]/g,'')
            result = result + parseFloat(num1)
        }
    }
    return result.toFixed(2)
}
//刷新页面计算总量
getEle('.changes').innerText=numberAll(goods)
//刷新页面计算总价
getEle('.total').innerText='￥'+countAll(goods)
//全选事件
for(var i=0;i<checkAll.length;i++){
    checkAll[i].onchange = function(){
        var active = this.checked
        allChange(check,active)
        getEle('.total').innerText='￥'+countAll(goods)
        getEle('.changes').innerText=numberAll(goods)
    }    
}
//单选店铺选中事件
for(var i=0;i<shop.length;i++){
    shop[i].onchange = function(){    
         var active=this.checked
        this.parentNode.querySelector('.name .goods').checked = active
        var onoff = true
        for(var m=0;m<shop.length;m++){
            if(shop[m].checked == false){
                onoff = false
                break
            }
        }
        if(onoff == true){
            allChange(checkAll,true)
        }else{
            allChange(checkAll,false)
        }
        getEle('.total').innerText='￥'+countAll(shop)
        getEle('.changes').innerText=numberAll(goods)
    }
}
//单选商品选中事件
for(var i=0;i<goods.length;i++){
    goods[i].onchange = function(){    
        var active=this.checked
        this.parentNode.parentNode.querySelector('.shop').checked = active
        var onoff = true
        for(var m=0;m<goods.length;m++){
            if(goods[m].checked == false){
                onoff = false
                break
            }
        }
        if(onoff == true){
            allChange(checkAll,true)
        }else{
            allChange(checkAll,false)
        }
        getEle('.total').innerText='￥'+countAll(goods)
        getEle('.changes').innerText=numberAll(goods)
    }
}
//点击加或减号
for(var i = 0;i<counts.length;i++){
    counts[i].onclick = function(event){
        var num = parseInt(this.getElementsByTagName('input')[0].value)
        var target = event.target
        if(target.className =="reduce"){
            if(num > 1){
                    num--
                }
        }else if(target.className =="add"){
            num++
        }
        this.getElementsByTagName('input')[0].value = num
        //小计
        var price = this.parentNode.parentNode.querySelector('.price').innerText.replace(/[^\d.]/g,'')
        this.parentNode.parentNode.querySelector('.name .subtotal').innerText= '￥'+(num * price).toFixed(2)
        getEle('.total').innerText='￥'+countAll(goods)
        getEle('.changes').innerText=numberAll(goods)
    }
}
//删除
getEle("section").onclick = function(event){
    var targetEle = event.target
        for(var i = 0;i<dele.length;i++){
            dele[i].onclick = function(){
                this.parentNode.parentNode.querySelector('.number').value=0
                this.parentNode.parentNode.querySelector('.subtotal').innerText='￥'+0
                getEle("section").removeChild(this.parentNode.parentNode.parentNode)
        }
        getEle('.total').innerText='￥'+countAll(goods)
        getEle('.changes').innerText=numberAll(goods)
    }
}

老师示例：（注意思维，先确定好每个事件要实现的功能，尽可能把重复部分写成函数来调用）
function getEle(selector){
        return document.querySelector(selector)
    }
    function getEles(selector){
        return document.querySelectorAll(selector)
    }
    //改变全部checkbox 状态 （点击全选或者店铺按钮）
    function allChange(checkboxObjs,active){
        for (var i = 0;i<checkboxObjs.length; i++) {
            checkboxObjs[i].checked = active
        }
    }
    //计算总价函数  把所有选中商品的小计加在一起
    function countAll(allGoods){
        //allGoods代表所有商品按钮
        var result = 0;
        //查找所有的商品按钮
        for(var i = 0;i<allGoods.length;i++){
            //判断该商品按钮是否为 true
            if(allGoods[i].checked === true){
                //通过 这个商品按钮找到商品小计
                var num1=allGoods[i].parentNode.parentNode.parentNode.querySelector('.money').innerText
                //只要商品按钮选中 就把总价加上小计   （之前的总价加上小计）
                result = result + parseFloat(num1)
            }
        }
        return result.toFixed(2)
    }
    //计算已选商品个数
    //allObj 代表所有全选按钮
    var allObj = getEles('.all')
    //checkboxAll 代表所有按钮
    var checkboxAll = getEles('input[type=checkbox]')
    //radioAll 代表所有商品按钮
    var radioAll = getEles('.commodity .radio')
    //每个商品下面的计算部分
    var counts = getEles('.commodity .count')
    //刷新页面计算总价
    getEle('.sum').innerText=countAll(radioAll)
    alert(countAll(radioAll))
    //点击全选
    for(var i = 0;i<allObj.length;i++){
        allObj[i].onchange = function(){
            //1改变按钮状态
            //获取点击的all的选中状态
            var active = this.checked
            //将所有checkbox的选中状态设置为 active
            allChange(checkboxAll,active)
            //2计算总价
            getEle('.sum').innerText=countAll(radioAll)
        }
    }
    //点击商品按钮
    for(var j = 0;j<radioAll.length;j++){
        radioAll[j].onchange = function(){
            //有可能改变全选按钮状态
            // （1当点击了商品按钮之后所有商品按钮都变为选中，此时全选选中）
            // （2所有商品按钮都为选中，当点击了商品按钮时，全选不选中）
            // 当所有商品按钮全部为true 全选选中 否则全选不选
            var num = 0 //存储true的个数
            var onoff = true  //默认所有商品全部选中
            for(var m = 0;m<radioAll.length;m++){
                // 1.商品为true 个数+1
                // if(radioAll[m].checked === true){
                //     //判断某个商品按钮是否为true，并不能给是否全部选中下结论
                //     //如果某个商品按钮为true num个数+1
                //     num++
                // }
                //2.默认商品全部选中，当一个不选中 就改变
                if(radioAll[m].checked === false){
                    onoff = false
                    break
                }
            }
            //判断true的个数是否等于单选按钮的个数
            // if(num === radioAll.length){
            //     allChange(allObj,true)
            //     // console.log('商品按钮全部选中，全选变为true')
            // }else{
            //     allChange(allObj,false)
            //     // console.log('商品按钮不全选中，全选变为false')
            // }
            //判断 onoff
            if(onoff === true){
                allChange(allObj,true)
                // console.log('商品按钮全部选中，全选变为true')
            }else{
                allChange(allObj,false)
                // console.log('商品按钮不全选中，全选变为false')
            }
            //计算总价
            getEle('.sum').innerText=countAll(radioAll)
        }
    }
    //点击加或减号
    for(var j = 0;j<counts.length;j++){
        counts[j].onclick = function(event){
            //获取当前商品下面的商品个数     获取的是字符串
            var num = parseInt(this.getElementsByTagName('p')[0].innerText)
            //获取当前商品下面的商品单价     获取的是字符串
            // var price = this.previousElementSibling.querySelector('p span').innerText
            var price = this.parentNode.querySelector('div>p>span').innerText
            //获取真正点击的目标对象
            var target = event.target
            //判断是否加号还是减号
            if(target.className === 'minus'){
                //减号
                if(num > 1){
                    num--
                }
            }else if(target.className === 'plus'){
                //加号
                num++
            }
            //计算个数和小计
            this.getElementsByTagName('p')[0].innerText = num    
            // 数字.toFixed(位数)  将数字转换为字符串 并且 四舍五入之后保留几位小数
            this.parentNode.querySelector('.money').innerText = (num * price).toFixed(2)
            this.parentNode.parentNode.parentNode.querySelector('.c_top .money3').innerText = (num * price).toFixed(2)
            //计算总价
            getEle('.sum').innerText=countAll(radioAll)
        }
    }
    </script>



















shopping.js:50 Uncaught TypeError: Cannot read property 'checked' of undefined
Uncaught ReferenceError: Invalid left-hand side in assignment
全局、局部
返回值





递归函数
递归函数    函数内部调用函数本身的函数叫做递归函数











js动画








js动画
for in语句    遍历数组    真正用法遍历对象
对象属性值的获取    不仅可以使用obj.属性名获取    还可以使用obj['属性名']获取 注意：[ ]内部要是字符串类型



回调函数    一个函数作为参数传递给另一个函数
回调函数作用      一个函数执行完毕之后再执行另一个函数，将后者写成回调函数


arguments    在函数内部使用    代表函数传入的参数的集合 （类数组）


项目注意事项
移动端用zepto做，原生，
所有宽，高，边距 都/100 写成rem
引公共样式
rem对于根节点来说
body,html{
font-size:x px;
}
不写 默认16px
字体太小或太大的话，使用scale放大缩小
能点的跳转必须用a去写
每一页都写一个返回历史纪录    history.back
单位都要用rem
document.documentElement.style.fontSize = document.documentElement.clientWidth / 6.4 + 'px'
移动端
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
初始化
html, body, div, span, applet, object, iframe,
    h1, h2, h3, h4, h5, h6, p, blockquote, pre,
    a, abbr, acronym, address, big, cite, code,
    del, dfn, em, font, img, ins, kbd, q, s, samp,
    small, strike, strong, sub, sup, tt, var,
    dl, dt, dd, ol, ul, li,
    fieldset, form, label, legend,
    table, caption, tbody, tfoot, thead, tr, th, td {
        margin: 0;
        padding: 0;
        border: 0;
        outline: 0;
        font-weight: inherit;
        font-style: inherit;
        font-size: 100%;
        font-family: inherit;
        vertical-align: baseline;
    }
    .clearfix:before,
    .clearfix:after {
                        content: "";
                        display: block;
                        clear: both;
                        visibility: hidden;
                        line-height: 0;
                        height: 0;
                        font-size:0;
}
.clearfix { *zoom:1;}


个人中心能点，我去和地图写字体图标    固定定位
加载更多和more要有效果
搜索，判断填南京才能跳
出发城市 行程天数 点谁默认选中谁    hasclass
蒙版   整一个和屏幕一样大小的盒子，定到顶部，透明度    点一下，带蒙版背景的大盒子弹出
形成简介 点击滚动 scrolltop
收藏什么的，点击写个变色效果
日历用插件，自己找
订票要能算
领队介绍的<点击跳转页面领队介绍页
领队介绍的文字点击跳转到领队详情页
领队产品跳转先不做
订单页能点，能计算，点击修改调到日历页
提交订单要填写完才能提交，要弹出警告信息放在上面
提交订单到确认订单页
支付页倒计时，选择方式不选不能点付款
用户个人中心调到订单列表页
订单列表随便点击一个订单跳转到订单详情页


1.自驾团 2                  点击境内跳转到2     点击商品跳转到3  输入南京点击搜索跳转到4
2.自驾团 1                  点击商品跳转到3     输入南京点击搜索跳转到4
3.自驾团详情页              点击出游日期与价格日历跳转5  点击领队介绍跳转12 点击领队详情跳转13
4.自驾团搜索结果页          点击我要报名跳转5
5.自驾团报名页              点击下一步跳转6
6.自驾团填写订单页          点击修改跳转到5  点击常用游客跳转7  点击提交订单
7.自驾团选择常用游客页      点击添加跳转8    点击确定跳转6
8.自驾团添加游客页          点击保存跳转7
9.自驾团确认订单页          点击修改跳转到5  点击常用游客跳转7  点击确认支付10
10.自驾团支付页             点击付款跳转11
11.自驾团支付成功页         点击关闭和返回继续订票跳转 1
12.自驾团领队介绍
13.自驾团领队详情页
14.个人中心 订单列表页         点击一个订单跳转
15.自驾团订单详情页

zepto.js
用法同jq,要引对应插件

自己写的js最后引

















返回上一个页面

GitHub


4 2，3，4



Administrator@zhaoshurui MINGW64 /g/github
$ git clone https://github.com/zsrzsrzsr-zsr/zsrzsrzsr-zsr.github.io.git
Cloning into 'zsrzsrzsr-zsr.github.io'...
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), done.
Administrator@zhaoshurui MINGW64 /g/github
$ git status
fatal: Not a git repository (or any of the parent directories): .git
Administrator@zhaoshurui MINGW64 /g/github
$ cd zsrzsrzsr-zsr.github.io/
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
        modified:   index.html
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        akela.html
        area.html
        detail.html
        group.html
        serp.html
no changes added to commit (use "git add" and/or "git commit -a")
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ git add .
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ git commit -m'first updata'
*** Please tell me who you are.
Run
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
to set your account's default identity.
Omit --global to set the identity only in this repository.
fatal: unable to auto-detect email address (got 'Administrator@zhaoshurui.(none)')
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ ^C
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$  git config --global user.email "691363707@qq.com"
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ git config --global user.name "zsrzsrzsr-zsr"
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ git commit -m"first updata"
[master b4ba9a9] first updata
 6 files changed, 787 insertions(+), 1 deletion(-)
 create mode 100644 akela.html
 create mode 100644 area.html
 create mode 100644 detail.html
 create mode 100644 group.html
 rewrite index.html (100%)
 create mode 100644 serp.html
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$ git push
Logon failed, use ctrl+c to cancel basic credential prompt.
Username for 'https://github.com': zsrzsrzsr-zsr
Counting objects: 8, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 9.36 KiB | 3.12 MiB/s, done.
Total 8 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/zsrzsrzsr-zsr/zsrzsrzsr-zsr.github.io.git
   107128b..b4ba9a9  master -> master
Administrator@zhaoshurui MINGW64 /g/github/zsrzsrzsr-zsr.github.io (master)
$
cd 
cd. ./
cd e:
