# 2 Probability and statistics introduction  

[TOC]

## Probability basics  



- Sample space （样本空间Ω） is the collection of all possible outcomes of a random experiment, often noted as Ω={𝝎}

- In simple coin tossing the sample space is
  > $$
  > Ω = \{𝐻𝑒𝑎𝑑𝑠, 𝑇𝑎𝑖𝑙𝑠\}
  > $$
  
-  When rolling a fair die the sample space is
  > $$
  > Ω = \{1,2,3,4,5,6\}
  > $$
### Event（事件）

- An event is a subset of the sample space to which we will assign a probability

- For the fair die we have, $e.g.$, for the event of  ”odd”

  > $$
  > 𝑃 (𝑜𝑑𝑑) = 𝑃( \{1,3,5\} )= 0.5
  > $$
### Operations on sets/events

- For two events 𝐴 and 𝐵 we introduce the operations:

- Union 𝐴 ∪ 𝐵 which means that either 𝐴 or 𝐵 or both occur (when we say ”or” we do not mean ”exclusive or”)

- Intersection 𝐴 ∩ 𝐵 which means that 𝐴 and 𝐵 both occur  

- The complement 𝐴𝑐 of an event 𝐴 is the event that 𝐴 does not occur  

  > ![image-20220507165723733](https://gitee.com/h-ruc/note/raw/master/image-20220507165723733.png)
  >
  > ![image-20220507165733677](https://gitee.com/h-ruc/note/raw/master/image-20220507165733677.png)

### Probability axioms  

- The cornerstones on which probability theory is built
- 𝑃(𝐴) ≥ 0
- 𝑃(𝑆) = 1
- 𝑃(𝐴∪𝐵) ≤ 𝑃(𝐴)+ 𝑃(𝐵) 
- 𝑃(𝐴^𝑐^) = 1 - 𝑃(𝐴)
- 𝑃 (𝐴∪𝐵) = 𝑃(𝐴) + 𝑃(𝐵) - 𝑃(𝐴∩𝐵)
- If 𝐴 is a subset of 𝐵 then 𝑃(𝐴) ≤ 𝑃(𝐵)
- Graphically verify these using Venn diagrams!  
### Independent events

- Two events 𝐴 and 𝐵 are said to be independent if  

  > 𝑃 (𝐴 ∩ 𝐵) = 𝑃(𝐴)𝑃(𝐵)  

### Random variables  

- A random variable 𝑋 is a mapping from the sample space to the real numbers  

  > 𝑋: 𝑆 → ℝ  
  >
#### Discrete r.v.’s

A r.v. 𝑋 is said to be discrete if 𝑃 (𝑋 = 𝑥~𝑖~) > 0 for some list of numbers {𝑥~𝑖~ }  

#### Continuous r.v.’s  

- A r.v. 𝑋 is said to be continuous if it can take any value in an interval (or collection of intervals)

- For a continuous r.v. there exists a (non-negative) density function 𝑓 such that

  > 𝑃 (𝑎 ≤ 𝑋 ≤ 𝑏) = $\int_a^b$𝑓(𝑥)𝑑𝑥
  > I.e., probabilities are areas under a certain curve   

- 𝑃(S)=$\int_{-∞}^∞$𝑓(𝑥)𝑑𝑥 = 1

- 𝑃 (𝑎 < 𝑋 < 𝑏) = 𝑃 (𝑎 ≤ 𝑋 < 𝑏) = 𝑃 (𝑎 < 𝑋 ≤ 𝑏) = 𝑃 (𝑎 ≤ 𝑋 ≤ 𝑏)

  > since 𝑃 (𝑋 = 𝑏) = 𝑃 (𝑋 = 𝑎) =$\int_{b}^{b}$𝑓(𝑥)𝑑𝑥 = $\int_{a}^{a}$𝑓(𝑥)𝑑𝑥=0

### Distribution function  

- For a random variable 𝑋 we define its distribution function by  

  > 𝐹 (𝑥) = 𝑃(𝑋 ≤ 𝑥)  
  >
  > Note that 𝐹(𝑥) → 0 as $𝑥 → -∞$, 𝐹(𝑥) → 1 as $𝑥 → ∞$ and 𝐹(𝑥) ≤ 𝐹(𝑦) for 𝑥 < 𝑦  

#### Distribution function of a discrete r.v  
- For a discrete r.v. 𝑋 the distribution function is given by  

  > $F(x)=\sum\limits_{y\le x}P(X=y)$

#### Distribution function of a continuous r.v.  

- For a continuous r.v. 𝑋 the distribution function is given by

  > 𝐹(𝑥) = $\int_{-∞}^{𝑥}$𝑓 (𝑦) 𝑑𝑦

- ”The area under the curve from far left up to 𝑥”

  > Note that 𝐹′ 𝑥 = 𝑓(𝑥)  S

### Expected value

- For a random variable 𝑋 we define its Expected value by

  > $E(X)=\int_{-\infty}^{x}xf(x) $

#### Expected value of a discrete r.v.  

- For a discrete r.v. 𝑋 the expected value or (theoretical) mean is given by weighting the possible values of 𝑋 with its respective probabilities and summing  

  > $𝐸( 𝑋 )= \sum\limits_{𝑎𝑙𝑙\ 𝑥 }𝑥𝑃(𝑋 = 𝑥)  $

#### Expected value of a continuous r.v  

- The (theoretical) mean or expected value of continuous r.v. is

  > 𝐸 (𝑋) = $\int_{-∞}^{∞}$𝑥𝑓 (𝑥) 𝑑𝑥 

- For a standard normal 𝑋, we have 𝐸 (𝑋) = 0 (verify this) 

###  Computational rule  

- Let 𝑎 and 𝑏 be constants and 𝑋 and 𝑌 be r.v.’s, Then

  > 𝐸 [𝑎𝑋 + 𝑏𝑌] = 𝑎𝐸[𝑋] + 𝑏𝐸[𝑌]

- For an arbitrary function 𝑔, we have  

  > $$
  > E[g(x)]=\left\{ \begin{array}{l}
  > 	\sum_{all\ x}{g\left( xP\left( X=x \right) \right)}\\
  > 	\int_{-\infty}^{\infty}{g\left( x \right) f\left( x \right)}\\
  > \end{array} \right.
  > $$
### Variance and standard deviation

- The variance of an r.v. 𝑋 is 

  >  𝑉𝑎𝑟 (𝑋) = 𝐸 [𝑋 - 𝐸[𝑋]^2^]

- So the the variance is a measure of dispersion around the mean

- The standard deviation of 𝑋 is the square root of 𝑉𝑎𝑟(𝑋)

  > $𝑆𝐷(𝑋) = \sqrt{𝑉𝑎𝑟(𝑋)} $  

#### Standard deviation  

- Standard deviation is often used as a measure of dispersion since it is expressed in the ”same units” as ”the data”
- If the units of ”the data” are USD the standard deviation is expressed in USD
-  Standard deviation may be used as a (crude) measure of risk of an asset  

#### Variance  

- Computational formula for variance
  𝑉𝑎𝑟(𝑋) = 𝐸[𝑋^2^] - (𝐸[𝑋])^2^

  > It is a good exercise to verify this and that **𝑉𝑎𝑟 (𝑋) ≥ 0**     ==ALWAYS!== 

#### Variance computational rule  

- If 𝑎 and 𝑏 are constants and 𝑋 is a random variable then

  > 𝑉𝑎𝑟(𝑎+𝑏𝑋) = 𝑏^2^𝑉𝑎𝑟(𝑋) 



### Covariance and correlation  

- For two continuous r.v.’s 𝑋 and 𝑌 there may exist a non-negative joint density function 𝑓 such that  

  > $𝑃(𝑎<𝑋<𝑏,𝑐<𝑌<𝑑)=\int_𝑏^𝑎\int_𝑐^𝑑𝑓(𝑥,𝑦)𝑑𝑥𝑑𝑦$

- Two continuous r.v.’s 𝑋 and 𝑌 are said to be independent if the joint density is product of the density of 𝑋 and the density of 𝑌

  > 𝑓(𝑥,𝑦)=𝑓~𝑋~(𝑥)𝑓~𝑌~(𝑦)

- So if 𝑋 and 𝑌 are independent then 

  > 𝑃( 𝑎<𝑋<𝑏 , 𝑐<𝑌<𝑑)=𝑃(𝑎<𝑋<𝑏)𝑃(𝑐<𝑌<𝑑)

- The linear dependence between 𝑋 and 𝑌 may be measured by their covariance

  > 𝐶𝑜𝑣 (𝑋, 𝑌) = 𝐸[𝑋𝑌] - 𝐸[𝑋]𝐸[𝑌]

- For two continuous r.v.’s 𝑋 and 𝑌

  > $𝐸[𝑋𝑌] = \int_{-∞}^∞\int_{-∞}^∞𝑥𝑦𝑓( 𝑥, 𝑦) 𝑑𝑥𝑑𝑦$

- Note that if 𝑋 and 𝑌 are independent then

  > 𝐶𝑜𝑣 (𝑋, 𝑌) = 0  

- However, 𝐶𝑜𝑣 𝑋, 𝑌 = 0 does not necessarily imply independence, since covariance only measures linear dependence

- 𝐶𝑜𝑣 (𝑋, 𝑋) = 𝑉𝑎𝑟(𝑋)  

- 𝑉𝑎𝑟 (𝑋 ± 𝑌) = 𝑉𝑎𝑟 (𝑋) + 𝑉𝑎𝑟(𝑌) ± 2𝐶𝑜𝑣(𝑋, 𝑌)  

  > ==There is NEVER a minus sign between 𝑉𝑎𝑟 (𝑋) and 𝑉𝑎𝑟(𝑌)==

- Note that for independent r.v.’s 𝑋 and 𝑌

  > 𝑉𝑎𝑟 (𝑋 ± 𝑌) = 𝑉𝑎𝑟 𝑋 + 𝑉𝑎𝑟(𝑌) 

- For independent r.v.’s 𝑋~1~, … , 𝑋~𝑛~ and constants 𝑎~1~, … , 𝑎~𝑛~ we have that

  > $𝑉𝑎𝑟(\sum\limits_{𝑖=1}^{𝑛}𝑎_𝑖𝑋_𝑖 )=\sum\limits_{𝑖=1}^{𝑛}𝑎_𝑖^2𝑉𝑎𝑟( 𝑋_𝑖)$

- The covariance of two r.v.’s may be any real number and it is more useful to have measure of linear dependence that takes values in a more narrow interval

- The correlation of 𝑋 and 𝑌 is given by  

  > $𝐶𝑜𝑟𝑟 (𝑋, 𝑌) =\cfrac{𝐶𝑜𝑣(𝑋, 𝑌)}{\sqrt{𝑉𝑎𝑟 (𝑋) 𝑉𝑎𝑟(𝑌) }}$

#### Correlation  

- In many books and papers correlation is denoted by 𝜌 (rho) and it can be shown that

  > -1 ≤ 𝜌 ≤ 1 

- Also if 𝜌 = -1 then Y = 𝑎𝑋 + 𝑏 for 𝑎 < 0

- And if 𝜌 = 1 then Y = 𝑎𝑋 + 𝑏 for 𝑎 > 0  

### Conditional probability/expectation  

- When wanting to express more general (than linear, though including linear) relationships between random variables the notion of conditional expectation is useful  

#### Conditional probabilities for events  

- For two events 𝐴 and 𝐵 the conditional probability of ”𝐴 given 𝐵” is given by

  > $𝑃(𝐴|𝐵) =\cfrac{𝑃(𝐴 ∩ 𝐵)}{𝑃(𝐵)}$

- We may think of this as reducing the sample space to 𝐵

-  **Bayes theorem**  

  >  $𝑃(𝐴|𝐵) =\cfrac{𝑃(𝐵|𝐴)𝑃(𝐴)}{𝑃(𝐵)}$

- If 𝐴 and 𝐵 are independent then 

  > 𝑃 (𝐴|𝐵) = 𝑃(𝐴)  

#### Conditional probabilities for r.v.’s

- For discrete r.v.’s 𝑋 and 𝑌 the conditional probability of 𝑋 = 𝑥 given 𝑌 = 𝑦 is

  > $𝑃 (𝑋 = 𝑥|𝑌 = 𝑦 )= \cfrac{𝑃(𝑋=𝑥,𝑌=𝑦)}{𝑃(𝑌=𝑦)}$
  > where 𝑋 = 𝑥, 𝑌 = 𝑦 should be interpreted as
  > \{𝑋 = 𝑥\} ∩ \{𝑌 = 𝑦 \}

- For continuous r.v.’s 𝑋 and 𝑌 conditional probabilities are given by introducing the conditional density

  > $𝑓 (𝑦|𝑥) =\cfrac
  > {𝑓(𝑥, 𝑦)}
  > {𝑓(𝑥)}$
  > where 𝑓(𝑥, 𝑦) denotes the joint density of 𝑋
  > and 𝑌 and 𝑓(x) denotes the density of 𝑋  

#### Conditional expectation  

- When trying to establish the relationship between the random variables 𝑋 and 𝑌 it is convenient to use the conditional expectation 𝐸[𝑌|𝑋 = 𝑥]

- This is a deterministic entity whose value is our ”best guess” of 𝑌 given that 𝑋 takes the value 𝑥  

  ##### If we know the distributions  

  - For discrete 𝑋 and 𝑌

    > $𝐸 [𝑌| 𝑋 = 𝑥] = \sum\limits_
    > {𝑎𝑙𝑙\ 𝑦}
    >  𝑦𝑃(𝑌 = 𝑦|𝑋 = 𝑥)$

  - For continuous 𝑋 and 𝑌

    > $𝐸[ 𝑌 |𝑋 = 𝑥 ]= \int_
    > {-∞}
    > ^∞
    > 𝑦 𝑓( 𝑦| 𝑥 )𝑑𝑦  $

##### Rules of conditional expectation  

- No matter if we condition on the event ”𝑋 = 𝑥”, the random variable 𝑋 or a larger information set ℱ the following (and then some, see e.g. Woolridge App. B) rules hold
  - 𝐸 [𝑎𝑌 + 𝑏𝑋|𝑋 = 𝑥] = 𝑎𝐸 [𝑌|𝑋 = 𝑥] + 𝑏𝑥 or 𝐸 [𝑎𝑌 + 𝑏𝑋|𝑋] = 𝑎𝐸 [𝑌|𝑋] + 𝑏𝑋
    or equivalently if the information generated by 𝑋 is contained in ℱ then 𝐸 [𝑎𝑌 + 𝑏𝑋|ℱ] = 𝑎𝐸 [𝑌|ℱ] + 𝑏𝑋
  - If 𝑌 is independent of 𝑋 or independent of ℱ then
    𝐸 [𝑌|𝑋 = 𝑥] = 𝐸[𝑌], 𝐸 [𝑌|𝑋] = 𝐸 [𝑌] or 𝐸 [𝑌|ℱ] = 𝐸[𝑌]
  - 𝐸 [𝐸 [𝑌|𝑋]] = 𝐸[𝑌] or 𝐸 [𝐸 [𝑌|ℱ] ]= 𝐸[𝑌]  

## In practice  

- In practical statistics or econometrics we often want to estimate population parameters from data

- If we observe a sample 𝑥~1~, … , 𝑥~𝑛~ from a normal population/r.v. with unknown mean 𝜇 it is natural to estimate 𝜇 by

  > $\bar𝑥 =\frac{1} {𝑛}\sum\limits^𝑛_{i=1}𝑥_𝑖$

- In the same manner we may estimate the variance by
  $\frac{1}{𝑛 - 1} \sum\limits_{𝑖=1}^𝑛(𝑥_𝑖 - \bar 𝑥) ^2$
- We get an estimate of the standard deviation if we take the square root in the above expression  
- Also, given pairwise observations (𝑥~1~, 𝑦~1~) , … , (𝑥~𝑛~, 𝑦~𝑛~) we may estimate the covariance of 𝑋 and 𝑌 by
  $\cfrac{1}{𝑛 - 1} \left(\sum\limits_{𝑖=1}^𝑛{𝑥_𝑖𝑦_𝑖} -\cfrac{\sum_{𝑖 =1}^{𝑛} 𝑥_𝑖 \sum_{𝑗 =1}^𝑛 𝑦_𝑗}{𝑛}\right)$
- The estimated correlation is given by dividing by the product of the estimated stanbard deviations of 𝑋 and 𝑌  

## Linear regression  

- Now lets assume that we want to find the straight line that ”fits best” to our data

- We may denote the line $\hat 𝑦 = 𝑏_0 + 𝑏_1𝑥$

- Our wish is to find the ”optimal” constants 𝑏~0~ and 𝑏~1~

- The ”y-coordinate” on the line for a given data point (𝑥~𝑖~, 𝑦~𝑖~) is $\hat 𝑦_𝑖 = 𝑏_0 + 𝑏_1𝑥_𝑖$

- We may find the optimal (in the mean square sense) 𝑏~0~ and 𝑏~1~ by minimizing

  > $\sum\limits^{𝑛}_{i=1}(𝑦_𝑖 -\hat 𝑦_𝑖 )^2 = \sum\limits_{𝑖=1}
  > ^{𝑛}({𝑦_𝑖 - 𝑏_0 - 𝑏_1𝑥_𝑖 })^2$
  > w.r.t. 𝑏~0~ and 𝑏~1~  

- A little calculus gives  

  > $$
  > 𝑏_1 =\cfrac
  > {\sum\limits_{𝑖 =1}^{𝑛} {𝑥_𝑖𝑦_𝑖} −\cfrac
  > {\sum\limits_{𝑖 =1}^{𝑛} {𝑥_𝑖} \sum\limits_{𝑗 =1}^n 𝑦_𝑗}
  > {𝑛}}
  > {\sum\limits_{𝑖 =1}^{𝑛} 𝑥_𝑖^2 − \cfrac{\left(\sum\limits_{𝑖 =1}^{𝑛} 𝑥𝑖\right) ^2}{n}}\\
  > 𝑏_0 = \bar 𝑦 − 𝑏_1\bar 𝑥
  > $$

- We may think of the linear regression as a case of conditional expectation

- For this we should consider the response variable 𝑌 and the explanatory variable 𝑌 as random entitities so that the line is given by

  > 𝑌 = 𝛽~0~ + 𝛽~1~𝑋 + 𝜀
  > where 𝜀 is independent of 𝑋 and has mean zero  

- The conditional expectation of 𝑌 given 𝑋 = 𝑥 is 

  > 𝐸 [𝑌|𝑋 = 𝑥] = 𝐸 [𝛽~0~ + 𝛽~1~𝑋 + 𝜀|𝑋 = 𝑥]= 𝛽~0~ + 𝛽~1~𝑥

- Then we estimate the intercept 𝛽~0~ and the slope 𝛽~1~ from data using e.g., least squares as above  

- Note that **𝐸 [𝑌|𝑋 = 𝑥]** is a deterministic entity 

- We may also define conditional expectation as
  a random variable **𝐸[𝑌|𝑋]**  

## Prediction of time series

- In time series analysis or econometrics it is often of interest to predict future values of the series {𝑋~𝑡~}~𝑡≥0~ using the information available up until the time when the predicition is made
- In this case, letting ℱ~𝑡~ denote the information available at time 𝑡, our best guess (in the mean square sense) of 𝑋~𝑡+ℎ~ is 𝐸 [𝑋~𝑡+ℎ~| ℱ~𝑡~]  

## Statics

### The most important distribution  

- A (continuous) r.v. 𝑍 is said to have standard normal distribution if its density is  

 > $$
 > f\left( x \right) =\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}},\;x\in \left( -\infty ,\;+\infty \right)
 > $$
 >
 > ![image-20220507210046916](https://gitee.com/h-ruc/note/raw/master/image-20220507210046916.png)

- The probability that 𝑍 ≤ 𝑧 is the area under the ”bell shape” from ”far left” to 𝑧  
- It should be noted that for a standard normal r.v. 𝑍 probabilities are not possible to ”calculate by hand” since there does not exist a primitive function for the density 
- In many books the distribution function of a standard normal r.v. is denoted
  $Φ(𝑧) = 𝑃(𝑍 ≤ 𝑧) =\frac{1}{\sqrt{2𝜋}}\int_{-∞}{𝑧}𝑒^{-\frac{𝑥^2}{2}} 𝑑𝑥$
- Values of $Φ$ for different values of 𝑧 are found in tables or using numerics  

#### Symmetries  

- Since the ”bell shape” is symmetric it follows that

  > $Φ (-𝑧) = 1 - Φ (𝑧)$ 

- Verify this by drawing some ”filled bell shapes” for different values of 𝑧  

#### Scale and location

- A (continuous) r.v. 𝑋 is said to have normal distribution with mean 𝜇 and standard deviation 𝜎 if 

  > 𝑋 = 𝜇 + 𝜎𝑍
  > where 𝑍 is standard normal  

#### Standardizing a normal r.v  

- If 𝑋 is normal with mean 𝜇 and standard deviation 𝜎 then $𝑍 =\frac{𝑋 - 𝜇}{𝜎}$ is standard normal  

#### Normal r.v.’s  

- The standard deviation of a standard normal r.v. is 1 (good exercise in integrating by parts)
- For a normal r.v. 𝑋 = 𝜇 + 𝜎𝑍, where 𝑍 is standard normal, we have (verify this)
  𝐸 [𝑋] = 𝜇 and  𝑉𝑎𝑟 (𝑋) = 𝜎2 and thus 𝑆𝐷 𝑋 = 𝜎  

#### Why is the normal distribution so important? (CGS)  

- Starting from a sample, i.e., a collection of independent and identically distributed r.v.’s 𝑋~1~, … , 𝑋~𝑛~, with mean 𝜇 and standard deviation 𝜎 it can be shown that the distribution of $\cfrac{\frac{1}{𝑛}\sum\limits_{𝑖=1} ^𝑛 𝑋_𝑖 - 𝜇}{𝜎\sqrt 𝑛}$ approaches the standard normal as the sample size 𝑛 increases  

### Some more statistics  

- In statistics the normal distribution is highly important since many statistical methods require normally, or at least approximately normally, distributed data
- There are also some important distributions derived from the normal upon which some important statistical methods are built

####   Some distributions derived from the normal  

- The $\chi^2$ (chi-square) distribution with 𝑛 degrees off reedom is what you get if you add 𝑛 squaredi ndependent standard normals

  > $𝑋 = \sum\limits_{𝑖=1}^{𝑛} 𝑍_𝑖^2$

  - This distribution is usually present when trying to estimate variances for normal popoulations  

- The (Student) 𝑡 distribution is what you get if you let

  > $𝑇 =\cfrac{𝑍}{\sqrt{𝑋/𝑛}}$
  > where 𝑍 is standard normal and 𝑋 is $χ^2$ with 𝑛 degrees of freedom and independent of 𝑍

  - This distribution is usually present when trying to estimate or compare means of normal populations for which the variance is unknown  

- The 𝐹 distribution with 𝑘 and 𝑙 degrees of freedom is what you get if you define

  > $𝐹 =\cfrac{𝑋_𝑘/𝑘}{𝑋_𝑙/𝑙}$
  > where 𝑋~𝑘~ and 𝑋~𝑙~ are independent ”chi-squares” with 𝑘 and 𝑙 degrees of freedom, respectively

  - This distribution is usually present when trying to compare
    variances of two independent normal populations  

### Central Limit Theorem  

- if you start with a sample from ==ANY== distribution (with well defined mean
  and std.dev) the sample mean $\bar𝑋 = \frac{1}{𝑛}\sum\limits_{𝑖=1}^ 𝑛 𝑋_𝑖$ has an approximate normal distribution  

### Point and interval estimates  

- In statistics it is often of interest two estimate population parameters and above we have seen some examples of point estimates for means, variances, covariances, slopes etc...
- To get better control of how precise your point estimates are it is useful to introduce confidence intervals  

### Confidence intervals  

- We say that a (1 - 𝛼) ∙ 100% confidence interval for the population parameter 𝜃 is a random interval [𝐿, 𝑈] such that

  > 𝑃 (𝐿 ≤ 𝜃 ≤ 𝑈) = 1 - 𝛼  

- For a normal population with known variance 𝜎^2^ a 95% c.i. for the **(unknown)** mean 𝜇, based on the sample 𝑋~1~, … , 𝑋~𝑛~, is 

  > $𝑃 (\bar𝑋 - 1.96 𝜎/\sqrt 𝑛 ≤ 𝜇 ≤ \bar𝑋 - 1.96 𝜎\sqrt 𝑛) = 0.95$

- The observed confidence interval in the above case is

  > $\bar𝑥 - 1.96 𝜎/\sqrt 𝑛 , \bar𝑥 - 1.96 𝜎/\sqrt 𝑛$

- It should be noted that at this point, i.e., once the confidence interval is realized it is pointless to think that it cointains the true value of 𝜇 with 95% probability since there is ”nothing random left” (all quantities comprising the interval are deterministic and the true, though unknown but deterministic, parameter value is either inside or outside the interval)

- When interpreting realized confidence intervals we should think; If we create a whole lot of 95% confidence intervals for a large bunch of different parameters, 95% of them will contain the true parameter values  

### Hypothesis testing  

- Related to parameter estimation is hypothesis testing for parameters

- Hypothesis testing may also concern more ”advanced matters” such as ”does the data at hand come from a normal distribution”  

  #### Hypothesis testing in general  

  - First we set up som hypotheses

    > 𝐻~0~: 𝑠𝑡𝑎𝑡𝑒𝑚𝑒𝑛𝑡 𝑡𝑟𝑢𝑒
    > 𝐻~1~: 𝑠𝑡𝑎𝑡𝑒𝑚𝑒𝑛𝑡 𝑓𝑎𝑙𝑠𝑒

  - 𝐻~0~ is called the null hypothesis

  - 𝐻~0~ is called the alternative hypothesis  

  - Based on sample data from a population we should decide whether to reject 𝐻~0~ or not

  - Calculations are made under the assumption of 𝐻~0~ being true

  - If the results of theses calculations turn out to be sufficiently unlikely 𝐻~0~ is rejected  

  #### Possible errors  

  > <img src="https://gitee.com/h-ruc/note/raw/master/image-20220508163239043.png" alt="image-20220508163239043" style="zoom:50%;" />
  >
  > 

#### 					Scheme  

- Set up hypotheses
- Decide on probability of Type I error
- Decide on test statistic and decision rule
- Given sample data, make computations under 𝐻~0~
- Decide wether to reject or not reject 𝐻~0~
- Interpret and find ”business implications” of your decision  

### p-value  

- p-value means that, under the null hypothesis, the probability that **the test statistic takes a value at least as extreme as the value at hand** is p
- In other words **a low p-value** means it is **unlikely** that **the data at hand comes from a population specified by the null hypothesis**
- We reject the null hypothesis if we get a p-value that is lower than 𝛼  