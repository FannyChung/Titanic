# Titanic
## 题目描述
预测每个乘客是否活下来(0代表没有，1代表活下来了），评价标准是accuracy.

提交文件是418个项和标题行组成的csv文件，形如：
```
PassengerId,Survived
 892,0
 893,1
 894,0
```

## 赛制
### private leaderboard vs public leaderboard
为了防止过拟合，设置了这两个部分。
public leaderboard是对所有参赛者一样的，有50%的测试集；private leaderboard是另外50%的测试集，在比赛结束前对参赛者不可见。比赛结束时，会公开private leaderboard的成绩，这才是决定最终成绩的部分。

### kernels
kernels是一个云计算环境，能够可重用，合作分析。支持R和python，Jupyter Notebooks和RMarkdown。可以看到所有公开分析的代码。可以自己新建kernel，也可以fork别人的。

### 排名
不考虑两个月前的提交，所以这两个月没有提交的话，队伍的排名会下降。


---
# NoteBooks
## Titanic Data Science Solutions
[Titanic Data Science Solutions][https://www.kaggle.com/startupsci/titanic-data-science-solutions]是官方推荐的一个比较简单的入门手册。
### 工作流
1. 问题定义
1. 获取训练和测试数据
1. 数据准备和清洗
1. 建模、预测&解决问题
1. 可视化，报告、呈现步骤和最终方案
1. 提交答案

注意：
* 可以多个步骤融合：通过可视化来分析数据
* 提前：先分析，后清洗
* 多次：可视化
* 删除一步：可能不需要获取数据


通过读题面可以获取一些信息：
> On April 15, 1912, during her maiden voyage, the Titanic sank after colliding with an iceberg, killing 1502 out of 2224 passengers and crew.

存活率：32%

> One of the reasons that the shipwreck led to such loss of life was that there were not enough lifeboats for the passengers and crew.

缺少救生船

> Although there was some element of luck involved in surviving the sinking, some groups of people were more likely to survive than others, such as women, children, and the upper-class.

一般女人、孩子、上层阶级活下来的多。

### 目标
* 分类
* 相关性分析
* 转换
* 补充：补充缺失的特征值
* 校正：分析训练集特征中的错误或者可能的不正确值，尝试改正或者删除样本。可以删除所有的离群值，或者删除没有贡献的特征。
* 创建：根据现有的一个或多个特征来创建新的特征，新特征可以帮助完成
* 画图：根据数据的特性和问题目标，选择正确的可视化图表