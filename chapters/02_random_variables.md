Random Variables
================

(??) Definitions of r.v. and abstract r.v.

Where we impose the condition in order to define the "image law", that is P_X given X on a probability space P.

## Basic RV

The simplest r.v. is the indicator function of a set from F: if the point is in the set A (parametrizing 1_A), the set checks, else it does not. 
It simply translates P_{1_A}(1) to P(A) and P_{1_A}(0) to P(A^c). 
[After [sec 2](#building--checking)] Moreover, the generated sigma-algebra is the minimal with these 2 events in it. 
<!-- that is how can use the set of random variables to reformulate the whole probability not as a measure, as much as a measureable function appropriately defined.  -->

We can get more creative: so-called *simple* r.v. are combinations of **finitely** many indicator functions pointing to (without loss of generality) the elements of **finite** partition on Omega. Here, P_X maps a_i to the probability P(A_i) (note that to request a_i to differ each from the other is always possible).
[After [sec 2](#building--checking)] Moreover, the generated sigma-algebra is the minimal with these n events in it. 

## RV Criterion

Now that we have the definition, one asks himself how to build a random variable. 

The involved elements are basically 3:

- The measurable space (starting)
- The measurable space (arrival)
- The law of X

Thus, given a combination of this 3 elements, we first try to understand which coherence conditions make it a random variable.
That is: we look for a criterion that implies (and, possibily, is equivalent) to the combination being a RV.

Our first approach, is to take partial information about these elements, and find the conditions that the 5th needs to satisfy.

- Given only the spaces, there exist infinite laws for X for which X is a RV. Thus, we suppose that the law X is a given.
- Now, for X to be given, it must be so over a set. Thus, the only other objects we could giggle with are the structures. 

Thus, we have an objective: we suppose that we miss one of the two structures, and try to rebuild it.

### Missing F

Let us start from enquiring what conditions on the structure F, that of Omega, need to be satisfied: by definition of X, we just check that each inverse image of a set in the structure of E belongs to F.
Insiemistically,

1. Consider C, the collection of inverse images of sets in the structure of E
2. Then, X is an r.v. iff such collection is in the sigma-alg F.

One could observe that X^-1 is likely conserving the structure, thanks to its good compatibility with set operations. 
This holds: one verifies that C is a sigma-algebra. 
Thus, (2) can be evolved into something more precise:

1. Consider C, the so-called "sigma-alg induced by E throgh X"
2. Then, X is an r.v. iff the sigma-algebra of Omega is larger than C

That is, C is the minimal sigma-algebra of Omega allowing X to be an r.v.

### Missing E

We now do the same. Only, this time we use the direct image. 
Here, though, a technical problem arises: that the definition of a function is asymmetric, and thus X() is not as well-behaved. 
In particular, the set D of direct images does not preserve the structure, and is, generally, not a sigma-algebra. 

Otherwise said, the (rude) charchterization

1. Consider D, the collection of direct images of sets in the structure of F
2. Then, X is an r.v. iff E is a sigma-alg is in such collection.

won't work, since in general we cannot guarantee that X^-1(X(A)) is in F, for in F. 

The (banana) solution is the following, which modifies (1) in order to keep (2): since X is a r.v. iff for all sets in E we have that X^-1(B) is in F, we take D to be that of sets whose inverse image is in F. 
This is not a subsets nor contains the precedent D, but thanks to the usage of X^-1 inherits the sigma-alg structure. 
Thus, we also gain access to the precedent charachterization:

1. Consider D, the so-called "sigma-alg allowed by F throgh X"
2. Then, X is an r.v. iff the sigma-algebra of Omega is smaller than D

That is, D is the maximal sigma-algebra on E allowing X to be an r.v.

Actually, everything would work as before, if X was a bijection.

### NS Criterion to be a RV
<!-- NS stands for Necessary and Sufficient -->

Still, these are not conditions one would call *easy*. For one, we have to produce a sigma-algebra in order to make the check, and then check the inclusion, set by set. 

The main idea though is that, frequently, a pi-system generating the sigma-algebra furnishes all the information we really need, by minimality. 

If we had P generating F, then we would need to verify that $\sigma_{gen}(X)$ \subset F, which is not really a place where we could apply such $pi$-class. Rather: we should find a pi-sys for the $\sigma_{gen}(X)$. Sadly, even though its the set of counter images from a sigma-algebra, it is false that if K is a pi-sys for E, then {X^-1(B) for B \subset K} is a pi-syst for \sigma_{gen}(X) in general. Possibly some extensions are available with monotone classes. Still, that would require an algebra, which is a daunting task of its own. 

Let's now suppose that K, pi-sys, generates E. This looks much more promising. We need to verify that K is a subset of the allowed sigma-algebra, to make a criterion. That amounts to make the check which would be required by the definition of X, that counter images are "allowed", just for the pi-system.

For E=R, E=B, or multidimensional equivalent, it holds that it is sufficient to check for  (-inf,r], for all r.

### Pertinent info to \sigma(\cdot)

After [sec 1](#basic-cases) it should be clear that the generated sigma algebra depends heavily on the numerosity of E, as the allowed sigma algebra depends on that of F.

Moreover, one sees that 2 events that output the same value of X are, effectively, just one event: that is looking at the outputs of X one cannot establish the functional structure of X, but only its bijective structure (that is the one highlighted by the generated sigma algebra). 

## Construction of RV

The collection of Random Variables is closed under
- algebraic operations (linear combination,*,/)
- limiting procedures (sup (=>) limsup => inf,liminf,lim)
- transformations (g(X))

PROOFS - The key ingredient is the criterion, which allows for checks just on the generating pi-sys. 
To show the first point, the key is using equivalence between sets. For example: {X+Y<=t} = {X<=r}\cap{Y<=r-t}. In the case of the second, for sup the same holds (provided you accept countable intersections). limsup, is just a combination of inf and sup, as lim for a monotone sequence is nothing more than the inf: limsup = lim of sup = inf of sup. Fors transformations, you just need to know the explicit characheterization of the inverse of the composition of functions.

## Discrete RV

## Discrete Random Vectors

If X is a vector or r.v., then it is a r.v. of its own
Similarly, if X is a r.v., that is a "random vector", then each of its components is a r.v

=> X is a r.v. iff X_i is a r.v. for all i

We can relate the image laws. The image law of X determines that of X_i, where we fix the subvector we care about and sum all the other probabilities with different garbage-part as if we concentrated their prob: we are consdiering a partition of the set given by the directions we care about, which we do not "concentrate", but rather "differ the partition on". These are called marginal probabilities. (??)

Note that even though it is enough for X_i to be rv to say that X is, it is not enough to have P_Xi to retrievve P_X. 

<!-- to end -->