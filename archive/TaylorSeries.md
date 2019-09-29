# Taylor Series

## Taylor polynomial of degree n of f(x)

- Centred at/about/around $x = a$:

$$
P_{n}(x) = f(a)+\frac{f'(a)}{1!}(x-a)+\frac{f''(a)}{2!}(x-a)^{2}+\dots+\frac{f^{(n)}(a)}{n!}(x-a)^{n}
$$

- Centred at/about/around $x = 0$:

$$
P_{n}(x) = f(0)+\frac{f'(0)}{1!}x+\frac{f''(0)}{2!}x^{2}+\dots+\frac{f^{(n)}(0)}{n!}x^{n}
$$

## Taylor series of f(x), P(x)

- Centred at/about/around $x = a$:

$$
P(x) = \lim_{n\rightarrow\infty}P_{n}(x)=\sum^{\infty}_{k = 0}\frac{f^{(k)}(a)}{k!}(x-a)^{k}
$$

- Centred at/about/around $x = 0 \textbf{ (Maclaurin series)}$:

$$
P(x) = \lim_{n\rightarrow\infty}P_{n}(x)=\sum^{\infty}_{k = 0}\frac{f^{(k)}(0)}{k!}x^{k}
$$
