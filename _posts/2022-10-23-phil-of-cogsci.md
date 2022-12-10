---
title: 'Essays on Philosophy of Cognitive Science'
date: 2022-12-10
permalink: /whatnot/2022/phil_of_cogsci/
tags:
  - philosophy of mind
  - cognitive science
  - course essays
---

*These are the weekly quizzes for the COGS517 Philosophy of Cognitive Science course I took during the Fall 2022 semester. They are relatively short (2-3 A4 sheets at most), so I decided to gather them in a single post as I write them. They are in chronological order, and as the course progresses they -more or less- follow a certain progression of topics and questions. While they start off heavily philosophy of mind centric, I expect them to turn more to the philosophy of cognitive science each week.*

1. [Is "autonomous" Same as "automated"?](/whatnot/2022/phil_of_cogsci/#autonomy)
2. [Turing Tests and Chinese Rooms for Other Minds](/whatnot/2022/phil_of_cogsci/#tt_cra_other_minds)
3. [Type 1 Theory of "Mind"](/whatnot/2022/phil_of_cogsci/#type2_mind)
4. [Tug-of-Mind](/whatnot/2022/phil_of_cogsci/#tug_of_mind)
5. [What Is It Like To Be In The Chinese Room?](/whatnot/2022/phil_of_cogsci/#wil_cra)
6. [Theory Type of Computational Neuroscience](/whatnot/2022/phil_of_cogsci/#cogsneuro_type)
7. [Intentional Stance and the Computer Metaphor](/whatnot/2022/phil_of_cogsci/#intentional_metaphor)

---

## <a id="autonomy"></a> Is "autonomous" the Same as "automated"?

First of all, I have to say that for all practical or everyday cases I can imagine, these two words seem to be synonymous: Both kinds of autonomy convey the meaning of a possibly complex process being performed independent of an external agent's interference or control. For sufficiently complex tasks I imagine both entail implementing some sort of auto-correction upon error detection, modelling of the environment and planning on that model, and much more. I have to admit my reluctance in positing the existence of a representation, though. After all, the falling of water at a water flow seems to occur autonomously at face value, while I find it questionable that there is a representation there at all.<sup><a id="footnotemark1_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext1_1">1</a></sup> So, I make no distinction between these two terms in terms of the existence of representation. Both may or may not have it, as far as I am concerned here.

When we probe the two words further and *look* for differences, however, I find that "automated" seems to suggest an "automator," while "autonomous" implies no such agent. Following this distinction, what is automated is inevitably conceptually dependent on its automator, as it is this automator that designs the automated. The input-output relations of the automation process or the internal state transitions are determined by this external agent, who itself must be able to compute and evaluate such decisions beforehand. If the automated has (internal) representations, it is the automator who puts them there. The validity and fitness of these representations are entirely dependent on them, which relieves the automated from accounting for its performance. Even when we are talking about a (machine/reinforcement/artificial) learning agent, what it learns, the rules it finds or the representations it develops cannot go outside the boundaries or the meta-rules its designer imposes. The complexity or performance in behaviour and autonomy of the automated can be considered illusory or misplaced, because it is not really the automated that possesses such qualities, it is the automator.

Putting the "autonomous" at the other side of this distinction, however, makes describing the autonomous significantly more challenging than describing the automated. Firstly, the discussion above seems to remove any sort of designer from the picture of an autonomous. How does the autonomous come to become competent in the complex task it performs? Even the constraints or the well-definition of the input-output relation the autonomous performs can lose their concreteness without such a designer. One way out suggested by Dennett (2018) seems to be resorting to natural selection and evolution. According to him, the trial-and-error mechanisms of natural selection and sufficient time (in the order of thousands or millions of years) can yield "competence without comprehension," or autonomy without a higher-level designer. The matter of representation is another problem for the autonomous: If it indeed has internal representations for aspects of its environment and its internal states (meaningful to us or otherwise), how can they come to "mean" what they do, without resorting to the God card or another higher-level being? In other words, autonomous seems a natural subject to the symbol grounding problem from which the automated is exempted, through the existence of its automator.

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

**The Turing Test** is the easier one to deal with among the two, as I find Turing (1950) makes its conditions rather explicit. A human questions a computer (program) and a human subject with the only means of communication with both of them being a textual medium. Both the computer and the human subject try to convince the questioner that they are human and the other is a computer through the answers they give to the questioner. In this summary, while the properties of the communication medium may seem irrelevant to the test, at least the delivery speed of the messages turns out to be of importance: While a computer can multiply large numbers in split seconds, an average human takes significantly longer.<sup><a id="footnotemark2_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext2_1">1</a></sup> Therefore if the two are communicating with pigeon messengers, the questioner will find it impossible to judge how long each side took to perform such a calculation and will not be able to use a criterion otherwise available. In light of this observation, here are the ingredients to a Turing Test:

- *Questioner,* a human who performs the test by asking questions.
- *Questionees,* one human and one computer (program) who are tested via their answers to the Questioner's questions.
- *Communication Medium,* a reliable and fast (let's say with no delay) textual medium that is the only means of passing questions and answers between the Questioner and Questionees.
- *Decision Criterion:* If the Questioner cannot confidently identify the Questionees as human and computer, the computer (program) is said to have passed the Turing test.

**The Chinese Room** thought experiment is more elusive to pin down than the Turing Test is. As pointed out by Hofstadter and Dennett (2010), Searle glosses over important details by appealing to intuition and innocent yet strong suppositions to make his point. However, my goal here is not to discuss the validity of the thought experiment, therefore I will take it as it is given by Searle (1980) with as much fidelity as possible: A human subject $S_1$ who knows language $L_1$ is located in a room with an instruction manual in $L_1$ that contains correlational rules between language $L_1$ and language $L_2$, which the subject does not speak or understand its alphabet. To $S_1$, the letters of $L_2$ are mere squiggles. Another subject $S_2$ who speaks $L_2$ passes written questions into the room. $S_1$ then analyses the written note with the help of the manual and cooks up an answer in $L_2$ that they themselves (supposedly) do not understand. A cornerstone supposition in this setup is that the manual on its own can pass the Turing Test,<sup><a id="footnotemark2_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext2_2">2</a></sup> so it can be taken as the written instructions to an artificial intelligence program; "Strong AI" in Searle's words.  Searle then proceeds with his conclusions, but this is enough for me now to list the following ingredients:

- *Two languages, $L_1$ and $L_2$,* that are significantly minimal overlap (e.g. in their alphabet) to prevent any "linguistic leakage" of meaning.
- *Two subjects, $S_1$ inside the room and $S_2$ outside,* who speak $L_1$ and $L_2$, respectively.<sup><a id="footnotemark2_3" href="/whatnot/2022/phil_of_cogsci/#footnotetext2_3">3</a></sup>
- *Manual that passes the Turing Test,* in $L_1$ that serves to take in questions in $L_2$ and generate an appropriate answer.
- *Communication Medium,* a written, reliable and reasonably fast that is the only means of communication between $S_1$ and $S_2$.

What I found most interesting through the above analysis is that both require one or more language(s) that provide(s) the ground for the evaluation of the test/experiment. A failure case is equivalent to ineptitude in the use of that one language, in comprehension or production. Furthermore, a written form of that language is also required to block unwanted communication. Although the underlying assumption these imply, that is the written language can provide sufficient proof of the adept use of that language in general and hence indicate the existence of a meaning-bearing mind, is rather interesting to me. This is because not even all human languages have written forms, and to what extent the written form of a language can represent its oral form is debatable.<sup><a id="footnotemark2_4" href="/whatnot/2022/phil_of_cogsci/#footnotetext2_4">4</a></sup> More so, a hypothetical mind that does not use *any* language (written and oral alike) to communicate with other members is also outside the boundaries of these thought experiments. That only leaves room for dialects of Mentalese, i.e. languages that are privy to each meaning-bearing yet solitary mind. I find it dubious that such minds can even exist or are discoverable even if they do, so I do not consider that case with comfort. Therefore further on, I will assume that a meaning-bearing mind uses a language in any form (sound waves, electromagnetic waves, etc.) that can be transcribed through a fixed set of written symbols (alphabet). And with these ingredients in mind, I can attempt to adapt the thought experiments to other meaning-bearing minds.

**The Turing Test** then has to be adapted first since the Chinese Room depends on it, and I find it rather easy to adapt. Simply the human is replaced with the other meaning-bearing mind (bird, Martian, etc.), and the pieces work together in the same way as before. Let's take it to be a Martian bird. Then The Martian-Bird Turing Test works as follows: A Questioner Martian Bird Martian-tweets questions that are passed to the Questionees computer and another Martian Bird. The computer and Martian Bird try to convince the Questioner that they are the true Martian Bird and the other is the computer. If the Questioner Martian Bird cannot reliably/confidently decide which is which, the computer passes the Martian Bird Turing test.

While this adaptation was rather easy, it makes no prediction on the possibility of success or failure for different species as it should, just like the original one. That is, even if we knew the Turing Test could be succeeded by a computer programmed to speak an arbitrary human language, we could not tell whether we could have a similar guarantee for another meaning-bearing mind. This implies the following scenario: Let's say we organise a universe-wide Turing Test festival and run the Turing Test (their adaptations) with all the different kinds of meaning-bearing entities from across the universe. Since anything computable can be computed by a Universal Turing Machine, we can comfortably take the computers in all of these tests to be the same hardware of sufficient capacity (memory, computational speed, etc.), although programmed differently to accommodate the necessary linguistic and semantic processing. What if it turns out that with the right computer program per species, one subset of meaning-bearing Questioners consistently identify the computer while others cannot? In other words, what if it turns out that the same hardware that consistently passes the Turing Test for certain kinds of meaning-bearing entities *fails* to do so for others? Would that imply a natural hierarchy between such meaning-bearing minds, say into "Turing-reducible" and "Turing-irreducible"? Would this be a binary classification or a spectrum between the two? I make no claim as to whether this possibility is a viable one, but I find it an interesting one.

**The Chinese Room** is adapted similarly under the assumption that the meaning-bearing minds use transcribable languages: Let's say a Martian Sparrow ($S_1$) that speaks Martian Sparrowese ($L_1$) is located in an isolated cage, together with a manual in Martian Sparrowish that correlates Martian Sparrowish with Martian Pigeonese ($L_2$, which is significantly different from Martian Sparrowish $L_1$) and serves to generate responses in Martian Pigeonese. Similar to our human case, we assume the manual passes the appropriate Turing Test. A Martian Pigeon ($S_2$) then passes written questions into the cage, the Martian Sparrow generates an answer via the manual and passes the answer back. Therefore the Chinese Room in this case becomes a (Martian) Pigeonese Cage quite easily.

The strategy I followed in making these adaptations was keeping the test or experiment species-specific. The goal of the Questioner in the Turing Test is to identify a computer from a subject of the same species who even speaks the same language. The Chinese Room stands differently than the Turing Test in that regard: It relies on the difference in languages and the lack of understanding of the subject in the room caused by it. Therefore I find the idea of a Chinese Room with an Martian Sparrow inside and a Chinese human outside just as reasonable, and it is no different than a Pigeonese Cage with a Martian Pigeon outside and an English person inside. I find the backbone of the thought experiment, that is the fact that the manual passes the appropriate Turing Test, remains intact in all cases. The subsidiary assumption that this manual can be written not in the language it passes the Turing Test but in another seems less critical.

### Notes

1. <a id="footnotetext2_1"></a> Turing mentions the delay can be mimicked by the computer, but I am taking precautions against possible questions that create a difference in reaction times. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark2_1)
2. <a id="footnotetext2_2"></a> I admit that I have not read the full target paper and its subsequent discussions. And since I have not seen the passage of Turing Test as a condition of the experiment in Searle's original article, I decided to take the version depicted by Dennett (2016) as a reliable summary. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark2_2)
3. <a id="footnotetext2_3"></a> Nothing in principle prevents the outside inquisitor $S_2$ from knowing $L_1$, but let's keep the matters simple. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark2_3)
4. <a id="footnotetext2_4"></a> This is important, since if the language cannot be transcribed, both thought experiments lose an important component that is the communication medium. Similarly, a subject that cannot write is useless in these experimental setups, but that is resolved quite easily with a mental reemployment of another subject more suitable for the job. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark2_4)

*Post-Script Note: I admit I originally wrote and submitted this one in a rush, so I noticed quite a number of grammar mistakes and typos while posting it here. I only fixed those in the essay. On the other hand, I was also surprised how I took the phrase "meaning-bearing mind" without questioning (it was given in the question text), and I think it is a term worth thinking on. Maybe later.*

### References

Dennett, D. C. (2016). Çince odası. In O. Karakaş (Trans.), *Sezgi Pompaları ve Diğer Düşünme Aletleri* (p. 302). Alfa Yayınları.

Hofstadter, D. R., & Dennett, D. C. (2010). *The Mind's I: Fantasies and Reflections on Self and Soul.* Basic Books.

Searle, J. R. (1980). Minds, brains, and programs. *Behavioral and Brain Sciences, 3* (3), 417-424.

Turing, A. M. (1950, 10). Computing Machinery and Intelligence. *Mind*, LIX(236), 433-460. doi: 10.1093/mind/LIX.236.433

---

## <a id="type2_mind"></a> Type 1 Theory of "Mind"

In his essay, Marr (1977) defines two classes of explanatory theories that could be provided to a problem in artificial intelligence: 

**Type 1** theories constitute a dichotomy of abstract and physical levels. The abstract level, in Marr's words, provides the "computational theory" behind the problem and defines **what** is being computed, as in what sort of abstract quantities are required to solve the problem (e.g. entropy, time, intensity, etc.), and **why** such quantities are computed, as in the goal of an intelligent agent in solving the problem of interest and how they are supposed to be related (e.g. maximize the entropy, perform in minimal time, detect sufficient input intensity, etc.). On the other hand, the physical level defines the specific implementation details and answers **how** the quantities and mechanisms defined by the abstract level are being realized physically (e.g. by neurons, transistors, domino pieces<sup><a id="footnotemark3_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext3_1">1</a></sup>, etc.).

**Type 2** theories are predominantly described by the lack of a structure that Type 1 theories possess. If the scientist cannot identify the abstract constituents of the problem and the mechanisms in between, the only remaining choice is to make do with an already existing solution that they cannot analyse at no level beyond the physical implementation. To Marr, this is a clear indication of the lack of sufficient understanding of the solution underlying the problem: The inability to "abstract away" the physical.

Before discussing the possibility of a Type 1 theory of the/a mind, I would like to evaluate this classification. Marr makes it clear that he sees the true solution to the problem even in a Type 1 theory as residing at the abstract level, and conversely, he sees the lack thereof as the absence of a well-understood theory. This is a clear indication of his functional lenience, with implications for the multiple realizability of the solution with different physical media (Levin, 2021). This makes Marr's classification subject to attacks on functionalism in general. 

An attack that exemplifies those on functionalism (or one of a similar spirit) on the possibility of a Type 1 theory of mind, I believe would come from Searle: If the mind were to have a Type 1 theory, it would be multiply realizable by more than one physical medium, likely those other than biological, as long as they complied with the **what**s and **why**s dictated by the abstract level. Searle would object by claiming intentionality is a biological property (Searle, 1980), and hence would conclude that such a theory cannot exist.

On the other hand, I find it difficult to locate where Turing would stand. His test can only identify intelligence in behaviouristic terms,<sup><a id="footnotemark3_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext3_2">2</a></sup> so it seems to suggest if a computer walks like a mind and quacks like a mind, it must be mind without checking whether it is filled with air, transistors, or neurons. In Marr's words, the computer passing the Turing Test might just as well be realized "by the simultaneous action of a considerable number of processes, *whose interaction is its own simplest description*" (Marr, 1977), therefore being a Type 2 theory. On the other hand, it is not difficult to imagine a computer realizing a Type 1 theory of a mind if it exists. So, the Turing Test does not distinguish between theories of different types, so long as they act like a mind.

My general standing on the matter relies heavily on a remark made by Marr: That Type 1 and Type 2 distinction is not a binary classification, but mere identification of the two extremes of a spectrum (Marr, 1977, footnote 3), and that even Type 1 theories can consist (and most likely *do* consist) of several intermediate Type 2 theories (Marr, 1977, p.40). With this remark as a cornerstone, I can imagine a Swiss cheese Type 1 theory of "mind" with Type 2 holes emerging one day. The Swiss cheese analogy is critical in the sense that the holes are what characterize the theory (the cheese). The Type 1 theory builds on the many aspects of the mind that are explicated only through Type 2 theories. So, calling them holes is in a sense discrediting them, implying as if they nibble away from the substance of the theory. Calling them the *postulates* of the overarching Type 1 theory would be more suitable: They are taken for what they are as a single module to be used with others to<sup><a id="footnotemark3_3" href="/whatnot/2022/phil_of_cogsci/#footnotetext3_3">3</a></sup>.

I find this similar to Hofstadter's idea that the mind could be understood in terms of a hierarchy<sup><a id="footnotemark3_4" href="/whatnot/2022/phil_of_cogsci/#footnotetext3_4">4</a></sup> of levels, each of which building on the other yet still being isolated in their explanations (1999). Hofstadter claims that a reductionistic explanation of the mind could exist in principle (in fact he is sure of it), yet it would be incomprehensible as it would necessarily be extremely far from our vocabulary of explanations. To comprehend such a theory, it is necessary to introduce levels built of objects made out of those on the lower levels yet whose interactions lose meaning once you go down. In this hierarchy of levels, I imagine the theory making more "familiar" sense (as in becoming comprehensible) as you go up, becoming more Type 1, and making more "unfamiliar" sense as you go down, becoming more Type 2. The level of abstraction and hence that of understanding is therefore found on the higher levels, but they are nothing but sensible modularizations of lower Type 2 theories. 

In other words, each of these modules' internal explanation as to how it comes to be such and such and solve the (sub)problem it is assigned is made by nothing less than the "simultaneous action of a considerable number of processes, *whose interaction is its own simplest description*" as Marr says. Once they are modularized, they become **what**s obeying the **why**s of a Type 1 theory, **how**ever they are realized. The type of a theory relies on the perspective. I would like to imagine Hofstadter would find the following (inverted) pictorial summary of my point entertaining.

<p float="left" align="middle">
    <img src="/images/phil_of_cogsci/oneTwo.png" width="35%" />
    <br> <em size="-2">Figure 1: Looking at the blacks, the theory is Type 2. Looking at the white, the theory is Type 1. Inverted Swiss cheese. </em>
</p>

### Notes

1. <a id="footnotetext3_1"></a> Parker (2014) constructs a binary adder with domino pieces by first constructing the necessary logic gates. The problem is that it only works once as the domino pieces are down in the end and the whole system has to be reset. This implies that the medium of domino pieces can host a UTM in principle, and if we can indeed simulate a mind on a computer (hence a UTM), we can also do it with domino pieces. That mind, although, would only think *once*. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark3_1)
2. <a id="footnotetext3_2"></a> I tiptoe away from what another way might be. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark3_2)
3. <a id="footnotetext3_3"></a> Funnily enough, I find this look on these Type 2 components similar to abstracting away from them. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark3_3)
4. <a id="footnotetext3_4"></a> Tangled Hierarchy in Hofstadter's words. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark3_4)

### References

Hofstadter, D. R. (1999). Strange Loops, Or Tangled Hierarchies. In *Gödel, Escher, Bach: An Eternal Golden Braid* (p. 708–709). Basic Books.

Levin, J. (2021). Functionalism. In E. N. Zalta (Ed.), *The Stanford encyclopedia of philosophy* (Winter 2021 ed.). Metaphysics Research Lab, Stanford University. https://plato.stanford.edu/archives/win2021/entries/functionalism/.

Marr, D. (1977, 8). Artificial Intelligence — A Personal View. *Artificial Intelligence, 9* , 37-48. doi:10.1016/0004-3702(77)90013-3

Parker, M. (2014, 4). *The 10,000 Domino Computer - Youtube*. Retrieved from https://www.youtube.com/watch?v=OpLU__bhu2

Searle, J. R. (1980). Minds, Brains, and Programs. *Behavioral and Brain Sciences, 3* (3), 424.3

---

## <a id="tug_of_mind"></a> Tug-of-Mind

When we talk about what the mind is, there seem to be two pathways one can take based on the discussions we had in the first week. One natural way of defining what the mind is is to take it from its most prominent possessors, the humans. This way, "mind" is taken as something solely the humans possess, implemented via their brain -- or their nervous system, for the sake of generality. This is in short what the mind-brain identity theory says (Kim, 2011b), that the mental processes are exactly brain processes. Along this line of thinking, the study of the mind becomes naturally the study of the brain, and so cognitive neuroscience would come to encompass cognitive science. The goal of the cognitive scientist -as a side to the cognitive neuroscientists- could become the analysis of the biological processes as discovered by the neuroscientist -- if that isn't already the job of the cognitive neuroscientist. The theories developed would not go beyond explanations of the biological, which means that any simulation of the mind processes would necessarily be simulations of (specific) biological processes. Since in this case, the jobs of the cognitive scientist and the cognitive *neuro*scientist are concurrent and inherently have the same object of inquiry, they should be concurring on any method of going about the business. Study the brain processes, whatever they are.

To most, including myself, this does not feel like a very natural way of understanding the mind. Let's go about a quick thought experiment to illustrate this point. Let's take a cognitive scientist with the above job description, with the usual funding of a thought experiment, i.e. sufficiently large (yet finite<sup><a id="footnotemark4_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext4_1">1</a></sup>) computational resources. If they were to simulate a mind process, the mind-ness of which is due to the fact that is grounded on a biological process, they would in fact be implementing the mind process in question on a non-brain hardware. If the process is indeed a mental process, the workings of which are inspired or modelled after real human nervous systems, then we contradict our own initial argument that mental processes are brain processes: Clearly, the simulated mind processes have now become not-brain processes. The only way I see to evade such a conclusion is to posit that such a simulation can never be done, but I find that casts doubt on the viability of the discoveries and the method of neuroscience.

Inspired by the above thought experiment, one could say another, braver way of defining what "mind" is, that it is to take it as something that is only *exemplified* by humans, and that in principle it could be possessed by many other species, be it organic (biological) or inorganic. While it may look innocent, this is not a real way of making a definition. In the first case, the definition is rather simple: Mind processes are nothing but brain processes by definition, so the mind is their totality. What have they become now? I doubt there is a unique way of definition, but for now, let's leave it at this (as we have done in the lectures): Mind is going above data, by whatever hardware it is implemented. This can also be taken as a starting point for defining functionalism (Kim, 2011a), taking "mind" as something larger than humans and condemning the opposition before as chauvinistic due to its restriction to them.

It is now the jobs of the cognitive scientist and the cognitive *neuro*scientist can start to diverge, for it seems while the cognitive neuroscientist studies mind as implemented by the brain, the cognitive scientist studies mind *simpliciter*. What they might consider as their isolated yet complex tasks as performed by their subject matter (and abstract mind for the cognitive scientist and the human mind-brain for the cognitive neuroscientist) can diverge significantly. 

For example, a cognitive scientist might consider language to be such a basic phenomenon. They take language *simpliciter*, i.e. with its syntax, semantics and pragmatics, or as an abstract pattern with supposed rules and dynamics. They might stipulate what the grounds are for the human brains to possess language, such as Chomsky's language acquisition device, but they do not necessarily worry about biological rigour, evidence or well-definition of such stipulations. The cognitive neuroscientist focuses majorly on those latter worries: What are the neurological grounds for such claims? Are the processes implemented in a distributed manner on (say) the brain or would they have dedicated regions of implementation? What are the neural mechanisms that implement various facets of language? How have these neural mechanisms come to be? 

Conversely, a cognitive *neuro*scientist might take motion control and planning as a basic phenomenon. They would not be interested in it from, say, the control theory perspective of general motion planning. Such theories and ideas become auxiliary, meaning they only have their importance in virtue that they might be implemented by neural mechanisms. The cognitive scientist might see such a framework as overly restrictive and desire to ask higher-level questions<sup><a id="footnotemark4_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext4_2">2</a></sup>. Perhaps<sup><a id="footnotemark4_3" href="/whatnot/2022/phil_of_cogsci/#footnotetext4_3">3</a></sup> a mind does not need to move the body in the same principles as the brain does (whatever they are). They would look for these principles, an algorithm and not the specific implementation details, the significance and role of the quantities being computed in a more abstract setting than "merely the brain."

In short, what is taken as a complex-yet-basic<sup><a id="footnotemark4_4" href="/whatnot/2022/phil_of_cogsci/#footnotetext4_4">4</a></sup> task of interest might differ between the two disciplines. And this could effectively create a tug-of-war -- a tug-of-"mind": The cognitive scientist pulls the starting point towards more general or higher-level concepts such as language, planning, representation and computational principles; while the cognitive neuroscientist pulls it towards more lower-level and physical/neural concepts such as vision, sensorimotor processes, sensorimotor integration and default mode networks. 

Such an opposition might disable a common ground  Newell’s (1973) if both disciplines were to follow his suggestion for clear reasons: They don't agree on what task to study! Cognitive science, choosing the "general mind" as its concept of interest, draws the circle of complex-yet-basic around phenomena too high-level for cognitive neuroscience. Cognitive neuroscience, on the other hand, studies the mind as implemented by the brain, and the circle of complex-yet-basic might not even come close to including the inquiries of cognitive science, and it would regard what's inside as too restricted to the human mind(brain).

But, I do think there is hope: Despite my talking about how the two disciplines could never work on the same problems, they do so all the time. I find this is possible if we take these two disciplines and their approaches as the two levels of Marr (1977): The abstract level and the physical level. Cognitive science wears the abstract level hat and tries to rise above the mind observed as performed by the brain, to generate what and why it should be computing, to better understand and formulate the problem. To this end, it must be well informed of the progress of its partner in mind, cognitive neuroscience wearing the physical level hat, as it is the one that provides the grounds and justifications for what is being implemented by the brain. The claims as to what minds are should inevitably apply to the human minds as well. This brings out the following compromise: These common grounds can effectively bring the two disciplines only in a Type 1 theory setting. 

Therefore as the cognitive scientist tries to generalize the present ideas to a general, likely unobserved and stipulated Mind with a capital M, the cognitive neuroscientist grounds them to the human mind-brain. Another compromise here is that they might not necessarily be studying their corresponding sets of complex-yet-basic phenomena. This, however, should not disturb Newell, I think, because the chess example he gives (justified with a "why not") is in neither sets. Besides, unless we study the two studies intersect, I imagine the development of a unified understanding of the mind as Newell desires would become far more difficult to achieve. 

### Notes

1. <a id="footnotetext4_1"></a> I find it rather safe to impose the finiteness constraint: After all, I as a mind possessor am finite. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark4_1)
2. <a id="footnotetext4_2"></a> At this point I find myself at a lack of a satisfactory example: It seems the cognitive scientist might as well ask the same questions as the cognitive neuroscientist framed in the same way, only look for a more general answer. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark4_2)
3. <a id="footnotetext4_3"></a> A very big “perhaps” here, one that I make intentionally for the sake of an example. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark4_3)
4. <a id="footnotetext4_4"></a> The “basic” here is not in the sense of elementary or fundamental, but more of the same spirit as the chess example of Newell (1973). [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark4_4)

### References

Kim, J. (2011a). Mind as a Causal System: Causal-Theoretical Functionalism. In *Philosophy of Mind* (3rd ed.). Westview Press.

Kim, J. (2011b). Mind as the Brain: Psychoneural Identity Theory. In *Philosophy of Mind* (3rd ed.). Westview Press.

Marr, D. (1977, 8). Artificial Intelligence – A Personal View. *Artificial Intelligence*, 9 , 37-48. doi:10.1016/0004-3702(77)90013-3

Newell, A. (1973). You can’t play 20 questions with nature and win: Projective comments on the papers of this symposium.

---

## <a id="wil_cra"></a> What Is It Like To Be In The Chinese Room?

Farrell (2016) in his work provides an account of what it means for a discussion to be technical. His motivation to do so stems from a need to clarify what terms we are referring to and what claims we are making. He claims for a discussion to be (philosophically) technical, it needs to involve

- **(T)**echnical terms
- **(I)**ntroduced by philosophers with specialized
- **(M)**eanings which allow the technical discourse.

So, let's try to analyze the Chinese Room Argument (CRA) (Searle, 1980) in terms of these criteria: Its reliance on concepts such as the Turing Test, computer and program clears out the (T) criterion, as they convey very specific meanings, with some even not belonging to daily use (such as the "Turing Test"). While some of these terms are not necessarily defined by philosophers, they certainly attain certain philosophical meanings and implications, which are introduced by philosophers, so (I) and (M) are also checked. Therefore we seem to conclude that CRA is a technical discourse in the sense of Farrell.

But let's take CRA another look. The argument as told by Searle is told in the first-person, so we are implicitly invited to think *what it is like* to be Searle in the situation described. Even if the discourse was not first-person, it is not too difficult to observe that it is a `what it is like' (WIL) argument: The whole punchline of the experiment relies on the reader's empathy with the subject of the experiment inside the room. We imagine ourselves being in the room, processing strings of Chinese characters through a manual that passes the Turing Test, making conversation with an actual Chinese person outside the room yet not knowing anything about it and then are led to agree with Searle with the conclusion of the thought experiment.<sup><a id="footnotemark5_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext5_1">1</a></sup>

What to make of this contradiction? On one hand, CRA seems to satisfy the requirements of a technical discourse as defined by Farrell, yet its main mechanism is a WIL argument, which Farrell denies to be technical. 

The conundrum can be resolved by noticing that the components of CRA as analysed previously are not the usual components which are considered by Farrell in his work. In the examples he gives, the WIL situations (e.g. being a bat as in Nagel, 1974) are themselves non-technical and therefore fail to account for all three conditions posited by Farrell. In CRA, however, the WIL situation crafted by Searle is a technical one: It relies on the reader's understanding of the technical terms such as the passage of the Turing Test, human being's story-understanding capacity, and many more. And so, only because the WIL situation at hand is selected carefully, I conclude CRA is a technical argument.

Lastly, while I may have concluded it is indeed technical, I find this technicality also makes it an unappealing WIL argument. In the examples given by Farrell, the WIL situations were all very much familiar and likely have a place (or a counterpart) in the readers' lives. While this familiarity provided the convincing power of these WIL statements,<sup><a id="footnotemark5_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext5_2">2</a></sup> it pushed them out of technical discourse. The converse, I believe, applies here: While the WIL argument of CRA is technical indeed, it loses its appeal to empathy exactly because it is technical. I, for one, find it difficult to imagine using a manual written in English yet passing the Turing Test in Chinese; yet the knowledge of Chinese not dawning on me as I use it. Or, why should we treat the subject in the room as part of the program as dictated by the manual and not simply as a substrate for the manual's program to run? I believe these questions that push the argument outside the boundaries of my intuition, as well as the many loose ends pointed out by Hofstadter and Dennett (2010) which are again results of technical analyses, are a result of this technical nature. And I doubt any more technical clarification will pull it back to the reaches of my intuition.

### Notes

1. <a id="footnotetext5_1"></a> I don't find it too difficult to see that any thought experiment about consciousness such as Mary the colour scientist and the cross-wired brain are essentially WIL arguments: What is it like to be Mary? What is it like to have our brains cross-wired? Perhaps such thinking is what led Nagel to define having consciousness as having the property of there being something it is like to be that organism (1974). [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark5_1)
2. <a id="footnotetext5_2"></a> Not necessarily philosophical arguments. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark5_2)

### References

Farrell, J. (2016). `What it is Like' Talk is not Technical Talk. *Journal of Consciousness Studies, 23* (9-10), 50 -- 65.

Hofstadter, D. R., & Dennett, D. C. (2010). *The Mind's I: Fantasies and Reflections on Self and Soul.* Basic Books.

Nagel, T. (1974). What is it like to be a bat? *The Philosophical Review, 83* (4), 435 -- 450.

Searle, J. R. (1980). Minds, brains, and programs. *Behavioral and Brain Sciences, 3* (3), 417 -- 424.

---

## <a id="cogsneuro_type"></a> Theory Type of Computational Neuroscience

In their survey of methods and models in computational neuroscience, Sejnowski, Koch, and Churchland (1988) mention the Hartline-Ratliff model which can explain the Hermann grid illusion. The model says that the cells to which the photoreceptors project (which I will refer to as the projected neuron) weigh the inputs of these photoreceptors in such a way that the contrast between the center of a certain region (called the receptive field) and its borders intensifies the projected cell activity, that the increase in the photoreceptors corresponding to the border of the receptive field inhibits the cell response. This indeed provides a theoretical account for the Hermann grid illusion, a theory which we can analyze in the framework of Marr (1977).

If this is indeed a Type 1 theory, then we should be able to clearly identify the three necessary components:

- **What** quantities are being computed?
- **Why** are they computed?
- **How** is the computation realized physically?

The easiest one to clear out seems to be the *how* of the model: The synaptic connections between the projected neuron and the relevant photoreceptors implement the physical realization of the inhibition and excitation. Excitation can be seen as an additive input to cell activity (i.e. output firing rate), while inhibition can be seen as subtractive. The *what* of the model seem to be the central illumination and the outer illumination of the receptive field's border in the simplest terms,<sup><a id="footnotemark6_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext6_1">1</a></sup> two physical quantities that are represented as the firing rates of two populations of photoreceptors that we categorize. The *why* of the model, however, seems to be harder to identify. Why indeed should a problem-solving (neuro)biological system realize such a mechanism?

To better understand our lack of an answer to this final question, let's go back to the start of our analysis and make an important remark. The subtle wording implies that the Hartline-Ratliff model aimed to account for the Hermann grid illusion. This is more a phenomenon that we experience, rather than a problem the organism solves in a so-and-so manner. Our inquisition led us to an account of the Hermann grid illusion, one that can even be realized in different physical substrates, but not the problem it solves. Defining the *why* of our model as ``to account for the Hermann grid illusion'' is a solution but a non-productive one, there is always the question of why any biological system would aim to implement it. Why should the neural image be constructed in this way?

While I suspect there may be an actual problem this Hartline-Ratliff model solves, one that I am unaware of, I am more interested in leaving this last piece of the puzzle lacking.<sup><a id="footnotemark6_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext6_2">2</a></sup> Since we can't complete our Type 1 picture, what are we left with? Some *how*s and *what*s, but no *why*. Should we discard our model for its lack of a computational problem it solves? This seems counterproductive, as the model clearly accounts for an observed phenomenon, serves to make predictions about it and even guides the way for different physical realizations for artificial systems to replicate the same phenomena; it is certainly not useless. 

On the other hand, recalling that Marr defines a Type 2 theory primarily by the lack of structure as in Type 1, should we label this theory as Type 2? I oppose this view as well, and turn to Newell (1973) for an answer: I consider the Type 1 vs. Type 2 as a false dichotomy. While it is useful to think about models that give a clear account (Type 1) vs. those that are explained solely by the explicit interaction of their multiple components (Type 2), it is not hard to imagine a whole spectrum of models that lie in between. Models often abstract away incompletely, with various Type 2 sub-theories that implement different parts of an overarching Type 1 model. These Type 2 sub-theories serve like the axiomatic basis of a mathematical theory: We assume they come to represent *what* they are without an account for *how* or *why*, we just make a match of our observations and the big *what*s of the overall Type 1 model. Their *why*s can be taken trivially as being actors or components of overarching Type 1 theory, which is not enough for their own sake but satisfactory for the Type 1 theory. Depending on how large/small and influential these Type 2 sub-theories are within the general Type 1 theory, the whole theory can shift towards being Type 1 or Type 2. This shift reflects our understanding of the guts of the model hand, and it is not hard to imagine a ``lowest level,'' below which there are no more Type 1 but only Type 2 accounts.

Going back to our *why*-deficit<sup><a id="footnotemark6_3" href="/whatnot/2022/phil_of_cogsci/#footnotetext6_3">3</a></sup> Hartline-Ratliff model, we can take it to be as a well but not fully accounted sub-theory of a yet-to-be-determined Type 1 theory. Its current explanatory power will have to be put to sleep so that in the future we might discover 

1. either the abstract problem the lateral inhibition solves and complete it to a Type 1 theory of its own, or 
2. a more general theory in which the *what*s and *how*s of the currently incomplete theory will live in.

The crucial point will be to remain open to both possibilities and reconcile with the fact that while it may never be a full Type 1 theory on its own, it still has explanatory and predictive power that can be put the use in other theories. This would make it neither Type 1 or Type 2 *simpliciter*, but this division should not be taken for granted anyways: Only as a guiding principle, the two extremes of a spectrum.

### Notes

1. <a id="footnotetext6_1"></a> To break the binary classification of the photoreceptors as inner or outer, we can give each photoreceptor variable weights so that when the total activity of the population is multiplied with the corresponding weights, the response is obtained. This way a photoreceptor does not have to be either inner or outer, but can reside in between. However, the inner-outer distinction is enough for me, and making the distinction will not change the course of the argument. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark6_1)
2. <a id="footnotetext6_2"></a> I apologize for the anti-climactic turn. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark6_2)
2. <a id="footnotetext6_3"></a> Supposedly, at least, for the sake of argument. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark6_3)

### References

Marr, D. (1977, 8). Artificial Intelligence — A Personal View. *Artificial Intelligence, 9*, 37-48. doi: 10.1016/0004-3702(77)90013-3

Newell, A. (1973). You can’t play 20 questions with nature and win: Projective comments on the papers of this symposium.

Sejnowski, T. J., Koch, C., & Churchland, P. S. (1988). Computational Neuroscience. *Science, 241* (4871), 1299–1306.

---

## <a id="intentional_metaphor"></a> Intentional Stance and the Computer Metaphor

Before thinking of the intentional stance and the computer metaphor together, let's clarify what we mean by each of these terms to have a solid foundation.

In his article, Dennett identifies three points of view, *stances* as he calls it, towards an agent in explaining its behaviour (1971).

- **Physical stance**, where we explain the behaviour in purely physical terms. This stance relies purely on natural science theories.
- **Design stance**, where we explain the behaviour as the result of a design process with certain goals,<sup><a id="footnotemark7_1" href="/whatnot/2022/phil_of_cogsci/#footnotetext7_1">1</a></sup> constraints, inputs and outputs.
- **Intentional stance**, where we explain the behaviour in folk psychological terms, such as beliefs and desires.

These stances serve us to explain behaviour in different resolutions, with different levels of confidence and in different time scales. If<sup><a id="footnotemark7_2" href="/whatnot/2022/phil_of_cogsci/#footnotetext7_2">2</a></sup> we can assume a physical stance towards the agent with confidence, our explanations are as solid and fine as the natural sciences we rely on, but making a simple prediction would require extremely lengthy reasoning. On the design level, we abstract away from the fine grains of the physical stance and can account for the agent's behaviour (and predict it) much faster, yet we take the subtle risk of missing our physical-level disturbances and hence of making prediction errors. These errors accumulate furthermore when we assume the intentional stance and twist and cram the agent's theory into folk psychology, in the comfort of making incredibly fast predictions.

On the other, the computer metaphor refers to the likening of the workings of the mind to that of a digital computer (Searle, 1990). While some scientists do believe there is a perfect match between the two, i.e. that the mind exactly works like a digital computer,<sup><a id="footnotemark7_3" href="/whatnot/2022/phil_of_cogsci/#footnotetext7_3">3</a></sup> some cognitive scientists often implicitly adopt this assumption in its partial form. Under this metaphor, the mental states are taken to abide by a certain syntax or a computer instantiation, where the word "computer" is taken in the most abstract sense, although they can be more than simple computational states. While I will not discuss the validity of the metaphor, it suffices to say that it is a problematic point of view and not a unanimous one.

Now, in light of the three stances of Dennett and this concept of a computer metaphor: Does adopting the intentional stance avoid adopting the computer metaphor? 

I find it important to note that all three stances are only explanatory tools. One can even say that adopting one stance does not automatically come with any uniqueness or ontological claims. One can adopt the algorithmic stance in explaining a reinforcement learning agent's behaviour, with its reward functions, observations and action policies; without explicitly committing that they are the only possible explanations for the behaviour in question. Similarly, one can take the intentional stance and make predictions about the same reinforcement learning agent, claiming it believes so-and-so because it desires this-and-that, without committing explicitly to the existence of beliefs and desires. The three stances are tools of explanation, at different time scales, resolutions and reliabilities. They don't have to (but may) put forward any theory about the *actual* underlying the observed agent's behaviour.

With this observation in mind, I find it evident that the intentional stance does indeed avoid the computer metaphor, as it simply does not make any commitments regarding the *actual* theory behind the mind. In taking the intentional stance, one simply ascribes folk psychological properties to an agent without claiming it indeed possesses them and makes some predictions regarding its current and future behaviour. This has nothing to do with likening or equating the *actual* workings of the mind to that of a computer. We may even go as far as to notice that the partial equivalences of the computer metaphor, such as calling one thing the "software" or the  "hardware," don't even find a place in folk psychology, so it is only natural that the two points of view don't overlap.

Lastly, I believe the computer metaphor can find a place to live in Dennett's three stances: The design stance. Claiming that the mind works like a digital computer instantiation, with mental states likened to computer states, the algorithmic stance can be taken to analyze the mind. By assuming the design stance we might come to implicitly assume that there is a "designer," much like coming to implicitly assume a "programmer" in the computer metaphor. The only problem is that in taking a stance --any stance- we imply that we are aiming to explain the behaviour of an agent, likely a human agent. To give such an explanation in the design stance, we require the underlying syntax or the program, which we currently do not have.

### Notes

1. <a id="footnotetext7_1"></a> Not to be confused with desires. This is a purely mathematical or algorithmic goal, such as the maximization of a certain quantity, like a reward function. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark7_1)
2. <a id="footnotetext7_2"></a> Big if. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark7_2)
3. <a id="footnotetext7_3"></a> See Searle (1990), endnote 2. [Back up.](/whatnot/2022/phil_of_cogsci/#footnotemark7_3)

### References

Dennett, D. C. (1971). Intentional Systems. *The Journal of Philosophy, 68* (4), 87–106.

Searle, J. R. (1990). Cognitive Science and the Computer Metaphor. In *Artifical Intelligence, Culture and Language: On Education and Work* (pp. 23–34). Springer.