# 【译】为什么要了解HTTP
原文地址：[Why should I care about HTTP?](https://dev.to/raddevon/why-should-i-care-about-http-2em3)  
原作信息：by Devon Campbell. Dec 15 '18 Originally published at raddevon.com on Dec 14, 2018  
关键词：HTTP ,BEGINNERS
***
正文：  
> HTTP are the four letters at the beginning of your URLs, right? That’s all you really have to know about it to build for the web, but, just like [understanding binary](https://raddevon.com/articles/the-basics-of-binary-and-other-number-systems-for-web-developers/), it can help you understand problems you otherwise wouldn’t. It’s not required material, but it makes you a more well-rounded developer.  

“HTTP”是URLs地址开头的前四个字母，对吧？这就是你构建网站所必须要知道它的原因。就像[理解二进制(binary)](https://raddevon.com/articles/the-basics-of-binary-and-other-number-systems-for-web-developers/)一样，它也会帮助你理解你在其他方面不会理解的问题。他不是你必须要掌握的知识点(material:材质、物料)，但是理解他会使你成为一个更全面(well-rounded)的开发者。

> Since it’s the primary communication protocol our software will be using, let’s learn a little about HTTP!

作为我们软件所必须要遵循的基本通信协议(communication protocol)，让我们来学习一下HTTP吧！

### 什么是HTTP？(What is HTTP?)
> HTTP stands for hypertext transfer protocol. That’s a set of rules (protocol) for sending and receiving (transfer) web pages (hypertext). Even though it’s still called HTTP, it’s now used for sending lots of things besides hypertext — for example, JSON and images.

HTTP就是超文本传输协议(Hypertext Transfer Protocol)，他是一个为发送和接收（传输）web页面（超文本）而设定的规则（协议）。尽管它被称作超文本传输协议(HTTP)，但它还可以被用来发送许多除超文本以外的其他内容 - 比如，JSON和images。

### HTTP是如何工作的？(How does HTTP work?)
![HTTP是如何工作的？](./images/http-flowchart.png)

> HTTP communication happens between a client and a server. The client makes the HTTP request, and the server responds to it. Your web browser is an HTTP client. When you visit a web page, your browser sends an HTTP request to a server which sends a response. It’s (almost) that simple.

HTTP通信发生在客户端和服务器之间。客户端发起HTTP请求，服务器响应客户端的请求。你的web浏览器就是一个HTTP客户端。当你浏览一个web页面的时候，你的浏览器发送一个HTTP请求到一个能响应的服务器上，它（几乎）就是这么简单。

> Actually, a single web page is usually comprised of multiple requests. What usually happens is a request is made for some HTML, and the server responds with the HTML. The browser starts rendering the HTML and makes additional requests for any other resources it needs to render the page — like Javascript files, CSS files, and images.

事实上，一个简单的web页面通常由多种请求组成(comprised:由...组成)。