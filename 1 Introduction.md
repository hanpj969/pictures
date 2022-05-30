# 1 Introduction

[TOC]

## What is econometrics?  

- Econometrics is about how we can use theory and data from
  economics, business, and the social sciences, along with tools
  from statistics, to answer ‘‘how much’’ questions.  

- 计量经济学是一门交叉学科，它**以经济学为基础**，利用**统计方法**来实现如下主要目标：

  - 估计经济现象之间的相关性
  - 检验经济理论
  - 预测重要的经济变量（如GDP的增长）
  - 评估政府政策 

> ![image-20220506214557618](https://gitee.com/h-ruc/note/raw/master/image-20220506214557618.png)

### 为什么要用统计学？  

- 经济理论主要用于引导模型的构建，建立各相关变量之间的联系

> 比如：消费量和收入之间的关系 （效用最大化理论为基础） 

- 但是，经济学模型表达的只是抽象的数学关系,模型能够囊括众多相关的因素，但是模型不可能囊括所有相关的因素，即：总有一些因素没有/不能包括在模型中.

> 比如：影响个人收入的因素（个人的能力常常不可观测）  

- *因此，我们需要用概率模型来替代确定模型  

> 如：$Y=beta_0+beta_1X+varepsilon$ 

### 为什么独立于统计学？  

- 大部分的经济学或者金融数据都是“非实验”数据 (观测数据)

> 难免存在测量误差或者非控制的因素

- 经济学家的工作犹如天文学家，他们基本上只能“观测”现象/数据，但是不能影响结果。

- 大部分的统计工具和分析方法的出现和发展都是立足于实验数据
- 但是，近几年，经济学研究中也逐渐通过“实验经济”的方法来获取实验数据

> 在实验经济里，经济学家可以影响结果  

### 为什么学习计量经济学？  

- Econometrics fills a gap between being a “student of economics” and being a “practicing economist”

  - It lets you tell your employer:
    - “I can predict the sales of your product”
    - “I can estimate the effect on your sales if your competition lowers its
      price by $1 per unit”
    - “I can test whether your new ad campaign is actually increasing your
      sales”

  - Helps you develop “intuition” about how things work and is invaluable if you go to graduate school  

## 计量经济学的研究内容  

- **理论计量经济学：**研究计量经济学的理论与方法
- **应用计量经济学：**研究计量经济学的方法在实际的应用  

## 什么是计量经济学模型？  

- An econometric model consists of :

  - a **systematic and deterministic** component

  - a **random and unpredictable**  component $e$ that we will call a **random error (随机扰动项）**  
    $$ {\left}
    \begin{align}&Q^d=f(P,P^s,P^c,INC)+e\\
    &f(P,P^s,P^c,INC)=\beta_1+\beta_2P+\beta_3P^s+\beta_4P^c+\beta_5INC\\
    &Q^d=\beta_1+\beta_2P+\beta_3P^s+\beta_4P^c+\beta_5INC+e
    \end{align}
    $$ {\right}

  - **<u>The systematic portion （deterministic component）</u>** is the part we obtain from economic theory, and includes an assumption about the functional form

  - **<u>The random component</u>** represents a ‘‘noise’’ component, which obscures our understanding of the relationship among variables, and which we represent using the random variable $e$  

  - The coefficients $ β_1, β_2, …, β_5$ are unknown parameters of the model that we estimate **<u>==using economic data and an econometric technique==</u>**

    - <u>The functional form</u> represents a hypothesis about the relationship between the variables
    - In any particular problem, one challenge is to determine a functional form that is compatible with economic theory and the data  

  - We use the econometric model as a basis for statistical
    inference

  - The ways in which statistical inference are carried out include:

    1. Estimating economic parameters, such as elasticities,
       using econometric methods
    2. Predicting economic outcomes, such as the enrollment in
       two-year colleges in the United States for the next ten
       years
    3. Testing economic hypotheses, such as the question of
       whether newspaper advertising is better than store
       displays for increasing sales  

## How is Data Generated?  

- We must have data

  - Where do data come from?
  - What type of real processes generates data?

- Economists and other social scientists work in a complex world in which data on variables are ‘‘observed’’ and rarely obtained from a controlled experiment

  - This makes the task of learning about economic parameters all the more difficult  

- One way to acquire information about the unknown parameters of economic relationships is to conduct or observe the outcome of an experiment

  - Such controlled experiments are rare in business and the social sciences

  - There are some examples of planned experiments in the social
    sciences

    > A notable example of a planned experiment is Tennessee’s Project Star

- An example of nonexperimental data is survey data

  - Data on all variables are collected simultaneously, and the values
    are neither fixed nor repeatable

    > These are nonexperimental data  

## 数据类型  

- 截面数据（cross-section data）

  > 给定某个时间点横跨多个横截面单位的数据，常常是在某一个时间点（如2010年），搜集的关于个体或企业的数据。
  >
  > 观测值之间没有优先序
  > 截面数据的搜集，主要采用的是**“随机抽样”**的方法。
  >
  > **基本假设：**这些观测值之间在统计上是相互独立的。
  >
  > - 例子：
  > 	- ![example](https://gitee.com/h-ruc/note/raw/master/image-20220506230956815.png)
  > 	- ![image-20220506231216718](https://gitee.com/h-ruc/note/raw/master/image-20220506231216718.png)  

- 时间序列数据（time series data）

  > 给定某个横截面单位，纵跨多个时间点的数据
  >
  > - 时间序列数据可以按日、按周、按月、按年搜集
  > - 观测值的排序非常重要
  > - 观测值之间常常相关，呈现一定的趋势  
  > - 很少（即使能够） 假设经济数据的观测独立于时间  
  >
  > - 例子：
  > 	-  ![image-20220506231335839](https://gitee.com/h-ruc/note/raw/master/image-20220506231335839.png)
  > 	- ![image-20220506231349182](https://gitee.com/h-ruc/note/raw/master/image-20220506231349182.png)

- 面板数据（panel data)

  > - 纵跨多个时间点、横跨多个横截面单位的数据  
  >
  > - 同一横截面数据的数据单位都被跟踪了一段特定的时期  
  >
  >
  > - 例子
  >
  > 	- ![image-20220506231419491](https://gitee.com/h-ruc/note/raw/master/image-20220506231419491.png)

## 计量经济学关注的重点：因果关系（causality）  

- 统计学关注的主要是变量之间的相关性，而计量经济学着重关注
  的是因果关系。

- 为了表示某个自变量对因变量有因果关系，那么其它自变量对因
  变量的影响必须是已经被控制住了的。

- 在自然科学中，可以通过做实验来研究某个现象对另外一个现象
  的影响（因-果）

- 在现实的经济生活中，我们很难获得实验数据；即使能获得，那
  么实验数据的获得成本常常非常高。

- 在经济学研究中，我们常常搜集“可被观察的数” (observational
  data)  
  

### 因果关系举例  

- Lack of sleep may shrink your brain  

  > Can a lack of sleep affect the size of your brain? It's possible, a recent study published in an online issue of Neurology suggests.  
  >
  > "It is not yet known whether poor sleep quality is a cause or consequence of changes in brain structure," said author Claire Sexton of the University of Oxford in the United Kingdom.  

- Dogs Walked by Men Are More Aggressive  

  > Dogs being walked by men are four times more likely to threaten and bite other dogs and dogs on a leash are more likely to act aggressively than dogs off the leash  
  >
  > "The increased incidence of bites when dogs are being handled by males, rather than females, may simply be a reflection of dogs mirroring the emotions of their handlers; if their handlers are acting either defensively or assertively upon meeting, their dogs are likely to sense and reflect that."  

- $log(Wage)=a+b\ Years\ of\ Schooling+U\\$
  
  > U = other factors, for example, ability  
  >
  > 由于我们很难控制/观察到“能力”，因此我们常常会对教育
  > 程度对工资水平的边际影响做偏高的估计  

- 警察力量和犯罪情况  

  > $Number\ of\ Crimes = a + b\ Size\ of\ the\ Police\ Force + U$
  >
  > 在很多情况下，犯罪活动活跃的地方，警力的部属也较强。如果我们只是依赖这种简单的相关关系，就会错误地得出警力对犯罪率有正的影响。  

- Sex on TV and teen pregnancy  

  > $Prob\ of\ teen\ pregnancy= F (b_0 + b_1\ Exposure\ to\ Sex\ on\ TV+b_2\ Total\ TV)$
  >
  > 上面的例子中，存在“自选择” ：因为很难控制住个人对于性的兴趣，因此，就不能得出“Sex on TV”和青少年怀孕之间的因果关系  

### Correlation vs. causation （相关关系vs. 因果关系）  

> ![image-20220507162310779](https://gitee.com/h-ruc/note/raw/master/image-20220507162310779.png)

## The Research Process  

- Econometrics is ultimately a research tool
  - Students of econometrics plan to do research or they plan to read
    and evaluate the research of others, or both
  - Research is a process, and like many such activities, it flows
    according to an orderly pattern
    - Research is an adventure, and can be fun!  

## Steps in the research process  

1. Use economic theory to think about the problem

2. Develop a working economic model leading to an econometric model
3. Obtain sample data and choose a desirable method of statistical analysis based on initial assumptions and an understanding of how the data were collected
4. Estimate the unknown parameters with the help of a statistical software package, make predictions, and test hypotheses
5. Perform model diagnostics to check the validity of assumptions
6. Analyze and evaluate the economic consequences and the implications of the empirical results   

## 学习这门课必备的基础 Mathematics & Statistics  

- Students on this course are not required to have studied
  statistics
- However, mathematics and statistics are very important
  tools for econometrics
- So a background in statistics certainly helps
- Absolutely essential material (mathematics):
  - Linear functions, $e.g.\ y = β_0 + β_1x$, where y, x are
    variables and $β_0 , β_1$ are parameters  (constants).
  - Proportions and percentages
  - The natural logarithm: $y = log(x) [or\ y=ln(x)]$
  - The exponential function: $y = \exp(x)$
  - Simple calculus  