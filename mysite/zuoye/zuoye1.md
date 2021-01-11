## **一、安装Ubuntu-20.04-Server** ##

1、下载Ubuntu 20.04

2、在虚拟机中安装Ubuntu20.04，添加光驱

3、启动虚拟机


## **二、配置虚拟机网络** ##

1、网卡1使用桥接网卡选择对应的电脑网卡；

2、在高级设置中的混杂模式选择全部允许；
![](http://qmrc945r4.hn-bkt.clouddn.com/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20210111145209.png)

3、网卡2连接方式选择仅主机网络。
![](http://qmrc945r4.hn-bkt.clouddn.com/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20210111145214.png)

## **三、配置命令行** ##

1、安装网络工具net-tools；

	sudo apt-get install
    
	sudo apt install net-tools
![](http://qmrc945r4.hn-bkt.clouddn.com/ea5950afea74b1845ab83cb70b29bcf.png)

2、输入ifconfig命令查看虚拟机guest的主机地址；

	ifcofig
![](http://qmrc945r4.hn-bkt.clouddn.com/c8d30f99747acb0ed6ea59a8bd4e09e.png)

3、在host主机端调出CMD命令指示符，查询host主机ip地址；

	ipconfig
![](http://qmrc945r4.hn-bkt.clouddn.com/ipconfig.png)


4、在虚拟机中的guest主机中ping通host主机；

	ping 192.168.56.1
![](http://qmrc945r4.hn-bkt.clouddn.com/006dff769ca402f637b996ddb58d964.png)

5、在host主机中ping通虚拟机中的guest主机。

    ping 192.168.56.101
![](http://qmrc945r4.hn-bkt.clouddn.com/194a1858da25e847d546ff05f8566ad.png)
    

## **四、使用http server** ##

1、虚拟机中的guest主机复制出github中的html包（此处弄了两个）；

    sudo apt install git
    git clone https://github,com/zxuqian/html-css-examples.git
	git clone https://github.com/html5-boilerplate.git
![](http://qmrc945r4.hn-bkt.clouddn.com/bdc21096859bda1ae5f7cfc75b9e1c9.png)
![](http://qmrc945r4.hn-bkt.clouddn.com/0f4e588fa37d177459e24aadf6fb8d5.png)
![](http://qmrc945r4.hn-bkt.clouddn.com/90247456fc038db4e088a869faa15bf.png)
![](http://qmrc945r4.hn-bkt.clouddn.com/395f518c03d123bf7af3f71a77ee4a8.png)

2、使用ls命令查看目录；
	ls
![](http://qmrc945r4.hn-bkt.clouddn.com/d672f17b0801e267d3e30de35c975be.png)

3、在虚拟机终端中开通http server服务；
	sudo npm install http-server -g
	http-sever
    python3 -m http.server --directory /root 8023
    python3 -m http.server --directory html-css-examples 8080
![](http://qmrc945r4.hn-bkt.clouddn.com/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20210111141318.png)
![](http://qmrc945r4.hn-bkt.clouddn.com/0413ae469288b143446c7eb8a34c11c.png)

4、在虚拟机中通过浏览器访问guest主机的地址。

    127.0.0.1:8080
![](http://qmrc945r4.hn-bkt.clouddn.com/28639f2e49b726baaed59e9d48995bf.png)

