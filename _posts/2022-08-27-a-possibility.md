---
title: 'A Scenario of Incompleteness'
date: 2022-08-27
permalink: /whatnot/2022/a_scenario_of_incompleteness/
tags:
  - philosophy
---

## Introduction

There is this possibility that I find intriguing regarding the explanatory power a scientific models holds on the problems regarding the human mind-brain. I think I can say without any citation or reference that we do not currently have a theory that can provide a unanimously satisfactory account of various aspects of interest such as consciousness, let alone a comprehensive one. Many theories and models exist each with their own strengths and deficits<sup><a id="footnotemark1" href="/whatnot/2022/a_scenario_of_incompleteness/#footnotetext1">1</a></sup>, but not one (as far as I am aware) that roots --

To best illustrate the possibility that I am entertaining, I would first like to tell two stories, one about one of the most elementary results in analysis that a mathematics undergrad student learns and one of my own concoction, about two curious assistants of stage magic. I hope to then use these two as a base in telling a third story that entertains a certain possibility. But before I start, I would like to stress one thing: This is not me making any claims regarding the current state of consciousness science/neuroscience/even science in general, nor me coming to philosophical conclusions regarding the epistemic accessibility of the questions regarding the human mind-brain. I just aim to throw some *what-if*s because I think the possibility is entertaining to, well, entertain.

## Three Stories of Incompleteness

### Of Rational Numbers

In the field of mathematics called analysis, a frequently encountered question is convergence. It provides the answer to the famous seemingly confusing problem of whether $1 = 0.\bar 9$ (and let's try to settle that discussion, too, while we're at it). What is meant by $0. \bar 9$ is actually the following sum:

$$
0. \bar 9 = \sum_{k = 1}^\infty \frac{9}{10^k}
$$

The problematic part of this expression is the infinity: How do you sum infinitely many numbers? What does that even mean? Had it been a *finite* sum, then we would be all good, everything would be well defined, so let's try building a solution on top of them. We construct a partial sums series, given as follows:

$$
S_n = \sum_{k = 1}^n \frac{9}{10^k}
$$

Notice how the upper limit of the sum are all $n\in \mathbb N$, so are all finite instead of infinite. Thus, the elements of this sequence (i.e. finite sums) are all well defined, going $0.9$, $0.99$, $0.999$, $0.9999$ and so on. It is clear that the infinite sum that we are after (that is equal to $0. \bar 9$) is the limit of this sequence. A remark here: What we are after is *the limit*, and it need not be an element occurring in the sequence itself. 

To our luck, the elements of this partial sum sequence can also be expressed analytically in another form with some algebraic manipulations through the geometric sum formula:

$$
S_n = \sum_{k = 1}^n \frac{9}{10^k} = \frac{9}{10} \sum_{k = 0}^{n-1} \frac{1}{10^k} = \frac{9}{10} \frac{1 - \frac{1}{10^n}}{1 - \frac{1}{10}} = 1 - \frac{1}{10^n}
$$

This shows evidently that the elements of the sequence get closer and closer to $1$, which is actually the definition of convergence. Somewhat more formally, a sequence $a_n$ is said to converge to the limit $L$ if the absolute difference between the elements of the sequence and $L$, namely $\lvert a_n - L\rvert$ can be made arbitrarily small if you go far enough.<sup><a id="footnotemark2" href="/whatnot/2022/a_scenario_of_incompleteness/#footnotetext2">2</a></sup> And therefore we conclude that the limit of the partial sum sequence $S_n$ is (exactly) $1$.

This was one of the most harmless cases. What should we do about the following one: Is it a convergent infinite sum?

$$
\sum_{k = 1}\frac{1}{k^2} = \frac{1} + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \dots
$$

Before skipping to the answer, let's try to be clever and see whether we can work our way from the previous example. If we stare at it long enough, we would notice that the terms we are adding get smaller and smaller with increasing $N$, furthermore they get closer and closer together. In fact, we can make the difference between different partial sums $S_n$ and $S_m$ as close to one another as we please. In a more formal notation, for any $\varepsilon > 0$, we can find an index $N \in \mathbb N$ such that $n,m > N$ implies $\lvert S_n - S_m \rvert < \varepsilon$. Such a sequence is called a *Cauchy sequence* after the mathematician [Augustin-Louis Cauchy](https://www.wikiwand.com/en/Augustin-Louis_Cauchy). The partial sum sequences of both of the above infinite sums are Cauchy sequences, and we already know that the first one is convergent. Then what about the second sum?

At the first glance, it seems like if a sequence is Cauchy, then it must be convergent to *some* number: The partial sums sequences have smaller and smaller differences in between them, and eventually this difference has to "die out" so that the sequence may reach somewhere, right? There is an important question to ask at this point though: Convergent *where?* And "where" as in in which set.<sup><a id="footnotemark3" href="/whatnot/2022/a_scenario_of_incompleteness/#footnotetext3">3</a></sup> In the first case, the summands of the infinite sum $\sum_{k = 1}^n \frac{9}{10^k}$ were all rational numbers (real, too, but let's restrict ourselves to the smallest possible set for now), and the result $1$ of the infinite sum was again a rational number, so everything seems fine.

This is another convergent sum, and without going into [details](https://www.wikiwand.com/en/Basel_problem), here is its limit:

$$
\sum_{k = 1}\frac{1}{k^2} = 1 + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \dots = \frac{\pi^2}{6}
$$

Now there are several interesting remarks that can be made regarding this sum (Where did $\pi$ come from to a sum of rational numbers? Why is it squared? How does any of this make sense? What?), but I would like to focus on one of them: The summands are all rational numbers yet the limit is an irrational number. This means that the partial sum sequence, which is necessarily a rational sequence as it is composed of finite sums of rational numbers, gets closer and closer to an irrational number.


### Of Stage Magic

### Of Theories of Consciousness

## Interlude

## The Cost of Completion

### Of Rational Numbers

### Of Stage Magic

### Of Theories of Consciousness

## Non-Conclusion

## Notes

1. <a id="footnotetext1"></a> See Seth (2007) for a summary. [Back up.](/whatnot/2022/a_scenario_of_incompleteness/#footnotemark1)
2. <a id="footnotetext2"></a> Even more rigour: A sequence $a_n$ is said to converge to $L$ if for all $\varepsilon > 0$ there exists an index $N\in \mathbb N$ such that
   
   $$
   m > N \quad \Rightarrow \quad \lvert a_m - L \rvert < \varepsilon
   $$

   [Back up.](/whatnot/2022/a_scenario_of_incompleteness/#footnotemark2) 
3. <a id="footnotetext3"></a> Even more rigour: I should say in which metric space to be precise, but I gloss over that so that I don't have to make another definition. If you're interested, and easy definition of a metric space is a set, say $X$, equipped with a sense of distance between its elements, given by its non-negative real-valued metric function $d:X \times X \to \R^+ \cup \{0\}$. [Back up.](/whatnot/2022/a_scenario_of_incompleteness/#footnotemark3) 

<!-- 1. <a id="footnotetext1"></a>  [Back up.](/whatnot/2022/a_scenario_of_incompleteness/#footnotemark1) 
<sup><a id="footnotemark1" href="/whatnot/2022/a_scenario_of_incompleteness/#footnotetext1">1</a></sup> -->

## References

Seth, A. (2007). Models of consciousness. Scholarpedia. 2(1):1328. Retrieved August 29, 2022, from http://www.scholarpedia.org/article/Models_of_consciousness 