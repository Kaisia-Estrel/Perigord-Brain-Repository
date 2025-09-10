# Entry Types

|               |                |              |
| ------------- | -------------- | ------------ |
| article       | book           | mvbook       |
| inbook        | bookinbook     | suppbook     |
| booklet       | collection     | mvcollection |
| incollection  | suppcollection | manual       |
| misc          | online         | patent       |
| periodical    | suppperiodical | proceedings  |
| mvproceedings | inproceedings  | reference    |
| mvreference   | inreference    | report       |
| set           | thesis         | unpublished  |
| custom        | conference     | electronic   |
| masterthesis  | phdthesis      | techreport   |
# Entry Fields
|               |              |               |                 |
| ------------- | ------------ | ------------- | --------------- |
| abstract      | addendum     | afterword     | annotate        |
| author        | authortype   | bookauthor    | bookpagination  |
| booksubtitle  | booktitle    | chapter       | commentator     |
| date          | doi          | edition       | editor          |
| editortype    | eid          | entrysubtype  | eprint          |
| eprinttype    | eprintclass  | eventdate     | eventtitle      |
| file          | foreword     | holder        | howpublished    |
| indextitle    | institution  | introduction  | isan            |
| isbn          | ismn         | isrn          | issue           |
| issuesubtitle | issuetitle   | iswc          | journalsubtitle |
| journaltitle  | label        | language      | library         |
| location      | mainsubtitle | maintitle     | month           |
| note          | number       | organization  | origdate        |
| origlanguage  | origlocation | origpublisher | origtitle       |
| pages         | pagetotal    | pagination    | part            |
| publisher     | pubstate     | reprinttitle  | series          |
| shortauthor   | shortedition | shorthand     | shorthandintro  |
| shortjournal  | shortseries  | shorttitle    | subtitle        |
| title         | translator   | type          | url             |
| venue         | version      | volume        | year            |
# Citation Format
```bibliography
@article{einstein,
    author = "Albert Einstein",
    title = "{Zur Elektrodynamik bewegter K{\"o}rper}. ({German})
    [{On} the electrodynamics of moving bodies]",
    journal = "Annalen der Physik",
    volume = "322",
    number = "10",
    pages = "891--921",
    year = "1905",
    DOI = "http://dx.doi.org/10.1002/andp.19053221004",
    keywords = "physics"
}

@book{dirac,
    title = {The Principles of Quantum Mechanics},
    author = {Paul Adrien Maurice Dirac},
    isbn = {9780198520115},
    series = {International series of monographs on physics},
    year = {1981},
    publisher = {Clarendon Press},
    keywords = {physics}
}

@online{knuthwebsite,
    author = "Donald Knuth",
    title = "Knuth: Computers and Typesetting",
    url  = "http://www-cs-faculty.stanford.edu/~uno/abcde.html",
    addendum = "(accessed: 01.09.2016)",
    keywords = "latex,knuth"
}

@inbook{knuth-fa,
    author = "Donald E. Knuth",
    title = "Fundamental Algorithms",
    publisher = "Addison-Wesley",
    year = "1973",
    chapter = "1.2",
    keywords  = "knuth,programming"
}
...
```

# Biblatex

Cheatsheet: https://tug.ctan.org/info/biblatex-cheatsheet/biblatex-cheatsheet.pdf

# Natbib
You may specify `\usepackage[natbib=true]{biblatex}` to use `natbib` commands in `biblatex`.

- `citep` - cite parenthetical, `citet` - cite textual

|                             |     |                                    |
| --------------------------- | --- | ---------------------------------- |
| \citet{jon90}               | --> | Jones et al. (1990)                |
| \citet[chap. 2]{jon90}      | --> | Jones et al. (1990, chap. 2)       |
| \citep{jon90}               | --> | (Jones et al., 1990)               |
| \citep[chap. 2]{jon90}      | --> | (Jones et al., 1990, chap. 2)      |
| \citep[see][]{jon90}        | --> | (see Jones et al., 1990)           |
| \citep[see][chap. 2]{jon90} | --> | (see Jones et al., 1990, chap. 2)  |
| \citet*{jon90}              | --> | Jones, Baker, and Williams (1990)  |
| \citep*{jon90}              | --> | (Jones, Baker, and Williams, 1990) |


http://merkel.texture.rocks/Latex/natbib.php
