 A set can be mentioned as amorphous if it is not the disjoint union of 2 infinite subsets.
 
## Disjoint Union
 - Indexed union
	 *i.e:* $\{1,2,3\} \sqcup \{3,4,5\} = \{\{1,0\},\{2,0\},\{3,0\},\{3,1\},\{4,1\},\{5,1\}\}$
	
	It may also be a union between disjoint sets

## Symmetric Set
- A nonempty subset of a group $G$ that contains the inverses of all its elements
	$S = S^{-1}$
## Permutation
- Defined as a bijection from a set to itself
	*ex:*
	$$
	\begin{flalign*}
	\pi&: S \rightarrow S \\
	S &= \{a,b,c\} \\
	\pi(a) &= b \\
	\pi(b) &= c \\
	\pi(c) &= a \\
	\end{flalign*}
	$$
	
## Permutation Group
A group whose elements are permutations of a set $M$ and whose operations are the composition of permutations.

# Structure
A structure is a set along with a collection of finitary operations and relations defined on it
# Model
For a given theory in model theory, a structure is called a model if it satisfies the defining axioms for that theory

## Axiom of Choice
Given a collection of non-empty sets, it is possible to construct a new set by choosing one element from each set.

# Fix
A permutation ($\pi$) on a set $S$ that fixes an element $x \in S$ permutes every element except $x$

A permutation fixing $x$:  
$\forall y \in S. y \ne x \implies \pi(y) = (\exists z \in S)$
$\pi(x) = x$
# Permutation Model
A model of set theory with atoms ([[ZFA]]) constructed using a [[Group]] of permutations on the atoms

Suppose $S$ is a set, $G$ is a group of permutations of $\mathbb{A}(S)$.
A [[Filter#Normal Filter | Normal Filter]] of $G$ is a collection $F$  $\forall x \in F. x \le G$
such that:
$$
\begin{flalign*}
&G \in F \\
&\forall a,b \in F. a \cap b \in F \\
&\forall H \le G. (\exists x \in H. x \in F) \implies H \in F \\
&\forall a \in F, b. (\exists g. gag^{-1} = b ) \implies b \in F \\
&\forall H \le G. (\forall \pi \in H. \exists a \in \mathbb{A}(S). \pi(a) = a) \implies H \in F
\end{flalign*}
$$


