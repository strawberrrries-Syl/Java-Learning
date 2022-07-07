# Big-O notation(bounds) （$O(n)$）
Let n be size of programs `input`.
Let T(n) ne function. e.g. running time
Let f(n) be another function. 

**FORMALLY** O(f(n)) is set of all functions T(n) that satisfy: There exist positive constants c and N such that, for all n >= N, T(n) <= cf(n).

给method一个上限(boundary), constant部分一般不表示出来（为了简化表达）。

* Big-Oh is UPPERBOUND ONLY. 
Algorithm is fast rather than is slow.

算时间复杂度时，取最大次方。

* Big-Oh notation is usually used to indicate the dominating(fastest-growing) term.

# Table of Important Big-Oh Sets.
smallerst to largets
```
Function    ||  common name    ||  Example
O(1)            constant                    
C O(log n)      logarithmic        Binary search
C O(log^2 n)    log-squared
C O(sqrt(n))    root-n
C O(n)          linear
C O(n log n)
C O(n^2)        quadratic
C O(n^3)        cubic
C O(n^4)        quartic
C O(2^n)        exponential
C O(e^n)        exponential
                (more so)
C O(n!)
C O(n^n)

```

* O(nlogn) or faster time considered "efficient".
* n^7 or slower time considered useless.

* Logorithms -> `换底公式` 等与log相关的知识

# $\Omega(f(n))$
$\Omega(f(n))$ is the set of all functions that satisfy: There exist positive constants d&N such that, for all n >= N, T(n) >= d f(n).
下限boundary.  Lower Bound on a function.

# $\Theta(f(n))$
既是上限也是下限。（常数可能不同）

 






