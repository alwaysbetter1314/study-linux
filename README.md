# linux-skills
collection for linux tools and useful skills

## 查看端口占用
- netstat  -anp  |grep   端口号
> 查看对应端口占用
- netstat   -nultp
> 查看所以已使用端口状况
- lsof -i:端口号 
> 用于查看某一端口的占用情况，比如查看8000端口使用情况，lsof -i :8000
- netstat -tunlp |grep 端口号，
> 用于查看指定的端口号的进程情况，如查看8000端口的情况，netstat -tunlp |grep 8000
```
-t (tcp) 仅显示tcp相关选项
-u (udp)仅显示udp相关选项
-n 拒绝显示别名，能显示数字的全部转化为数字
-l 仅列出在Listen(监听)的服务状态
-p 显示建立相关链接的程序名
```
## shell版99乘法表
```bash
for i in `seq 9`
do
    for j in `seq $i`
    do
        echo -n "$i*$j=$[i*j]"
    done
    echo
done
```

## 和电脑猜拳
```bash
game=(石头 剪刀 布)
num=$[RANDOM%3]
computer=${game[$num]}
#随机生成出拳可能并存入数组game[$num]:game[0],game[1],game[2]分别代表石头,剪刀,布
echo "请根据以下提示选择出拳手势"
echo "石头:1 剪刀:2 布:3"
read -p "请出拳:(1,2,3)": person
case $person in
1)
 if [ $num -eq 0 ];then
  echo "平局"
 elif [ $num -eq 1 ];then
  echo "你赢"
 else
  echo "计算机赢"
 fi;;
2)
 if [ $num -eq 0 ];then
  echo "计算机赢"
 elif [ $num -eq 1 ];then
  echo "平局"
 else
  echo "你赢"
 fi;;
3)
 if [ $num -eq 0 ];then
  echo "你赢"
 elif [ $num -eq 1 ];then
  echo "计算机赢"
 else
  echo "平局"
```

# openbullet2
```
docker run --name openbullet2 --rm -p 8069:5000 -v /root/openbullet2:/app/UserData/ -it openbullet/openbullet2:latest
```
