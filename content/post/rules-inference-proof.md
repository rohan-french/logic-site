+++
date = "2015-08-19T04:35:45+01:00"
title = "McGee on Necessitation and Conditional Proof"
description = "In which I muse on a common error concerning the rule of necessitation"

+++

<p>I&rsquo;ve been taking great pleasure in reading <a href="https://sites.google.com/site/olehjortland/">Ole Hjortland</a> and <a href="https://sites.google.com/site/colincaret/">Colin Caret</a>&rsquo;s recent edited
<a href="http://ukcatalogue.oup.com/product/9780198715696.do">collection of papers</a> from the long running Arche &lsquo;Foundations of Logical Consequence&rsquo;
project. So far I&rsquo;ve greatly enjoyed every paper in the collection. What I want to point out
here is a rather curious passage in Van McGee&rsquo;s contribution &ldquo;The Categoricity of Logic&rdquo;.
After claiming that the meanings of the sentential-connectives are given by their natural
deduction rules McGee goes on to make the following, rather curious, comment.</p>

<!-- more -->

<blockquote>
<p>&ldquo;In proposing this, I don&rsquo;t want to go to the extreme of saying that any inferential system
whose methods of reasoning with the classical connectives don&rsquo;t include the rules is deficient
or defective. Normal systems of modal logic include the rule of necessitation (From $\varphi$,
you may infer $\Box\varphi$). If they also included conditional proof, you could assume $\varphi$,
derive $\Box\varphi$ by necessitation, then discharge the assumption to derive the invalid
conclusion $(\varphi \supset \Box\varphi)$.&rdquo;</p>
</blockquote>

<p>McGee then goes on to argue that this is not a problem, because the rules of normal systems of
modal logic are &ldquo;intended to preserve modal validity&rdquo;, while natural deduction rules like
conditional proof preserve &lsquo;being entitled to accept&rsquo; but not &lsquo;modal validity&rsquo;.</p>

<p>There are a few strange things going on in this passage. Firstly, we have a rather awkward
comparison of logical frameworks. Typical presentations of normal modal logics are in the
<em>FMLA</em> framework<span class="badge"><a href="#fn1">[1]</a></span>, where we convieve of logics
as consisting of sets of valid formulas closed under various rules. In this setting necessitation
is the closure condition which tells us that whenever $A$ is in the set (i.e. is a theorem of the
logic) then so is $\Box A$. In settings like this we cannot even talk about rules in the <em>SET-FMLA</em>
framework like Conditional Proof. To do this we would need to consider appropriate consequence
relations for modal logics where we can properly ask about the status of rules like conditional
proof. Lifted to such a setting the rule of necessitation becomes the
rule which takes us from $\emptyset\vdash A$ to $\emptyset\vdash\Box A$ &ndash; i.e. if $A$ follows from the empty
set of premises, then so does $\Box A$. This is because necessitation is (to use terminology
popularised by Timothy Smiley) a <em>rule of proof</em>, telling us that if we have proved $A$
then we can conclude $\Box A$. By contrast conditional proof, the rule which takes us from
$\Gamma, A \vdash B$ to $\Gamma\vdash A\supset B$ is a <em>rule of inference</em>, telling us that if
we can deduce $B$ on the basis of some assumptions along with $A$ then we can conclude $A\supset B$
on the basis of those assumptions. What McGee is appealing to in the above quotation, though, is
the rule which allows us to transition from $\Gamma\vdash A$ to $\Gamma\vdash\Box A$.</p>

<p>I think this is the most natural way of reading the above passage, and in this case our diagnosis
of the above &lsquo;problem&rsquo; is quite simple: there is none, any appearance to the contrary arising due
to a confusion between rules of inference and rules of proof. This is a somewhat under-recognised
distinction, in part due to the phenomena, pointed out in section 4 of Lloyd&rsquo;s paper &lsquo;<em>Smiley&rsquo;s Distinction
between Rules of Inference and Rules of Proof</em>&rsquo; <span class="badge"><a href="#fn2">[2]</a></span>,  of logicians thinking in terms of undifferentiated
axiomatisations (where an axiomatisation consists solely of a collection of axioms and rules) rather
than dividing up our rules into rules of inference and rules of proof).</p>

<p>This is not the only way to read
this passage, though. There are presentations of normal modal logic which are closed under
the rule McGee seems to have in mind in the above quotation. Fix on a class of modal frames
and understand a model as being a model on one of those frames and let us define the following
two notions of validity:</p>

<ul>
<li><p>$\Gamma\vdash A$ is <em>locally valid</em> iff, for all models, $A$ is true at a world if all the formulas in $\Gamma$ are true there.</p></li>

<li><p>$\Gamma\vdash A$ is <em>globally valid</em> iff, for all models, $A$ is true at all worlds in the model if all the formulas in $\Gamma$ are true at all worlds in that model.</p></li>
</ul>

<p>So local consequence preserves truth at a point in a model, while global consequence preserves
being true throughout (i.e. at all worlds in) a model. Now the rule mentioned above which takes
us from $\Gamma\vdash A$ to $\Gamma\vdash \Box A$ is globally valid, but is not locally valid.
By contrast, conditional proof preserves local validity but not global validity. If we think
in terms of global validity then we can say a bit more about what McGee might have in mind by
&lsquo;modal validity&rsquo;: preservation of modal validity is just preservation of truth in all possible
worlds. Reading McGee in this way will make this passage come out true, but personally I&rsquo;m dubious
about whether this is the intended reading of this passage.</p>

<p>The moral of the story here? People ought to be more attentive to the rule of inference/rule
of proof distinction. Also, comparing logics typically concieved of in different frameworks
can quite quickly get you into trouble.</p>

<hr />

<p><strong>NOTES</strong>
</br>
[1] <a name="fn1"></a> The notion of &lsquo;logical framework&rsquo; which I have in mind, and the labels <em>FMLA</em> and <em>SET-FMLA</em>
for particular logical frameworks is due to Lloyd Humberstone. More information on this (and much
more besides) at <a href="http://plato.stanford.edu/entries/connectives-logic/">http://plato.stanford.edu/entries/connectives-logic/</a>.</p>

<p>[2] <a name="fn2"></a>L. Humberstone, &ldquo;Smiley&rsquo;s Distinction
between Rules of Inference and Rules of Proof&rdquo;, In T. J. Smiley, Jonathan Lear &amp; Alex Oliver (eds.), <em>The Force of Argument: Essays in Honor of Timothy Smiley</em>. Routledge 107&ndash;126 (2010)</p>
  
