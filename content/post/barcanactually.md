+++
date = "2015-04-09T04:35:45+01:00"
title = "The Barcan Formula, Necessary Existence and the Actuality Operator"
description = "In which I muse about The Barcan Formula and Actuality"

+++

<p>One of the problems which those of us who believe that there are things which exist contingently (<em>Contingentists</em> to use Timothy Williamson&rsquo;s terminology) usually have with the Barcan Formula (=$\Diamond\exists x A \supset \exists x\Diamond A$) is that it somehow entails that everything which exists exists
necessarily. Usually this is demonstrated by appealing to the Converse Barcan Formula as well, which by itself already makes trouble for
the contingentist.</p>

<p>This might lead one to suspect that the Barcan
Formula is somehow &lsquo;safe&rsquo; so long as it doesn&rsquo;t bring the Converse Barcan Formula with it. Particular instances may have odd consequence,
perhaps, but one might wonder whether it brings with it undesirable purely logical consequences. <!-- more --> So long as its truth still allows that
there are <em>some</em> things which are contingent existents then perhaps all is well. As it happens, though, this position is untenable, as  as surely the contingentist
must reject the principle of &lsquo;Necessary Actual Existence&rsquo;
$$
(N@E):\quad \Box\forall x @ \exists y (x = y)
$$
That is, the principle that necessarily everything is actual. Unfortunately, this principle is derivable from the Barcan Formula in the logic of actually.</p>

<p>Interestingly we do need quite a bit of the logic of actually to do this, in particular we need to appeal to the schemata which is
characteristic of `real world&rsquo; validity: $@A \equiv A$.</p>

<ul>
<li>Assume $\Diamond \exists x \lnot @ \exists y ( x = y)$ for a reductio.</li>
<li>By the Barcan Formula we get $\exists x \Diamond\lnot @\exists y (x =y)$ by Modus Ponens.</li>
<li>From the principle that $\lnot @ A \equiv @\lnot A$ we get $\exists x \Diamond @\lnot\exists y (x =y)$ by the replacement of equivalents.</li>
<li>From the principle that $\Diamond @A \equiv @A$ we get $\exists x @\lnot\exists y (x =y)$ by the replacement of equivalents.</li>
<li>From the principle that $@A \equiv A$ we get $\exists x\lnot\exists y (x =y)$ by the replacement of equivalents.</li>
<li>But in classical predicate logic we can derive $\lnot\exists x\lnot\exists y (x =y)$.</li>
<li>So by reductio we can discharge our assumption and conclude $\lnot\Diamond \exists x \lnot @ \exists y ( x = y)$</li>
<li>So by principles valid in quantified <strong>K</strong> we can finally conclude with $(N@E)$</li>
</ul>

<p>Some comments are worth making on this proof. In the logic of real-world validity replacement of equiavlents is not, in general, validity preserving. What the first few steps of the above proof show, though, is that $\exists x @\lnot\exists y (x =y)$ is generally valid. Then we can go from the instance of the real-world validity schema $@\lnot\exists y (x =y) \equiv \lnot\exists y(x = y)$ to
$\exists x(@\lnot\exists y (x =y) \equiv \lnot\exists y(x = y))$ by $(\exists I)$, which implies $\exists x@\lnot\exists y (x =y) \equiv \forall x\lnot\exists y(x = y))$, allowing us to conclude $\forall x\lnot\exists y(x = y)$ and (on the assumption that the domain is non-empty)
$\exists x\lnot\exists y(x = y)$ as desired.</p>

<p>So even putting aside worries about us having to include some possibilia in our ontology,
in the presence of the logic of actually the Barcan Formula seems to commit us to the conclusion that in fact all possibilia are actual existents.</p>
 
