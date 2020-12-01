# linux-skills
collection for linux tools and useful skills

## 查看端口占用
- netstat  -anp  |grep   端口号
> 查看对应端口占用
- netstat   -nultp
> 查看所以已使用端口状况
- lsof -i:端口号 
> 用于查看某一端口的占用情况，比如查看8000端口使用情况，lsof -i:8000
- netstat -tunlp |grep 端口号，
> 用于查看指定的端口号的进程情况，如查看8000端口的情况，netstat -tunlp |grep 8000
```
-t (tcp) 仅显示tcp相关选项
-u (udp)仅显示udp相关选项
-n 拒绝显示别名，能显示数字的全部转化为数字
-l 仅列出在Listen(监听)的服务状态
-p 显示建立相关链接的程序名
```
