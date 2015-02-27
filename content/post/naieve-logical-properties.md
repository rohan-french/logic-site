+++
date = "2015-02-26T00:53:45+01:00"
title = "Musings on Naieve Logical Properties"
draft = "true"
+++

There’s something very funny going on in Elia Zardini’s “Naieve Truth and Logical Properties”. There Elia sketches
a paradox involving the naive (single-premise) inconsistency predicate $I$, which he takes to be governed by the 
following left- and right-insertion rules:

$$\frac{\varphi\not\vdash \emptyset}{I(``\varphi') \vdash\emptyset}(I\mbox{-}L)$$
$$\frac{\varphi\vdash\emptyset}{\emptyset\vdash I(`\varphi')}(I\mbox{-}L)$$

The paradox which Elia sketches is as follows (and I’ll quote here):

>“We assume that the language contains a sentence $\iota$ identical to $I(‘\iota’)$. It would then seem that we 
>could reason as follows. Suppose that $\iota\not\vdash\emptyset$ holds. Then, by I-L $I(‘\iota’)\vdash\emptyset$ 
>holds. But, by definition of ‘$\iota$’, that is tantamount to $\iota\vdash\emptyset$ holding, and hence, by 
>reduction, $\iota\vdash\emptyset$ holds. Therefore, by I-R, $\emptyset\vdash I(‘\iota’)$ holds. But, by 
>definition of ‘$\iota$’, that is tantamount to $\emptyset \vdash\iota$ holding. Thus, both $\emptyset\vdash\iota$ 
>and $\iota \vdash\emptyset$ hold, and hence, by transitivity, $\emptyset\vdash\emptyset$ holds, and so, by
>monotonicity, $\vdash$ is trivial. (Let’s label this paradox ‘(I)’)” (p. 355)

Now I think there are a few interesting things going on here. Firstly, this paradox is very different from the 
usual semantic paradoxes like the Liar, in that the reasoning involved isn’t reasoning in the logic at issue but 
in fact metatheoretic reasoning concerning that logic’s relation of consequence. So, for example, we have the odd 
move of assuming a sequent and then reasoning about that sequent, and applying reductio to our assumption. Let’s 
not take issue with that here (in fact the whole point of Elia’s paper is that if we want to admit naive logical 
properties like $I$ into our language then we need to move to a non-classical metalanguage where the moves used 
above aren’t going to make a consequence relation with I trivial. 

What I think is *very* strange here is the left-insertion rule for I given above. In fact, on many notions of what 
a rule is this isn't even going to count as a rule at all, but I’m happy to put that issue aside here. How am I to 
derive a premise for an application of this rule? It appears to me that I’ve got to do some kind of metatheoretic 
reasoning (perhaps internalised via higher-order rules of some kind). 

