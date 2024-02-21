[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

Show that $log_2(n)$ is equivalent to $log_5(n)$: <br>
Let T(n) be equal to anything that makes the big O definition true and $f(n) = log_5(n)$. 
Now if we suppose this is true, then $T(n) \in O(log_5(n))$ for some value of c and $n_0$, 
which means $T(n) \leq c * log_5(n)$. Using the change of base formula ($ log_a(b) = \frac{log_c(b)}{log_c(a)} $)
we can change $log_5(n)$. So, $log_5(n) = \frac{log_2(n)}{log_2(5)}$. Now we have 
$T(n) \leq c * \frac{log_2(n)}{log_2(5)}$. Since $log_2(5)$ is a constant value we can
combine it with the c, which leaves us with $T(n) \leq c * log_2(n)$. 

Show that $log_5(n)$ is equivalent to $log_2(n)$: <br>
Let T(n) be equal to anything that makes the big O definition true and $f(n) = log_2(n)$.
Now if we suppose this is true, then $T(n) \in O(log_2(n))$ for some value of c and $n_0$,
which means $T(n) \leq c * log_2(n)$. Using the change of base formula (mentioned above)
we change $log_2(n)$. So, $log_2(n) = \frac{log_5(n)}{log_5(2)}$. Now we have
$T(n) \leq c * \frac{log_5(n)}{log_5(2)}$. Since $log_5(2) is also a constant value we can
combine it with the c, which leaves us with $T(n) \leq c * log_5(n)$.

This shows that $log_2(n)$ can be transformed into $log_5(n)$ and vice versa with a constant value
of difference, which we know that constants don't impact the asymptotic complexity. Therefore, the log base
does not affect the asymptotic complexity of an algorithm as changing the base will still lead to a log(n)
asymptotic complexity.

