+++
date = "2015-03-13T04:35:45+01:00"
title = "Urn Logic, Quantification and Modal Logic"
description = "In which I muse about the connections between quantificational logic and modal logic"

+++

<p>One of the great pleasures of doing logic is finding problems in one area which can be solved using the techniques and
insights from another. What I want to briefly mention here is a neat example of this involving an interesting approach
to quantificational logic due to Veikko Rantala called <a href="http://dx.doi.org/10.1007/BF00558760">&lsquo;Urn Logic&rsquo;</a>. The core idea behind urn logic&rsquo;s semantics for the
quantifiers is that the objects which the quantifiers range over can vary over the course of the evaluation of a formula,
depending on which objects are selected from the domain by earlier quantifiers. Veikko&rsquo;s original semantics for this is
in the style of Hintikka&rsquo;s game theoretic semantics, and I&rsquo;ve proposed a more standard version of the semantics in my
<a href="/writing/urn-logic.pdf">&lsquo;A Sequent Calculus for Urn Logic&rsquo;</a>. What I&rsquo;m interested in here, though, is a &lsquo;classical&rsquo; semantics for Urn Logic proposed
by Max Cresswell, and how a question he asks about the expressivity of this semantics can be answered using a very familiar
construction from modal logic.</p>

<!--more-->


<h2 id="cresswell-s-classical-exposition:e11132a276315be53ce9adcebdd68daf">Cresswell&rsquo;s &lsquo;Classical Exposition&rsquo;</h2>

<p>Cresswell&rsquo;s semantics for Urn logic, which he articulates in his excellent paper
<a href="http://dx.doi.org/10.1007/BF00370339">Urn Models: A Classical Exposition</a>, are as follows. A model is a triple
$\langle A, D, V\rangle$, with $A$ being a set of individuals (approximately, our initial domain), and $V$ an assignment
of extensions to predicate letters (done in the usual manner). All the action in the semantics concerns $D$, which is
a function from sequences of objects from $A$ to subsets of $A$. We also change the recursive clause for the quantifiers
as follows
$$
\langle A, D, V\rangle\models \forall x \varphi[s] \iff \langle A, D, V\rangle\models \varphi[s&rsquo;]
$$<br />
where $s&rsquo;$ is an $x$-variant of $s$ s.t. $s&rsquo;(x)\in D(\langle s(x_{1}), \ldots, s(x_{n})\rangle)$ where
$x_{1}, \ldots, x_{n}$ are the free-variables in $\forall x\varphi$. For convenience (so that we don&rsquo;t have to make
some kind of choice concerning the order of the free-variables in formulas) we also need to impose the constraint that
$D(\langle a_{1}, \ldots, a_{n}\rangle) = D(\langle b{1}, \ldots, b{n}\rangle)$ whenever $b{1}, \ldots, b{n}$ is a
permutation of $a_{1}, \ldots, a_{n}$.</p>

<p>What we&rsquo;re going to focus on here is a constraint on Urn Models which Cresswell singles out in the course of his completeness
proof, which we&rsquo;ll call (Dist.) (in Cresswell&rsquo;s paper it appears as <strong>4.3</strong>)</p>

<blockquote>
<p>(Dist.) If $b \in D(\langle a_{1}, \ldots, a_{n}\rangle)$ then $b$ is distinct from each $a_{1}, \ldots, a_{n}$.</p>
</blockquote>

<p>Concerning this condition Cresswell has the following to say:</p>

<blockquote>
<p><em>&ldquo;The satisfaction of [(Dist.)] is interesting because it is not a condition one
would want to put on all urn models. This means that there would seem to
be no formula which entails that</em> $a_{i} \in D(\langle a_{1}, \ldots, a_{n}\rangle)$ <em>for</em> $1 \leq i \leq n$.&rdquo;
(Cresswell 1982, p.121)</p>
</blockquote>

<p>Cresswell is indeed right that (Dist.) is not a condition we want to place on all our urn models. As it happens, though, placing this
constraint on our models doesn&rsquo;t make a difference to the validities of the logic as, given a model $\mathcal{M}$ which doesn&rsquo;t
satisfy (Dist.) we can always construct a model $\mathcal{M^{d}}$ so that for every $\mathcal{M}$-assignment, there is a
$\mathcal{M^{d}}$-assignment s.t. $\mathcal{M}$ and $\mathcal{M^{d}}$ agree on which formulas are satisfied.</p>

<p>To demonstrate this we just need to use a construction which is reminiscient of the &lsquo;unravelling&rsquo; construction which is often used
to show that the class of all irreflexive frames is not modally definable&mdash;which is not entirely surprising, considering the
extent to which (Dist.) looks like a combination of irreflexivity and antisymmetry on our &lsquo;accessibility relation&rsquo;. The construction
is relatively simple. First let us establish some notation. Given a sequence $s$ and a sequence $s&rsquo;$ let $s\ast s&rsquo;$ be the
concatenation of $s$ and $s&rsquo;$, similarly given an object $a$ let $s\ast a$ be the result of concatenating $a$ to the end of $s$. Given a sequence of sequences $s = \langle s_{1}, \ldots, s_{n}\rangle$ say that $s_{i}$ is the maximal element of $s$ iff $s{i}$ is the longest member of $s$. Finally, given a sequence $s$ let $s^{l}$ be the final element of $s$.</p>

<h2 id="the-construction:e11132a276315be53ce9adcebdd68daf">The Construction</h2>

<p>Suppose that $\mathcal{M} = \langle A, D, V\rangle$ is an urn model. Let $\mathcal{M}^{d} = \langle A^{d}, D^{d}, V^{d}\rangle$ be defined as follows:</p>

<ul>
<li>$A^{d}$ is the set of all sequences $\langle a_{1}, \ldots, a_{n}$ of elements from $A$ where $a_{n}\in D(\langle a_{1}, \ldots, a_{n-1}\rangle)$ (with $\langle a_{1}\rangle\in A^{d}$ iff $a_{1}\in D(\emptyset)$)</li>
<li>$D^{d}(\emptyset) = D(\emptyset)$</li>
<li>$s \in D^{d}(a_{1}, \ldots, a_{n})$ iff $s= a_{i}\ast b$ for some $b\in A$, where $a_{i}$ is the maximal element of $\langle a_{1}, \ldots, a_{n}\rangle$ and $b\in D(a_{i})$</li>
<li>$V^{d}(F) = {\langle s_{1}, \ldots, s_{n}\rangle | \langle s_{1}^{l}, \ldots s_{n}^{l}\rangle \in V(F)}$</li>
</ul>

<p>It should be fairly obvious to see that $\mathcal{M}^{d}$ is an urn model (all we need to do is check that it satisfies the permutation condition). Readers who are familiar with the model theory for modal logic will notice the striking resemblence between this model
construction and the <em>unravelling</em> construction (due, to the best of my knowledge, to either Henrik Sahlqvist or M. Dummett and E.J. Lemmon) which we can use to show (for example) that the smallest normal modal logic <strong>K</strong> is
determined by the class of all trees.</p>

<p>Given urn models $\mathcal{M}$ and $\mathcal{M}^{d}$ let us say that a $\mathcal{M}^{d}$-assignment $s&rsquo;$ is <em>safe relative to</em> $x1, \ldots xn$
for a $\mathcal{M}$-assignment $s$ if and only if there is a sequence $\langle s{1}, \ldots, s{n-1}\rangle$ of length $n-1$ constructed out of
$s(x_{i})$ ($1\leq i \leq n$), and some ordering $\langle a_{x_1}, \ldots, a_{x_n}\rangle$ of $x_{1}, \ldots, x_{n}$,  $s&rsquo;(a_{x_i})=\langle s{1}, \ldots, s{i-1}\rangle \ast\langle s(a_{x_i})\rangle$. Approximately speaking assignments which are safe relative
to some variables are ones where the values assigned to those variables could have come from some sequence of legal selections of objects from
our model. With this in hand we can then prove that, for all urn models $\mathcal{M}$, assignments $s$ and formulas $\varphi$ we have
$$
\mathcal{M}\models\varphi[s] \iff \mathcal{M}^{d}\models\varphi[s&rsquo;]
$$
where $s&rsquo;$ is safe relative to the free-variables in $\varphi$ for $s$. Given that the condition that $s&rsquo;$ be safe relative to
the free-variables in $\varphi$ for $s$ is vacuously satisfied in the case where $\varphi$ is a sentence we can quite easily conclude
that there is no <em>sentence</em> which is true in precisely those urn models in which for all $n$ we have $a_{i} \in D(\langle a_{1}, \ldots, a_{n}\rangle)$ for $1 \leq i \leq n$.  In order to show that there is no such formula of any kind we would need to show that for every
set of variables $x_1, \ldots x_{n}$ and $\mathcal{M}$-assignment $s$ there is a $\mathcal{M}^{d}$-assignment $s&rsquo;$ which is safe
for $x_1, \ldots x_{n}$. In the great tradition of leaving unknowns as exercises, I leave this as an exercise to the reader.</p>
 
