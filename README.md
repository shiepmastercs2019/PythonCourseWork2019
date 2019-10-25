# PythonCourseWork2019
Python大作业交流展示
(注意Python的P要大写)

这里是一个Python大作业的交流展示分享的地方。

前期大家可以放自己的需求表在上面，虽然可能会有借鉴需求，同时也鼓励借鉴，但是互联网就是开放的，交流才会有进步，在学习的阶段更加鼓励能够把需求实现出来，这才是重要的。后面希望同学们在每个需求上增加相应项目的源代码链接，增加彼此交流。

## 目录

模型研究

* [面向股市的量化交易模型研究](#stockAnalysize)

图像处理

* [基于图像处理的自动连连看](#imageAutoWatch)

* [基于单目视觉的目标测距](#monocularVisionRange)

人脸属性

* [帅哥美女年龄、颜值打分系统](#girlBoyRank)

语言处理

* [基于深度学习的古诗生成器](#ancientPoetryGenerate)

* [某地区电力工单项目分析](#electricAnalysize)

* [基于深度学习的音乐生成(Jazz)](#musicGenerate)

人脸识别

* [Python考勤点名](#checkInDetection)

* [实时人脸检测特征提取并识别](#faceDetection)

智能推荐

* [智能电影推荐](#movieRecomm)

* [智能书籍推荐](#BookRecomm)

物体检测

* [自动驾驶交通指示牌识别](#autoDrive)

* [基于深度学习的植物识别](#plantIdentificate)

* [基于Python的口红色号识别器](#lipstickRecog)

* [自动驾驶路况检测系统](#roadStatusRecog)

* [基于神经网络的猫狗识别](#catDogRecog)

* [验证码识别](#vertificationCodeRecog)

* [基于深度学习的故事人物情感变化分析](#newsSpider)

网络爬虫

* [爬虫分析<我和我的祖国>影评
](#movieSpider)

* [爬虫分析之京东商品数据分析](#jdGoodsSpider)

* [基于爬虫的智能租房推荐系统](#lianjiaSpider)

* [爬虫分析(汽车价格)
](#carPriceSpider)

* [新浪微博数据爬虫爬取](#weiboSpider)

* [游山玩水旅游-爬虫](#travelSpider)

* [基于Python的招聘信息分析](#zhaopinSpider)

* [我该去哪儿](#whereCitySpider)

* [一种爬取电影评论等数据并可视化分析的方法](#filmReviewSpider)

* [去哪儿网国庆旅游景点数据爬虫分析](#scenicSpotSpider)

* [短租数据大师](#shortRentSpider)

* [12306点触验证码的识别登陆及自动抢票](#verificationCodeSpider)

游戏设计

* [猫咪跑酷](#catParkourGame)

* [植物大战僵尸改编版](#plantsV.S.ZombiesGame)


<!--[Hs blog](http://hslovelal.top) --> 

## 项目:面向股市的量化交易模型研究
<span id="stockAnalysize"/>

### Introduction

本设计面向中国金融股市A股，获取自04年以来的所有工作日交易数据，其中包括交易日期、股票代码及名称、所属地区、所属行业、每日开盘最高价、最低价、开盘价、收盘价、交易量、交易额度、前一日收盘价、涨跌幅及涨跌额度等信息，通过交易信息构建机器学习量化模型进行数据的挖掘预测。

为了从技术面分析对量化交易预测股市价格走向研究，小组主要工作有：

1．从量化交易的本质-管理概率出发研究了量化交易的可行性，通过模拟交易过程构建三个不同的交易模拟不同盈利概率下交易的情况验证进行管理概率盈利的可行性，同时也证明运用历史数据预测价格的可行性与必要性。

2．基于web获取历史交易数据并建立本地数据库，对数据进行清洗、归一化等操作之后进行特征工程二次挖掘特征中潜在的技术指标并进行可视化，使得从直观上感受股价走向并完成了可以导入模型的一般数据清洗。

3．为了进行海量数据的挖掘，小组分工针对建立的股市数据库构建几种不同的机器学习模型。使用监督学习方法线性回归算法建模拟合交易数据时，通过比较不同拟合函数的阶数、数据集的大小、不同股票数据预测探究与模型效果相关的影响要素，旨在提高模型拟合效果。其次使用时间序列模型arima模型研究面向时间序列数据的模型预测，其中特别是对数据平稳化研究和平稳化处理从另一角度数据平稳性认识了对所研究的数据。最后，在比较弱分类模型和时间序列模型在时间序列数据回归方面的效果之后，设计搭建循环神经模型RNN使得在学习数据时添加遗留机制，增强了当前预测数据与之前数据之间的关系。模型的效果通过计算均方根误差值从数据角度上说明实际数据与回归数据偏差程度，通过绘制所构建模型直观感受模型预测效果。

量化的实际价值意义在于研究使用机器学习对已产生的海量股市交易数据进行挖掘，证明了使用技术分析预测股价现实意义具有可实现性，为一般投资人在实际操盘交易中具有一定的指导意义，在研究了模型预测之后展望使用强化学习模型和每日新闻作为影响因子构建模型。

### Feature&Technology


### Team&Members
  

## 项目:基于图像处理的自动连连看
<span id="imageAutoWatch"/>

### Introduction

功能：
获取游戏窗体 
对图像处理并进行比对
判断游戏逻辑
编写窗体 实现GUI界面
使用的技术与整体思路：
整体思路：
获取连连看程序的窗口并前置；
获取游戏区域，并分割为19*11的图片，进行各个图片的比对，转换成数字二维列表；
遍历二维数组，找到值相同的位置即为可消除的图片。

### Feature&Technology

实现算法：
两个图标相邻。（一条线连接）
两个图标同行，同列，且中间的图标全部为空（数值为0）（一条线连接）
两条线连接，转弯一次，路径上所有图标为空。（二条线连接）
三条线连接，转弯二次，路径上所有图标为空。（三条线连接）
分别点击两个图标，并将对应的二维数据值置为0

使用技术：
Python程序设计
图像识别技术

### Team&Members

## 项目：基于单目视觉的目标测距
<span id="monocularVisionRange"/>

### Introduction

视觉测距作为机器视觉领域内基础技术之一而受到广泛的关注，其在机器人领域内占有重要的地位，广泛应用于机器视觉定位、目标跟踪、视觉避障等。单目视觉结构简单，运算速度快而具有广阔的应用前景。本课题拟针对单目视觉原理，研究目标图像的预处理、识别、定位方法与测距模型，采用Python+OpenCV+ QT、Matlab等工具，实现演示原型系统开发与性能比较。

### Feature&Technology

1、调研基于单目视觉的目标识别与测距的国内外研究现状，基于USB可调焦摄像头实现相机标定，采集图像数据，对采集图像进行预处理操作；

2、在完成必要图像预处理的基础上，研究目标物体的识别与深度估计算法，针对识别的物体根据测距模型计算深度信息，对测量误差利用误差补偿方法进行适当修正；

3、熟悉Python+OpenCV双目立体视觉处理系统开发过程，设计实现一个目标识别与定位测距原型系统，可实现对关键环节的过程与结果的演示。

### Team&Members

## 项目:帅哥美女年龄、颜值打分系统
<span id="girlBoyRank"/>

### Introduction

1.使用tkinter绘制程序界面

2.使用opencv以及百度api来进行人脸识别，获得年龄以及打分

3.基于opencv进行照片的加工功能，如加滤镜等等

### Feature&Technology

### Team&Members

## 项目:基于深度学习的古诗生成器
<span id="ancientPoetryGenerate"/>

### Introduction

输入一组关键词，生成藏头诗，或者相关的古诗。

### Feature&Technology

网站前端作为输入，接受关键词（flask+bootstrap）

基于RNN的后端给出结果(tensordflow 2.0)

### Team&Members 

## 项目:某地区电力工单项目分析
<span id="chatRobots"/>

### Introduction

利用Flask框架，连接Mysql数据库建立一个模拟电力公司工单项目存储，读取与维护的网页项目，允许已注册的账户对其进行各种操作。

### Feature&Technology

程序可以进行注册登录，生成模拟电网工单项目的数据集，查看台区列表，增加新的台区，查找并编辑已有台区，查看全部工单，上传新的工单，并根据深度学习技术预测可能出现的新的台区工单数量等操作，操作方式均为生成网页的图像界面操作。

### Team&Members

负责电力工单数据页面的编写，基于机器学习的数据预测代码的编写。

数据集查找与统一处理，项目期间数据库的建立和维护。

基于机器学习分析当前数据，提取有效数据，并用图表展示。后期预测数据的图表展示。

负责搭建网页框架，台区数据页面的编写。

## 项目:基于深度学习的音乐生成(Jazz)
<span id="musicGenerate"/>

### Introduction

输入原始音乐数据，神经网络经过训练后可以生成相应类型的音乐。

### Feature&Technology

本项目使用LSTM（长短期记忆网络），由于LSTM适合于处理和预测时间序列中间隔和延迟非常长的重要事件，所以用它来作为生成音乐的基础神经网络。

生成界面；
通过不同按钮来实时生成并播放相应音乐，暂定音乐类型有Jazz
可以设定生成音乐长度。

### Team&Members

## 项目:考勤点名
<span id="checkIn"/>

### Introduction

功能详细说明：可以使用图形化界面进行人脸识别，人脸检测和活体检测功能，并可以通过摄像头对人脸进行拍摄并输入姓名进行保存，再次识别时可将图片库中的数据提取出来与当前人脸数据进行比对，并显示姓名学号。在考勤时通过检测人脸数据进行考勤数据的统计并得到人数，来确保考勤人数。

### Feature&Technology

使用技术说明：人脸检测部分使用MTNN算法进行人脸检测，使用FaceNet进行人脸数据的比对，并通过Opencv调用摄像头来获得图像信息。活体检测部分采用Opencv对人脸特征点进行提取，并通过判断是否眨眼来判断是图片还是真人。图形化界面采用TKinter或QT来进行设计。初步暂定识别率为90%。

### Team&Members

## 项目:实时人脸检测特征提取并识别
<span id="faceDetection"/>

### Introduction

功能说明 ：

1.调用笔记本内置摄像头，对人脸进行检测，找到合适的位置后提示并拍照

2.根据拍摄的照片，提取人脸特征，取均值存入文件中

3.调用笔记本摄像头，检测人脸数据并与存入的数据比较，实现人脸识别

调用库：
Dlib          人脸处理库

Numpy        数据处理库

Cv2           opencv库

Scikit-image   图像处理库

### Feature&Technology

### Team&Members

## 项目:智能电影推荐
<span id="movieRecomm"/>

### Introduction

技术：html，css，ajax，python

框架：Django

实现功能：根据用户对电影评分的数据集实现推荐功能。

### Feature&Technology

### Team&Members


## 项目:智能书籍推荐
<span id="BookRecomm"/>

### Introduction

加载数据集（图书、用户、评分表）、检查各个数据集等，并实现基于流行度的简单推荐系统和基于协同过滤的推荐系统

功能

热门书籍推荐 : 将评分排名最高的几本书推荐给每个用户

个性推荐 : 根据不同用户对书籍的喜好, 通过书籍类型的相似性进行个性化推荐

### Feature&Technology


### Team&Members

## 项目:自动驾驶交通指示牌识别
<span id="autoDrive"/>

### Introduction

我们将要处理的交通标志数据集是GTSRB（德国交通标志）。
 
所使用的方法是深度学习。

使用的神经网络类型是与线性分类器配对的卷积神经网络（CNN）。

使用Python作为主要的编程语言。

实现步骤：

1.首先对数据进行预处理

（1）需要对图片做去均值处理、归一化处理。

（2）为了适应更复杂的实际情况，还需要对图片做增强处理。增强处理使图片变得扭曲、倾斜，这样扩充了数据集，提高了识别难度，同时也增强网络鲁棒性。

2.模型架构的实现：

模型结构如下图所示：

主要的思路是：

进行卷积的VGG Net Blocks

每个VGGNet块都有两个2D卷积和一个子采样层（最大池化）

我们使用4层VGG Net将深度从32增加到128

将输出的结果传进全连接层，在softmax部分实现预测和判断

### Feature&Technology

### Team&Members

## 项目:植物识别
<span id="plantIdentificate"/>

### Introduction

基于卷积神经网络训练模型并实现对用户给定图片的判别，并判断属于默认植物的种类。之后通过风格迁移输出另外一种风格的图片。

### Feature&Technology

使用技术

python程序设计

图像识别技术

实现结果：

输出判断结果与风格迁移后的图像

简单交互界面与植物识别模型构建与训练

风格迁移并输出图像

### Team&Members

## 项目:基于Python的口红色号识别器
<span id="lipstickRecog"/>

### Introduction

让我们假设，元旦前夕，小姐姐发来一张美妆博主的美照，并暗示你，“人家也喜欢这个颜色。”

这个时候用我们的口红色号识别器，就能定位嘴唇区域，并迅速给出它的颜色隶属哪家品牌的哪个色号。

如果后期时间充足，还可以做成实时的人像口红色号预测，即打开摄像头，读取每一帧的图片，结合人脸识别功能，实时地截取到嘴唇区域的图片，然后交给计算机预测。

### Feature&Technology

1.首先我们使用的编程语言是Python，一是和课程内容契合，二是由于它具备开发效率快、程序集成度高等优点。

2.其次是获取现在流行的各大品牌口红色号相关数据，包括品牌、色号、颜色名称。

3.最后需要用到的技术是人脸识别，主要是甄别出人脸中的嘴唇区域，然后选择合适的像素矩阵点。

### Team&Members

人脸嘴唇区域检测

口红数据收集

代码编写，功能实现

## 项目:智能驾驶路况识别
<span id="roadStatusRecog"/>

### Introduction

输入照片，路况检测系统对其中的车辆和交通信号灯进行标注，如若发现信号灯则指示信号灯状态，并将结果进行实时反馈。

### Feature&Technology

将汽车前部安装的摄像头所拍摄到的照片作为输入，路况检测系统进行实时检测，识别出其中的车辆、交通信号灯。系统使用YOLOv2目标检测模型进行目标检测，并对检测到的车辆、交通信号灯使用方框进行标注。另外，检测系统使用Mobilenet图像分类模型判别路口交通信号灯的状态，是红灯还是绿灯。系统将检测结果进行实时反馈。

### Team&Members

*    丁同学  交互反馈：车辆目标检测结果标注，交通信号灯状态反馈
*    冯同学  目标检测：目标检测模型实现、训练、测试
*    黄同学  图像分类：图像分类模型实现、训练、测试 

## 项目:基于神经网络的猫狗识别
<span id="catDogRecog"/>

### Introduction

该项目是基于 Keras 的猫狗识别 web 应用。

本项目所用到的数据集是来自 Kaggle 上的猫狗大赛数据集，其中训练集 train 包含了
猫的图片 12500 张以及狗的图片 12500 张，测试集 test 包含了猫狗的图片 12500 
张。本项目准备采用基于 Keras 的自己构造的 CNN 网络训练以及 Keras 中的
VGG16 卷积神经网络模型来进行训练数据，将两种训练方式进行比较，分析各个模型
之间的优劣之处。

最后准备采用 Python 的 Django 框架做页面展示，其中主要实现的功能有项目介绍、
图片上传以及预测结果展示等。

### Feature&Technology

本项目中准备使用的技术大致如下：

Keras 搭建卷积神经网络

 Keras VGG16 搭建自己的卷积神经网络

OpenCV 图像识别

 Django 框架

Python 文件操作

前端流程

后端流程

前后端交互

前端传输图片到后端进行预测，后端将预测结果返回给前端。

### Team&Members

利用 CNN 自己搭建卷积神经网络

 利用 VGG16 搭建卷积神经网络

OpenCV 简单处理图像、Django 页面展示

## 项目:验证码识别
<span id="vertificationCodeRecog"/>

### Introduction

1.提取文本图片

2.提取单个字符图片

3.向量空间图像识别

### Feature&Technology

1.图像处理模块 pillow 基础

2.向量空间和相似度计算

3.完成简单验证码的识别

### Team&Members

## 项目:爬虫分析<我和我的祖国>影评
<span id="movieSpider"/>

### Introduction

运用爬虫爬出豆瓣和猫眼上《我和我的祖国》的电影短评数据
统计评论中词汇出现频率，进行词云图分析，以获得观众们的关注热点。

对观众的地域分布进行分析

对观众的评分画出一个饼状图

### Feature&Technology

开发环境：Pycharm  

数据库：SQLserver

### Team&Members

爬取影评

数据分析

## 项目:爬虫分析之京东商品数据分析
<span id="jdGoodsSpider"/>

### Introduction


### Feature&Technology

技术说明：基于request库进行爬虫；基于numpy和pandas进行数据分析等

功能说明：

功能1：成功爬取数条手机产品信息；

功能2：进行手机销售信息分析，生成手机价格对比图（或表）；

功能3：进行手机销售信息分析，生成手机销量对比图（或表）。

### Team&Members

## 项目:基于深度学习的故事人物情感变化分析
<span id="newsSpider"/>

### Introduction

使用技术说明：

深度学习框架，
    
命名实体识别。

功能详细说明：

使用“常识故事”数据集用于模型训练。最终达成输入一个故事进行故事中不同人物的情感变化分析，并将这种情感分析进行可视化。

### Feature&Technology

### Team&Members

## 项目:链家爬虫分析
<span id="lianjiaSpider"/>

### Introduction

简介：智能租房推荐系统是致力于解决大城市租房人群在信息爆炸时代，无法快速找到适合个人需求的房源的问题。同时，对大量房源数据进行分析，获取城市中的热门地区、租金情况、受众人群等信息特点，并通过图表实现大数据可视化。

主要使用的框架为Flask、Vue-webpack，用来实现前后端分离，并通过RESTful-API实现相互通信。在后端通过一些开放API，例：高德地图开放式API，辅助系统实现更加精确的推荐；而前端则通过Echarts实现图表，以凸显数据的特征。同时还使用了ElementUI和iViewUI进行前端展示风格的优化。异步计算部分实现了数据获取的功能，其中使用Scrapy框架加MongoDB数据库的组合，为数据分析提供了良好的条件。数据库方面，主要的关系型数据库为MySQL，非关系型数据可还引入了Redis，用于对异步任务的结果等提供缓存服务，同时也对部分页面以及接口数据实现缓存，减少项目对MySQL、MongoDB的依赖。并配合Gunicorn和Nginx提高项目的并发处理能力。

### Feature&Technology

2.1在技术方面，项目是一个前后端分离的项目，使用Python、VUE.js所完成。

2.2功能实现方面 :

1.使用Redis的发布订阅功能，实现消息推送。
2.使用MongoDB实现现大量房源数据的存储与查询。
3.利用Redis的list 和 MySQL实现对用户的收藏列表和浏览列表的维护。
4.使用Redis的计数功能，实现对房源的热点排名。
5.使用Echarts数据可视化。使用Redis实现无状态Flask服务下用户身份认证和session共享。
6.使用百度地图API实现地图，路径相关功能。

2.3高并方面：

1.使用Redis实现用户信息缓存和鉴权功能。
2.使用Nginx做代理转发。
3.使用Gunicorn实现请求并行的处理。
4.对于计算密集型功能，使用Crontab实现异步计算，并使用Redis进行缓存。

2.4安全方面：

1.使用MD5对用户密码加密，数据库中不存在明文密码
2.登录时，随机生成唯一的八位的key，存在Redis和Cookie两地。
3.全部接口使用HTTP Basic Auth认证。

2.5功能方面

用户模块：
1.用户信息、以及用户对房屋的选择习惯分析。
2.管理员身份情况下，用户信息的管理。

房屋信息模块：
1.房屋展示模块，客观的展示房源的分数，并添加到浏览队列中。
2.房屋搜索模块，采用前端无限滚动的方式，动态的加载，降低对MongoDB的压力
3.用户的收藏和浏览列表存在Redis的列表中，方便快速的查看浏览历史。

2.6数据分析模块：
1.地理位置和住房习惯分析，因为是查询密集型功能，对MongoDB为强依赖，故，使用异步计算，数据定时缓存在MySQL之中。
2.城市热力图和价格分析是计算密集型，故，依然使用异步计算，同时将信息缓存在Redis中。

### Team&Members

## 项目:爬虫分析(汽车价格)
<span id="carPriceSpider"/>

### Introduction

在某一汽车网络平台上，爬取各种品牌汽车价格等信息。

### Feature&Technology

网络请求框架，如requests等

正则表达式

若是JSON 数据，使用 Python自带的模块 json；若是HTML 数据，使用BeautifulSoup、lxml 等库去处理；若是XML据，使用 untangle、xmltodict 等第三方库

负责获取网页信息和相关网页url，并写入文件

负责获取网页信息和相关网页url，并写入文件

负责数据处理分析。如不同月份的汽车销量；汽车价格的涨幅；热门车型等；并通过可视化结果展示。

### Team&Members

## 项目:新浪微博数据爬虫爬取
<span id="weiboSpider"/>

### Introduction

连续爬取一个或多个新浪微博用户（如朱亚文、郭碧婷）的数据，并将结果信息写入文件。写入信息几乎包括了用户微博的所有数据，主要有用户信息和微博信息两大类，前者包含用户昵称、关注数、粉丝数、微博数等等；后者包含微博正文、发布时间、发布工具、评论数等等，具体的写入文件类型如下：

写入csv文件

写入MySQL数据库

下载用户微博中的原始图片

下载用户微博中的视频

### Feature&Technology

运行环境：

开发语言：python2/python3

系统： Windows

MySQL数据库写入

将爬取信息写入MySQL，安装MySQL。


程序首先会创建一个名为"weibo"的数据库，然后再创建"user"表和"weibo"表，包含爬取的所有内容。爬取到的微博用户信息或插入或更新，都会存储到user表里；爬取到的微博信息或插入或更新，都会存储到weibo表里，两个表通过user_id关联。
输出：

包含爬取到的所有微博信息，如微博id、正文、原始图片url、视频url、位置、日期、发布工具、点赞数、转发数、评论数、话题、@用户等。如果爬的是全部微博(原创+转发)，除上述信息之外，还包含原始用户id、原始用户昵称、原始微博id、原始微博正文、原始微博原始图片url、原始微博位置、原始微博日期、原始微博工具、原始微博点赞数、原始微博评论数、原始微博转发数、原始微博话题、原始微博@用户等信息。

### Team&Members

## 项目:爬虫分析旅游情况
<span id="travelSpider"/>

### Introduction

使用爬虫对旅游网站如途牛，去哪儿网的数据进行爬取，对旅游景点旅游城市的一些情况进行分析并呈现。

### Feature&Technology

使用scrapy框架对旅游数据进行爬取分析，
暂定用Dijango搭建后台，调用pyecharts库进行可视化展示。采用mysql作为数据库存储数据。
分析节假日的旅游景点的情况，给用户出行提供一个大体的出行方案。

### Team&Members

## 项目:基于Python的招聘信息分析
<span id="autoDrive"/>

### Introduction

运用爬虫技术爬取招聘网站上计算机专业的各种职位类型，薪资水平，与就业要求，并对得到的数据进行可视化处理，比较直观的展现目前计算机就业现状。

### Feature&Technology

1.运用爬虫爬取相关招聘信息

2.进行数据存储

3.对数据进行分析，进行可视化分析

### Team&Members

## 项目:一种爬取电影评论等数据并可视化分析的方法
<span id="filmReviewSpider"/>

### Introduction

如今电影行业发展飞速，几乎隔几天，就会有新电影上映，作为学生的我们，消费水平有限，不可能都去电影院看来判断电影好不好看，往往我们会通过别人的评论来进行判断。但在翻阅评论时，需要一页一页浏览，显得很麻烦，要是能一下子看到就好了。此时，爬虫技术就显得尤其重要了，通过爬取网页上用户留下对电影的言论，将其存放在TXT文件中，能看到所有评论。当然仅仅是文字表述会略显粗糙，本文希望将数据可视化处理，将评论中重要的信息以图片的形式来呈现，从而更直观的看出这个电影的好坏。

### Feature&Technology
在爬取数据时，我们主要使用了request库。在获取数据时，为了防止失败，我们使用了一个代理。在数据处理时，我们选择了几大类：姓名、城市、内容、评分以及时间，并充分考虑了不存在的情况。最后就是将数据存储到TXT文件中，通过创建然后分别写入。
在数据可视化阶段，我们使用了pyecharts对爬取到的星级评分进行饼图可视化处理。首先是提取TXT文件中的评分信息；其次是设置星级，每个星级对应了一个的评分范围；最后使用pie库对数据作画饼图处理。到此，我们就将基本工作完成了，为了对爬取的数据获取更多信息，我们打算做如下尝试：
	额外内容：
使用pyecharts对爬取到的电影评论进行词云图可视化处理
基本思路：主要使用了wordcloud库。首先导入背景图，作为词云背景；其次，获取TXT文件中的评论部分，通过jieba库设置分词，此项需要考虑电影等无意义的关键词，我们要将这些词屏蔽掉；最后就可以将分词后的数据导入云图。

挑战内容：
	使用pyecharts对爬取到的粉丝位置进行可视化处理
	基本思路：需要加上城市的包。读取TXT文件中位置的内容，并根据城市生成地理坐标图。
个性内容：
	对于爬取的TXT文件跟据用户的不同需求，可实现加密处理。对初始数据加密后，那么后续的数据分析都无法正确分析。

### Team&Members

## 项目:去哪儿网国庆旅游景点数据爬虫分析
<span id="scenicSpotSpider"/>

### Introduction
平台：anaconda+pycharm
目的：主要分析节假日期间值得推荐的各大旅游景点。
功能：
1.爬取所需景点的数据
2.景点门票销量排名分析
3.景点销售额排行分析
4.推荐景点分析
功能：子弹选择：一次一个，一次两个
  地方飞机：两种或者三种
  难度：根据积分升高难度加大
改进：增加大飞机的血槽显示
主要用pycharm pygame

### Feature&Technology
实现过程：
第一部分
利用网站爬取到的数据进行分析，对于所需要的内容id进行提取然后保存文件。
第二部分
读取保存的文件，对数据进行处理，将处理后的数据通过柱状图的形式展示出来。

### Team&Members

## 项目:短租估价大师
<span id="shortRentSpider"/>

### Introduction

共享，通过让渡闲置资源的使用权，在有限增加边际成本的前提下，提高了资源利用效率。随着信息的透明化，越来越多的共享发生在陌生人之间。短租，共享空间的一种模式，不论是否体验过入住陌生人的家中，都可以从短租的数据里挖掘有趣的信息。

### Feature&Technology
数据来源：
本项目数据来自Airbnb于2019年4月17日公开的北京地区数据。数据均来源于Airbnb网站的公开信息，不包含任何个人隐私数据。

拟定项目流程：
1）数据清洗：因为给的数据不一定都为完整有效的，所以要进行数据清洗。
2）预测房屋价格模型：通过机器学习的方法分析数据，提取数据特征，进行训练。
3）地图可视化：通过geopandas绘制北京地区的房源分布图。
4）高频词提取：利用jieba对房屋名称进行拆词分析，获取高频词汇。

项目成果：
拟完成一个平台实现，用户输入自己的房源信息（初步只在北京），给出相应的房屋价格估计，并对房价提高的小技巧提供一些建议。
### Team&Members

## 项目:12306点触验证码的识别登陆及自动抢票
<span id="verificationCodeSpider"/>

### Introduction

通过Python程序模拟登陆中国铁路12306，自动实现下单功能。

### Feature&Technology
涉及知识：点触验证码的攻克、自动化测试工具 Selenium 的使用、对接在线打码平台.

实现方案：
1.利用Selenium模拟人的行为方式完成验证
2.发送请求，剪裁并保存验证码图片 
3.打码平台识别验证码，返回验证码的坐标信息
4.定义点击坐标，模拟点击验证码，完成验证后点击登陆
5.选择人物，提交确认订单

### Team&Members

## 项目:猫咪跑酷
<span id="catParkourGame"/>

### Introduction

1.主要工具：python和pycharm

2.主要实现功能：
(1)用户登录页面（数据库的链接）
(2)键盘操控猫咪运动
(3)关卡设计
(4)结束时显示最高分和当前分数
(5)跑酷时分数更新
(6)有背景音乐及相应音效

### Feature&Technology

### Team&Members

## 项目：植物大战僵尸改编版
<span id="plantsV.S.ZombiesGame"/>

### Introduction

1  主要应用软件：Pycharm，PS

2  Pycharm编程的内容一共包括两个.py文件，即PvsZ_main.py和PvsZ_sprite.py。
	2.1  PvsZ_sprite.py的功能是为PvsZ_main.py主程序提供一些基本的参数常量和游戏精灵类（其中包括游戏背景精灵、僵尸精灵，植物精灵、炮弹精灵），换句话说PvsZ_sprite.py就是主程序的工具包，目的是为了提高主程序书写代码的质量与可读性。
	2.2  PvsZ_sprite.py是本游戏的主程序，包括主游戏类的构建（其中包括游戏的初始化、游戏开始、游戏结束），最后由主游戏类创建一个游戏对象，借助对象调用两个文件的方法从而达到游戏运行的目的。
	2.3  编程设计Pycharm的相关知识主要有库的调用、类、对象、函数、判断分支循环结构、静态变量等。

3  用PS所做的工作主要是图像的处理美化，使游戏界面更加人性化。

4  预期效果：游戏有内容，有特效，有声音。

5  总结：通过设计这个小游戏，把已经学的python编程知识得到运用。当然为了达到最终的效果，编程过程中还需要学习新的知识、新的库，培养了我们较强的学习能力。做一个游戏不仅需要编程，还需要有底层建筑的支撑，比如本例中用PS处理游戏设计的图片，用PR做一点音频的处理。

### Feature&Technology

### Team&Members

## 项目:我该去哪里(爬虫)
<span id="whereCity"/>

### Introduction

运用爬虫爬出国内各大城市的房价和薪资水平，对数据进行加工处理并展示到网站上，以较直观地方式展示各个城市的性价比。

### Features&Technology:

* 爬虫(对拉勾-BOSS直聘等招聘网站和链家-安居客等房产网站的分析和爬虫定制化制作)
* 网站搭建(Django作为后台，使用Vue+ElementUI等作为前端框架，MySql做数据库)

项目采用Git-flow作为Git工作流。采用敏捷开发模式。主要用PyCharm作为开发工具。

爬虫方面我们首先对各个网站做分析，找出可用数据的API接口，在本地调试好相应接口和数据返回，并将其存储到MySql数据库上，再将其放到腾讯云服务器上。后续可开放出API。
网站也架设在云服务器上。

后续可能会做Docker,CLI等。在功能点上，增加各个城市的男女比例，教育资源，医疗资源等来作为权重系数放在性价比评选中。用户可选中多个参数来得出自己的性价比。

### Thanks

如有雷同，纯属借鉴。


## 项目:自动驾驶路况检测系统
<span id="autoDrive"/>

### Introduction

输入照片，路况检测系统对其中的车辆和交通信号灯进行标注，如若发现信号灯则指示信号灯状态，并将结果进行实时反馈。

### Feature&Technology

将汽车前部安装的摄像头所拍摄到的照片作为输入，路况检测系统进行实时检测，识别出其中的车辆、交通信号灯。系统使用YOLOv2目标检测模型进行目标检测，并对检测到的车辆、交通信号灯使用方框进行标注。另外，检测系统使用Mobilenet图像分类模型判别路口交通信号灯的状态，是红灯还是绿灯。系统将检测结果进行实时反馈。

### Team&Members

*    丁同学  交互反馈：车辆目标检测结果标注，交通信号灯状态反馈
*    冯同学  目标检测：目标检测模型实现、训练、测试
*    黄同学  图像分类：图像分类模型实现、训练、测试 
