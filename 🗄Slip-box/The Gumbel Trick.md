
https://lips.cs.princeton.edu/the-gumbel-max-trick-for-discrete-distributions/

https://arxiv.org/pdf/1611.00712.pdf

https://arxiv.org/pdf/2110.01515.pdf

## Generate Exponential Variable from Uniform Variable

Goal: draw z from standard exponential distribution.
Draw $x \sim \mathcal{U}(0,1)$ and let $z = -\ln x$. Then for any $a>0$,
$$
P(z \le a) = P(-\ln x \le a) = P(\ln x \ge -a) = P(x \ge \exp^{-a}) = 1 - e^{-a}
$$
which coincides with the CDF of the exponential distribution.

## Generate Gumbel Variable from Uniform Variable

Draw $x \sim \mathcal{U}(0,1)$ and let $z = -\ln (\ln x)$. Then for any a>0,
$$
\begin{align*}
P(z \le a) &= P(-\ln (-\ln x) \le a) = P(\ln (-\ln x) \ge -a) = P(-\ln x \ge \exp(-a)) \\ &= P(\ln x \le -\exp(-a)) = P(x \le \exp(-\exp(-a)))
\end{align*}
$$
Which coincides with the CDF of the Gumbel distribution.



---







