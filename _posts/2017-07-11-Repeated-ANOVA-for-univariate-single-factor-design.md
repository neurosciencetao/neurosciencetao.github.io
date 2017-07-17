---
layout: post
title: "单因素重复测量方差分析"
date: 2017-07-11
---

# 摘要
本文介绍如何使用SPSS 20.0做单因素重复测量方差分析。

# 引言
下面这些链接提供了更加详细的解释或操作方法：
- [Lared.com上的ANOVA介绍](https://statistics.laerd.com/statistical-guides/repeated-measures-anova-statistical-guide.php)
- [Laerd.com上的ANOVA步骤指导](https://statistics.laerd.com/spss-tutorials/one-way-anova-repeated-measures-using-spss-statistics.php)
- [重复测量方差分析的SPSS实现](https://www.spss-tutorials.com/spss-repeated-measures-anova/)
- [怎样做重复测量方差分析的事后分析](https://www.spss-tutorials.com/spss-repeated-measures-anova-example-2/#workflow)
- [怎样计算因素的效应量](https://www.spss-tutorials.com/spss-partial-eta-squared/)

方差分析是通过分析两个及以上分组之间方差的差异，来进行均数之间是否有差异的统计分析。其基本思想是：
> - 测量的方差有两个来源：不可控制的随机误差和实验设计引起的系统偏差。
> - 如果没有系统误差，则组间不会有显著差异。
> - 比较组间均方差和组内均方差可以提示组间误差来自实验设计引起的系统偏差的可能性。  

这篇小文章介绍一下如何SPSS 20.0做单因素重复测量方差分析。用到的数据可以在[这里](/img/poster_ANOVA/RT.sav)下载。
数据来自于一个汉字类别判断实验，记录了被试（N=22） 在三种状态（1.专注，2.走神并没有意识到，3.走神并且意识到）下的平均反应时。在此数据中，自变量为被试的注意状态，因变量为反应时。

# 分析方法和结果
## 用SPSS打开数据
文件”-->"打开"-->“数据”，选择下载的数据，如下图所示，应为21行×3列的数据。  

![打开数据](/img/poster_ANOVA/data.png)
## 定义变量名称
1. 选择：“分析”-->“一般线性模型”-->“重复测量”;
2. “被试内因子名称：”为自变量名称，填写“report”，或者你希望的名称；“级别数”填写3，按“添加”；
3. “测量名称：”为因变量名称，填写“RT”，按“添加”；  

![定义变量名称](/img/poster_ANOVA/variable_name.png)

## 定义变量
接上步，按“定义”，将左边栏中的变量分别引入到“主体内部变量”中  

![定义变量](/img/poster_ANOVA/define_variable.png)
## 选择分析内容
### 模型：默认选项
### 对比：默认选项
### 绘图：把“因子”中的“report”选入“水平轴”，选择“添加”；
### 事后多重比较
重复测量方差分析的事后多重比较(post hoc analysis)和非重复测量方差分析不同。此处保持默认选项，事后比较在“选项”中进行。
### 保存
保存特定信息供后续分析，在这个分析中不需要设定“保存”里面的选项。
### 选项：在这一步中选择事后多重比较方法，以及其他关心的描述统计信息
1. 将“因子与因子交互”中的"report"导入到“显示平均值”；
2. 勾选“比较主效应”；
3. “置信区间调节”选择“Bonferroni”;
4. “输出”中勾选“描述统计”和“功效估计”  
5. 点击“继续”  
![选项](/img/poster_ANOVA/define_option.png)

## 结果报告
结果如下图所示：
![结果报告](/img/poster_ANOVA/report.png)

# 讨论
## 在文章中报告结果
可以参考以下写法：  
A single-factor repeated measure ANOVA did not show a significant difference among the three conditions (on-task, mind wandering without awareness, and mind wandering with awareness): F(2,40) = 2.712, P = 0.079.
## 报告事后多重比较结果
假设这个分析的结果显著，需要报告时候多重比较结果。  

_未完待续。。。_
