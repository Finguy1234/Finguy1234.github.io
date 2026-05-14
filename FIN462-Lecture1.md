# Lecture Notes: Return Measurement, Compounding, Risk, Taxes, and the Microfoundations of the Cost of Equity

## 1. The Basic Question

Investment analysis begins with a simple question:

> If I give up resources today, what compensation do I require in the future?

That compensation is a **return**. But the return is not merely a mechanical number. It reflects time, risk, inflation, taxation, and equilibrium pricing. At the deepest level, the required return on an investment is determined by the preferences and opportunities of investors. Firms then take that required return as their **cost of capital** and use it as a hurdle rate when deciding whether to invest.

The logic of the lecture is:

1. Firms generate cash flows from production.
2. Investors value those cash flows by discounting them.
3. The discount rate comes from equilibrium investor preferences.
4. Expected returns depend on risk, especially covariance with the stochastic discount factor.
5. Return measurement requires careful treatment of compounding, inflation, taxes, and statistical risk.

---

# 2. The Firm in a Competitive Market

Begin with a firm operating in a competitive product market.

Let the firm produce output ( q ). The market price of output is ( P ). Because the firm is competitive, it takes ( P ) as given.

The firm has a cost function:

$C(q)$

Profit is:

$\pi(q) = Pq - C(q)$

The firm chooses output to maximize profit:

$\max_q ; Pq - C(q)$

The first-order condition is:

$P = C'(q)$

That is:

$P = MC(q)$

The competitive firm produces until price equals marginal cost.

Total profit at the optimal output ( q^* ) is:

$\pi^* = Pq^* - C(q^*)$

Graphically, if price exceeds average total cost, the firm earns positive economic profit. If price equals average total cost, profit is zero. If price is below average total cost but above average variable cost, the firm may operate in the short run while losing money.

---

# 3. A Two-Period Firm Valuation Model

Now suppose the firm operates in a simple two-period world.

At date ( t=0 ), investors buy claims to the firm.

At date ( t=1 ), the firm produces, sells output, pays costs, and distributes profit to shareholders.

Let the firm’s date-1 profit be:

$\pi_1$

If the relevant required return is ( r ), then the date-0 market value of equity is:

$E_0 = \frac{\pi_1}{1+r}$

If date-1 profit is uncertain, the expression becomes:

$E_0 = \frac{\mathbb{E}_0[\pi_1]}{1+r}$

but that formulation is incomplete unless the profit is riskless. For risky profit, the correct valuation is not simply expected profit divided by a single risk-free discount rate. Risk matters.

The more general valuation formula is:

$E_0 = \mathbb{E}_0[M_1 \pi_1]$

where ( M_1 ) is the **stochastic discount factor**.

This equation says:

> A payoff is valuable today if it pays off in states of the world where investors value consumption highly.

That is the central microfoundation of investment analysis.

---

# 4. Where Does ( r ) Come From?

In a basic finance class, we often write:

$PV = \frac{CF_1}{1+r}$

But this leaves open a deeper question:

> Where does the discount rate ( r ) come from?

It is not arbitrary. It is determined in equilibrium by investors’ preferences over consumption today versus consumption tomorrow, and by the riskiness of future payoffs.

To see this, use a simple Lucas tree model.

---

# 5. A Simple Lucas Tree Economy

Imagine an economy with one representative investor and one asset: a tree.

The tree produces fruit each period. Fruit is the consumption good.

At date ( t=0 ), the investor consumes ( C_0 ).

At date ( t=1 ), the tree produces a random dividend ( D_1 ), and the investor consumes ( C_1 ).

The investor has expected lifetime utility:

$U = u(C_0) + \beta \mathbb{E}_0[u(C_1)]$

where:

* ( u(C) ) is the utility function,
* ( u'(C) > 0 ): more consumption is preferred to less,
* ( u''(C) < 0 ): marginal utility declines as consumption rises,
* ( \beta \in (0,1) ) is the subjective discount factor.

No special functional form is required. We do not need logarithmic utility, CRRA utility, or quadratic utility. The key object is the ratio of marginal utilities.

Suppose the investor can buy an asset with price ( P_0 ) that pays payoff ( X_1 ) next period.

The investor chooses how much of the asset to buy. The first-order condition implies:

$P_0 u'(C_0) = \beta \mathbb{E}_0[u'(C_1) X_1]$

Divide both sides by ( u'(C_0) ):

$P_0 = \mathbb{E}_0 \left[ \beta \frac{u'(C_1)}{u'(C_0)} X_1 \right]$

Define the stochastic discount factor:

$M_1 = \beta \frac{u'(C_1)}{u'(C_0)}$

Then:

$P_0 = \mathbb{E}_0[M_1 X_1]$

This is the fundamental asset-pricing equation.

---

# 6. Interpretation of the Stochastic Discount Factor

The stochastic discount factor is:

$M_1 = \beta \frac{u'(C_1)}{u'(C_0)}$

It is high when future marginal utility is high.

Future marginal utility is high when future consumption is low. Therefore, payoffs that occur in bad states are especially valuable.

A payoff that arrives during a recession, crisis, or low-consumption state provides insurance. Investors value it highly.

A payoff that arrives mainly in boom states is less valuable, because investors already have high consumption in those states.

This is why risk is not merely variance. What matters is **covariance with marginal utility**.

---

# 7. Returns and the Asset-Pricing Equation

Let an asset have price ( P_0 ) and payoff ( X_1 ). Its gross return is:

$R_1 = \frac{X_1}{P_0}$

Using:

$P_0 = \mathbb{E}_0[M_1 X_1]$

divide both sides by ( P_0 ):

$1 = \mathbb{E}_0[M_1 R_1]$

This is the central return-pricing equation:

$\boxed{1 = \mathbb{E}_0[M_1 R_1]}$

Using the identity:

$\mathbb{E}[MR] = \mathbb{E}[M]\mathbb{E}[R] + \operatorname{Cov}(M,R)$

we get:

$1 = \mathbb{E}[M]\mathbb{E}[R] + \operatorname{Cov}(M,R)$

So:

$\mathbb{E}[R] = \frac{1 - \operatorname{Cov}(M,R)}{\mathbb{E}[M]}$

For the risk-free asset, ( R_f ) is known in advance. Therefore:

$1 = \mathbb{E}[M]R_f$

so:

$R_f = \frac{1}{\mathbb{E}[M]}$

Substitute into the expected return equation:

$\mathbb{E}[R] = R_f - R_f \operatorname{Cov}(M,R)$

Therefore, the expected excess return is:

$\mathbb{E}[R] - R_f = -R_f \operatorname{Cov}(M,R)$

This is one of the most important results in asset pricing.

If an asset has a **negative covariance** with the stochastic discount factor, it pays off poorly when marginal utility is high. In other words, it performs badly in bad times. Investors dislike this risk and demand a higher expected return.

If an asset has a **positive covariance** with the stochastic discount factor, it pays off well in bad times. It provides insurance, so investors accept a lower expected return.

---

# 8. Connecting This to the Firm’s Cost of Equity

A firm’s equity is a claim on its future profits:

$X_1 = \pi_1$

Therefore:

$E_0 = \mathbb{E}_0[M_1 \pi_1]$

The expected return on the firm’s equity is:

$\mathbb{E}[R_E]$

This expected return is the firm’s **cost of equity**.

Why?

Because shareholders require compensation for holding the firm’s risky profits. If the firm wants to raise equity capital, it must offer investors an expected return high enough to persuade them to hold its shares.

The firm’s cost of equity is not determined by management preference. It is determined in capital-market equilibrium by investors’ valuation of the firm’s risk.

A firm whose profits are high in booms and low in recessions will generally have a high cost of equity because its profits covary negatively with the stochastic discount factor.

A firm whose profits are stable or countercyclical will generally have a lower cost of equity.

---

# 9. Cost of Equity as a Capital Budgeting Hurdle Rate

Suppose the firm is considering an investment project.

The project costs ( I_0 ) today and produces expected future cash flow ( CF_1 ).

The project should be accepted if its net present value is positive:

$NPV = -I_0 + PV(CF_1)$

If the project has the same risk as the firm’s existing equity, then the firm may discount using its cost of equity:

$NPV = -I_0 + \frac{\mathbb{E}[CF_1]}{1+r_E}$

Accept the project if:

$NPV > 0$

Equivalently, accept if the project’s expected return exceeds the cost of equity:

$\mathbb{E}[R_{\text{project}}] > r_E$

The cost of equity is therefore a **hurdle rate**.

However, the correct hurdle rate depends on project risk, not merely firm identity. A safe project should not be discounted at the same rate as a highly cyclical project. The discount rate should reflect the project’s covariance with the stochastic discount factor.

The theoretically correct valuation is:

$PV = \mathbb{E}[M_1 CF_1]$

The common textbook discount-rate approach is a simplified version of this deeper principle.

---

# 10. Total Return

Now turn to return measurement.

The **total return** on an asset has two components:

1. Income return
2. Capital gain return

Suppose an asset has initial price ( P_0 ), ending price ( P_1 ), and pays income ( D_1 ), such as a dividend, coupon, or rent.

The holding-period return is:

$R = \frac{P_1 + D_1 - P_0}{P_0}$

This can be decomposed as:

$R = \frac{D_1}{P_0} + \frac{P_1 - P_0}{P_0}$

The first term is the income component:

$\frac{D_1}{P_0}$

The second term is the capital gain component:

$\frac{P_1 - P_0}{P_0}$

So:

$\boxed{\text{Total return}= \text{Income return} + \text{Capital gain return}}$

Example:

A stock begins the year at ( $100 ), pays a ( $3 ) dividend, and ends the year at ( $108 ).

The income return is:

$\frac{3}{100} = 0.03 = 3%$

The capital gain return is:

$\frac{108-100}{100} = 0.08 = 8%$

The total return is:

$0.03 + 0.08 = 0.11 = 11%$

---

# 11. Holding-Period Returns

A **holding-period return** is the return earned over the actual period during which the asset is held.

The formula is:

$HPR = \frac{\text{Ending value} + \text{Income} - \text{Beginning value}}{\text{Beginning value}}$

Or, as a gross return:

$1+HPR = \frac{\text{Ending value} + \text{Income}}{\text{Beginning value}}$

If an asset is purchased for ( $50 ), pays a ( $2 ) dividend, and is sold for ( $55 ), then:

$HPR = \frac{55 + 2 - 50}{50}$

$HPR = \frac{7}{50} = 0.14 = 14%$

The gross return is:

$1+HPR = 1.14$

Holding-period returns are useful because they directly measure what happened over the investor’s actual holding period.

However, they are not always directly comparable across investments with different holding periods. A 10% return over one month is not the same as a 10% return over five years.

That is why we annualize returns.

---

# 12. Annual Percentage Rate and Effective Annual Rate

The **annual percentage rate**, or APR, is a quoted annual rate that does not fully incorporate the effect of compounding within the year.

The **effective annual rate**, or EAR, is the actual annual rate earned after accounting for compounding.

If the APR is ( r_{\text{APR}} ), and compounding occurs ( m ) times per year, then:

$EAR = \left(1 + \frac{r_{\text{APR}}}{m}\right)^m - 1$

For example, if the APR is 12% and interest is compounded monthly, then:

$EAR = \left(1 + \frac{0.12}{12}\right)^{12} - 1$

$EAR = (1.01)^{12} - 1$

$EAR \approx 0.1268 = 12.68%$

So a 12% APR compounded monthly is not actually a 12% annual return. It is a 12.68% effective annual return.

The more frequently interest compounds, the higher the effective annual rate, holding the APR fixed.

---

# 13. Continuous Compounding

As compounding becomes more frequent, the compounding interval becomes smaller. In the limit, we get **continuous compounding**.

If ( r_c ) is the continuously compounded annual rate, then the future value of ( PV ) after ( T ) years is:

$FV = PV e^{r_c T}$

The present value of ( FV ) received ( T ) years from now is:

$PV = FV e^{-r_c T}$

The relationship between an effective annual rate ( EAR ) and a continuously compounded rate ( r_c ) is:

$1 + EAR = e^{r_c}$

Therefore:

$r_c = \ln(1+EAR)$

and:

$EAR = e^{r_c} - 1$

Example:

If the effective annual rate is 10%, then the continuously compounded rate is:

$r_c = \ln(1.10)$

$r_c \approx 0.09531 = 9.531%$

If the continuously compounded rate is 9.531%, then:

$EAR = e^{0.09531} - 1 \approx 0.10 = 10%$

Continuously compounded returns are especially useful in theory because log returns add across time.

If the price of an asset changes from ( P_0 ) to ( P_1 ), the continuously compounded return is:

$r = \ln\left(\frac{P_1}{P_0}\right)$

If the asset then moves from ( P_1 ) to ( P_2 ), the second continuously compounded return is:

$r_2 = \ln\left(\frac{P_2}{P_1}\right)$

The two-period continuously compounded return is:

$\ln\left(\frac{P_2}{P_0}\right)$

and:

$\ln\left(\frac{P_2}{P_0}\right)= \ln\left(\frac{P_1}{P_0}\right)+\ln\left(\frac{P_2}{P_1}\right)$

So log returns are time-additive.

---

# 14. Worked Example: The Effects of Compounding

Suppose an investor places ( $10,000 ) in an account with a quoted APR of 8%.

Compare annual, quarterly, monthly, daily, and continuous compounding over 10 years.

The general formula is:

$FV = PV \left(1 + \frac{r}{m}\right)^{mT}$

where:

* ( PV = 10{,}000 ),
* ( r = 0.08 ),
* ( T = 10 ),
* ( m ) is the number of compounding periods per year.

### Annual Compounding

$FV = 10{,}000(1.08)^{10}$

$FV \approx 10{,}000(2.1589)$

$FV \approx 21{,}589$

### Quarterly Compounding

$FV = 10{,}000\left(1+\frac{0.08}{4}\right)^{40}$

$FV = 10{,}000(1.02)^{40}$

$FV \approx 22{,}080$

### Monthly Compounding

$FV = 10{,}000\left(1+\frac{0.08}{12}\right)^{120}$

$FV \approx 22{,}196$

### Daily Compounding

$FV = 10{,}000\left(1+\frac{0.08}{365}\right)^{3650}$

$FV \approx 22{,}251$

### Continuous Compounding

$FV = 10{,}000e^{0.08(10)}$

$FV = 10{,}000e^{0.8}$

$FV \approx 22{,}255$

The results are:

| Compounding Frequency | Future Value |
| --------------------: | -----------: |
|                Annual |      $21,589 |
|             Quarterly |      $22,080 |
|               Monthly |      $22,196 |
|                 Daily |      $22,251 |
|            Continuous |      $22,255 |

The lesson is:

> More frequent compounding increases wealth, but the gains become smaller as compounding frequency rises.

The jump from annual to quarterly compounding is meaningful. The jump from daily to continuous compounding is tiny.

---

# 15. Nominal and Real Interest Rates

A **nominal interest rate** measures the percentage increase in dollars.

A **real interest rate** measures the percentage increase in purchasing power.

If an investment earns 8% but prices rise by 3%, the investor’s purchasing power does not rise by the full 8%.

Let:

* ( i ) be the nominal interest rate,
* ( r ) be the real interest rate,
* ( \pi ) be the inflation rate.

The exact relationship is:

$1+i = (1+r)(1+\pi)$

Solving for the real interest rate:

$1+r = \frac{1+i}{1+\pi}$

$r = \frac{1+i}{1+\pi} - 1$

Example:

If the nominal rate is 8% and inflation is 3%, then:

$r = \frac{1.08}{1.03} - 1$

$r \approx 0.0485 = 4.85%$

The approximate relationship is:

$i \approx r + \pi$

So:

$r \approx i - \pi$

Using the approximation:

$r \approx 8% - 3% = 5%$

The approximation is close, but not exact.

---

# 16. The Fisher Equation

The Fisher equation relates nominal interest rates, real interest rates, and expected inflation.

The exact Fisher equation is:

$1+i = (1+r)(1+\mathbb{E}[\pi])$

The approximate Fisher equation is:

$i \approx r + \mathbb{E}[\pi]$

where ( \mathbb{E}[\pi] ) is expected inflation.

The Fisher equation says that nominal rates compensate investors for two things:

1. The real return required for postponing consumption.
2. Expected loss of purchasing power due to inflation.

If expected inflation rises while the real rate is unchanged, nominal interest rates should rise.

---

# 17. The Fisher Hypothesis

The **Fisher hypothesis** is the proposition that nominal interest rates adjust one-for-one with expected inflation, leaving real interest rates unchanged.

If expected inflation rises by 1 percentage point, nominal interest rates should rise by approximately 1 percentage point.

Formally:

$\Delta i \approx \Delta \mathbb{E}[\pi]$

if the real rate ( r ) is constant.

The Fisher hypothesis is an equilibrium claim. It assumes that investors care about real purchasing power, not merely dollar payoffs.

If lenders expect higher inflation, they demand higher nominal interest rates to preserve their real return.

If borrowers expect higher inflation, they may be willing to pay higher nominal rates because they expect to repay in dollars with lower purchasing power.

In practice, real rates are not always constant. They vary with productivity, time preference, risk, monetary policy, fiscal conditions, and the demand and supply of saving. Therefore, the Fisher hypothesis is a useful benchmark, not an iron law.

---

# 18. Arithmetic Average Returns

Suppose an asset earns returns:

$R_1, R_2, \ldots, R_T$

The arithmetic average return is:

$\bar{R}*A = \frac{1}{T}\sum*{t=1}^T R_t$

Example:

Suppose returns over three years are:

$20%, -10%, 15%$

The arithmetic average is:

$\bar{R}_A = \frac{0.20 - 0.10 + 0.15}{3}$

$\bar{R}_A = \frac{0.25}{3}$

$\bar{R}_A = 0.0833 = 8.33%$

The arithmetic average is the appropriate estimate of the expected one-period return if each historical return is treated as an equally likely future outcome.

It answers the question:

> What is the average return in a typical single period?

---

# 19. Geometric Average Returns

The geometric average return measures the constant per-period return that would compound to the same terminal wealth.

The formula is:

$\bar{R}*G =
\left[
\prod*{t=1}^T (1+R_t)
\right]^{1/T}
-1$

For the same returns:

$20%, -10%, 15%$

we calculate:

$\bar{R}_G =
[(1.20)(0.90)(1.15)]^{1/3} - 1$

$\bar{R}_G =
[1.242]^{1/3} - 1$

$\bar{R}_G \approx 0.0750 = 7.50%$

The geometric average is lower than the arithmetic average when returns are volatile.

That is because losses require larger subsequent gains to recover.

For example, a 50% loss followed by a 50% gain does not break even:

$100 \rightarrow 50 \rightarrow 75$

The arithmetic average is:

$\frac{-50% + 50%}{2} = 0%$

But the investor lost 25% of wealth.

The geometric return is:

$[(0.5)(1.5)]^{1/2} - 1$

$= (0.75)^{1/2} - 1$

$\approx -13.4%$

The geometric average answers:

> What constant return would have produced the same compound growth?

Use the arithmetic average for estimating expected one-period returns. Use the geometric average for measuring long-run realized compound performance.

---

# 20. Expected Returns

An expected return is a probability-weighted average of possible returns.

Suppose there are ( N ) possible states of the world. State ( s ) occurs with probability ( p_s ), and the asset return in that state is ( R_s ).

The expected return is:

$\mathbb{E}[R] = \sum_{s=1}^N p_s R_s$

Example:

| State     | Probability | Return |
| --------- | ----------: | -----: |
| Boom      |        0.25 |    20% |
| Normal    |        0.50 |     8% |
| Recession |        0.25 |   -10% |

Then:


$\mathbb{E}[R]=
0.25(0.20)
+
0.50(0.08)
+
0.25(-0.10)$

$\mathbb{E}[R]=
0.05 + 0.04 - 0.025$

$\mathbb{E}[R] = 0.065 = 6.5%$

The expected return is not necessarily the return that will occur. It is the probability-weighted mean of the distribution.

---

# 21. Variance and Standard Deviation

Variance measures the average squared deviation of returns from their expected value.

For a probability distribution:

$\sigma^2 = \operatorname{Var}(R)=
\sum_{s=1}^N p_s (R_s - \mathbb{E}[R])^2$

Standard deviation is the square root of variance:

$\sigma = \sqrt{\operatorname{Var}(R)}$

Using the previous example:

$\mathbb{E}[R] = 6.5%$

The deviations are:

* Boom: ( 20% - 6.5% = 13.5% )
* Normal: ( 8% - 6.5% = 1.5% )
* Recession: ( -10% - 6.5% = -16.5% )

The variance is:

$\sigma^2=
0.25(0.135)^2
+
0.50(0.015)^2
+
0.25(-0.165)^2$

\sigma^2=
0.25(0.018225)
+
0.50(0.000225)
+
0.25(0.027225)$

$\sigma^2=
0.00455625 + 0.0001125 + 0.00680625$

$\sigma^2 = 0.011475$

The standard deviation is:

$\sigma = \sqrt{0.011475}$

$\sigma \approx 0.1071 = 10.71%$

Standard deviation is useful because it is measured in the same units as returns.

Variance is mathematically convenient, but standard deviation is easier to interpret.

---

# 22. Skewness

Variance treats upside and downside deviations symmetrically. But investors often care about asymmetry.

**Skewness** measures the asymmetry of a distribution.

A return distribution has **positive skewness** if it has a long right tail. That means a small chance of very large positive returns.

Examples:

* Venture capital
* Call options
* Lottery-like stocks
* Early-stage biotechnology firms

A return distribution has **negative skewness** if it has a long left tail. That means a small chance of very large losses.

Examples:

* Selling insurance
* Selling put options
* Leveraged carry trades
* Highly levered financial institutions

The population skewness is:

$\text{Skewness}=
\mathbb{E}
\left[
\left(
\frac{R - \mu}{\sigma}
\right)^3
\right]$

where:

* ( \mu = \mathbb{E}[R] ),
* ( \sigma ) is the standard deviation.

Positive skewness is often attractive because investors like upside potential.

Negative skewness is dangerous because ordinary periods may look stable while rare crashes impose severe losses.

A strategy that earns small steady gains and occasionally crashes may have high average returns for a while, but its negative skewness can be economically important.

---

# 23. Kurtosis

**Kurtosis** measures the thickness of the tails of a distribution relative to the normal distribution.

The population kurtosis is:

$\text{Kurtosis}=
\mathbb{E}
\left[
\left(
\frac{R - \mu}{\sigma}
\right)^4
\right]$

A normal distribution has kurtosis equal to 3.

Excess kurtosis is:

$\text{Excess kurtosis} = \text{Kurtosis} - 3$

High excess kurtosis means the distribution has fat tails. Extreme observations occur more often than they would under a normal distribution.

In investment analysis, kurtosis matters because many financial return distributions have fat tails. Crashes and extreme rallies occur more frequently than a simple normal model predicts.

Variance and standard deviation summarize ordinary dispersion. Skewness and kurtosis help describe tail risk.

---

# 24. Probability Concepts and the Investor’s Problem

The probability concepts are not merely descriptive statistics. They matter because investors choose portfolios under uncertainty.

An investor does not care only about the expected return of an asset. The investor cares about how the asset affects lifetime utility.

Recall the asset-pricing condition:

$1 = \mathbb{E}[M R]$

Using covariance:

$1 = \mathbb{E}[M]\mathbb{E}[R] + \operatorname{Cov}(M,R)$

This equation connects probability directly to equilibrium expected returns.

The expected return of an asset depends on:

1. The average payoff.
2. The timing of the payoff across states.
3. The covariance of the payoff with marginal utility.
4. The investor’s willingness to substitute consumption across time and states.

Standard deviation alone is not enough.

An asset can have high variance but still be valuable if it pays off in bad states.

An asset can have modest variance but command a high expected return if it fails exactly when investors most need wealth.

This is why covariance is the central risk concept in modern asset pricing.

---

# 25. A Simple Numerical SDF Example

Suppose there are two states next period:

| State | Probability | Consumption | Marginal Utility | SDF (M) |
| ----- | ----------: | ----------: | ---------------: | ------: |
| Good  |         0.5 |        High |              Low |    0.80 |
| Bad   |         0.5 |         Low |             High |    1.20 |

The stochastic discount factor is high in the bad state because marginal utility is high.

Consider two assets.

### Asset A: Procyclical Equity

| State | Return |
| ----- | -----: |
| Good  |    20% |
| Bad   |    -5% |

Gross returns are:

| State | Gross Return |
| ----- | -----------: |
| Good  |         1.20 |
| Bad   |         0.95 |

Compute:

$\mathbb{E}[M R_A]=
0.5(0.80)(1.20)
+
0.5(1.20)(0.95)$

$0.48 + 0.57= 1.05$

If ( \mathbb{E}[MR] > 1 ), the asset is too cheap relative to equilibrium, or its expected return is too high for its risk. In equilibrium, its price would be bid up until:

$\mathbb{E}[MR] = 1$

The important point is that this asset pays more in good states and less in bad states. That makes it risky in the economically relevant sense.

### Asset B: Insurance-Like Asset

| State | Return |
| ----- | -----: |
| Good  |     0% |
| Bad   |    10% |

Gross returns:

| State | Gross Return |
| ----- | -----------: |
| Good  |         1.00 |
| Bad   |         1.10 |

Compute:

$\mathbb{E}[M R_B]=
0.5(0.80)(1.00)
+
0.5(1.20)(1.10)$

$0.40 + 0.66= 1.06$

This asset is valuable because it pays well when the stochastic discount factor is high. Investors would accept a relatively low expected return on this asset because it provides insurance.

The broader lesson:

> Expected returns compensate investors for bearing bad-state risk, not merely for accepting volatility.

---

# 26. Taxes and After-Tax Returns

Investors care about after-tax returns.

Suppose an investment earns a pre-tax return ( R ), and the tax rate on the return is ( \tau ).

If the entire return is taxed at rate ( \tau ), then the after-tax return is:

$R_{\text{after-tax}} = R(1-\tau)$

Example:

If the pre-tax return is 10% and the tax rate is 25%, then:

$R_{\text{after-tax}} = 0.10(1-0.25)$

$R_{\text{after-tax}} = 0.075 = 7.5%$

But actual taxation is more complicated because different components of return may be taxed differently.

For stocks, the income component may be dividends, and the capital gain component may be taxed only when realized.

The total pre-tax return is:

$R = \frac{D_1}{P_0} + \frac{P_1 - P_0}{P_0}$

Let:

* ( \tau_D ) be the tax rate on dividends,
* ( \tau_G ) be the tax rate on realized capital gains.

Then the after-tax return is:

$R_{\text{after-tax}}=
\frac{D_1(1-\tau_D)}{P_0}
+
\frac{(P_1-P_0)(1-\tau_G)}{P_0}$

if the capital gain is realized immediately.

Example:

A stock is purchased for ( $100 ), pays a ( $4 ) dividend, and is sold for ( $110 ). The dividend tax rate is 20%, and the capital gains tax rate is 15%.

Pre-tax return:

$R = \frac{4}{100} + \frac{110-100}{100}$

$R = 4% + 10% = 14%$

After-tax dividend return:

$\frac{4(1-0.20)}{100} = \frac{3.20}{100} = 3.2%$

After-tax capital gain return:

$\frac{10(1-0.15)}{100} = \frac{8.50}{100} = 8.5%$

Total after-tax return:

$R_{\text{after-tax}} = 3.2% + 8.5% = 11.7%$

Taxes reduce the investor’s realized return and can change preferences across securities.

Taxable investors may prefer:

* lower dividend yields,
* deferred capital gains,
* municipal bonds,
* tax-advantaged accounts,
* tax-loss harvesting strategies.

Taxes also affect firms. Because interest payments are often tax-deductible at the corporate level while dividends are not, debt financing can create a tax shield. That changes the weighted average cost of capital.

---

# 27. Taxes, Compounding, and Deferral

Tax timing matters.

Suppose two investments both earn 8% before tax.

Investment A distributes all returns annually, and taxes are paid each year at a 25% tax rate.

Investment B compounds tax-free for 10 years, with tax paid only at the end.

### Investment A: Taxed Annually

The after-tax annual return is:

$0.08(1-0.25) = 0.06$

A ( $10,000 ) investment grows to:

$FV_A = 10{,}000(1.06)^{10}$

$FV_A \approx 17{,}908$

### Investment B: Tax Deferred

Before tax, the investment grows to:

$10{,}000(1.08)^{10}$

$\approx 21{,}589$

The gain is:

$21{,}589 - 10{,}000 = 11{,}589$

Tax on the gain at 25% is:

$0.25(11{,}589) = 2{,}897$

After-tax ending wealth is:

$21{,}589 - 2{,}897 = 18{,}692$

Tax deferral creates value because pre-tax dollars compound for longer.

Investment B leaves the investor with:

$18{,}692 - 17{,}908 = 784$

more after 10 years.

The lesson:

> Taxes affect not only the level of returns, but also the compounding path.

---

# 28. Pulling the Pieces Together

Investment analysis is not just the calculation of historical returns. It is a unified theory of valuation, risk, and choice.

The firm produces profits:

$\pi = Pq - C(q)$

Investors value those profits:

$E_0 = \mathbb{E}[M_1 \pi_1]$

The stochastic discount factor comes from intertemporal marginal rates of substitution:

$M_1 = \beta \frac{u'(C_1)}{u'(C_0)}$

Expected returns satisfy:

$1 = \mathbb{E}[M R]$

Risk premia are determined by covariance with the stochastic discount factor:

$\mathbb{E}[R] - R_f=-R_f \operatorname{Cov}(M,R)$

The firm’s cost of equity is the expected return investors require to hold the firm’s risky profits.

That cost of equity becomes a hurdle rate for capital budgeting.

Return measurement then tells us how to describe realized investment performance:

$R = \frac{D_1}{P_0} + \frac{P_1-P_0}{P_0}$

Compounding tells us how returns accumulate through time.

Inflation tells us the difference between nominal and real returns.

Taxes tell us the difference between pre-tax and after-tax returns.

Statistical moments tell us about the shape of the return distribution:

* mean: central tendency,
* variance and standard deviation: dispersion,
* skewness: asymmetry,
* kurtosis: tail thickness.

But the most important risk concept is not volatility by itself. It is whether the asset pays off when investors most value payoffs.

---

# 29. Key Takeaways

1. **Total return equals income return plus capital gain return.**

$R = \frac{D_1}{P_0} + \frac{P_1-P_0}{P_0}$

2. **Holding-period returns measure actual performance over the investor’s holding period.**

$HPR = \frac{P_1 + D_1 - P_0}{P_0}$

3. **APR is a quoted rate; EAR is the true annual rate after compounding.**

$EAR = \left(1+\frac{APR}{m}\right)^m - 1$

4. **Continuous compounding uses the exponential function.**

$FV = PV e^{rT}$

5. **Real returns adjust nominal returns for inflation.**

$1+i = (1+r)(1+\pi)$

6. **The Fisher equation links nominal rates, real rates, and expected inflation.**

$i \approx r + \mathbb{E}[\pi]$

7. **Arithmetic average returns estimate a typical one-period return.**

$\bar{R}*A = \frac{1}{T}\sum*{t=1}^T R_t$

8. **Geometric average returns measure compound growth.**

$\bar{R}*G =
\left[
\prod*{t=1}^T(1+R_t)
\right]^{1/T}
-1$

9. **Variance and standard deviation measure dispersion.**

$\sigma^2 = \mathbb{E}[(R-\mu)^2]$

10. **Skewness and kurtosis describe asymmetry and tail risk.**

$\text{Skewness}=
\mathbb{E}
\left[
\left(
\frac{R-\mu}{\sigma}
\right)^3
\right]$

$\text{Kurtosis}=
\mathbb{E}
\left[
\left(
\frac{R-\mu}{\sigma}
\right)^4
\right]$

11. **The stochastic discount factor prices assets.**

$P = \mathbb{E}[MX]$

12. **Expected returns compensate investors for covariance with the SDF.**

$\mathbb{E}[R] - R_f=-R_f \operatorname{Cov}(M,R)$

13. **The firm’s cost of equity is the expected return required by investors.**

14. **That cost of equity becomes the hurdle rate for capital budgeting.**

15. **Taxes reduce returns and alter the value of compounding, income, and capital gains.**
