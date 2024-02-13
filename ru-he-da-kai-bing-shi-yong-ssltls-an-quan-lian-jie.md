---
description: 我们这里列举了各个矿工常用的挖矿软件开启SSL/TLS安全连接的方法，以便大家能够正常使用糖心池加密转发服务！
---

# 如何打开并使用SSL/TLS安全连接

**敬请注意：如果您使用的是ASIC矿机，您可以在图形用户界面自行开启SSL/TLS，如您不知道如何开启，请您联系您的矿机生产商，因为所有的矿机都支持！**

**CPU：**

XMRig：在XMRig的配置文件（config.json）的pools参数里找到tls，将false改为true即可开启SSL/TLS

**GPU：**

GMiner：在.bat文件的最后加入--ssl 1 即可开启SSL/TLS，0则为关闭SSL/TLS

NBMiner：在.bat文件的-o参数处，将stratum+tcp改为stratum+ssl即可开启SSL/TLS，如-o stratum+ssl://pool.exp.com:8888

其他许多挖矿工具其实也大同小异，如果不知道可以去找找挖矿软件的文档！大部分有stratum+tcp://什么的就直接替换成ssl就行了。注意，有些挖矿软件的ssl参数可能是true（开启）false（关闭）而不是GMiner的1（开启）0（关闭），自己试试就知道了，很容易的。

<mark style="color:red;">**糖心池的所有连接你都要用SSL/TLS，不然都没法连上，唯一的区别就是你可以选全程加密或半程加密，总之矿机到糖心池服务器的这一程一定要加密！**</mark>
