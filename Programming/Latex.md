# Tips
- Use`\pagenumbering{gobble}` to remove page numbering.
- with the `blindtext` package, use `\blindtext[n]` to generate sample text. `n` for repititions. Use `\Blindtext[n][m]` to generate `n` paragraphs of `m` repitition.
- Use ` \usepackage[margin=0.25in]{geometry}` to set margins
- use `\today` to get the current date.
- add `\noindent\rule{\linewidth}{0.4pt}` to get a horizontal line.
- use longtable for tables that span pages
# Tables
use `\multicolumn`
# Text formatting
- `\textbf{}` for **bold**
- `\underline{}` for underline
- `\textit{}` for *italics*
- `\texttt{}` for `monospace`, `\verb||` is also useable. "tt" is abbreviation for "teletype".
![[Pasted image 20250406194512.png]]
- medium:`\textmd{Sample Text 0123}`
	- toggle: `\mdseries`
	![F-textmd.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/1/1d/F-textmd.png)
- bold:`\textbf{Sample Text 0123}`|
	- toggle: `\bfseries`
	![F-textbf.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/3/31/F-textbf.png)
- upright:`\textup{Sample Text 0123}`
	- toggle:  `\upshape`
	![F-textrm.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/4/48/F-textrm.png)
- italic:`\textit{Sample Text 0123}`
	- toggle:`\itshape`
	![F-textit2.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/e/e3/F-textit2.png)
- slanted:`\textsl{Sample Text 0123}`
	- toggle: `\slshape`
	![F-textsl.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/2/29/F-textsl.png)
- small caps:`\textsc{Sample Text 0123}`
	- toggle: `\scshape`
	![F-textsc.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/e/ee/F-textsc.png)
- serif (roman): `\textrm{Sample Text 0123}`
	- toggle: `\rmfamily`
	![F-textrm.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/4/48/F-textrm.png)
- sans serif:`\textsf{Sample Text 0123}`
	- toggle: `\sffamily`
	![F-textsf.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/e/e3/F-textsf.png)
- typewriter (monospace):`\texttt{Sample Text 0123}`|
	- toggle: `\ttfamily`
	![F-texttt.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/0/01/F-texttt.png)
  
## \emph{}
Text can be emphasized using the `\emph` command. Sometimes the `\emph` command behaves just as `\textit`, but is not exactly the same.

What the `\emph` command actually does with its argument depends on the context—inside normal text the emphasized text is italicized, but this behaviour is reversed if used inside an italicized text—see example above. Moreover, some packages, e.g. [Beamer](https://www.overleaf.com/learn/latex/Beamer "Beamer"), change the behaviour of the `\emph` command

## Lists
with `\begin{itemize}`, the command is much more complex: https://www.overleaf.com/learn/latex/Lists
`\begin{enumerate}` for numbered lists.
`\begin{description}` for lists without labels.
### Enumitem
add package `enumitem` to specify custom label: 
- `\arabic*` will be replaced by the list number. `\roman*` and `\alph*` to use roman numerals or letters respectively 
- `\begin{enumerate}[label*=_]` to add extra items in front of the previous label. Simulate nested numbering with `\begin{enumerate}[label*=\arabic*.]`

Use the following code sample to automatically set nesting numbering
```latex
\renewcommand{\labelenumii}{\arabic{enumi}.\arabic{enumii}}
\renewcommand{\labelenumiii}{\arabic{enumi}.\arabic{enumii}.\arabic{enumiii}}
\renewcommand{\labelenumiv}{\arabic{enumi}.\arabic{enumii}.\arabic{enumiii}.\arabic{enumiv}}
```

# Tikzpicture
## \node
arguments
- draw: ??
- circle 
- line width: `pt` or `mm`, can also be replaced with predefined thickness levels:
```latex
\draw[ultra thin] (0,0) -- (2,0);
\draw[very thin] (0,0.5) -- (2,0.5);
\draw[thin] (0,1) -- (2,1);
\draw[semithick] (0,1.5) -- (2,1.5);
\draw[thick] (0,2) -- (2,2);
\draw[very thick] (0,2.5) -- (2,2.5);
\draw[ultra thick] (0,3) -- (2,3);

```
- specifying colors alone changes the stroke color, specify `fill` to change fill color

# Math
- `\frac{}{}` to define fractions
- `\binom{}{}` to put numbers on top of each other $\binom{a}{b}$, (requires `amsmath`)
- import `amsmath` and use `\begin{align*}` to align equations along `&=`
# Citations
```latex
\usepackage{biblatex} %Imports biblatex package
\addbibresource{sample.bib} %Import the bibliography file
\printbibliography %Prints bibliography
```
[Further Reference on #Biblatex](Biblatex.md)

# Figure
| Parameter | Position                                                                                                                                                               |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| h         | Place the float _here_, i.e., _approximately_ at the same point it occurs in the source text (however, not _exactly_ at the spot)                                      |
| t         | Position at the _top_ of the page.                                                                                                                                     |
| b         | Position at the _bottom_ of the page.                                                                                                                                  |
| p         | Put on a special _page_ for floats only.                                                                                                                               |
| !         | Override internal parameters LaTeX uses for determining "good" float positions.                                                                                        |
| H         | Places the float at precisely the location in the LaTeX code. Requires the `float` package, though may cause problems occasionally. This is somewhat equivalent to h!. |
- use `wrapfigure` to wrap text around a figure
# Color
the package `xcolor` adds the ability to color various elements of your document.
## \definecolor{\<name\>}{\<values\>}
`<values>` can be a single value `0.0 - 1.0`, or `rgb` values `{r,g,b}`

# Code Blocks
use package `minted`to use `\begin{minted}{<language>}` for more advanced syntax highlighting in codeblocks, requires the python package `Pygments`.
- use the option `[linenos]` to specify line numbers.
- use the option `[bgcolor=]`
- use `\begin{verbatim}` instead for simple code blocks.
You can also use the package `fancyvrb` to improve or extend verbatim environments
```latex
\DefineVerbatimEnvironment{CodeVerbatim}{Verbatim}{bgcolor=LightGray}
```
# Latex Commands
- `\overline{A}`: $\overline{A}$
- `\mathbb{A}`: $\mathbb{A}$
# Latex Symbols
- `\land`: $\land$
- `\lor`: $\lor$
- `\lnot`: $\lnot$
- `\oplus`(exclusive or): $\oplus$
- `\implies`: $\implies$
- `\impliedby`: $\impliedby$
- `\iff`: $\iff$
- `\varnothing`: $\varnothing$
- `\in`: $\in$
- `\notin`: $\notin$
- `\leftrightarrow` $\leftrightarrow$
- `\leftarrow` $\leftarrow$
- `\rightarrow` $\rightarrow$
- `\cup`: $\cup$
- `\cap`: $\cap$
- `\sqcup`: $\sqcup$
- `\supset`: $\supset$
- `\supseteq`: $\supseteq$
- `\subset`: $\subset$
- `\subseteq`: $\subseteq$
- `\complement`: $\complement$
- `\wp`: $\wp$
- `\le`: $\le$
- `\ge`: $\ge$
- `\cong`: $\cong$
- `\equiv`: $\equiv$
- `\ne`: $\ne$
- `\vdash`: $\vdash$
- `\bot`: $\bot$