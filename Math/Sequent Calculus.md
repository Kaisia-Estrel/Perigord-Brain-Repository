Style of formal logic argumentation wherein each line of a proof is a conditional tautology

$$
\begin{prooftree}
\Axiom$A,X \fCenter\vdash Y,B$
\UnaryInf$X \fCenter\vdash Y, A \rightarrow B$
\end{prooftree}
$$
# Sequent Rules
## Negation
$$
\begin{prooftree}
\Axiom$A,X \fCenter\vdash Y$
\UnaryInf$X \fCenter\vdash Y, \lnot A$
\end{prooftree}
$$
$$
\begin{prooftree}
\Axiom$X \fCenter\vdash Y,A$
\UnaryInf$\lnot A, X \fCenter\vdash Y$
\end{prooftree}
$$
## Disjunction
$$
\begin{prooftree}
\Axiom$X \fCenter\vdash Y, A, B$
\UnaryInf$X \fCenter\vdash Y, A \lor B$
\end{prooftree}
$$
$$
\begin{prooftree}
\Axiom$A, B, X \fCenter\vdash Y$
\UnaryInf$A \lor B, X \fCenter\vdash Y$
\end{prooftree}
$$

# Example
## Law of excluded middle
$$\huge p \lor \lnot p$$

$$
\begin{prooftree}
\def\fCenter{\ \vdash\ }
\Axiom$A \fCenter A$
\UnaryInf$\fCenter A, \lnot A$
\UnaryInf$\fCenter A \lor \lnot A$
\end{prooftree}
$$


