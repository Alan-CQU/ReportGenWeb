## 录屏软件调研报告生成系统

基于Django搭建的Web平台，

需要的用户输入：

- 产品名字
- 产品URL
- 想在产品之间做对比的特性

系统在后台进行爬虫，语句提取。综合整理成一篇调研报告，给出网页上的展示和word版本的下载（word版本下载暂时未实现）。

目前版本v 0.0.3

---
*环境配置*

安装依赖
pip install -r requests.txt

修改setting.py数据库配置为自己的数据库

python manager.py migrate 生成必要表

python manager.py createsuperuser 创建超级管理员

---




**仍待优化的问题**

- 产品特性对比中，筛选算法比较简单，准确率无法达到100%
- 文本生成中，筛选算法比较简单， 内容相关性不如预期的高

---

## 版本迭代
---

### v 0.0.4

新增了可选产品的类别，现在总共可选的产品类别有

- 录屏类软件
- 视频剪辑类软件
- 笔记类软件
- 单词类软件
- 在线会议类软件

存在的问题，新增的产品类，在文本内容筛选中仍然需要继续优化，可读性不强。

部分网站兼容性不强，如企业微信和飞书，仍需改进调试。

以下是部分演示截图，


![image-20200706213249935](picForMarkDown/image-20200706213249935.png)

视频剪辑类软件

![image-20200706213347099](picForMarkDown/image-20200706213347099.png)

![image-20200706213410505](picForMarkDown/image-20200706213410505.png)

![image-20200706213440271](picForMarkDown/image-20200706213440271.png)

笔记类软件

![image-20200706213522572](picForMarkDown/image-20200706213522572.png)

![image-20200706213540417](picForMarkDown/image-20200706213540417.png)

![image-20200706213553596](picForMarkDown/image-20200706213553596.png)

单词类软件

![image-20200706213717033](picForMarkDown/image-20200706213717033.png)

![image-20200706213740101](picForMarkDown/image-20200706213740101.png)

![image-20200706213759644](picForMarkDown/image-20200706213759644.png)

在线会议类软件

![image-20200706214008171](picForMarkDown/image-20200706214008171.png)

![image-20200706214034673](picForMarkDown/image-20200706214034673.png)

![image-20200706214055626](picForMarkDown/image-20200706214055626.png)



---

### v 0.0.3

对界面进行部分CSS美化，用户可以输入和录屏软件相关的自定义特性。

特性仅限于以下

```
支持平台，支持水印，摄像头桌面组合录制，区域录制，音频录制，画质调整，鼠标特效，费用，付费
```

**界面**

![image-20200521141638426](picForMarkDown/image-20200521141638426.png)

**默认特性对比**

![image-20200521141716797](picForMarkDown/image-20200521141716797.png)

![image-20200521141953687](picForMarkDown/image-20200521141953687.png)

![image-20200521142019136](picForMarkDown/image-20200521142019136.png)



**自选特性对比**

![image-20200521142138873](picForMarkDown/image-20200521142138873.png)

![image-20200521142155211](picForMarkDown/image-20200521142155211.png)



---

### v 0.0.2

新增功能：首次访问目标产品网址时，使用selenium+tkinter 完成截取系统官网屏幕截图，并缓存，再放置到报告当中。再次访问时无需再次截取。

效果图如下：

![image-20200411142152225](picForMarkDown/image-20200411142152225.png)

![image-20200411142207793](picForMarkDown/image-20200411142207793.png)

---
### v 0.0.1

**初始界面展示（注意是index目录）**

![初始界面](./picForMarkDown/image-20191213101025635.png)



**用户进行输入，然后提交，特性暂时采用默认**



![image-20191213101140515](./picForMarkDown/image-20191213101140515.png)



**展示结果**

![image-20191213101302162](./picForMarkDown/image-20191213101302162.png)



系统生成的报告是粗糙的，需要经过人工二次审校放能使用。（V 0.0.1）

---
