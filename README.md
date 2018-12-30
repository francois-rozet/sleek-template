# Sleek Template

Sleek Template is a modular LaTeX template.

It splits in three main parts : `main.tex`, `head.tex` and `titlepage.tex`.

## Main

`main.tex` is the actual `tex` file of the document where is written the `document` environment.

```latex
\begin{document}
...
\end{document}
```

It is `main.tex` that should be compiled in order to produce a `pdf` or a `dvi`.

## Head

`head.tex` is included in `main.tex` before the `document` environment.

```latex
\input{./include/head.tex}
...
\begin{document}
```

This file calls essential packages that setup style parameters of the document such as headers/footers, margins, fonts, etc.

It also defines a few commands :

* `\romantableofcontents` displays the table of contents in a new page while temporarily changing the page numbering to `roman`.

## Titlepage

`titlepage.tex` is included as first command in the `document` environment.

```latex
\begin{document}
\input{./include/titlepage.tex}
...
\end{document}
```

It creates the cover page of the document according to the filling of the followings above the `document` environment.

```latex
\def\logopath{}
\def\toptitle{}
\title{}
\def\subtitle{}
\def\authorhead{}
\author{}
\def\rightauthorhead{}
\def\rightauthor{}
\def\context{}
\date{}
```

Among these, only `\title{}`, `\author{}` and `\date{}` have to be filled in for the code to figure out what to output. However, none of these should stay empty. Prefer deleting or commenting the line if so.

## Languages

To set the languages of the document, the `\languages` variable has to be defined **before** the call to `head.tex`.

```latex
\def\languages{vietnamese, japanese, danish}
...
\input{./include/head.tex}
```

If not, languages will be set to `english` by default. It should be noted that the actual language of the document is defined by the last name of the chain, `danish` in the example.

If the actual language owns its own file in the [languages](./include/languages/) folder, this one will be automatically included. Therefore it can be used to modify further settings depending on the language.

## Libraries

The [libraries](./include/libraries/) folder contains additional libraries that can be included after `head.tex` if needed.

```latex
\input{./include/head.tex}

\input{./include/libraries/mathematics.tex}
\input{./include/libraries/units.tex}
```

Each library calls a few packages which are essential in their field. Some also configure new environments, commands or macros.

## Wiki

The [wiki](https://github.com/Donshel/sleek-template/wiki) acts both as a sleek-template features' wiki and a latex essential packages inventory.

## Authors

* **François Rozet** - [Donshel](https://github.com/Donshel)
