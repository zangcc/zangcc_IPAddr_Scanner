# zangcc_IPAddr_Scanner

这算是一个爬虫图形化工具了，因为最近在HW，所以很多IP需要处理，特别是IP归属地的排查情况，每天要写表格统计十分麻烦。因此开发这个工具来减轻工作量，并解决实际问题，提高办公效率。

JDK版本支持:

java 16.---> java16_IPAddr_Scanner.jar

java 8（也就是传说中的最稳定最常用版本jdk1.8） --->java8_IPAddr_Scanner.jar

**都建议用命令运行！java -jar 去运行文件，因为在命令行能看到程序运行的内容，可以更直观看到爬取的进度。如果直接双击运行jar，会让你觉得程序卡死，其实不是，只是程序在扫描，等扫描完了再显示回文本框而已，所以我的建议是用命令行去运行，能够看得更清楚。**

**这里顺带提一句，再提醒一句，用纯真去扫描是很慢的，但是不代表不行，仅仅只是慢而已，可以在命令行看得爬取进度的。**

<img src="https://user-images.githubusercontent.com/64825932/182035441-c5b701da-0c3d-43d4-ae6c-41afee9d9304.png" width="650px">


**开发的原因**

1、网络上免费查询IP归属地的有站长之家、微步社区、IP138.com、纯真网等等。

2、微步的批量查询需要会员，得充钱。

3、站长之家的批量IP会自动过滤重复的IP地址，对于列表中重复的IP（有不同的攻击行为）很难做到统计。并且这个自动过滤重复IP的功能无法关闭，默认开启。

4、其他的免费查询网站每次查询只能50条，而且每次输入都要输入验证码，十分不方便。

5、以上所有网站，批量扫描结果都不能下载结果，每次复制归属地的地址都不能精准复制，必须整个页面一起复制，最后再把无关的信息一一删除，实在是麻烦。

**解决的实际问题**

1、自由搜索，可以批量，可以单个。

2、IP信息和归属地分开，这样复制的时候就不会连在一起复制，可单独精准复制归属地。

3、国内IP库是不一样的，所以查询结果的归属地址会有出入。因此我加了两个算是比较权威的平台来爬取，一个是IP138.com的，这个的IP库就是站长之家的库，而且百度的IP查询也是用的这个站点的，加上这个站点爬取的速度快，所以用起来也舒服。另一个是纯真网————“中国IP地理位置数据库首创者，超十六万软件开发者和企业共同改进，数十年耕耘专注于打造精准的全球IP地址数据库。”缺点是国外的地址会有所出入的，但是国内的地址非常准确！

**注意事项**

1、一次不能批量爬取超过100个，否则会报错，被官网封禁，要一天后才能解封，所以谨慎大量、频繁、重复地批量爬取。

2、批量查询的IP要换行，且不能有逗号或者其他任何的字符。

**使用步骤**

1、cmd打开，命令行运行：

java -jar java16_IPAddr_Scanner.jar

<img src="https://user-images.githubusercontent.com/64825932/182025623-a0711b8c-9106-4267-a8b7-2932451214a8.png" width="650px">

2、显示结果：

<img src="https://user-images.githubusercontent.com/64825932/182025808-77653103-a1cb-4a62-97a4-90ad38eab396.png" width="650px">

注意了，这里的纯真查询爬取会相对于IP138来说会很慢，但是都能爬取得到，工具界面 **显示（未响应）**是正常现象！！可以在命令行处看到程序在正常运行，IP地址和输出的结果都在正常显示，只需要等待爬取结束，工具界面就会正常显示了，所以慢慢等就行。

3、IP318的爬取结果和上面的一样，就是速度会快很多，但是一定不能一次性扫太多，分开来爬，保证不被封禁。

<img src="https://user-images.githubusercontent.com/64825932/182025993-9f496e4e-fa8e-4f34-9606-9daaa6375db0.png" width="650px">
细心的会发现，两个网站爬取的地址会有所出入，这是正常的，因为IP库不一样。

4、如果怕得太多或者是太频繁，网站就会把你封了，工具也用不了，就像下面这样：

<img src="https://user-images.githubusercontent.com/64825932/182026062-fa6286f4-a5ad-4b50-8916-272a162b11df.png" width="650px">


