# STSCI 4780 Lecture Resources

In the reference lists below, references with "&sext;" are particularly recommended. *Kruschke* refers to John Kruschke's  [*Doing Bayesian Data Analysis* (2nd edition)](https://sites.google.com/site/doingbayesiandataanalysis/), the recommended text for STSCI 4780. *Rethinking* refers to McElreath's *Statistical Rethinking*. *BDA3* refers to the third edition of [*Bayesian Data Analysis*](http://www.stat.columbia.edu/~gelman/book/) by Gelman et al. (2013), the standard statistics PhD-level reference on Bayesian data analysis.

## Lec01 - The big picture

Slides:  [Lec01-BigPicture.pdf](Lec01-BigPicture.pdf)

### Suggested reading

While not covering the Bayesian approach from a technical perspective, as we did in Lec01, Sharon McGrayne's 2012 book, [&sext; The Theory That Would Not Die](https://yalebooks.yale.edu/book/9780300188226/theory-would-not-die), provides a popular-level treatment of the history of Bayesian inference and its place in modern science. This book was a *New York Times* "Editor's Choice" selection; see the 2011 [pre-publication review](http://www.nytimes.com/2011/08/07/books/review/the-theory-that-would-not-die-by-sharon-bertsch-mcgrayne-book-review.html). For more info about the book, see [Sharon Bertsch McGrayne's "The Theory..." web page](http://www.mcgrayne.com/the_theory_that_would_not_die__how_bayes__rule_cracked_the_enigma_code__hunted_d_107493.htm). The book was timed to come out just before the 250th anniversary of the publication of Bayes's paper presenting a special case of what came to be called Bayes's theorem.  McGrayne was the dinner speaker at [Bayes 250 Day](https://web.archive.org/web/20161011035530/https://bayesian.org/meetings/Bayes250), a meeting held by the [International Society for Bayesian Analysis (ISBA)](https://bayesian.org/) in 2013 to honor the anniversary.

I can't resist a personal, astronomical note on the book. McGrayne interviewed me as part of her research for it. I get a brief mention (for helping to introduce Bayesian methods into modern astronomy). But our main correspondence and discussion was about Laplace's work, especially a famous calculation he did estimating the mass of Saturn. He used Bayes's theorem to estimate Saturn's mass from noisy data. His late-18th century parlance for what we today call a *credible region* went as follows:

> Applying to them my formulae of probability I find that it is a bet of 11,000 against one that the error of this result is not 1/100 of its value....

Indeed, today's best estimate is well within a percent of Laplace's estimate; he would have won that bet! See the Lec02 notes below for more from and about Laplace.

The main technical part of Lec01 concerned a key distinction between Bayesian and frequentist approaches: both approaches involve *computing averages and integrals*, but **over different spaces**. Bayesian probabilities typically involve sums or averages over the hypothesis or parameter space; frequentist probabilities instead sum or average over the data or sample space. Two papers of mine elaborate on this distinction:

* [The Promise of Bayesian Inference for Astrophysics | SpringerLink](https://link.springer.com/chapter/10.1007%2F978-1-4613-9290-3_31) — An *old* (1991) paper using some simple examples to highlight this difference. For a longer version, see: [The Promise... (unabridged)](http://hosting.astro.cornell.edu/staff/loredo/bayes/promise.pdf).
* [Bayesian Astrostatistics: A Backward Look to the Future | SpringerLink](https://link.springer.com/chapter/10.1007/978-1-4614-3508-2_2) — This focuses more on concepts than calculations, and addresses some misunderstandings about the difference between Bayesian and frequentist approaches to quantifying uncertainty.

If you are very familiar with frequentist statistics, you may appreciate this old paper by Ed Jaynes offers several example calculations displaying the difference results one can get when adopting Bayesian vs. frequentist approaches to simple problems; this paper inspired my 1991 paper cited above:

* [Confidence Intervals vs Bayesian Intervals | SpringerLink](https://link.springer.com/chapter/10.1007%2F978-94-010-1436-6_6) — Also available as item 32 in the "E. T. Jaynes: Articles" section of [Probability Theory As Extended Logic - Bayesian resources at Washington U.](https://bayes.wustl.edu/)

## Lec02 - Probability theory as logic

Slides:  [Lec02-Logic+Probability.pdf](Lec02-Logic+Probability.pdf)

* Propositions and arguments
* Valid vs. sound arguments
* Propositional logic: unary and binary operations/connectives, truth tables
* Inductive vs. deductive logic
* Probability theory as a calculus for inductive logic

### Suggested reading on Bayesian foundations

* For a *brief* overview of the historical connections between logic and probability theory, see: [&sext; "Bayesian Methods: General Background"](http://bayes.wustl.edu/etj/articles/general.background.pdf) by Ed Jaynes (1986).

* The earliest extensive work using probability theory in this way to tackle data analysis problems is Laplace's [*Théorie analytique des probabilités*](https://en.wikipedia.org/wiki/Pierre-Simon_Laplace#Analytic_theory_of_probabilities) (TAP). Despite its enormous importance, to my knowledge TAP has never been translated into English.  Laplace summarized his main ideas in *Essai philosophique sur les probabilités*  (*Philosophical Essay on Probabilities*, 1814), which is available in English.  A fairly recent translation is by Andrew Dale: [*Philosophical Essay on Probabilities*](https://link.springer.com/book/10.1007%2F978-1-4612-4184-3). This is a free download via the CULib SpringerLink subscription, but it is not for the faint of heart.  Laplace offers the essay as a non-mathematical description of his approach, but he accomplishes this by the artifice of writing out key equations in words! For further details about Laplace's work in probability theory, see [Laplace on probability and statistics](http://www.cs.xu.edu/math/Sources/Laplace/index.html) (part of a site on the history of probability hosted by the Xavier University CS department).

* The approach Laplace adopted came to be known as the method of **inverse probability**. It's what we would today call parametric Bayesian inference, with use of uniform priors by default—setting the posterior to be proportional to the likelihood function, "inverting" the conditional. If you're interested in the complicated historical path from "inverse probability" to "Bayesian inference," see ["When did Bayesian inference become 'Bayesian'?"](https://projecteuclid.org/euclid.ba/1340371071) by Stephen E. Fienberg (2006). *Spoiler:* Fisher appears to have invented the modern usage of "Bayesian," intending it as somewhat of an insult, referring to methods different from the *fiducial probability* approach he advocated, which failed to develop a following. (Fisher, probably the most influential statistician of the 20th century, had a reputation of being more than a bit ornery!) The modern (non-derogatory!) usage only became common in the statistics literature in the 1960s.

* When scientific interest in Bayesian methods revived in the early 20th century, key early figures expounding the **probability theory as generalized logic** viewpoint were [Harold Jeffreys](https://en.wikipedia.org/wiki/Harold_Jeffreys) (geophysicist, mathematician), [John Maynard Keynes](https://en.wikipedia.org/wiki/John_Maynard_Keynes#In_the_1920s) (economist, mathematician), and [Rudolf Carnap](https://en.wikipedia.org/wiki/Rudolf_Carnap) (philosopher). From among the writings of these thinkers, Jeffreys's [_Theory of Probability_](https://global.oup.com/academic/product/theory-of-probability-9780198503682?cc=us&lang=en&) offers the most accessible and useful account of this viewpoint for scientist and engineer readers (philosophers may prefer Carnap and Keynes). A trio of leading French Bayesian statisticians recently looked back at this historically important book: ["Harold Jeffreys’s Theory of Probability Revisited"](https://projecteuclid.org/euclid.ss/1263478373).  Jeffreys's book played a major role in my own early education in Bayesian methods. It's still a good read.

* The most clear and forceful mid-20th century advocates of the probability-as-logic viewpoint were two physicists, Richard Cox ([Richard Threlkeld Cox - Wikipedia](https://en.wikipedia.org/wiki/Richard_Threlkeld_Cox)) and Ed Jaynes ([Edwin Thompson Jaynes - Wikipedia](https://en.wikipedia.org/wiki/Edwin_Thompson_Jaynes)).  They built on the legacies of Laplace and Jeffreys.  An accessible early exposition is the article, ["How Does the Brain Do Plausible Reasoning?"](http://bayes.wustl.edu/etj/articles/brain.pdf), by Ed Jaynes (1957; the link is to a 1988 reprint of the original report). For a brief (4pp) overview of the line of argument, see section 3 of my first Bayesian publication: ["From Laplace to Supernova SN 1987A: Bayesian Inference in Astrophysics"](http://www.astro.cornell.edu/staff/loredo/bayes/L90-LaplaceToSN1987A-scan.pdf) (1990; note the errata at the end, and be patient with the sometimes-polemical tone, reflecting the controversial status of Bayesian methods ca. 1990; this paper became half of my PhD thesis).

* The most thorough recent treatment is in the first two chapters of Jaynes's posthumously published book, [*Probability theory: The logic science* (PTLOS) ](http://www.cambridge.org/us/academic/subjects/physics/theoretical-physics-and-mathematical-physics/probability-theory-logic-science?format=HB&isbn=9780521592710#trCy9CBbIU08dEfg.97) (on course reserve).  [&sext; These two chapters are available online](http://bayes.wustl.edu/etj/prob/book.pdf) via Washington University, where Jaynes worked and where his last PhD student, G. Larry Bretthorst, maintains an archive of Jaynes's work: [Probability Theory As Extended Logic](http://bayes.wustl.edu/).  More chapters from a pre-publication version of the book are [available via archive.org](https://web.archive.org/web/20180122210541/http://omega.albany.edu:8008/JaynesBook.html). This book is truly outstanding, though it was written mostly before the advent of powerful computational methods for Bayesian inference, and thus is not the most practical book on modern Bayesian data analysis.

* For a fun read about Jaynes's book, see the entertaining review by Stanford (formerly Cornell) statistician/mathematician Persi Diaconis: [&sext; "A Frequentist Does This, A Bayesian That"](https://www.siam.org/news/news.php?id=81):  

  >  There are many places in which I want to yell at him. He's so full of himself. That's what makes the book so terrific. It's the real thing—the best introduction to Bayesian statistics that I know.

* An alternative viewpoint on Bayesian probability theory is the **subjective Bayes** approach. This considers probability theory as a kind of calculus for guiding bets based on personal beliefs about uncertain outcomes. This approach arose nearly contemporaneously to the "probability as logic" approach in the early 20th century, but in different literature—in economtrics and statistics. The two approaches are close in spirit and execution, although they take different attitudes toward how objective or subjective calculations should be (especially in regard to assigning priors). In particular, part of the subjective Bayes literature is concerned with *prior elicitation*—techniques for working with domain experts in order to build priors that attempt to quantify expert pre-experiment knowledge.

* Prominent founders of subjective Bayes include [Frank P. Ramsey (Wikipedia)](https://en.wikipedia.org/wiki/Frank_P._Ramsey) and [Bruno de Finetti (Wikipedia)](https://en.wikipedia.org/wiki/Bruno_de_Finetti); prominent early proponents of this viewpoint in applied statistics include [Leonard "Jimmie" Savage (Wikipedia)](https://en.wikipedia.org/wiki/Leonard_Jimmie_Savage) and [Dennis Lindley (Wikipedia)](https://en.wikipedia.org/wiki/Dennis_Lindley). [Abraham Wald (Wikipedia)](https://en.wikipedia.org/wiki/Abraham_Wald) also played an important role, establishing connections between this approach and (frequentist) decision theory. Lindley was active until his death, at 90, in 2014, and was probably the most influential of the early "neo-Bayesians" in terms of impact on applied statistics.

* Two particularly clear recent books explaining the subjective Bayes outlook are Dennis Lindley's [&sext; *Understanding Uncertainty*](http://onlinelibrary.wiley.com/book/10.1002/0470055480) (a free download via CULib) and Jay Kadane's [*Principles of Uncertainty*](https://www.crcpress.com/Principles-of-Uncertainty/Kadane/p/book/9781439861615) (2011; on course reserve and also available as a free PDF via [Kadane's book site archived at archive.org](https://web.archive.org/web/20170914095926/http://uncertainty.stat.cmu.edu/)).  Lindley's book is largely nontechnical; Kadane's is mathematical, but with an emphasis on concepts, especially in the early chapters (I'd give it a &sext;, but it's more technical than other starred resources).  See also *CHANCE* magazine's interview: ["Discussing *Principles of Uncertainty* with Jay Kadane"](http://chance.amstat.org/2013/04/kadane-interview/). Lindley published an article-length overview: [&sext; "The Philosophy of Statistics"](https://www.jstor.org/stable/2681060?seq=1#page_scan_tab_contents) (2000; this was published in *The Statistician*, a Royal Statistical Society journal intended for a wide, not-too-technical audience; this journal became the magazine *Significance* in 2004, a joint publication of the RSS and the American Statistical Society).

* The **objective Bayes** viewpoint rests on the subjective Bayes foundational arguments (optimal betting), but seeks to use rule-based priors as much as possible. It has a lot of overlap with the probability-as-logic viewpoint. Many practitioners who favor logical Bayes foundations nevertheless would happily accept "objective Bayes" as a fair description of their approach. 

## Lec03 - Key theorems

Slides:  [Lec03-KeyTheorems.pdf](Lec03-KeyTheorems.pdf)

* Bayes's theorem (BT)
* The law of total probability (LTP)
  - Extending the question/"wishful thinking"
  - Marginalization
* Normalization for exclusive, exhaustive alternatives

BT was illustrated with a binary hypothesis/binary data problem: Cancer diagnosis.

### Suggested reading/viewing

*Kruschke* Chapter 5 treats Bayes's theorem (also known as "Bayes' rule").

For fans of video lectures, Harvard statistician Joe Blitzstein covers Bayes's theorem ("conditioning") and the law of total probability in [Lecture 5: Conditioning Continued, Law of Total Probability | Statistics 110 - YouTube](https://www.youtube.com/watch?v=JzDvVgNDxo8). He discusses the Monty Hall problem in a subsequent lecture. These are chalk-on-blackboard lectures. Blitzstein is the person from whom I got the "wishful thinking" characterization of LTP that I shared in Lec04.

**Case diagrams:** The "case diagrams" or "case lattices" in the binary classification/cancer diagnosis example of Lec03, are more popularly known as "natural frequency trees," a pedagogical tool that's been widely popularized by German social scientist [Gerg Gigerenzer](https://en.wikipedia.org/wiki/Gerd_Gigerenzer). (I don't use that term because the frequencies are not "natural"—they're *ideal*—and the diagram is technically not a tree.) His popular-level book, [*Calculated Risks*](http://www.simonandschuster.com/books/Calculated-Risks/Gerd-Gigerenzer/9780743254236), uses such diagrams to teach basic Bayesian reasoning. Gigerenzer has done research on teaching people how to understand risk and uncertainty; the research demonstrates the value of such tools. 

* Cornell mathematician [Steven Strogatz](http://www.stevenstrogatz.com/), a widely-lauded popularizer of mathematics and regular NPR guest and commentator, used to write a popular math column for the *New York Times*. He covered Gigerenzer's *Calculated Risks* book in a 2010 column: [&sext; "Chances Are"  (*The New York Times*)](https://opinionator.blogs.nytimes.com/2010/04/25/chances-are/). This is a fast and fun summary of Gigerenzer's main ideas.
* For a recent presentation of some of this research, see ["Natural frequencies improve Bayesian reasoning in simple and complex inference tasks"](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4604268/) (Hoffrage et al., 2015).
* See [Gerd Gigerenzer's *Calculated Risks* site | Max Planck Institute for Human Development](https://www.mpib-berlin.mpg.de/en/research/adaptive-behavior-and-cognition/publications/books/calculated-risks) for links to more of his research.
* See [Frequency format hypothesis - Wikipedia](https://en.wikipedia.org/wiki/Frequency_format_hypothesis) for an overview of the research (with pros and cons).



## Lec04 - Inference in discrete spaces

Slides:  [Lec04-DiscreteSpaces.pdf](Lec04-DiscreteSpaces.pdf)



### Suggested reading

The last example in Lec04—the possibly biased coin problem—is a discretization of a problem that is inherently continuous (i.e., the probability for heads could be any number in $[0,1]$, which we treat in Lec05 in all its labyrinthian glory). The book, [&sext; *Think Bayes: Bayesian Statistics Made Simple*](http://greenteapress.com/wp/think-bayes/), by Allen Downey (2012), uses similar discretizations of many problems to teach Bayesian ideas in an accessible manner (including providing Python code to do the required calculations over discrete spaces). I found the book too, well, *discrete* to be a good teaching resource at the level of STSCI 4780. But Downey does a very good job covering key Bayesian concepts in the context of simple problems. The book is a free download and a quick read. It won't directly help you set up calculations for problems of realistic complexity, but it may help you better understand the fundamental ideas, which may well *indirectly* help you solve real problems. My favorite take-away from Downey's book is something simple: his introduction of the term *suite* as a convenient shorthand for "a collection of mutually exclusive, exhaustive alternatives."

## Lec05 - Continuous parameter estimation with discrete data, 1

Slides:  [Lec05-ParamEstmn-BetaBinomial.pdf](Lec05-ParamEstmn-BetaBinomial.pdf)

* The continuum: PDFs vs. PMFs
* Binary outcome data: Bernoulli, binomial, negative binomial distributions
* Beta distribution posterior PDFs
* Conjugate families (beta-Bernoulli, beta-binomial...)
* The likelihood principle

### Suggested reading

*Kruschke* Chapter 6 works through the beta-bernoulli model.

## Lec06 - Continuous parameter estimation with discrete data, 2

Slides:  [Lec06-ParamEstmn-DirichletMultinomial.pdf](Lec06-ParamEstmn-DirichletMultinomial.pdf)

* Probability and frequency:
  - Bernoulli's weak law of large numbers: predict frequency from a given probability
  - Bayes's theorem: Inferring per-trial probability from frequency data
* Categorical data: categorical and multinomial distributions
* Dirichlet distribution posterior PDFs
* Dirichlet-categorical and Dirichlet-multinomial conjugacy
* The Dirac delta function


### Suggested reading

**The Dirichlet-multinomial conjugate model:** See my [notes on this model](DirichletMultinomialNotes.pdf). This document reproduces the calculations of the lecture, but with more details. It also describes some additional calculations. I've adapted this from old notes for a colleague; as a result, some of the notation doesn't *exactly*  match the notation of Lec06 (e.g., I use $i$ rather than $k$ as the category index), but it's close. The section on model comparison won't make sense until a later lecture.

**The Dirac delta function:** The $\delta$ function is named for physicist Paul Dirac, who devised it to make some formulas in quantum mechanics easier to interpret and manipulate. He was interested in generalizing some quantum mechanics methods that were developed in discrete spaces, extending them to work in the continuum. Specifically, he aimed to generalize the *Kronecker $\delta$* symbol, $\delta_{ij}$, a common tool used in discrete sums. It's basically the identity matrix in component form:
$$
\delta_{ij} = 
  \begin{cases}
    1 & \mbox{if } i=j, \\
    0 & \mbox{if } i\ne j.
  \end{cases}
$$
In a sum with a Kronecker $\delta$ multiplying vector or matrix components, summing over a $\delta$ index eliminates the sum and causes all occurrences of that index to be replaced with the other index. For example, for a vector $\vec{a}$ with components $a_j$,
$$
\sum_{j} a_{j} \delta_{ij} = a_i.
$$
Essentially, summing over $j$ sets $j=i$ everywhere in the summand. The Dirac $\delta$ function works analogously: integrating $f(x)\delta(x-c)$ over $x$ replaces $x$ with $c$, returning just $f(c)$—it just sets $x=c$ everywhere in the integrand. Incidentally, the $\delta$ function is symmetric; $\delta(c-x)$ has the same effect as $\delta(x-c)$. I sometimes exploit this, choosing the order of terms in the argument of a $\delta$ function to make it more readable.

A few years after Dirac's introduction of $\delta(x)$, mathematician Laurent Schwartz put it on a firm mathematical footing, basically creating a new area of mathematics to do so: the theory of *distributions* (distinct from probability distributions) or *generalized functions* (there were hints of $\delta(x)$ and generalized functions in earlier work). The math literature in this area tends to be formal and technical, and not very accessible to non-mathematicians.

Wikipedia has a helpful article on the $\delta$ function: [Dirac delta function - Wikipedia](https://en.wikipedia.org/wiki/Dirac_delta_function). Two recent overviews by physicists are worth a look:

* [Appendix A: The Dirac Delta Function](http://onlinelibrary.wiley.com/doi/10.1002/9783527618460.app1/summary), in David Griffiths' *Introduction to Elementary Particles* (free PDF). This gives a few-page overview along the lines of the approach we took in Lec06, and includes material on transformations of $\delta$ functions that we will use later, when we cover *propagation of uncertainty* (an important application of $\delta$ functions).

* Nicholas Wheeler's "Simplified Dirac Delta" notes at [Nicholas Wheeler's Documents](http://www.reed.edu/physics/faculty/wheeler/documents/) (look under "Miscellaneous Math: Delta Functions"). This is a lengthier treatment, relating the $\delta$ function to the simpler *Heaviside step function*. Even if you're not interested in Wheeler's step function approach, the early part of his notes is very much worth reading; it provides a very accessible account of the history of the $\delta$ function. He emphasizes a point we made in class, that the $\delta$ function only really makes sense in the context of integrals, describing Schwartz's generalized functions as new mathematical entities "that live always in the shade of an implied integral sign." He quotes Dirac on this point:

  > There are a number of elementary equations which one can write down about $\delta$ functions. These equations are essentially *rules of manipulation* for algebraic work involving  $\delta$ functions. The meaning of any of these equations is that its two sides give equivalent results [when used] as *factors in an integrand*.

  Wheeler's companion article, "Delta Interrelations," explicitly demonstrates a point I made but did not demonstrate in class—that you can use a wide variety of "parameterized peak" functions to define the $\delta$ function, all of them giving the same results in the limit of an infinitesimally narrow, infinitely tall peak. We used normalized boxes; Wheeler also uses Gaussian PDFs and other functions.

