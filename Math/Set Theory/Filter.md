A filter on a set $X$ is a non-empty collection of $F$ subsets of $X$ that satisfies the following properties:
- $\emptyset \notin F$
- $A \in F \land A \subseteq B \subseteq X \implies B \in F$ 
	(closure under supersets)
- $A,B \in F \implies A \cap B \in F$
	(closure under intersection)

A generalization: a filter is a set which has a lower bound and which contains anything larger than those lower bounds.

The above definition is a specialization utilizing subset relationships as ordering
$a < b \iff a \subset b$

A subset $F$ of a partially ordered set $(P, \le)$ is a filter or a dual ideal if the following are satisfied
- Downwards Directness - Every subset of $F$ has a lower bound
	$|F| \ne \varnothing$
	$\forall x,y \in F. \exists z \in F. z \le x \land z \le y$
- Upwards Closure 
	$\forall x \in F, p \in P. x \le p \implies p \in F$

![[Pasted image 20250916093034.png]]
The picture above shows a subset of integers ordered by divisibility

- Green - Filter
- Dark Green - Ultrafilter

## Examples:
- The collection of all subsets of $X$ which contain a fixed element $x \in X$

## Cofiniteness
A cofinite subset is an example of a filter

A cofinite subset of a set $X$ is a subset $A$ whose complement in $X$ is a finite set

