Socat公网ipv6转发内网ipv4
-----------
系统要求：支持CentOS 6+ 、Debian 7+、Ubuntu 14+

脚本说明：脚本默认开启`UDP`、`TCP`转发，带开机自启功能，且一次只能转发单个端口，如果想转发多个端口请重复运行本脚本。

使用`root`运行以下命令：

    wget https://raw.githubusercontent.com/lzw981731/Socat/master/socat.sh && bash socat.sh

按要求输入ipv6端口，要转发的ipv4端口即可！

默认转发localhost

> 原来的脚本是将本地ipv4端口映射到指定的远程服务器端口上，现改为将本地localhost的ipv4端口映射到到公网ipv6的端口上，
> 这样就算一些应用不支持ipv6访问，也可以通过映射ipv4端口的形式来进行ipv6的访问
>
> 开机自启功能使用的是rc.local
>
> 参考文章：
> [用SOCAT简单实现公网IPV6端口转发内网IPV4访问](https://blog.csdn.net/alal001/article/details/86365856)
> [Ubuntu rc.local 的开启与配置](https://blog.csdn.net/qz652219228/article/details/125107694)
