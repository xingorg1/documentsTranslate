# 【译】为什么要了解HTTP
原文地址：[Why should I care about HTTP?](https://dev.to/raddevon/why-should-i-care-about-http-2em3)  
原作信息：by Devon Campbell. Dec 15 '18 Originally published at raddevon.com on Dec 14, 2018  
关键词：HTTP ,BEGINNERS
***
正文：  
> HTTP are the four letters at the beginning of your URLs, right? That’s all you really have to know about it to build for the web, but, just like [understanding binary](https://raddevon.com/articles/the-basics-of-binary-and-other-number-systems-for-web-developers/), it can help you understand problems you otherwise wouldn’t. It’s not required material, but it makes you a more well-rounded developer.  

“HTTP”是URLs地址开头的前四个字母，对吧？这就是你构建网站所必须要知道它的原因。就像[理解二进制(binary)](https://raddevon.com/articles/the-basics-of-binary-and-other-number-systems-for-web-developers/)一样，它也会帮助你理解你在其他方面不会理解的问题。他不是你必须要掌握的知识点(material:材质、物料)，但是理解他会使你成为一个更全面的开发者。  
【注：(well-rounded：更全面的)】  
> Since it’s the primary communication protocol our software will be using, let’s learn a little about HTTP!

作为我们软件所必须要遵循的基本通信协议(primary communication protocol)，让我们来学习一下HTTP吧！  

## 什么是HTTP？(What is HTTP?)
> HTTP stands for hypertext transfer protocol. That’s a set of rules (protocol) for sending and receiving (transfer) web pages (hypertext). Even though it’s still called HTTP, it’s now used for sending lots of things besides hypertext — for example, JSON and images.

HTTP就是超文本传输协议(Hypertext Transfer Protocol)，他是一个为发送和接收（传输）web页面（超文本）而设定的规则（协议）。尽管它被称作超文本传输协议(HTTP)，但它还可以被用来发送许多除超文本以外的其他内容 - 比如，JSON和images。

## HTTP是如何工作的？(How does HTTP work?)
![HTTP是如何工作的？](./images/http-flowchart.png)

> HTTP communication happens between a client and a server. The client makes the HTTP request, and the server responds to it. Your web browser is an HTTP client. When you visit a web page, your browser sends an HTTP request to a server which sends a response. It’s (almost) that simple.

HTTP通信发生在客户端和服务器之间。客户端发起HTTP请求，服务器响应客户端的请求。你的web浏览器就是一个HTTP客户端。当你浏览一个web页面的时候，你的浏览器发送一个HTTP请求到一个能响应的服务器上，它（几乎）就是这么简单。

> Actually, a single web page is usually comprised of multiple requests. What usually happens is a request is made for some HTML, and the server responds with the HTML. The browser starts rendering the HTML and makes additional requests for any other resources it needs to render the page — like Javascript files, CSS files, and images.

事实上，一个简单的web页面通常由多个请求组成。通常情况下，一个请求由一些HTML发起，然后服务器响应这个HTML请求。浏览器开始渲染这个页面，紧接着会发起更多渲染这个页面时所需的其他资源的请求 —— 像JavaScript文件、CSS文件和图片等的请求。  
【注：(comprised:由..组成)、(additional：额外的)】

## 请求的部分组成 (Parts of a Request)

> Here’s what a raw request to RadDevon.com for the home page looks like:

下边就是访问RadDevon.com的主页时原始(raw：未加工的)请求的样子：

```
GET / HTTP/2
Host: raddevon.com
User-Agent: curl/7.54.0
Accept: */*
```

> When you type raddevon.com into your address bar and press return, your browser sends this request to my host. Here are the parts:

当你在地址栏输入“raddevon.com”并按下回车后，你的浏览器就会发送这个请求到我的主机上，以下是部分内容：

> * ```GET``` – The request method. It tells the server what the request is intended to do. This request wants the server to send back some data. MDN has a nice request method reference.  

* ```GET``` —— 请求方法。它告诉服务器这个请求想要做什么。这个请求希望服务器能够返回一些数据。MDN有一个很好的[请求方法参照表](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)。  
【注：(be intended to do：打算做...，想要...)】

> * ```/``` – The resource we’re requesting. Since the homepage is at the root of the server, that’s the resource we’re requesting here.

* ```/``` —— 我们请求的资源地址。由于我们请求的主页就在服务器的根目录下，所以“/”就是我们请求资源的地址。  
【注：(Since：自从、因为、由于、既然、自...以来)】

> * ```HTTP/2``` – The protocol. This particular request is made using version 2 of HTTP.

* ```HTTP/2``` —— 协议。这说明了该特殊请求是基于http/2.0版本的协议发出的。  
【注：(particular：特别的、详细说明)】
