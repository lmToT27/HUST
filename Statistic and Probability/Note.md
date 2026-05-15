## Bernoulli Trial
- Denoted by Ber(p): P(success) = p
- Mean = $p$
- Variance = $p * q$
## Binomial Distribution
- Denoted by B(n, p): n independent Bernoulli Trials, P(success) = p
- Mean = $n * p$
- Variance = $n * p * q$
- $n * p - q$ <= mode <= $n * p - q + 1$
## Possion Distribution
- Denoted by P(x, μ) = $\frac{e^{-μ} * μ^x}{x!}$ is the probability that the event X occurs x times
- Mean = Variance
## Normal Distribution
$$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
- Denoted by $X \sim N(\mu, \sigma^2)$
- Standardization Rule: $Z \sim N(0, 1)$, where: $$Z = \frac{X - \mu}{\sigma}$$
- After standardization, instead of calculating integral, we just need to look up probability values from a table called $\Phi(z)$ function. Example: P(X < x) = $\Phi(\frac{x - \mu}{\sigma})$
- $\Phi(x) = 1 - \Phi(-x)$
## Hypergeometric Distribution
- $X \sim \text{Hypergeometric}(N, K, n)$: N marbles, K "success" marbles, choose n marbles but don't put it back
- PMF is $$ P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}} $$
- Mean: $$ \mathbb{E}[X] = n \frac{K}{N} $$
- Variance: $$ \text{Var}(X) = n \frac{K}{N} \left(1 - \frac{K}{N}\right) \frac{N-n}{N-1} $$
## Exponential Distribution
- PDF: $$  f(x) = \begin{cases} \lambda e^{-\lambda x} \ \ if  \ \ x > 0\\ 0 \ \ otherwise \end{cases}$$
- Mean: $$\frac{1}{\lambda}$$
- Variance: $$\frac{1}{\lambda^2}$$
- Memoryless Property: $$ P(X > s + t \mid X > s) = P(X > t) $$
## Uniform Distribution
- In interval $[a, b]$, $$ f(x) = \begin{cases} \frac{1}{b - a} \ \ if \ \ x \in [a, b] \\ 0 \ \ otherwise\end{cases} $$
- Mean = Median = $\frac{a + b}{2}$
- Variance = $\frac{(b - a) ^ 2}{12}$