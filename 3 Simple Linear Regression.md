# 3 Simple Linear Regression

[TOC]  

## What is regression analysis?  

Regression analysis is concerned with the study of the dependence of one vari-able, the dependent variable, on one or more other variables, the explanatory vari-ables, with a view to estimating and/or predicting the (population) mean or aver-age value of the former in terms of the known or fixed (in repeated sampling) values of the latter. 

## Some Terminology（术语）  

### In the simple linear regression model, ==$y = \beta_0 + \beta_1x + u$==  

- We typically refer to y as the
  - Dependent Variable, or
  - Left-Hand Side Variable, or
  - Explained Variable, or
  - Regressand
- We typically refer to x as the
  - Independent Variable, or
  - Right-Hand Side Variable, or
  - Explanatory Variable, or
  - Regressor, or
  - Covariate, or
  - Control Variables  

> ![image-20220508173450193](https://gitee.com/h-ruc/note/raw/master/image-20220508173450193.png)

- Error term u contains ：

  - Effects of other factors

    > e.g. habit, food structure

  - Measurement error 测量误差

    > e.g. calculation mistake

## A Simple Assumption: Mean Error Term  

- The average value of u, the error term, in the population is 0. That is, $E(u) = 0$

  > Note: this is not a restrictive assumption, since we can always use b~0~ to normalize $E(u)$ to 0  

## Zero Conditional Mean  

- We need to make a crucial assumption about how u and x are related: we want it to be the case that knowing something about x does not give us any information about u, so that they are completely unrelated, i.e. $E(u|x)=0$.
- $E(u|x)$ implies $E(y|x)$ = b~0~ + b~1~x 
- When $E(u|x) =0$, we have $E(u) = 0  $

## Ordinary Least Squares （普通最小二乘法）  

- The basic idea of regression is to estimate **the population parameters** from a <u>sample.</u>

- Let $\{(xi,yi): i=1, …,n\}$ denote a random sample of size n from the
  population that satisfifies $y = \beta_0 + \beta_1x + u$

- Then, for each observation i (任意一个观测值i) in this sample,it will be the case that $y_i = \beta_0 + \beta_1x_i + u_i$

- Population regression line, data points and the associated error termsf  

  > ![image-20220508175618536](https://gitee.com/h-ruc/note/raw/master/image-20220508175618536.png)

- $E(y|x)$ as a linear function of x, where for any x, the distrihution of y is centered about $E(y|x) $

  > ![image-20220508180306002](https://gitee.com/h-ruc/note/raw/master/image-20220508180306002.png)

### Population regression function/line  

> ![image-20220508180813523](https://gitee.com/h-ruc/note/raw/master/image-20220508180813523.png)

- Regression evaluates numerical relation between economic
  variables.

  - Linear regression： assuming population parameters are linear

  - Simple regression： relation of one variable and the other variable

    > $y_i = E(y | x_i ) + u_i = \beta_0 + \beta_1x_i + u_i$  

    - 𝑦~𝑖~: dependent variable(因变量)
    - 𝑥~𝑖~:independent variable(自变量 )
    - 𝛽~0~: Intercept(截距项)
    - 𝛽~1~: Slope(斜率 )
    - 𝑢~𝑖~: error term(误差项)

### Sample regression function (SRF)  

- The sample counterpart of PRF can be written as:

  > $𝑌_𝑖 = \hat 𝛽_0 + \hat 𝛽_1 𝑋_𝑖 + \hat 𝑢_𝑖 = \hat 𝑌_i + \hat 𝑢_𝑖$

  - where $\hat 𝑌$ is read as "Y-hat" or "Y-cap" ,$\hat 𝑌_i$ = estimator of $E(Y | X_i) $
  - $\hat𝛽_0$: the estimator of population parameter 𝛽~0~（总体参数𝛽~0~ 的估计值）
  - $\hat𝛽_1$: the estimator of population parameter 𝛽~1~（总体参数𝛽~1~ 的估计值）

  > ![image-20220508181848631](https://gitee.com/h-ruc/note/raw/master/image-20220508181848631.png)

### Deriving M.O.M. （矩估计） Estimates  

- The method of moments （ M.O.M.） approach to estimation implies imposing the population moment restrictions on the sample moments

- To derive the M.O.M. estimates we need to realize that our main assumption of $E(u|x) = E(u) = 0$ also implies that $Cov(x,u) = E(xu) = 0$

  > ==Note:==
  >
  > - Remember from basic probability that $Cov(X,Y) = E(XY) – E(X)E(Y)$
  > - What does $E(u) =E(y – \beta_0 – \beta_1x) = 0$ mean? Recall that for E(X), the mean of a population distribution, a sample estimator of E(X) is simply the arithmetic mean of the sample  

- We can write our 2 restrictions just in terms of x, y, $\beta_0$ and $\beta_1$ ,since $u = y – \beta_0 – \beta_1x$

  > **==population moment restrictions==**  

  - $E(u)=E(y – \beta_0 – \beta_1x) = 0$
  - $E(xu)=E[x(y – \beta_0 – \beta_1x)] = 0$

- Based on population moment restrictions, we find sample analogy as follows, using <u>the law of large samples</u>: 

  > **==Sample analogy==**  
  > $$
  >  \begin{align}
  >  &\sum(𝑦_𝑖 − 𝑏_0 − 𝑏_1𝑥_𝑖) = 0 \\
  >  &\sum𝑥_𝑖(𝑦_𝑖 − 𝑏_0 − 𝑏_1𝑥_𝑖) = 0
  >  \end{align}
  > $$
  >  **注**：这里隐含了$n→ ∞$时，样本均值才依概率收敛于总体的均值。因此， n的数量必须不能小于一定的数（通常至少不能小于30） .  

### Ordinary Least Squared (OLS) Estimation  

- Assume we have data on income and expenditure, how to calculate β~0~ and β~1~ ？

- OLS calculates b~0~, b~1~ , estimation of β~0~,β~1~ by minimizing sum of squared residuals

  - Residual: $\hat 𝑢_𝑖 = 𝑦_𝑖 - 𝑏_0 - 𝑏_1𝑥_𝑖$

  - Minimize sum of squared residuals

    > $\min \limits_{𝑏_0,𝑏_1} \sum\limits_{𝑖=1}^{𝑛}(𝑦_𝑖 - 𝑏_0 - 𝑏_1𝑥_𝑖)^2$

  - $$
    \begin{align}
    &\cfrac{𝜕}
    {𝜕𝑏_0} = -2 \sum(𝑦_𝑖 - 𝑏_0 - 𝑏_1𝑥_𝑖) = -2 \sum \hat𝑢_𝑖 = 0 \\
    &\cfrac{𝜕}
    {𝜕𝑏_1} = -2 \sum 𝑥_𝑖(𝑦_𝑖 - 𝑏_0 - 𝑏_1𝑥_𝑖) = -2 \sum 𝑥_𝑖\hat 𝑢_𝑖 = 0 
    \end{align}
    $$

#### Calculate b~1~

- $$
  \begin{align}
  &\bar{y}-b_00-b_1\bar x=0⇒ 𝑏_0 = 𝑦 − 𝑏_1𝑥\\
  &\sum 𝑥_𝑖[𝑦_𝑖 − ( 𝑦 − 𝑏_1𝑥) − 𝑏_1𝑥_𝑖] = 0\\
  &\sum 𝑥_𝑖[(𝑦_𝑖 − \bar 𝑦) − 𝑏_1(𝑥_𝑖 − \bar 𝑥)] = 0\\
  &\sum 𝑥_𝑖(𝑦_𝑖 − \bar 𝑦) − 𝑏_1 \sum 𝑥_𝑖(𝑥_𝑖 − \bar 𝑥) = 0\\
  &𝑏_1 =
  \sum \cfrac{𝑥_𝑖(𝑦_𝑖 − \bar 𝑦)}
  {\sum 𝑥_𝑖(𝑥_𝑖 − \bar𝑥)} =\cfrac
  {\sum(𝑥_𝑖 − \bar𝑥)(𝑦_𝑖 − \bar𝑦)}
  {\sum(𝑥_𝑖 − \bar𝑥)^2}
  \end{align}
  $$

#### Algebraic Properties of OLS Estimation  

- $\cfrac{\partial}{\partial b_0}=-2\sum (y_i-b_0-b_1x_1)=-2\sum\hat u_i=0$

- $\cfrac𝜕 {𝜕𝑏_1} = -2 \sum 𝑥_𝑖(𝑦_𝑖 - 𝑏_0 - 𝑏_1𝑥_𝑖) = -2 \sum 𝑥_𝑖\hat 𝑢_𝑖 = 0   $

- $\bar 𝑦 - 𝑏_0 - 𝑏_1\bar 𝑥 = 0   ⇒ \bar 𝑦 = 𝑏_0 + 𝑏_1 \bar x $

- ==注：无论E(u)=0和E(xu)=0这两个条件是否成立，以上三条永远成立。原
  因：它们是从OLS的优化过程中推导出来的代数性质。==

  > ![image-20220511211802513](https://gitee.com/h-ruc/note/raw/master/image-20220511211802513.png)

#### When $n→∞$  

- $\lim\limits_{𝑛→∞}𝑏_1 =\cfrac{𝐶𝑜𝑣(𝑥_𝑖, 𝑦_𝑖)}{𝑉𝑎𝑟(𝑥_𝑖)}  $

### 拟合优度  

- $𝑦_𝑖 = \hat 𝑦_𝑖 + \hat 𝑢_𝑖$

- $\hat y_𝑖 = 𝑏_0 + 𝑏_1𝑥_𝑖$, is explained part

- $\hat u_𝑖 = 𝑦_𝑖 - \hat 𝑦_𝑖$, is unexplained part෍

-  $\sum (𝑦_𝑖 - \bar𝑦)^ 2$ is the total sum of squares **(SST)** 总平方和

-  $\sum(\hat y_𝑖 - \bar 𝑦)^ 2$ is the explained sum of squares **(SSE)** 解释平方和

-  $\sum \hat𝑢_𝑖^2$ is the residual sum of squares **(SSR)** 残差平方和

- Then **SST = SSE + SSR**

  > $R^2 = \cfrac{𝑆𝑆𝐸}{𝑆𝑆𝑇} = 1 -\cfrac{𝑆𝑆𝑅}{𝑆𝑆𝑇} $ evaluates how well SST in 𝑦~𝑖~ is explained by 𝑥~𝑖~
  >
  > ![image-20220512223916542](https://gitee.com/h-ruc/note/raw/master/image-20220512223916542.png)

## Assumptions underlying the OLS method  

- Our goal is not only to obtain the estimated values of $\beta_0,\beta_1$, but also to draw inferences about the true.In other words, we need **unbiased estimators**. To this end, we need to make some assumptions for OLS method. This is often known as **==“Gauss-Markov assumptions”==**

  ### Assumptions for unbiasedness of SLR  

  - SLR 1： population model is linear in parameters

    > $y=\beta_0+\beta_1x+u$

  - SLR 2： random sampling

    > $Cov({X_i,X_j})=Cov({u_i,u_j})=0$

  - SLR 3： there are variations in X

    > $\sum\limits_{i=1}^n(x_i-\bar x)^2\ne0$

  - SLR 4： Zero conditional mean $E(u|x)=0$

    > b.c. random sampling, $E(u_i|x_i)=0$
    > – a： Zero mean E(u)=0
    > – b： uncorrelated E(ux)=0
    >
    > 𝑂𝐿𝑆的数值特征
    > $\sum\hat 𝑢_𝑖 = 0$
    > $\sum\hat 𝑢_𝑖𝑥_𝑖 = 0  $

  
  ### 		Homoscedasticity assumption  
  
  - SLR 5: homoscedasticity $Var(u|x)= σ^2$
  
    > $$
    > \begin{align}
    > &𝑉𝑎𝑟(𝑢|𝑥) = E(𝑢^2|𝑥) - [E(𝑢|𝑥)] ^2\\
    > &b.c. E(𝑢|𝑥) = 0， 𝑉𝑎𝑟(𝑢|𝑥) = 𝜎^2\\
    > &so E(𝑢^2|𝑥) = 𝜎^2\\
    > &so E(𝑢^2) = 𝜎^2
    > 
    > \end{align}
    > $$
  
  - 