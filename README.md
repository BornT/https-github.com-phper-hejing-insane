# insane自动化测试接口压测工具

一个 Go 编写的 http 并发测试客户端.

技术栈：go react

```
Header
    KEY:Content-Type VALUE:application/x-www-form-urlencoded // 发送表单数据
    KEY:Content-Type VALUE:application/json // 发送Json数据
Body
    KEY:username  TYPE:Int  LENGTH:10  DEFAULT:insane
    KEY:password  TYPE:string  LENGTH:10  DEFAULT:
    KEY:age  TYPE:Int  LENGTH:2  DEFAULT:

    sendData:{username:"insane", password:"wI27Ayy2S2", age:24} // 不填写默认值会随机生成一个值
Cookie
        sample1:123;sample2:456;sample3:789;...
```

## 使用

示例的机器只有 1M 带宽，方便大家观看，要使用可以下载到本地测试。

进入到项目根目录

windows: insane.exe

linux: ./insane

访问：http://localhost:9500

## 压测例子

压测机器：4 核 8G，模拟 5000 用户，发起 http 请求

受压测机器：2 核 4G，获取参数写入 log

#### go

![go](https://i.imgur.com/4Oczg88.png)
![go](https://i.imgur.com/voq27ou.png)

#### php

![php](https://i.imgur.com/NGkJuQM.png)
![php](https://i.imgur.com/KUJyFEB.png)
