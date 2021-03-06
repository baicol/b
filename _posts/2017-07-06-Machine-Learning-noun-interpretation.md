---
layout: post
title:  "机器学习，从专有名词开始"
date:   2017-07-05 15:45:05
categories: 机器学习之专有名词篇
tags: 基础概念 机器学习 名词解释
---

* content
{:toc}

>~~你本寻常人，曾经辉煌过。若要再辉煌，再做寻常人。~~  
什么都不要说，就是干！！

## 写在前面
&emsp;&emsp;终于有一个比较系统的时间来搞一下拖沓已久的事情了 。从今天起吧，争取多push点足迹来总结自己坎坷的机器学习之路。书写哥的AI启示录，一切从雾水开始。  
&emsp;&emsp;一本书，一台电脑。起航！

## 有监督学习、无监督学习
&emsp;&emsp;是否有监督（supervised），就看输入数据是否有标签（label）。输入数据有标签，则为有监督学习，没标签则为无监督学习。

## 半监督学习、聚类、分类
&emsp;&emsp;最简单也最普遍的一类机器学习算法就是`分类`（classification）。**对于分类，输入的训练数据有特征（feature），有标签（label）。所谓的学习，其本质就是找到特征和标签间的关系（mapping）。这样当有特征而无标签的未知数据输入时，我们就可以通过已有的关系得到未知数据标签。**在上述的分类过程中，**如果所有训练数据都有标签，则为`有监督学习`（supervised learning）。如果数据没有标签，显然就是`无监督学习`（unsupervised learning）了，也即`聚类`（clustering）。**  
&emsp;&emsp;目前分类算法的效果还是不错的，但相对来讲，聚类算法就有些惨不忍睹了。确实，无监督学习本身的特点使其难以得到如分类一样近乎完美的结果。这也正如我们在高中做题，答案（标签）是非常重要的，假设两个完全相同的人进入高中，一个正常学习，另一人做的所有题目都没有答案，那么想必第一个人高考会发挥更好，第二个人会发疯。  
&emsp;&emsp;这时有人可能会想，难道有监督学习和无监督学习就是非黑即白的关系吗？有没有灰呢？Good idea。灰是存在的。二者的中间带就是`半监督学习`（semi-supervised learning）。**对于`半监督学习`，其训练数据的一部分是有标签的，另一部分没有标签，而没标签数据的数量常常极大于有标签数据数量（这也是符合现实情况的）。**隐藏在`半监督学习`下的基本规律在于：**数据的分布必然不是完全随机的，通过一些有标签数据的局部特征，以及更多没标签数据的整体分布，就可以得到可以接受甚至是非常好的分类结果。**

## 关系
	有监督学习（分类，回归）
	↕
	半监督学习（分类，回归），transductive learning（分类，回归）
	↕
	半监督聚类（有标签数据的标签不是确定的，类似于：肯定不是xxx，很可能是yyy）
	↕
	无监督学习（聚类）

注：以上内容来源于https://www.zhihu.com/question/23194489/answer/25028661

## 逻辑回归
&emsp;&emsp;Logistic回归与多重线性回归实际上有很多相同之处，最大的区别就在于它们的因变量不同，其他的基本都差不多。正是因为如此，这两种回归可以归于同一个家族，即广义线性模型（generalizedlinear model）。  

&emsp;&emsp;这一家族中的模型形式基本上都差不多，不同的就是因变量不同。

	如果是连续的，就是多重线性回归；
	如果是二项分布，就是Logistic回归；
	如果是Poisson分布，就是Poisson回归；
	如果是负二项分布，就是负二项回归。

&emsp;&emsp;Logistic回归的因变量可以是二分类的，也可以是多分类的，但是二分类的更为常用，也更加容易解释。所以实际中最常用的就是二分类的Logistic回归。  

&emsp;&emsp;Logistic回归的主要用途：

    寻找危险因素：寻找某一疾病的危险因素等；
    预测：根据模型，预测在不同的自变量情况下，发生某病或某种情况的概率有多大；
    判别：实际上跟预测有些类似，也是根据模型，判断某人属于某病或属于某种情况的概率有多大，也就是看一下这个人有多大的可能性是属于某病。  

&emsp;&emsp;Logistic回归主要在流行病学中应用较多，比较常用的情形是探索某疾病的危险因素，根据危险因素预测某疾病发生的概率，等等。例如，想探讨胃癌发生的危险因素，可以选择两组人群，一组是胃癌组，一组是非胃癌组，两组人群肯定有不同的体征和生活方式等。这里的因变量就是是否胃癌，即“是”或“否”，自变量就可以包括很多了，例如年龄、性别、饮食习惯、幽门螺杆菌感染等。自变量既可以是连续的，也可以是分类的。

(持续更新中...)
