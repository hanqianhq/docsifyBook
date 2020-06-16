# HTML

## 谈一谈元素属性 href 和 src 的区别？

### 字面区别

#### href
Hypertext  Reference  
  超文本  &nbsp;&nbsp;引用或参照

#### src
Source 资源

<br>
英文字面上看来，好像是差不多意思

### 主要使用场景

#### href
- link
- a

#### src 
- img
- style
- script
- input
- iframe

<!-- ![avatar](/images/src_link.png) -->

    <img src="smile.png">
    <a href="smile.png">笑一下</a>

这个结果带来的区别是什么呢？  
img 会直接把图片渲染在页面上  
而 a 标签不会渲染图片，需要点击a标签，才能在另一个地址看到图片

href 建立了一个通道，这个通道联系着其他资源  
src 引用的资源直接成为了当前文档的一部分，因为它把资源下载了下来并绑定在文档上，浏览器遇到这个属性会先下载这个资源并编译，执行完了之后才会进行下一步 
<br> 

就像汽车加油，加完了才能走

> href 建立超链接，通过通道联系引用资源  
> src 会把资源下载下来，代替当前元素，嵌入到文档中

---

## 什么是标签语义化

## doctype 的作用

## 块级标签都有哪些？

ssh root@192.168.31.90

编辑 vim ~/.ssh/config 文件添加以下内容

> Host houdunren
> Hostname 192.168.31.90
> Port 22
> User root

现在直接使用 ssh houdunren 就可以登录服务器了

# CSS


## 伪类和伪元素有什么区别？

## 为什么要清除浮动？如何清除？

## 不同选择器的权重怎么算的

## 前端几大经典布局的实现方案？

## toB 和 toC 的区别

## VUE 的性能优化

## 对 Vue3.0 的新特性有没有了解？

## 移动端布局的几大方案？

#### 1、media（主流)
适合 Pc 端移动端用一套项目  
像京东这种，pc端移动端是不一样的，那就不适合用这种

#### 2、rem（主流)
针对移动端有单独设计

#### 3、flex
部分布局可以用 flex 

#### 4、vh/vw
通过调整视口百分比，跟百分比类似，也称为百分比布局

---

## css 的 display 可以取什么值？

## 用 ts 实现一个数组的去重

## mvvm 框架原理

## 手写 promise 的实现


## flex 布局和传统布局的区别

## http 各种状态码的含义

## 什么时候用 flex ？除了这种方式居中还能用什么？响应式布局还能怎么做？盒子模型？

## opacity 兼容处理？

> 上面的操作也已经实现的 VSCODE 远程开发的基础步骤

## 介绍一下 postion 属性

## CSS 中 link 和 import 的区别

- link 属于 HTML 标签，@import 是 CSS 提供的
- 页面被加载的时候 link 就会被加载，而 @import 需要等到页面加载完才会加载
- import 只能在 IE5 以上使用，link 是 HTML 标签，无兼容问题
- link 的权重高于 @import

#配置源

## filter 还能做哪些事？

通过添加源可以加快软件下载，同时更多的源也提供更丰富的软件

如果下载速度可以就不用配置了

---

## 盒子水平垂直居中的方案？

这个问题在项目中很常见，开始我用的什么。。<br>
后来 css3 出现，我尝试用什么。。。<br>
后来我在博客上看到了还有什么什么技术。。于是尝试使用。。<br>

---

<strong>记住一共有五中方案</strong>

- 定位三种
- display：flex
- javascript
- display：table-cell

###### 哈哈

<strong> 定位

## 不同选择器的权重怎么算的

## 说一说盒模型吧

## position 和 float 的区别？

## CSS 怎么画出一个三角形

## 旋转动画怎么做？

---

## rem 和 em 的区别

##### 区别
- rem:基于html元素字体大小
- em：根据使用它的元素大小决定（其实不是根据父元素，是因为继承了父元素，所以造成误解）


##### 深刻理解
> 他们都是灵活可以扩展的单位  
> 你使用 1rem 或者 1em ，其实都可以被浏览器翻译成 16px-160px 以及其他任何值

 浏览器使用 px，那 1px 就显示为 1px

- rem：如果默认根元素字体为 16px，那你的 10rem 就会渲染成 160px
- em：如果一个 div 有18px 字体大小，那此时你的元素 10em 就是 180px  

浏览器默认虽然是16px，但是浏览器的这个默认参数，用户是可以自己改变的
它支持9-72px之间的任何值！！

> html 根元素 继承的就是 浏览器设置的字体大小！除非重写一个具体单位来覆盖
> 所以表面上 rem 根据的是 html 根元素的字体大小，但实际可能是来自浏览器的设置大小

如果我们使用 rem，请确保无论用户如何设置自己的浏览器，我们都要显示正常

---

# JavaScript

## 复制一个数组有哪些方法？哪个方法最好

## cdn 的作用和原理？

## 响应式的浏览器原理？

## async await 原理？

## 了解 vue-lazyloader 吗

## 如何判断一个类型是数组？instanceOf 实现？

## 提交表单有哪些常用方法？应用层通信层发生了哪些过程？

## let、const 及 var 的区别？
> 这个问题，涉及到变量提升

    console.log(a);  // undefined
    var a = 1;

  上述代码就是一个变量提升  
  在声明变量之前，我们就可以使用它

  这段代码可以翻译为： 

    var a   
    console.log(a)
    a = 10  

  好了，不仅变量可以提升  
  函数也会提升  

    console.log(a)  // f a(){}
    function a(){}
    var a = 1

看了上面两个例子，我们差不多知道 var 存在的问题了  
接下来我们来看 let 和 const  

    var a = 1
    let b = 1
    const c = 1
    console.log(window.b)  //undefined
    console.log(window.c)  //undefined

    function test(){
      console.log(a)
      let a
    }
    test()



我们发现，使用了 let 和 const 后  
变量不会被挂载到 window 上
这就和 var 有了明显的区别

---

## 解构赋值和拓展运算符

## Set/Map 数据结构

---

## null 和 undefined 有什么区别

- undefined  声明了变量，但没有赋值，它存在，但没有值
- null 没有值，根本就不存在，没有任何可读的东西              
 <br>


    var a ;      

声明了，但没有赋值，此时 a 就是 undefined


   <br>

   ##### 用 typeof 判断类型，会看到两者的区别

    typeof(null)  //object
    typeof(undefined)  //undefined



  ##### 和数字相加的区别
  - undefined + 数字 = NaN
  - null + 数字 = 数字
---

## 事件委托是什么？主要解决什么问题？

---

## 了解基本的数据类型吗

##### 先了解一下为什么需要数据类型？
计算机中，不同数据占据的存储空间是不同的  
为了充分利用空间，需要定义不同数据类型 

> 简单类型又叫基本数据类型，或者值类型  
> 复杂类型又叫做引用类型

当我们声明一个变量时  

    var x = "变量"  

实际是在内存空间中开辟了一块地方来存储这个数据  
但是我们调用这个变量的时候不能靠输入十六位进制来取值吧，太麻烦了  
所以起了一个变量名，实际就是在引用内存地址

#### String
单引号或双引号
<br><br>

#### Number

常规包含：
- 浮点类、整数
- 二进制
- 十六进制

三个特殊值：
- Infinity，无穷大，大于任何值
- -Infinity，无穷小，小于任何值
- NaN，非数值
<br><br>

#### Boolean

有两个值
- true == 1
- false == 0

javascript 中任何值都可以转换为布尔值。

<br><br>

#### Undefined

变量没有赋值时的默认值

<br>

#### Null

---

## Promise 设计模式？

## 移动端的触摸事件了解吗

## Interator 迭代器

## 闭包怎么理解？项目中用到过吗

## 一般怎么判断基本的数据类型

## 普通函数和构造函数的区别

## 深拷贝一个数组怎么做

## async / await 及实现原理

## 了解 return 吗？

## AJAX 核心四步操作？交互过程？

## 底层运行机制：微任务宏任务和事件循环机制

## Generator 生成器函数

## 手写懒加载函数

## 说一下原型链吧（proto，prototype）

## JS 底层运行机制：单线程和同步异步编程

## 了解作用域吗？怎么预防作用域污染

## 堆栈内存的理解

## 箭头函数和普通函数的区别

## 说一下拷贝对象吧，深拷贝浅拷贝

## fetch 基础和实战

## 谈一谈变量提升？

## json 的数据格式都介绍一下

## JS 是否了解过函数式编程

## 跨域怎么处理？都知道什么方法？ jsonp 和 cors 哪个更安全

## 异步的处理方式？都是怎么处理的

sudo sed -i 's/mirrorlist=/#mirrorlist=/g' CentOS-Base.repo CentOS-AppStream.repo CentOS-Extras.repo
sudo sed -i 's/#baseurl=/baseurl=/g' CentOS-Base.repo CentOS-AppStream.repo CentOS-Extras.repo
sudo sed -i 's/http:\/\/mirror.centos.org/https:\/\/mirrors.aliyun.com/g' CentOS-Base.repo CentOS-AppStream.repo CentOS-Extras.repo

yum makecache

CENTOS 7

# Vue

## 双向绑定原理是怎么实现的？

## Vue 和 Vuex 的差异？

## Vue 设计原则的理解？

## vue 从 data 改变到页面渲染的过程

## 如果没有 vue-router，你们还会做单页面应用吗

## Vuex 的触发过程 （actions，state，view）？

## 关于 VUE 的性能优化

## 双向绑定原理？

## 组件的设计原则

## 对 flutter 的了解

## 讲一下 vue 有哪些特性

## 谈谈对 Vue 组件化的理解

## 为什么使用 vue 框架而不是使用其他框架

## vue 中 key 的作用？说说对它的理解

## 对 Vue 源码了解吗

## vue 里的虚拟 dom 是怎么回事

## Vue 的设计思路有了解吗

# 计算机和浏览器原理

## 如何保证浏览器不受脚本的恶意攻击

---

## 浏览器渲染页面的过程

## 浏览器输入 URL 到整个页面渲染出来经历的过程详细讲解一下

# 网络协议

## http 和 https 有什么区别？比如性能方面

## http 的请求头都包括哪些？

## OSI 七层协议？

## dns 劫持是什么？

## 304 状态码的理解？

## 移动端 300 毫秒延迟怎么解决？

## https 讲一下过程

## 移动端点击穿透

## TCP 和 UDP 的区别？TCP 怎样保证传输可靠

## http2.0 了解多少

## http 各种状态码的含义

# Getting Started

# 其他

## 做微信小程序有什么亮点，什么难点？

## 用户反馈进入页面白屏，如何排查错误

## 你在团队中的优势是什么？尤其是技术方面

## 前端性能优化？

## 登陆注册的前后端处理机制

## 加密策略 encodeURI-Component 和 MD5

## 存储方案 cookie、webStorage、session 等

## 用户权限和登陆的校验处理

## 常见的排序方法？都熟悉哪些

## 做 PC 端多一些还是移动端多一些？遇到了什么难以解决的兼容性问题？

## nodejs 用过吗？

## 同一个对象上绑定了多个事件，执行顺序是怎样的

## 正则表达式的使用程度

## vue 的生命周期讲一下

## token 的校验处理

## 有遇到过跨域问题吗？跨域的原理是什么

## 谈谈对 MVC、MVP、MVVM 的理解？

## 前端缓存了解多少？分为哪几类

## 对 SEO 有什么了解

## 前端鉴权了解过吗？

## 设计模式了解多少？

## 快速排序的思路是怎样的

## 对 JS 单线程的理解

## 事件模型能介绍一下吗

## 原型链理解多少？

## 对算法了解怎么样？常用的排序算法？

## 讲一下性能优化？具体哪些优化的收益更大一些

This header won't appear in the sidebar table of contents.
sudo cp /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak

sudo wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo

sudo rpm -import http://mirrors.aliyun.com/centos/RPM-GPG-KEY-CentOS-7
sudo rpm -Uvh http://mirrors.aliyun.com/epel/epel-release-latest-7.noarch.rpm
sudo sudo rpm -import http://mirrors.aliyun.com/epel/RPM-GPG-KEY-EPEL-7
sudo rpm -import http://mirrors.aliyun.com/epel/RPM-GPG-KEY-EPEL-7Server
sudo yum install -y yum-axelget

#防火墙
在学习阶段可以先关闭防火墙，保证端口不受访问限制，以下是 LINUX 管理防火墙的基本指令

sudo systemctl stop firewalld.service

练习时也可以永久关闭防火墙

sudo systemctl disable firewalld.service

查看防火墙状态

sudo systemctl status firewalld.service

关闭 setlinux

修改配置文件

sudo vim /etc/selinux/config

修改 SELINUX 值为 disabled，永久有效但需要重起系统

SELINUX=disabled

可以执行以下命令，立刻生效（建议和上面命令一起使用）

setenforce 0

#基本操作
关机重起

#关机
init 0

#重起系统
reboot

查看版本

cat /etc/redhat-release

语言支持

如果安装软件时提示 Failed to set locale, defaulting to C 或中文出现乱码，是因为在安装时没有选择设置 language support 语言支持选项，下面是安装后的调整方法

编辑语言文件

vim /etc/profile.d/lang.sh

设置以下内容

export LANG=en_US.UTF-8
export LANGUAGE=en_US.UTF-8
export LC_COLLATE=C
export LC_CTYPE=en_US.UTF-8

重新加载配置

source /etc/profile.d/lang.sh
