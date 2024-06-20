<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人首页</title>
    <link rel="stylesheet" href="./css/main.css"><!-- 链接首页的css -->
        <style>#layout{
        width:1200px;
        margin-left: auto;
        margin-right: auto;
    }
    /* 凝胶布局 */
    #canvas{
        position: fixed;
        left: 0px;
        top: 0px;
        z-index: -1;
        /* canvas定位在最下层 */
    }
    /* 元素相对于浏览器窗口进行定位 */
    #top{
    height: 80px;
    background-color:#5CADAD	;
    font-size: 250%;
    text-align: center;
    }
    
    #tc{
    display: table;
    border-spacing: 150px;
    }
    /* 表格单元格设置 */
    #tr{
    display: table-row;
    text-align: center;
    justify-content: center;
    align-items: center;
    }
    /* 水平，垂直居中 */
    #individulprint{
    width: 400px;
    height: 400px;
    margin: 50px;
    background: rgba(0, 0, 0, 0.2);
    display: table-cell;
    border-radius: 100%;
    text-align: center;
    justify-content: center;
    align-items: center;
    
    }
    #introduce ul{
        text-align: center;
        padding: 0px;
        font-size: 120%;
        line-height: 30px; 
    
    }
    #introduce li{
        padding: 10px;
        font-size: 120%;
        line-height: 30px; 
    
    }
    #introduce{
    width: 400px;   
    height: 400px;
    margin: 50px;
    display: table-cell;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 100%;
    }
    #ii{
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 120%;
    line-height: 40px; 
    }
    #bottom{
        background-color: #5CADAD;
        color: #efe5d0;
        text-align: center;
        height: 80px;
        width: 100%;
        font-size: 90%;
        font-family:  Georgia, "Times New Roman", Times, serif;
        line-height: 30px;
    }
    
    body{
        margin: 0;/* 外边距 0不用给单位 */
    }
    ul{
        list-style: none;/* 清除小黑圆点 */
        margin: 0;
        padding: 0;/* 内边距 */
    }
    #nav{
        height: 40px;
        width: 100%;
        background-color: #ADFEDC;
        text-align: center;
    }
    #nav ul { 
        margin: 0 0 0 30px; 
        padding: 0px; font-size: 120%;
        color: #FFF; 
        line-height: 40px; 
        white-space: nowrap;  
        /* 文本不会换行，会在在同一行上继续 */
    } 
    #nav li { 
        list-style-type: none; 
        display: inline; 
    }
    #nav li a { 
        text-decoration: none; 
        font-family: Arial, Helvetica, 
        sans-serif; padding: 5px 50px; 
        color: #0a0a0a; 
    } 
    #nav li a:hover { 
        color: #ff0; 
        background-color: #ffaad5;
    }
    </style>
</head>
<body>
<!-- 主体布局是凝胶布局 -->
    <canvas id="canvas" height="1000" width="1644"></canvas>
    <!-- 创建一个画布 -->
<!-- 页眉区 -->
<!-- begin -->
    <header id="top">
      个人首页
    </header>
<!-- end -->
<!-- 导航区 -->
<!-- begin -->
    <nav id="nav">

            <ul class="ul_nav">
                <li class="list"><a href="./index/index.html">个人首页</a></li>               
                <li class="list"><a href="./index/introduce.html">个人简介</a></li>
                <li class="list"><a href="./index/habit.html">个人爱好</a></li>
                <li class="list"><a href="./index/picture.html">生活快照</a></li>
                <li class="list"><a href="./index/career.html">我的童年</a></li>
            </ul>
            <!-- 用列表来创建导航区 -->
    </nav>
<!-- end --> 
<!-- 内容区 -->
<!-- begin -->
    <div id="layout">
    <section id="inner">
      <div id="tc">
        <!-- 这里使用的是表格布局 -->
        <div id="tr">
          <article id="individulprint">
            <img src="../image/IMG_20240617_135216.png" alt="显示错误">
          </article>
          <article id="introduce">
            <ul>
                <li>姓名：颜盛杰</li>
                <li>性别：男</li>
                <li>年龄：19岁</li>
              </ul>
            <p id="ii">
            简介：在校在读大学生，<br>
              社恐人但喜欢唠嗑,<br>
              爱好是看书，听音乐，<br>
              看动漫和竞走。</p>
          </article>
        </div>
      </div>
    </section>
    </div>
<!-- end --> 
<!-- 页脚区 -->
<!-- begin -->
    <footer id="bottom">
制作人：颜盛杰<br>
@2024--06--16
    </footer>
<!-- end --> 
<!-- canvas脚本区 -->
<!-- begin -->
    <script>
        var canvas = document.getElementById('canvas');
        // 获取canvas的id
        var ctx = canvas.getContext('2d');
        // 设定为2d的模式并赋值ctx
        var gradient1 = ctx.createRadialGradient(822, 500, 200, 822, 500, 500);
        // 用ctx的createRadialGradient方法创建一个径向渐变对象，并将创建的渐变对象赋值给变量gradient1
        gradient1.addColorStop(0, "#fffc96");
        // 添加渐变颜色，下同
        gradient1.addColorStop(1, "skyblue");
        ctx.fillStyle = gradient1;
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        // 用ctx的fillRect方法绘制一个矩形并填充
    </script>
<!-- end -->
<!-- js脚本区 -->
<!-- begin -->
    <script type="text/javascript">
        window.onload= ! function (e, t, a) {
            function r() {
                for (var e = 0; e < s.length; e++) s[e].alpha <= 0 ? (t.body.removeChild(s[e].el), s.splice(e, 1)) : (s[
                        e].y--, s[e].scale += .004, s[e].alpha -= .013, s[e].el.style.cssText = "left:" + s[e].x +
                    "px;top:" + s[e].y + "px;opacity:" + s[e].alpha + ";transform:scale(" + s[e].scale + "," + s[e]
                    .scale + ") rotate(45deg);background:" + s[e].color + ";z-index:99999");
                requestAnimationFrame(r)
            }
            // 定义一个名为r的函数，用于更新粒子的位置、大小、透明度等属性，并调用requestAnimationFrame来实现动画效果
            function n() {
                var t = "function" == typeof e.onclick && e.onclick;
                e.onclick = function (e) {
                    t && t(), o(e)
                }
            }
            // 定义一个名为n的函数，用于重写onclick事件，使得在点击页面时同时触发原有的onclick事件和自定义的o函数
            function o(e) {
                var a = t.createElement("div");
                a.className = "heart", s.push({
                    el: a,
                    x: e.clientX - 5,
                    y: e.clientY - 5,
                    scale: 1,
                    alpha: 1,
                    color: c()
                }), t.body.appendChild(a)
            }
            // 定义一个名为o的函数，用于创建一个新的心形粒子元素，并将其添加到页面中
            function i(e) {
                var a = t.createElement("style");
                a.type = "text/css";
                try {
                    a.appendChild(t.createTextNode(e))
                } catch (t) {
                    a.styleSheet.cssText = e
                }
                t.getElementsByTagName("head")[0].appendChild(a)
            }
            // 定义一个名为i的函数，用于向页面的<head>标签内添加一个<style>标签，用于设置心形粒子的样式
            function c() {
                return "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math
                    .random()) + ")"
            }
            // 定义一个名为c的函数，用于生成随机颜色值
            var s = [];
            // 初始化一个空数组s，用于存储所有的心形粒子对象
            e.requestAnimationFrame = e.requestAnimationFrame || e.webkitRequestAnimationFrame || e                // 使用requestAnimationFrame函数来实现动画效果，并调用i函数设置心形粒子的样式
                .mozRequestAnimationFrame || e.oRequestAnimationFrame || e.msRequestAnimationFrame || function (e) {
                    setTimeout(e, 1e3 / 60)
                }, i(
                    ".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"
                ), n(), r()
                // 调用n函数重写onclick事件，使得在点击页面时同时触发原有的onclick事件和自定义的o函数
        }(window, document);
    </script>
<!-- end -->
</body>
</html>
