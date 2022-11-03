---
title: 'Essays on Philosophy of Cognitive Science'
date: 2222-10-30
permalink: /whatnot/2022/phil_of_cogsci/
tags:
  - cognitive science
  - course essays
---

*These are the weekly quizzes for the COGS517 Philosophy of Cognitive Science course I took during the Fall 2022 semester.*

1. [Is "autonomous" same as "automated"?](/whatnot/2022/phil_of_cogsci/#autonomy)
2. [Back up.](/whatnot/2022/phil_of_cogsci/#tt_cra_other_minds)

---

## <a id="autonomy"></a> Is "autonomous" same as "automated"?

First of all, I have to say that for all practical or everyday cases I can imagine, these two words seem to be synonymous: Both kinds of autonomy convey the meaning of a possibly complex process being performed independent of an external agent's interference or control. For sufficiently complex tasks I imagine both entail implementing some sort of auto-correction upon error detection, modelling of the environment and planning on that model, and much more. I have to admit my reluctance in positing the existence of a representation, though. After all, the falling of water at a water flow seems to occur autonomously at face value, while I find it questionable that there is a representation there at all.<sup><a id="footnotemark1_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext1_1">1</a></sup> So, I make no distinction between these two terms in terms of the existence of representation. Both may or may not have it, as far as I am concerned here.

When we probe the two words further and *look* for differences, however, I find that "automated" seems to suggest an "automator," while "autonomous" implies no such agent. Following this distinction, what is automated is inevitably conceptually dependent on its automator, as it is this automator that designs the automated. The input-output relations of the automation process or the internal state transitions are determined by this external agent, who itself must be able to compute and evaluate such decisions beforehand. If the automated has (internal) representations, it is the automator who puts them there. The validity and fitness of these representations are entirely dependent on them, which relieves the automated from accounting for its performance. Even when we are talking about a (machine/reinforcement/artificial) learning agent, what it learns, the rules it finds or the representations it develops cannot go outside the boundaries or the meta-rules its designer imposes. The complexity or performance in behaviour and autonomy of the automated can be considered illusory or misplaced, because it is not really the automated that possesses such qualities, it is the automator.

Putting the "autonomous" at the other side of this distinction, however, makes describing the autonomous significantly more challenging than describing the automated. Firstly, the discussion above seems to remove any sort of designer from the picture of an autonomous. How does the autonomous come to become competent in the complex task it performs? Even the constraints or the well-definition of the input-output relation the autonomous performs can lose their concreteness without such a designer. One way out suggested by  seems to be resorting to natural selection and evolution. According to him, the trial-and-error mechanisms of natural selection and sufficient time (in the order of thousands or millions of years) can yield "competence without comprehension," or autonomy without a higher-level designer. The matter of representation is another problem for the autonomous: If it indeed has internal representations for aspects of its environment and its internal states (meaningful to us or otherwise), how can they come to "mean" what they do, without resorting to the God card or another higher-level being? In other words, autonomous seems a natural subject to the symbol grounding problem from which the automated is exempted, through the existence of its automator.

Lastly, I would like to make a brief discussion on the computer scientist's view over these two kinds of autonomy. Taking Knuth's definition of computer science, i.e. as the study of what can be automated<sup><a id="footnotemark1_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext1_2">2</a></sup> (and I take the word "automated" here to include both kinds of autonomy), I find that the autonomous and the automated alike are subject to the computer scientist's inquiry, although with significant distinctions. Because the automated comes equipped with its automator, the computer scientist's empirical reliance is somewhat relieved. The validity and performance of the algorithm they develop can be contrasted the automator's design criteria directly. However, without assuming the existence of a supernatural designer (like a God) or access to what can be their design process (like heresy), what is automated is almost inevitably a coder's design. This makes the study of the automated by the computer science a search for simplification, refinement or improvement. On the other hand, the solitary nature of the autonomous challenges the empirical needs of the computer scientist: No designer, no access to internal state transition or even the guarantee of them and even no well-defined target problem with any description of desirable outputs to possible inputs. The computer scientist is left to their own devices in narrowing down and solidifying the scope of all of these open questions in the case of the autonomous. The tests of performance of any candidate algorithm/hypothesis must be based on the assumption that the observed inputs and outputs are sufficient in this assessment.

### Notes

1. <a id="footnotetext1_1"></a> I suspect this debate will lead the way to "nature computes" type of arguments, but more in a "nature represents" way. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark1_1)
2. <a id="footnotetext1_2"></a> While we talked as if this is Knuth's definition in class, I discovered that in fact Knuth is quoting George E. Forsythe, who wrote about the central questions of computer science. See Knuth (1974, p. 323) for the quote.  [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark1_2)

*Post-Script Note: I only added the Knuth (1974) reference as I discovered that later.* 

### References

Dennett, D. C. (2018). *From Bacteria to Bach and Back: The Evolution of Minds.* Penguin Books.

Knuth, D. E. (1974). Computer Science and its Relation to Mathematics. _The American Mathematical Monthly_, _81_(4), 323-343.

---

## <a id="tt_cra_other_minds"></a> Turing Tests and Chinese Rooms for Other Minds

Before attempting to adapt the Turing Test and the Chinese Room to meaning-bearing minds possibly other than humans', I find it important to clarify what we take these experiments to be. This will allow me and the reader to judge the accuracy of the adaptation and whether the hypothesis tested by the original test is still tested in the adaptation, or what the new hypothesis tested is.

### Notes

1. <a id="footnotetext2_1"></a>  [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark2_1)
2. <a id="footnotetext2_2"></a>  [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark2_2)

### References

Dennett, D. C. (2016). Çince odası. In O. Karakaş (Trans.), *Sezgi Pompaları ve Diğer Düşünme Aletleri* (p. 302). Alfa Yayınları.

Hofstadter, D. R., & Dennett, D. C. (2010). *The Mind's I: Fantasies and Reflections on Self and Soul.* Basic Books.

Searle, J. R. (1980). Minds, brains, and programs. *Behavioral and Brain Sciences, 3* (3), 417-424.

Turing, A. M. (1950, 10). Computing Machinery and Intelligence. *Mind*, LIX(236), 433-460. doi: 10.1093/mind/LIX.236.433