# Chapter 6: Continuous Probability Distributions

## Continuous Uniform Distribution

$$f(x; A,B) = \begin{cases}
        \frac{1}{B-A}, \ A \leq x \leq B \\
        0, \ \text{elsewhere}
    \end{cases}$$

-   Thus the density function is a rectangle with base $B-A$ and
    constant height $1/(B-A)$

-   **Statistics:**

    -   $\mu = \frac{A+B}{2}$ and $\sigma^2 = \frac{(B-A)^2}{12}$

## Normal Distribution

$$n(x; \mu, \sigma) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{1}{2\sigma^2}(x-\mu)^2}$$

-   A normal distribution is fully described by $\mu$ and $\sigma$

-   Interesting points:

    -   The mode and median occur at the mean $x= \mu$

    -   The curve has inflection points at $x = \mu \pm \sigma$

-   Note that the parameters $\mu$ and $\sigma$ can be proven to be the
    mean and standard deviation

## Standard Normal

-   It makes no sense to integrate for every new mean and variance,
    thus, we transform the random variable $X$ into a random variable
    $Z$ with mean 0, and variance 1 $$Z = \frac{X-\mu}{\sigma}$$

-   This is done as follows
    $$P(x_1 <X<x_2) = \int_{x_1}^{x_2} n(x, \mu, \sigma) dx \implies \int_{z_1}^{z_2} n(z;0,1) dz = P(z_1 <Z< z_2)$$

-   Thus, we can make use of the standard normal CDF $\Phi$,
    $P(z_1<Z < z_2) = \Phi(z_2) - \Phi(z_1)$

## Normal Approximation to the Binomial

-   The binomial distribution is approximated by the normal as
    $n \rightarrow \infty$

-   If $X$ is a binomial random variable with mean $\mu = np$ and
    variance $\sigma^2 = npq$, then we can apply the standard normal
    transformation (convenient, since $\Phi$ is tabulated already)
    $$Z = \frac{X-np}{\sqrt{npq}} , \ n \rightarrow \infty$$

-   When looking for inclusive probabilities, we add and subtract 0.5
    from the upper and lower bound respectively (since after all,
    Binomial is a discrete distribution)
    $P(a \leq X \leq b) \approx P(\frac{a-0.5 - np}{\sqrt{npq}} \leq Z \leq \frac{b+0.5 - np}{\sqrt{npq}})$

-   When looking at exclusive probabilities, do the same except add and
    subtract 0.5 from the lower and upper bounds.
    $P(a < X < b) \approx P(\frac{a+0.5 - np}{\sqrt{npq}} \leq Z \leq \frac{b-0.5 - np}{\sqrt{npq}})$

## Gamma Distribution

RV $X$ has a gamma distribution with parameters $\alpha > 0$ and
$\beta >0$

$$f(x; \alpha, \beta) = 
\begin{cases}
    \frac{1}{\beta^\alpha \Gamma(\alpha)} x^{\alpha -1} e^{-x/\beta}, \ x > 0 \\
    0, \ else
\end{cases}$$ Statistics:

-   $\mu = \alpha \beta$

-   $\sigma^2 = \alpha \beta^2$

## Chi Squared Distribution

$$f(x;v) = 
\begin{cases}
    \frac{1}{2^{v/2} \Gamma(v/2)}x^{v/2 -1}e^{-x/2}, x > 0 \\ 
    0, \ else
\end{cases}$$ Statistics:

-   $\mu = v$

-   $\sigma^2 = 2v$

## Exponential Distribution

**this is just Gamma distribution** with a value $\alpha = 1$
$$f(x;\beta) = 
\begin{cases}
\frac{1}{\beta} e^{-x / \beta}, x \geq 0 \\
0, \ else
\end{cases}$$ Statistics:

-   $\mu = \beta$

-   $\sigma^2 = \beta^2$

### Relation to the Poisson Process

-   Consider the probability of no event occurring in t, so we have
    $p(0;rt) = e^{-rt}$ from the Poisson distribution

-   Let $X$ be the RV of time until the first event, thus
    $P(X > x) = e^{-rx}$

-   Similarly, we have $P(X \leq x) = 1 - e^{-rx}$

-   Recall, that the CDF is the integral of the PDF
    $$f(x) = \frac{d}{dx} P(X \leq x) = re^{-rx}$$

-   Which is just the exponential distribution with
    $r = \frac{1}{\beta}$

    -   Thus, if we have a random variable $X$ that follows an
        exponential distribution, then we can use a Poisson PMF to count
        occurrences over a period of time $t$ with $r = 1/\beta$ using
        $$p(x;rt) = \frac{e^{rt}(rt)^x}{x!}$$

### Memoryless Property of Exponential

$$P(X\geq s+t| X \geq s) = P(X \geq t)$$ The probability that a
component lasts t more days given that it has already lasted s days is
the same as it lasts t days. This basically says that the previous s
days that it had lasted for do not impact its ability to last t more
days. Say a component has been running for s days, and a new component
has just been implemented. The probability of failure of either two
components (new and old) within an extra time t is the same for both.

# Chapter 7: Functions of Random Variables

## Transformation of Random Discrete Variables

### Single Variable

-   Given $X$ is discrete RV with distribution $f(x)$ let $Y = u(X)$
    define a one to one transformation between the values of $X$ and $Y$
    s.t. the equation $y=u(x)$ can be uniquely solved for $x$ i.t.o $y$
    , say $x = w(y)$

-   then the probability distribution of $Y$ is $$g(y) = f[w(y)]$$

    -   Intuitively we have $f(x)$ the PMF of $X$, to find $g(y)$, we
        simply plug in the transformation of $x$ in terms of $y$ .

### Two Variables

-   Suppose $X_1$ and $X_2$ are discrete RV with joint probability
    distribution $f(x_1, x_2)$. Let $Y_1 = u_1(X_1, X_2)$ and
    $Y_2 = u_2(X_1, X_2)$ define a one to one transformation between
    $(x_1, x_2)$ and $(y_1,y_2)$. By finding the inverse functions
    $x_1 = w_1(y_1,y_2)$ and $x_2 = w_2(y_1, y_2)$, then the joint
    probability distribution of $Y$ is
    $$g(y_1, y_2) = f[w_1(y_1,y_2),w_2(y_1,y_2)]$$

## Transformation of Random Continuous Variables

### Single Variable

-   Suppose that $X$ is a continuous random variable with probability
    distribution $f(x)$. Let $Y = u(X)$ define a one-to-one
    transformation. Writing x i.t.o y, we have $x = w(y)$. Then the
    probability of $Y$ is $$g(y) = f[w(y)] |J|$$

-   Where $|J| = |w'(y)|$ is the Jacobian of the transformation

-   Proof:

    -   CDF of $Y$ is given as $G(y)$ and
        $$G(y) = P(Y \leq y) = \int_{-\infty}^{u^{-1}(y)} f(t) \ dt$$

    -   Using the Leibniz Integral Rule (FTC1), to find the pdf $g(y)$
        $$g(y) = \frac{d}{dy}G(y) = f(u^{-1}(y)) |\frac{du^{-1}y}{dy}|$$

### Two Variables

-   Suppose $X_1$ and $X_2$ are discrete RV with joint probability
    distribution $f(x_1, x_2)$. Let $Y_1 = u_1(X_1, X_2)$ and
    $Y_2 = u_2(X_1, X_2)$ define a one to one transformation between
    $(x_1, x_2)$ and $(y_1,y_2)$. By finding the inverse functions
    $x_1 = w_1(y_1,y_2)$ and $x_2 = w_2(y_1, y_2)$, then the joint
    probability distribution of $Y$ is
    $$g(y_1, y_2) = f[w_1(y_1,y_2),w_2(y_1,y_2)]|J|$$

-   Where the Jacobian is taken w.r.t $y_1$ and $y_2$

### Process for finding the joint probability distribution of transformed variables

1.  If both variables are independent, multiply them together to find
    the joint probability distribution

2.  Solve for the inverse transformation functions: in the given
    transformations, solve for your original variables. If you are given
    one transformation function, create another that is equal to one of
    your original variables.

3.  Compute the Jacobian: take the partials of your non-transformed
    variables ($-$) w.r.t your transformed variables ($|$)

4.  Using step 2, plug your new expressions into the joint probability
    distribution and multiply by $|J|$

5.  Find the bounds

6.  Compute the marginal probability distribution using the bounds.

## Moment about the Origin

-   The rth moment about the origin of the random variable $X$ is given
    by $$\mu_r' = E(X^r)$$

-   This can be applied to both discrete and continuous distributions

-   Note that the first and second moments are $\mu_1' = E(X)$ and
    $\mu_2' = E(X^2)$

    -   $\mu = \mu_1'$

    -   $\sigma^2 = \mu_2' - \mu^2$

## Moment Generating Function

-   The moment-generating function of the RV $X$ is given as $E(e^{tX})$
    and is denoted by $M_X(t)$

-   Then the r-th moment is found by differentiating the
    moment-generating function r times
    $$\frac{d^rM_X(t)}{dt^r}|_{t=0} = \mu_r'$$

```{=html}
<!-- -->
```
-   Let $X$ and $Y$ be two random variables with moment-generating
    functions $M_X(t)$ and $M_Y(t)$. If $M_X(t) = M_Y(t)$ , for all
    values of $t$, then $X$ and $Y$ have the same probability
    distribution

-   **Some Theorems**

    -   $M_{X+a}(t) = e^{at} M_X(t)$

    -   $M_{aX}(t) = M_X(at)$

-   If $X_1, X_2, ... , X_n$ are independent random variables with
    moment generating functions, and $Y = \sum_{i=1}^{n} X_i$, then
    $M_Y(t) = \Pi_{i=1}^{n}M_{Xi}(t)$

## Linear Combination of Random Variables

-   Given some $X_1$ with normal distribution and $\mu_1, \sigma^2_1$
    and some $X_2$ also normal with $\mu_2, \sigma^2_2$ and
    $Y = a_1 X_1 + a_2 X_2$, how might we find the mean and variance of
    $Y$. Applying the above theorems:
    $$M_Y(t) = M_{a_1 X_1}(t) M_{a_2 X_2}(t) \implies M_Y(t) = M_X(a_1 t) M_{X_2}(a_2 t)$$$$M_Y(t) = \exp(a_1 \mu_1 t + a_1^2 \sigma_1^2t^2/2) \exp(a_2 \mu_2 t + a_2^2 \sigma_2^2t^2/2)$$

-   These two expressions are combined, and we find that this is a
    moment-generating function of a distribution that is normal with
    mean $a_1 \mu_1 + a_2 \mu_2$ and variance
    $a_1^2 \sigma_1^2 + a_2^2 \sigma_2^2$

-   Generalizing these findings: if $X_1, X_2, ... , X_n$ are
    independent random variables having normal distrbiutions with means
    $\mu_1, \mu_2, ... , \mu_n$ and variances
    $\sigma^2_1, \sigma^2_2, ..., \sigma^2_n$ , then the random variable
    $Y = a_1 X_1 + a_2 X_2 + ... + a_n X_n$ has a normal distrbiution
    with mean $\mu_Y = a_1 \mu_1 + a_2 \mu_2 + ... + a_n \mu_n$ and
    variance
    $\sigma_Y^2 = a_1^2 \sigma_1^2 + a_2^2 \sigma_2^2 + ... + a_n^2 \sigma_n^2$

-   Note that the Poisson and Chi-Square distributions have the same
    property of reproducibility

### Notes on the Chi Squared Distribution

-   If $X_1, X_2, ..., X_n$ are mutually independent random variables,
    with $v_1, v_2, .. , v_n$ degrees of freedom, then the random
    variable $Y = X_1 + X_2 + ... +X_n$ has a chi-squared distribution
    with $v = v_1 + v_2 + ... + v_n$ degrees of freedom.

-   If $X_1, X_2, ..., X_n$, are independent, random variables having
    **identical normal distributions** with mean $\mu, \sigma^2$ then
    $$Y = \sum_{i=1}^n (\frac{X_i-\mu}{\sigma})^2$$

-   Has a chi-squared distribution with $v=n$ degrees of freedom

-   **Note, that this also works when $X_i$ has its own
    $\mu_i, \sigma_i$**:
    $$Y = \sum_{i=1}^{n} (\frac{X_i - \mu_i}{\sigma_i})^2$$

-   And still has $v = n$ degrees of freedom

# Chapter 8: Sampling Distributions 

## Central Limit Theorem

-   In the limit as $n \rightarrow \infty$, the mean $\bar{X}$ of a
    random sample of size $n$ from a population with mean $\mu$ and
    finite variance $\sigma^2$, then the limiting form of the of
    $Z = \frac{\bar{X} - \mu}{\sigma/\sqrt{n}}$ is the standard normal
    distribution $n(z;0,1)$

## Sampling Distribution: Difference of Means $\bar{X}_1 - \bar{X}_2$

-   Independent samples of size $n_1$ and $n_2$ are drawn at random from
    two populations with $\mu_1, \sigma^2_1$ and $\mu_2, \sigma^2_2$.
    Then the sampling distribution of $\bar{X}_1 - \bar{X}_2$ is
    approximately normal with the following statistics:

-   $\mu_{\bar{X_1} - \bar{X_2}} = \mu_1 - \mu_2, \sigma^2_{\bar{X_1} - \bar{X_2}} = \frac{\sigma^2_1}{n_1} + \frac{\sigma^2_2}{n_2}$

$$Z = \frac{\bar{X_1} - \bar{X_2} - (\mu_1 - \mu_2)}{\sqrt{\frac{\sigma^2_1}{n_1} + \frac{\sigma^2_2}{n_2}}}$$

## Sample Distribution: Sample Variance $S^2$ 

-   Consider the distribution of the statistic $(n-1)S^2/\sigma^2$.
    Through some algebra we receive a $\chi^2$ squared distribution.

-   If $S^2$ si the variance of a random sample of size $n$ taken from a
    normal population having the variance $\sigma^2$, then the statistic
    $$\chi^2 = \frac{(n-1)S^2}{\sigma^2} = \sum_{i=1}^n \frac{(X_i - \bar{X})^2}{\sigma^2}$$

## Degrees of Freedom as Measure of Sample Information

$$\chi^2 = \sum \frac{(X_i - \mu)^2}{\sigma^2}$$

-   Has $n$ degrees of freedom, where as the same statistic but with
    $\bar{X}$, we lose out on one degree of freedom.

## t-Distribution $T$

-   When we do not know the population variance
    $$T = \frac{\bar{X} - \mu}{S/\sqrt{n}}$$

-   Let us divide both the numerator and denominator by
    $(\sigma/\sqrt{n})$, s.t. the numerator becomes the standard normal.

-   $$T = \frac{\bar{X} - \mu}{S/\sqrt{n}} = \frac{(\bar{X} - \mu)/ (\sigma/ \sqrt{n})}{S/(\sqrt{n}) / (\sigma/\sqrt{n})} = \frac{Z}{\sqrt{S^2/\sigma^2}} = \frac{Z}{\sqrt{V/(n-1)}}$$

-   Where $V = \frac{(n-1)S^2}{\sigma^2}$ has $\chi^2$ distribution with
    $v= n-1$ degrees of freedom

    -   $\chi^2 = \frac{(n-1)S^2}{\sigma^2} = \sum \frac{(X_i - \bar{X})^2}{\sigma^2}$

## F-Distribution

-   Consider two independent samples of size $n_1$ and $n_2$.
    Application in comparing sample variances:
    $$F = \frac{U/v_1}{V/v_2}$$

-   $U$ chi-squared with $v_1$ dof
    $$\chi^2_1 = \frac{(n_1 -1)S_1^2}{\sigma^2_1}$$

-   $V$ chi-squared with $v_2$ dof
    $$\chi^2_2 = \frac{(n_2 -1)S_2^2}{\sigma^2_2}$$

-   $U, V$ are
    independent$$F = \frac{S_1^2/\sigma_1^2}{S_2^2/\sigma_2^2 }$$ has an
    F-distribution with $v_1 = n_1-1$ and $v_2 = n_2 -1$ dof

-   F-distribution depends on $v_1, v_2$ **and its order**

-   $f_\alpha$ : f-value which area is $\alpha$

-   $$f_{1-\alpha}(v_1, v_2) = \frac{1}{f_{\alpha(v_2, v_1)}}$$

# Monday March 4

## Quantiles and Probability Plots

**Quantiles**

-   Definition: a quantile of a sample, $q(f)$ is a **value** for which
    a specific fraction $f$ of the data values is less than or equal to
    $q(f)$:

-   For example, the median is $q(0.5)$ the 75th percentile is $q(0.75)$

**Quantile Plot**

-   A quantile plot displays the data values **against the proportion of
    observation** they exceed (quantile v fraction)

-   The fraction for the $i$-th data point is
    $f_i = \frac{i - \frac{3}{8}}{n + \frac{1}{4}}$

-   This plot visualizes the sample's empirical distribution function

    -   Flat areas indicate clusters

    
    -   Steep areas are sparse

-   Note that if you rotate the quantile plot, you get an
    **approximation for the CDF**

-   To sketch a quantile plot:

    -   Arrange the sample in increasing order, denoted as
        $x_1, x_2, ... x_n$

    -   For each data point indexed by $i$ (where $i = 1,..., n)$, plot
        the pair

-   Example: ${28,28,29.2,...}$

    -   Calculate, $f_1$ and $f_2$, $f(3)$

-   Example: $-2, 0, 0, 1, 3, 3,3, 4,6$

    -   Plot $q(f)$ against $f$

    -   For each $f$ value of the current point, plot the value of the
        function

    -   Thus, the three 3s, take values of $f = 5,6,7$ , and
        $f(5,6,7) = 3$

**Relation of quantile function to CDF**

-   Let $X$ be a continuous random variable with probability density
    function $f(x)$ and cumulative distribution function $F(x)$

-   $F(x)$ represents the probability that an outcome is less than or
    equal to x

-   Consider a \"theoretical\" quantile $q(f) =x$, such that a fraction
    $f$ of the data is less than or equal to $x$

-   $q = F^{-1}$ informally,

**Normal Quantile-Quantile Plots**

-   A normal quantile quantile Q-Q plot is a graphical tool to compare a
    sample's distribution to a normal distribution.

-   The plot displays the ordered sample values against the theoretical
    quantiles that are found from a normal distribution with mean and
    standard deviation, $\mu, \sigma$

-   $$q_{\mu, \sigma}(f) = \mu + \sigma{4.91[f^{0.14} -(1-f)^{0.14}]} \rightarrow y = mx + b$$

-   For a standard normal curve:
    $$q(f) ={4.91[f^{0.14} -(1-f)^{0.14}]} \rightarrow y = mx + b$$

-   So we essentially linearity the quantiles that associate with the
    normal distribution

-   Note that the above is an approximation

-   This is derived from the Normal CDF, and $q(f) = \Phi^{-1}(f)$

**usage**

-   A nearly straight line pattern indicates that the sample
    distribution is approximately normal

**interpretation**

-   In a normal sample distribution, the quantile plot would look sparse
    at either end of the sample values (top and bottom), but near the
    center, it would seem most dense

    -   At either end, the frequency of values far away from the mean is
        less

    -   Near the center, most of the values will be concentrated around
        the mean

**plotting a normal q-q plot**

-   Plot $$(q_{0,1}(f_i), x_i)$$

-   Where $q_{0,1}(f_i)$ is the standard normal linearized approximation
    $$q(f) ={4.91[f^{0.14} -(1-f)^{0.14}]} \rightarrow y = mx + b$$

## Discussion on Central Limit Theorem and the F-distribution

-   CLT: $\sigma$ is known

-   F, T distributions: $\sigma$ is unknown

# Thursday March 7

-   Consider observed data values $x_1, x_2, ... x_n$

-   Assume that they are realization of IID random variables
    $X_1, X_2, ... ,X_n$

-   **Sample mean as a point estimate**

    -   The sample statistic for mean is $\bar{X}$

    -   The observed sample mean is $\bar{x}$

    -   And $\mu$ represents the true but unknown population mean

-   **General notation for point estimates**

    -   $\theta$ denotes the **true parameter of the population**, same
        thing as $\mu$

    -   $\hat{\theta}$ is the point estimate observed from the sample,
        it is the actual realization of, akin to $\bar{x}$

    -   $\hat{\Theta}$ is the statistical estimator, **and thus is a
        distribution** similar to $\bar{X}$

-   Note that point estimates like the sample mean are used to infer
    properties of the population from the sample data

\
**Unbiased Estimator**

-   An estimator $\hat{\Theta}$ is an **unbiased** for a parameter
    $\theta$ is the expected value of $\hat{\Theta}$ is equal to
    $\theta$ $$E[\hat{\Theta}] = \theta$$

-   Example, the sample variance (when dividing by $n-1$), is an
    unbiased estimator of the population variance $\sigma^2$

-   **is $\mu$ an unbiased estimator**

-   yes because we can show that $E[\bar{X}] = \mu$ , as
    $\hat{\Theta} = \bar{X}$

-   $E[\bar{X}] = \frac{1}{n} \sum E[X_i] = \frac{1}{n} (n \mu)$, note
    this is because $E[X_i] = \mu$

-   **Note that any $X_i$ is also an unbiased estimator** since the
    expectation of any $X_i$ is equal to the population mean $\mu$ by
    definition $E[X_i] = \mu$

    -   Note, that this will likely not be the best estimator

\
**Efficient Estimators**

-   Among all the unbiased estimators of a parameter $\theta$, the one
    with the **smallest variance** is considered the most **efficient**
    estimator of $\theta$.

why do we use the sample mean $\bar{X}$ instead of any $X_i$

-   Look at variance of both:

    -   $var(X_i) = \sigma^2$

    -   $var(\bar{X}) = \frac{\sigma^2}{n}$

-   We see that the standard deviation of $\bar{X}$ is lower than that
    of $X_i$, thus, it is a more efficient estimator than a random i-th
    sample. The CLT informs us that the variance of the estimator
    $\bar{X}$ decreases at a rate of $n$, as $n$ becomes larger.

\
**Interval Estimation**

-   A point estimate $\hat{\theta}$ is a single best guess at the true
    parameter value $\theta$ but it is rarely exact.

-   An interval estimate provides a range
    $\theta_L \leq \theta \leq \theta_U$, which likely contains $\theta$

-   Acknowledging uncertainty is critical in statistical estimation

-   Example: weather forecasts for temperature always have a high and
    low

\
**Confidence Intervals**

-   The lower and upper bounds of a confidence interval, $\Theta_L$ and
    $\Theta_U$ are based on sample data

-   We seek to express our certainty in the interval with a statement
    like: $$P(\Theta_L \leq \theta \leq \Theta_U) = 1 - \alpha$$

-   Here $\alpha$ is a level of uncertainty that we are willing to
    accept

-   For example, if $\alpha = 0.05$, we obtain a $95\%$ confidence
    interval

    -   Intuition: the probability inside $\Theta_L$ and $\Theta_U$ is
        equal to 0.95

    -   Intuition: there is a 95% chance that the **sample parameter**
        is within our range

\
**Confidence Intervals for the Mean**

-   Sample mean $\bar{X}$

-   Variance of the sample mean from CLT:
    $\sigma_{\bar{X}}^2 = \frac{\sigma^2}{n}$

-   Statistic, $Z$ following a standard normal distribution if $\bar{X}$
    are normal or $n$ is large

-   for $\beta < 0.5$, $z_\beta$ satisfies $P( z < z_{\beta}) = \beta$

-   find a $z_\beta$ such that $\phi(-z_\beta) = \beta$ i.e.
    $z_\beta = - \phi^{-1}(\beta)$

-   **Confidence interval**

    -   $$P(-z_{\alpha/2} \leq Z \leq z_{\alpha/2}) = P(-z_{\alpha/2} \leq \frac{\bar{X} - \mu}{\sigma/\sqrt{n}}\leq z_{\alpha/2}) = 1 - \alpha$$

    -   $$P(\bar{X} - z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}} \leq \mu \leq \bar{X} + z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}})$$

### Example

-   Given $n = 20$

-   observed sample mean is $\bar{x} = 4$

-   the population standard deviation is known $\sigma = 2$

-   we aim to find the $95\%$ confidence interval

$$P(\mu_L < \mu < \mu_U) = 0.95$$
$$P(-z_{\alpha/2} < z < z_{\alpha/2}) = 0.95$$ The lower limit should be
$P(\frac{\mu_L-\bar{X}}{\sigma/\sqrt{n}} < \frac{\mu-\bar{X}}{\sigma/\sqrt{n}} < \frac{\mu_U-\bar{X}}{\sigma/\sqrt{n}})$

So $\mu_L = \bar{X}  - Z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}}$ So
$\mu_U = \bar{X}  + Z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}}$
$$z_{\alpha/2} = z_{(1-0.95)/2} = -\Phi^{-1}(0.025) \approx 1.96$$

### Example

-   $n=36$, $\bar{X} = 2.6$, $\sigma = 0.3$

-   Find the $95$ and $99 \%$ confidence intervals for the mean zinc
    concentration in the river.

-   $P(-z_{0.025} < z < z_{0.025}) = 0.95$

-   Therefore $-z_{0.025} = \frac{\mu_L - 2.6}{0.3/6}$ and
    $z_{0.025} = \frac{\mu_U - 2.6}{0.3/6}$ and thus
    $\mu_L, \mu_U = 2.6 \mp 1.96 (0.3/6)$

-   Similarly, for the $99\%$ confidence interval, we look for
    $\pm z_{0.005}$, which can be found by looking at
    $\Phi^{-1}(0.005) = z_{0.005} = -2.58$

-   Thus, $\mu_L, \mu_U = 2.6 \mp 2.58(0.3/6)$

# Friday March 8

### Note on Z-scores

-   $z_{0.025} = 1.96$

-   having $\beta < 0.5$, we know that we are looking for some $z_\beta$
    such that the probability of our random variable $z$ is less than
    $z_\beta$ is equal to $\beta$

-   Similarly, $P(z > z_\beta) = \beta$ as the distribution is symmetric

-   So we will have $-z_{0.025}$ and $z_{0.025}$

-   By looking at the table, we have the left tail (cumulative), so
    technically $z_{0.025} = z_{0.975}$

**One-sided confidence intervals**

-   $n, \bar{x}, \sigma^2$

-   For a one-sided confidence interval:
    $$1-\alpha = P(Z \leq z_{\alpha})$$

-   Where $z_\alpha = - \Phi^{-1}(\alpha)$

-   The upper bound for the one-sided interval (LEFT):
    $$\bar{X_U} = \bar{x} + z_c \frac{\sigma}{\sqrt{n}}$$

-   The lower bound for the one-sided interval (RIGHT)
    $$\bar{X}_L = \bar{x} - z_c \frac{\sigma}{\sqrt{n}}$$

### Example

-   $n = 25$

-   $\sigma^2 = 4$

-   $\bar{x} = 6.2$

-   give a 95 % bound for the mean reaction time

    -   So we need to find some $z_c$ s.t. $P(Z \leq z_c) = 0.95$

    -   This value is equal to 1.645. **Since this is an upper bound,
        the value of $z_c$ should be positive**

-   $$\bar{X}_U = 6.2 + 1.645 \times \frac{2}{5}$$

**Confidence intervals for the mean with unknown standard deviation**

-   When we don't know $\sigma$, the population standard deviation

-   **When $\sigma$ is unknown and the distribution is normal, use the
    t-distribution**

-   We use t distribution

-   The statistic is $T = \frac{\bar{X} -\mu}{S/\sqrt{n}}$ with $v= n-1$
    degrees of freedom

-   **Confidence interval** of a two-sided confidence interval with
    confidence level $1- \alpha$

-   $$1-\alpha = P(-t_{\alpha/2} \leq T \leq t_{\alpha/2})$$

-   $$P(\bar{X} - t_{\alpha/2} \frac{S}{\sqrt{n}} \leq \mu \leq \bar{X} + t_{\alpha/2} \frac{S}{\sqrt{n}})$$

-   Where $S$ is the sample variance

### Example

-   The contents of seven similar containers of sulfuric acid are
    $9.8., 10.2, 10.4, 9.8, 10.0, 10.2, 9.6$ Find a 95% confidence
    interval for the mean contents of all such containers, assuming an
    approximately normal distribution

-   Calculate $S$

-   $v =6$ degrees of freedom (n=7-1 )

-   Use t-distribution to find $t_{\alpha/2}$ s.t.
    $P(T \leq t_{0.025,6})$

-   $-t_{0.025, 6} = -2.447$

### Example

-   Sample is $9.8,10.2,10.4,9.8,10.0,10.2,9.6$

-   Find a $95\%$ confidence interval for the mean, assuming normal
    distribution

-   **Solution:** population variance is not given and population is
    normal, so **T-distribution**

-   $\bar{x} = 10$,
    $s = \frac{1}{7-6} \sum_{i=1}^{7}(\bar{x} - x_i)^2 \rightarrow \sqrt{s} = 0.283$

-   Now, we look for t-values: $t_{0.025, 6}$ with 6 degrees of freedom
    and we get $2.447$, thus our confidence level is
    $10.0 - 2.447 (\frac{0.283}{\sqrt{7}}) \leq \mu \leq 10.0 + 2.447 (\frac{0.283}{\sqrt{7}})$

-   Again, all we are doing is finding t-values for $95\%$ confidence
    levels in the t-domain. Once we see this confidence interval, we
    return to our original coordinates, using these t-values to compute
    the interval that produces the same $95\%$ confidence interval.

## Standard Error

-   When we draw samples $X_1, ..., X_n$ from a distribution with
    unknown mean $\mu$ and variance $\sigma^2$

-   The standard deviation of $Z$, which we term the **standard error**,
    is approximately $\sigma/\sqrt{n}$

## Prediction **Intervals** with Known Variance

-   Say we have normal samples, with population variance $\sigma^2$ and
    some sample mean $\bar{X}$

-   For a new observation $X_o$ (prediction), we use $\bar{X}$ as a
    point estimate and we define
    $$Z = \frac{X_o - \bar{X}}{\sigma \sqrt{1+\frac{1}{n}}}$$

-   Then the confidence interval for our prediction is
    $$\bar{x} - z_{\alpha/2} \sigma \sqrt{1+\frac{1}{n}} \leq x_o \leq \bar{x} + z_{\alpha/2} \sigma \sqrt{1+ \frac{1}{n}}$$

### Example

-   $n=50$, $\bar{x} = 257300$, $\sigma =25000$

-   Find $95\%$ prediction interval for the **next point**

-   **Solution**: we are given $\sigma$ and $n > 30$, so we use the z
    distribution; however, we must use the above z-score for our
    prediction

-   $$257300 \pm (1.96)(25000)\sqrt{1+\frac{1}{50}}$$

# Tuesday, March 11

## Tolerance limits for normal distributions

-   Tolerance limits define a range within which we expect a certain
    proportion of the population to fall. Unlike confidence or
    prediction intervals, tolerance limits do not shrink with increasing
    sample size but are intended to encompass a fixed percentage of the
    population.

::: center
::: tcolorbox
***Definition:***\
\
For a normal distribution of measurements with unknown mean $\mu$ and
unknown standard deviation $\sigma$ tolerance limits are given by
$\bar{x} \pm ks$, where $k$ is determined such that one can assert with
$100(1-\gamma)\%$ confidence that the limits contain at least proportion
$1-\alpha$ of the measurements
:::
:::

Given

-   IID observations $x_1, ..., x_n$

-   The sample mean $\bar{x}$ and sample variance $S^2$

-   The tolerance interval is then expressed as $\bar{x} \pm ks$

### Example

-   $1.01, 0.97,1.03,1.04,0.99,0.98,0.99,1.01,1.03$

-   $n= 9$, $\bar{x} = 1.0056$ and $s= 0.0246$

-   Calculate 99% confidence interval on mean

    -   **Solution:** find $t_{0.005,8} = 3.355$:
        $$\bar{x} \pm t_{0.005}\frac{s}{\sqrt{n}} = 1.0056 \pm 0.0275$$

-   Calculate 99% prediction interval:

    -   **Solution:** $t_{0.005,8} = 3.355$:
        $$\bar{x} \pm t_{0.005} s \sqrt{1+ \frac{1}{9}} = 1.0056 \pm(3.355)(0.0246)\sqrt{1+1/9}$$

-   Calculate the 99% tolerance limit that will contain 95% of the
    population

    -   **Solution:** thus, we know that $1-\gamma = 0.99$ and
        $1 -\alpha = 0.95$

    -   From the table, we find that for $n=9$ $k = 4.550$, thus
        $$\bar{x} \pm ks = 1.0056 \pm (4.550)(0.0246)$$

    -   Thus, we are 99% confident that 95% of the population will have
        measurements between 0.8937 and 1.1175

## Comparison of various Interval Estimates

-   **Confidence intervals:**

    -   Based on IID observation $x_1, ... ,x_n$

    -   There is a $100(1-\alpha) \%$ chance that the true mean $\mu$ is
        within the interval around $\bar{x}$

    -   z-scores: if $\sigma$ is known and $n$ is large (or if $X_i$ is
        normal and $\sigma$ known)

    -   t-scores: if $s$ is known

-   **Prediction Interval**

    -   Based on IID observation $x_1, ... ,x_n$

    -   A $100(1-\alpha) \%$ chance that the next observation will fall
        within the interval around $\bar{x}$

    -   z-scores: same as above

    -   t-scores: same as above

-   **Tolerance Limits (interval)**

    -   Based on IID observation $x_1, ... ,x_n$

    -   Assert with $100(1-\gamma)\%$ confidence that $100(1-\alpha)\%$
        of all future measurements are expected to fall within the
        interval $\bar{x} \pm ks$

    -   Use **statistical tables** to find the value of $k$

## Two Samples with Known but different Distributions

-   Sample sizes $n_1$ and $n_2$

-   Sample means $\bar{X_1}$ and $\bar{X}_2$

-   Estimating the difference between two means:

    -   The point estimate for $\mu_1 - \mu_2: \bar{x}_1 - \bar{x}_2$

    -   Sample distribution of the difference is approximately normal

    -   Mean: $\mu_1 - \mu_2$

    -   Variance: $\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}$

-   $$Z = \frac{\bar{X}_1 - \bar{X}_2 - (\mu_1 - \mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma^2_2}{n_2}}}$$

-   Thus, we can find a $100(1-\alpha)\%$ confidence interval for
    $\mu_1 - \mu_2$, which is given by
    $$(\bar{x}_1 - \bar{x}_2) - z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} < \mu_1 - \mu_2 < (\bar{x}_1 - \bar{x}_2) + z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}$$

### Example

-   $n_1 =50$, $n_2 = 75$

-   $\bar{x}_1 = 36$, $\bar{x}_2 =42$

-   $\sigma_1 = 6$, $\sigma_2 = 8$

-   Find a 96% confidence interval on $\mu_2 - \mu_1$

-   **Solution:** we want to find 96%, so we take $\alpha = 0.04$. We
    also are given the population ST. dev, so we look for z-scores,
    specifically $z_{0.02}=+2.05$, thus we simply apply the formula:
    $$\mu_2 - \mu_1 = 42 - 36 \pm 2.05 \sqrt{\frac{6^2}{50} + \frac{8^2}{75}}$$

## Two Samples with Unknown but equal Variance 

-   assume $\sigma_1 = \sigma_2$ but are both unknown

-   Sample sizes $n_1, n_2 < 30$ are normally distributed

-   We don't know the population variance, so we use $T$ distribution

-   $$T = \frac{(\bar{X_1} - \bar{X_2}) - (\mu_1 - \mu_2)}{S_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}$$

-   Where $S_P^2$ is the sample size weighted average of $S_1^2$ and
    $S_2^2$. Note that we use the pooled variance because it is assumed
    that the variances are to be similar in value:
    $$S_p^2 = \frac{(n_1-1)S_1^2 + (n_2 -1)S^2_2}{n_1 + n_2 -2}$$

-   This distribution has $v=n_1 +n_2 - 2$ degrees of freedom

-   The two-sided confidence interval is of the form

-   $$(\bar{x}_1 - \bar{x}_2) - t_{\alpha/2} s_p \sqrt{1/n_1 + 1/n_2}) < \mu_1 - \mu_2 < (\bar{x}_1 - \bar{x}_2) + t_{\alpha/2} s_p \sqrt{1/n_1 + 1/n_2})$$

-   Once again, intuitively, we are just finding the t-values that give
    us our desired confidence level with a given number of degrees of
    freedom. From there, we can use the t-values to transform back into
    our original coordinate system.

### Example

-   $n_1 =12$, $n_2 =10$

-   $\bar{x}_1 = 3.11$, $\bar{x}_2 = 2.04$

-   $s_1 = 0.771$, $s_2 = 0.448$

-   Find a 90% confidence interval for the mean $\mu_1 -\mu_2$

-   **Solution:** calculate the sample size weighted variance $= 0.417$.
    Next, we find that the degrees of freedom are $v = 12 + 10 - 2 =20$.
    Now we note that $1- \alpha = 0.9$, so $\alpha = 0.1$ and we look
    for values of $\pm t_{0.05, 20} = \pm 1.725$, and we plug, NOTE that
    we use $s_p$
    $$\mu_1 - \mu_2 = (3.11 - 2.04) \pm (1.725)(\sqrt{0.417})\sqrt{1/12 +1/10}$$

## Two Samples with Unknown but different Variance 

-   $\sigma_1$ and $\sigma_2$ are **both unknown and unlikely to be
    equal**

-   Test statistic
    $$T' = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2) }{ \sqrt{S_1^2/n_1 + S_2^2/n_2}}$$

-   Thus the interval with $1(1-\alpha)\%$ certainty is
    $$(\bar{x}_1 - \bar{x}_2 - t_{\alpha/2, v} \sqrt{s_1^2/n_1 + s^2_2,n_2}) < \mu_1 - \mu_2 < (\bar{x}_1 - \bar{x}_2 + t_{\alpha/2, v} \sqrt{s_1^2/n_1 + s^2_2,n_2})$$

-   **Note that we approximate the degrees of freedom as** (look at
    figure)
    $$v \approx \frac{(S_1^2/n_1 + S_2^2/n_2)^2}{\frac{(S_1^2/n_1)^2}{n_1-1} + \frac{(S_2^2/n_2)^2}{n_2-2}}$$

    ![Enter
    Caption](Screenshot 2024-03-12 at 12.49.23 PM.png){#fig:enter-label
    width="0.5\\linewidth"}

-   $$P(-t_{\alpha/2} \leq T' \leq t_{\alpha/2}) \approx 1 - \alpha$$

### Example

-   $\bar{x}_1 = 3.84$, $\bar{x}_2 = 1.49$

-   $s_1 = 3.07$, $s_2 = 0.80$

-   $n_1 = 15$, $n_2 =12$

-   Find the 95% confidence interval for $\mu_1-\mu_2$

-   **Solution:** Since the sample standard deviations are not similar,
    we must approximate the degrees of freedom and then use the
    t-distribution: $v=16.316 = 16$, now, we use the t-distribution
    tables to find $t_{0.025, 16}$ and plug
    $$(\mu_1-\mu_2) = (3.94 - 1.49) \pm 2.120 \sqrt{3.07^2/15 + 0.80^2/12}$$

# Thursday March 14

# Paired Observations

## Confidence Intervals for Paired Observations

-   If $\bar{d}$ and $s_D$ are the mean and standard deviation of the
    normally distributed differences of $n$ pairs of measurements, a
    $100(1-\alpha)\%$ confidence interval for $\mu_D = \mu_1 -\mu_2$ is
    $$\bar{d} - t_{\alpha/2} \frac{s_d}{\sqrt{n}} < \mu_D < \bar{d} + t_{\alpha/2} \frac{s_d}{\sqrt{n}}$$

-   where $t_{\alpha/2}$ is the t-value with $v = n-1$ degrees of
    freedom, leaving an area of $\alpha/2$ on the right

-   Intuition: imagine two RV, $X,Y$ with samples $x_1, ...$ and
    $y_1...$, then, the difference $d_1 = x_1 - y_1$

### Example

-   The point estimate of $\mu_D$ is $\bar{d} = -0.87$ with
    $s_d = 2.9773$ and $n=20$

-   We wish to find a 95% confidence interval for
    $\mu_D  = \mu_1 - \mu_2$

-   **Solution:**

    -   We find t-value $t_{0.025, 19}$ and then plug
        $$\mu_D = -0.87 \pm (2.093) \frac{2.9773}{\sqrt{20}})$$

## Analysis and Application

-   Comparison of two related samples with one-to-one correspondence
    (e.g. comparing efficiency before and after process improvements)

-   Let $(X_i, Y_i)$ represent the paired samples for $i = 1,...,n$. Let
    us assume that $X_i$ and $Y_i$ are normally distributed with means
    $\mu_X, \mu_Y$ and $\sigma_X, \sigma_Y$. By defining the difference
    between the i-th pair as $D_i = X_i - Y_i$, then the variance of
    $D_i$ is
    $$\text{Var}(D_i) = \sigma^2_X + \sigma^2_Y - 2 \text{Cov}(X_i, Y_i)$$

-   Thus, the variance of $D$ is
    $$S^2_D = \frac{1}{n-1} \sum_{i=1}^{n} (D_i - \bar{D})^2$$

## Confidence Intervals Estimating a Proportion (single sample)

-   A point estimator of the proportion $p$ in a binomial experiment is
    given by the statistic $\hat{P} = X/n$, where $X$ represents the
    number of successes in $n$ trials. Therefore, the sample proportion
    $\hat{p} = x/n$ will be used as the point estimate of the parameter
    $p$

-   By the CLT, for $N$ sufficiently large, $\hat{P}$ is normally
    distributed with mean $\mu_{\hat{P}} = p$ and variance
    $\sigma^2_{\hat{P}} = \frac{pq}{n}$ and
    $$P(-z_{\alpha/2} < \frac{\hat{p} -p}{\sqrt{pq/n}}<z_{\alpha/2}) = 1 - \alpha$$

-   For $n$ large,
    $$1 - \alpha = P(\hat{p} - z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p}}{n})}\leq p \leq \hat{p} + z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p}}{n})})$$

### Example

-   $n = 500$, $r=340$ subscribe to HBO, find a $95\%$ confidence
    interval for the actual proportion of families that subscribe to HBO

-   **Solution:** $1-\alpha = 0.95\rightarrow \alpha = 0.05$. We can use
    $\hat{p}= x/n$ as the point estimate of $p$ (the real value of a
    success). In this case $\hat{p} = 340/500$. Now, we can use the
    standard normal to find $\pm z_{0.05/2}$ and from there we can
    transform $$0.6391 < p < 0.7209$$

## Choice of Sample Size

-   Suppose we want $100(1-\alpha_\%$ confidence that the estimator is
    less than $\delta$

-   $$\delta = z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$

-   $$n = \frac{z^2_{\alpha/2} \hat{p} (1-\hat{p})}{\delta^2}$$

-   **Safe lower bound** $n \geq \frac{z^2_{\alpha/2}}{4\delta^2}$

-   This is used when we have yet to approximate $p$ with a point
    estimate.

-   In practice, first computing $\hat{p}$ and then using
    $n = \frac{z_{\alpha/2}^2\hat{p}\hat{q}}{\delta^2}$ will lead to a
    smaller $n$ than if we hadn't computed $\hat{p}$

### Example

-   How large of sample $n$ is needed if we want a $95\%$ confidence
    interval that our estimate of $p$ in the previous example is within
    0.02 of the true value

-   **Solution:** $\delta = 0.02$, $\hat{p} = 0.68$ and
    $z_{\alpha/2} = 1.96$
    $$n = \frac{1.96^2 (0.68)(1-0.68)}{0.02^2} = 2090$$

# Week 10-2 Thursday March 21

## Interval Estimation of Variance

-   **Estimator of Variance:** if a sample size $n$ is drawn from a
    normal population with variance $\sigma^2$ and the sample variance
    $s^2$ is computed (realization), we obtain **a** value of the
    statistic $S^2$. This computed sample variance is used as a point
    estimate of $\sigma^2$. Hence the statistic $S^2$ is an estimator of
    $\sigma^2$

-   Interval estimate of $\sigma^2$ can be established using the
    statistic $$\chi^2 = X^2 = \frac{(n-1)S^2}{\sigma^2}$$ which has a
    chi-squared distribution with $n-1$ degrees of freedom when samples
    are chosen from a normal population

    -   Note, $\chi^2$ must can take on values from $[0, \infty)$

    -   

## Confidence Interval for Variance

-   The confidence interval for $\sigma^2$ is written as
    $$P(X^2_{\alpha/2} < X^2 < X^2_{1-\alpha/2}) = 1- \alpha = P\left(\frac{(n-1)S^2}{\chi^2_{\alpha/2}} \leq \sigma^2 \leq \frac{(n-1)S^2}{\chi^2_{1-\alpha/2}}\right)$$

-   Where $X^2_{1-\alpha/2}$ and $X^2_{\alpha/2}$ are the values of teh
    chi squared distribution with $n-1$ degrees of freedom, leaving
    areas $1- \alpha/2$ and $\alpha/2$ **to the right**

-   Note, the chi-squared distribution is not symmetric like the z and t
    distributions.

-   Note, to find the area, subtract the chi-squared value of the
    smaller one.

### Example

-   $n=10$, $s^2 = 0.286$

-   **Solution:** $\alpha/2 = 0.025$, find $\chi^2$ values with 9
    degrees of freedom
    $\chi^2_{0.025, 9} = 2.70 \ \chi^2_{0.975,9}= 19.023$

-   $\sigma^2 \in (0.135, 0.953)$

## Maximum Likelihood Estimation (MLE)

-   For some context, so far we've used intuitive statistics for
    parameter estimation

    -   Sample mean, $\bar{X}$ as an estimator for the population mean
        $\mu$

    -   Sample variance, $S^2$ as an estimator for the population
        variance $\sigma^2$

    -   Sample proportion $\hat{P} = X/n$ for the probability of
        sucesses $p$ in binomial trials

-   **Maximum likelihood estimation** is used for more complex models.
    MLE provides a method for estimating parameters by maximizing the
    likelihood function.

## Liklelihood Function

-   Given a sample $x_1, ..., x_n$ and a joint PDF
    $f(x_1, ..., x_n; \theta)$. The likelihood is defined as
    $$L(x_1, ...,x_n; \theta) = \prod_{i=1}^{n} g(x_i; \theta)$$

-   The MLE of $\theta$ is given by
    $\hat{\theta} = \text{arg max}_{\theta} = L(x_1, x...,x_n; \theta)$

-   Note, you need to know the distributions $g(x_i, \theta)$ to find a
    likelihood function

-   Note, to find the MLE, you take the derivative of $L$ and set it
    equal to zero. To check for minima/maxima, find the concavity.

### Example

-   Sample from a Bernoulli trial $\{1,0,1,1\}$, we aim to find the
    probability of a sucess $\theta = p$

-   **Solution:** Bernoulli trials with either fail or success is
    Binomial. Take the product of the bernoulli trials, prob of 3
    sucesses and 1 failure, is$$L(1,0,1,1;p) = {4 \choose 3} p^3 (1-p)$$

-   We differentiate w.r.t p, and we set the derivative = 0:
    ${4 \choose 3} (3\hat{p}^2 - 4\hat{p}^3) = 0 \rightarrow 3- 4\hat{p} = 0 \rightarrow \hat{p} = 3/4$

# Week 10-3 Friday March 22

## Log-Likelihood

-   When dealing wiht distributiosn that involve exponential functions,
    optimziing the likelihood cand be simplified by considering the
    logarithm of the likelihood (normal, Poisson, exponential
    distributions all involve exponentials)

-   Due to the non-lienarity of exponential functions, we apply
    logarithms. By taking the logarithm of the lilhood function, known
    as the log-likelihood simplifies the process:

    -   It reomves the exponential, resulting in a simplier function

    -   Since the logarithmic function is strictly increasing, the max
        of the likelihood is preserved

### Example: MLE for Normal Distrbiution

-   Given the following normal distrbiution, find the MLE:
    $$n(x;\mu , \sigma) = \frac{1}{\sqrt{2\pi}\sigma} e^{- \frac{1}{2}(\frac{x-\mu}{\sigma})^2}$$

-   **Solution:**

-   $$L(x_1, ..., x_n \sigma^2) = \prod_{i=1}^{n} \exp \left[-\frac{1}{2} (\frac{x_i - \mu}{\sigma})\right] = (2\pi \sigma^2)^{-n/2} \exp \left[- \frac{1}{2} \sum_{i=1}^n \left(\frac{x_i - \mu}{\sigma}\right)^2\right]$$
    $$= - \frac{n}{2}\ln(2\pi \sigma^2) - \frac{1}{2} \sum_{i=1}^{n} \left(\frac{x_i - \mu}{\sigma^2}\right)$$

-   Now we can take the derivativce w.r.t $\mu$ or $\sigma^2$
    $$\frac{\partial \ln(L)}{\partial \mu} = \sum_{i=1}^{n}(\frac{x_i - \mu}{\sigma}) = 0$$

-   We set the above equal to zero to find the estimator of $\hat{\mu}$
    we make $\mu \rightarrow \hat{\mu}$
    $$0 = \frac{1}{\sigma^2} \sum_{i=1}^{n} (x_i -\mu) \rightarrow \sum_{i=1}^n x_i - n \hat{\mu} \rightarrow \hat{\mu} = \frac{1}{n}\sum_{i=1}^{n} x_i = \bar{x}$$

-   Note, we take the same derivative w.r.t $\sigma^2$, the MLE of
    $\sigma^2$ is $\hat{\sigma}^2$ which has $n$ degrees of freedom, as
    such, it is a biased estimator of $\sigma^2$. Recall that the
    unbiased estimator $S^2$ had $n-1$ degrees of freedom.

### Example:

-   Given $12,11.2,13.5, 12.3, 13.8, 11.9$ comes fro ma population with
    density function $$f(x;\theta) = \begin{cases}
            \frac{\theta}{x^{\theta+1}}, \ \ x > 1, \\ 0, \ \ \text{else}
        \end{cases}$$

-   Where$\theta > 0$. Find the MLE of $\theta$
    $$L(x_1, ..., x_{6}; \theta) = \prod_{i=1}^{n} \frac{\theta}{x_i^{\theta+1}} = \frac{\theta^n}{(\prod_{i=1}^{n} x_i)^{\theta+1}}$$

-   $$= n \ln \theta  - (\theta +1 ) \ln \left(\prod_{i=1}^n x_i\right) = n \ln \theta - \sum_{i=1}^{6}(\theta + 1) \ln  x_i$$

-   now take the derivative of $\ln(L)$

-   $$\frac{\partial \ln(L)}{\partial \theta} = \frac{6}{\theta} - \sum_{i=1}^6 \ln(x_i) \rightarrow  0 = \frac{6}{\hat{\theta}} \sum_{i=1}^{6} \ln x_i \rightarrow \hat{\theta} = \frac{6}{\sum_{i=1}^6 x_i}$$

-   Note that it is easier to work with $x_i$ and then take the sum at
    the end.

-   Note, we only change the paramater to its estimator form
    $\theta \rightarrow \hat{\theta}$ when we set the derivative equal
    to 0.

-   $\hat{\theta} = 0.397$
