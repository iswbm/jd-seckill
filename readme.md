## 0. 最新下载地址

原项目无法下载了，最新脚本代码请点击这边下载:https://wws.lanzous.com/iMmQ8jwxjng

## 1. 环境搭建

**第一步**

把项目代码（https://wws.lanzous.com/iMmQ8jwxjng） 下载到本地并解压。

**第二步**

进入到解压后的目录中，使用 venv 创建一个虚拟环境，注意一定要使用 Python 3，创建完成后，使用如下命令进入进入虚拟环境。

```shell
# 创建虚拟环境
$ python3 -m venv .

# 进入虚拟环境
$ source bin/activate
```

不同电脑系统操作虚拟环境的方法不一样，上面我的命令适用于 Mac 和 Linux，如果 你的电脑是 Windows 的请参考我的另一篇文章进行学习：http://python.iswbm.com/

![](http://image.iswbm.com/image-20210103100700014.png)

**第三步**：

往虚拟环境中安装依赖包

如果是 mac 或者 linux 只要执行这条命令就行

```shell
$ python -m pip install -r requirements.txt
```

而如果你使用 windows ，在依赖中有一个 `lxml` 库，这个库在 windows 中你使用 pip 是安装不上的，你得从网上下载 wheel 文件来手动安装，然后再执行上面的命令，下载链接在下面，记得选择对应 Python 的版本，由于这个页面里的 lxml 版本是 `4.6.2`，因此你要手动改动 `requirements.txt` 文件里的 lxml 版本。

```shell
# lxml 下载地址
https://www.lfd.uci.edu/~gohlke/pythonlibs/#lxml
```

如此你的运行环境就搭建好了。

## 2. 准备工作

在开始抢之前 ，有一些配置需要你手动弄好，主要有这几项：

**京东的 eid 和 fp**

登陆你的京东网页版，随便选个商品下单，然后使用 浏览器的F12 跟踪 `_JdTdudfp` 变量，就能得到 eid 和 fp

![](http://image.iswbm.com/image-20210103100818959.png)

并把这两个值写入到项目根目录下的 `config.ini` 文件中。

在 `config.ini` 中还有一个很重要的设置，那就是抢购时间 `buy_time`，记得设置成未来的最近一天的日期。

![](http://image.iswbm.com/image-20210103100925244.png)

## 3. 开始抢购

上面的配置全部完成后，就可以开始抢了。

抢的过程分为两步：

**第一步：开 PLUS会员**

某东真行，这一波营销做的，原来是想让我开 PLIUS 会员，我一个网易云音乐会员都舍不得开的人，居然为了抢茅台而开了一个我用都用不上的 PLUS 会员，这个会员只能最少季付也要 78元，我忍痛开了，就当是投资了。

**第二步：预约抢购**

只有预约的用户才能参与抢购，你可以手动搜索 `茅台` 进去预约，也可以使用这个脚本来帮你预约。

执行 `python main.py` 然后输入 `1`，会弹出一个二维码，打开你手机上的 京东 app 授权登陆，接着脚本就会去帮你预约。

![](http://image.iswbm.com/image-20210103100940709.png)



**第二步：开始抢购**

一切都准备好了，你只要在快到早上 10 点的时候执行 `python main.py`，然后输入 `2` ，就行了。接下来就看你的运气了。

![](http://image.iswbm.com/image-20210103100953967.png)

以上就是使用 jd_seckill 抢茅台的完整过程，我写得非常清楚，甚至比 github 上的官方文档还要清楚。。真的是为广大读者谋福利操碎了心。

如果有非技术朋友不知道如何搭建这个环境，可以联系我微信：hello-wbm

最后祝大家好运，抢个好采头~
