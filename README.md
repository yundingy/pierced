# pierced
钉钉内网穿透

TCP 穿透需要在数据库里面执行：
GRANT ALL PRIVILEGES ON *.* TO root@'%' IDENTIFIED BY '123456';
FLUSH PRIVILEGES;
数据库连接命令：
mysql -h vaiwan.com -u root -p -P 1234 //端口号地址

第一步： 
clone  git仓库执行命令：git clone https://github.com/open-dingtalk/pierced.git 

 
第二步：开始配置
注意：在pierced根目录下执行命令

Mac:

 (1) 

cd mac_64

 (2)

./ding -config=./ding.cfg -subdomain=abcde 8080

Windows:

 (1) 

cd windows_64

 (2)

ding -config=ding.cfg -subdomain=abcde 8080

第三步：测试
启动完客户端后，你访问http://abcde.vaiwan.com/xxxxx都会映射到 http://127.0.0.1:8080/xxxxx

