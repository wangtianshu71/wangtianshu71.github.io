---
layout: post
title: "《用户体验度量》背景知识"
author: "wts"
header-style: text
tags:
  - 用户体验
---
背景知识
=====================
## 选择参加者
可用性领域常见的组别和分类标准：
* 在一些领域中，自我报告的专业化程度（新手、中等熟练水平、专家）
* 使用频率（例如，每个月的网站访问量或交互量）
* 使用相关物品的经验程度（日、月、年）
* 人口统计学变量（例如性别、年龄、地理位置等）
* 行为（例如特定功能或特点的使用）  

## 样本大小
不存在一个既定规则规定一个可用性研究需要多少个参加者，再确定样本大小时，应该基于两个要素：你的研究目标和你所能容忍的误差范围。 

如果你只对发现主要的可用性问题感兴趣，那么在三、四个有代表性的参加者就能获得有用的反馈。**小样本能够确定一些比较重要比较明显的问题，在设计的早期你需要较少的参加者来确定主要的可用性问题，随着设计逐渐完成，你需要更多的参加者以发现剩余的问题。**  

还需要考虑：你接受多大程度的误差。比如80%的参加者成功完成了一个任务，并不能说明较大群体中的80%的用户能完成这个任务。要考虑**置信区间**  
下图表示，在完成度为80%的情况下
置信区间作为样本大小函数的变化情况：  

![1](/img/in-post/1.png)

## 组内或组件研究
* **组内设计**：比较每个参加者的不同数据
* **组间设计**：比较参加者之间的数据  

* **组内研究**又称重复测量设计，常用于评估参加者学习使用特定产品时的难易程度。通过比较同一批参加者多次施测上的度量（完成时间/错误率），可以判断参加者多亏和多久就能熟练使用被评估的产品。  

组内设计的缺点是需要考虑传递效应（前一次的测试能够影响下一次的测试）。  

**组间研究**用于比较不同参加者之间的结果，例如新手和专家在满意度上的差异、年轻参加者和年长参加者在任务完成时间上的差异  

**混合研究**同时包括组件因素和组内因素。比如采用混合设计探讨男女在几次施测过程中完成某些任务的方式上是否存在差异。  

## 解决传递效应——平衡
参加者对于产品的学习通常会随着使用经验的增加而增长。这个问题可以通过平衡的方法以控制顺序效应而加以解决。  

平衡是指简单的变换不同任务的实施顺序。如下图：  

![2](/img/2.png)

 `如果任务之间没有任何关联度或者任务之间是存在自然顺序的时候，平衡是不恰当的。任务的顺序有时是不能更改的，否则会导致测试没有意义`
## 自变量和因变量
可用性研究中，必须确定自变量和因变量。  

## 可用性测量中的数据类型
1. 称名数据  
使用简单的描述统计：技术/频率来分析这类数据，需要注意的是，这类数据的编码不能拿来分析。
2. 顺序数据  
比如前100名的电影。顺序数据的排序可以是较好/较坏、更为满意/比较不满意等等。相对等级在统计中最重要，平均等级/等级之间的距离是没有意义的。  
对于顺序数据来说，最常用的方法是频率统计。例如40%的参加者评定为“极好”...
3. 等距数据  
等距数据的测量值之间的差异是有意义的。可用性量表是一个等距数据的例子。量表各点之间的距离是有意义的。表示感知可用性上的递增或递减程度。  
下图展示了顺序数据和等距数据：  
![3](/img/3.png)
4. 比率数据  
身高、年龄、体重都是比率数据的例子。  

不同的数据类型用在不同的度量任务上，也有着不同的统计方法，如下图：  
![4](/img/4.png)  

在报告时，所使用的有效位数不要超过原始数据有效位数的一位。

## 变异性测量  
变异性测量显示数据总体中数据的分散或离散程度，这对于知道数据的可置信程度是很重要的。变异性或离散程度越低，将样本的结果推论到全体的置信度就越大。三种最常见的变异程度测量指标为：全距（range）、方差（variance）、标准差（standard deviation）。  
 * 全距是最小数据点与最大数据点之间的距离。它可以用来确定极端值、检验数据编码是否正确
 * 方差：数据相对于平均数的离散程度
 * 标准差是方差的平方根  

## 置信区间  

 置信区间是一个范围，用来估计某统计值的总体实际值。使用excel中的confidence函数即可计算：  
 `=confidence(α系数，标准差，样本大小)`  
 α是显著性水平，一般值是0.05，计算标准差可以使用excel中的stdev函数，计算样本数量使用count函数。

## 比较平均数  

### 独立样本（t检验）：  
 比较基于独立样本的平均数意味着这些组别是不同的。比如：在满意度评价中专家级参加者与新手参加者之间的比较。可以使用t检验，看P值。  

### 配对样本（t检验）：  
 当要比较同一组参加者的平均数时，应该使用配对样本t检验，比如想要测量两个原型设计之间是否存在差异，则使用配对样本t检验。**在配对样本检验中要注意：所比较的来自于两个分布的样本量要相等；在独立样本条件下，样本量无需相等。**  

### 方差分析（t检验）：  

 当想要比较多个样本之间的差异时，就用方差分析（ANOVA）。比如比较三个原型图的“设计”，这里属于单因素方差分析，主要看F值和P值。F值越大，P越小，差异越显著。但是也只能表明“设计”这一因素的效应显著，不一定表示每种设计的均值都与其他各种设计的均值有显著差异。如果要看任意一堆平均数之间是否有显著差异，可以对两组数值进行两样本t检验。  

## 变量之间的关系  
 
* 正相关
* 负相关  
使用excel：数据分析-->相关系数  

## 图形化显示数据  
* 条形图
* 折线图
* 散点图
* 饼图
* 堆积条形图  

注意：画图的时候要标出置信区间，在画散点图时，要标出拟合度和趋势线。堆积条形图不可分割部分过多。  

## 总结
![5](/img/5.png)

