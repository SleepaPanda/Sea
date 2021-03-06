## Python 网络编程

## Header请求

HTTP 协议的 Header 是一块数据区域，分为请求头和响应头两种类型，客户端向服务区发送请求时带的是请求头，而服务器响应客户端数据时带的是响应头。

请求header的内容

#### 1) accept

表示当前浏览器可以接受的文件类型，假设这里有 image/webp，表示当前浏览器可以支持 webp 格式的图片，那么当服务器给当前浏览器下发 webp 的图片时，可以更省流量。

#### 2) accept-encoding

表示当前浏览器可以接受的数据编码，如果服务器吐出的数据不是浏览器可接受的编码，就会产生乱码。

#### 3) accept-language

表示当前使用的浏览语言。

#### 4) **Cookie**

很多和用户相关的信息都存在 Cookie 里，用户在向服务器发送请求数据时会带上。例如，用户在一个网站上登录了一次之后，下次访问时就不用再登录了，就是因为登录成功的 token 放在了 Cookie 中，而且随着每次请求发送给服务器，服务器就知道当前用户已登录。

#### 5) user-agent

表示浏览器的版本信息。当服务器收到浏览器的这个请求后，会经过一系列处理，返回一个数据包给浏览器，而响应头里就会描述这个数据包的基本信息。



**响应头**里的关键信息有：

#### 1) content-encoding

表示返回内容的压缩编码类型，如“Content-Encoding :gzip”表示这次回包是以 gzip 格式压缩编码的，这种压缩格式可以减少流量的消耗。

#### 2) content-length

表示这次回包的数据大小，如果数据大小不匹配，要当作异常处理。

#### 3) content-type

表示数据的格式，它是一个 HTML 页面，同时页面的编码格式是 UTF-8，按照这些信息，可以正常地解析出内容。content-type 为不同的值时，浏览器会做不同的操作，如果 content-type 是 application/octet-stream，表示数据是一个二进制流，此时浏览器会走下载文件的逻辑，而不是打开一个页面。

#### 4) set-cookie

服务器通知浏览器设置一个 Cookie；通过 HTTP 的 Header，可以识别出用户的一些详细信息，方便做更定制化的需求，如果大家想探索自己发出的请求中头里面有些什么，可以这样做：打开 Chrome 浏览器并按“F12”键，唤起 Chrome 开发者工具，选择 network 这个 Tab，浏览器发出的每个请求的详情都会在这里显示。

