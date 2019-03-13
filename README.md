# Sleek Template

Sleek Template is a modular LaTeX template.

It splits in three main parts : `main.tex`, [title pages](#title-pages) and [libraries](#libraries).

## Main

`main.tex` is the actual `tex` file of the document where is written the `document` environment.

```latex
\begin{document}
...
\end{document}
```

It is `main.tex` that should be compiled in order to produce a `pdf` or a `dvi`.

## Title pages

The title page is included as first command in the `document` environment.

```latex
\begin{document}
\input{./include/titlepages/default.tex}
...
\end{document}
```

> Sleek Template offers a `default` title page. However, feel free to add your own.

#### Default

The `default` title page creates the cover page of the document according to the filling of the followings above the `document` environment.

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

## Libraries

The [libraries](./include/libraries/) are included in `main.tex` before the `document` environment.

```latex
\input{./include/libraries/default.tex}
\input{./include/libraries/mathematics.tex}
\input{./include/libraries/units.tex}
...
\begin{document}
```

Each library calls a few packages which are essential in their field. Some also modify style settings or configure new environments, commands or macros.

> These features are explained and illustrated in the [wiki](https://github.com/Donshel/sleek-template/wiki). There is also a bunch of cool stuff like LaTeX tutorials and examples. Have a look !

It is not mandatory to include them. Precisely, it's a better habit to include only needed libraries.

> Since it is the core of this template, `default` library should always be included.

> `bibliography` library has to be included before `default`.

## Languages

To set the languages of the document, the `\languages` variable has to be defined **before** the call to the `default` library.

```latex
\def\languages{vietnamese, japanese, danish}
...
\input{./include/libraries/default.tex}
```

If not, languages will be set to `english` by default. It should be noted that the actual language of the document is defined by the last name of the chain, `danish` in the example.

If the actual language owns its own file in the [languages](./include/languages/) folder, this one will be automatically included. Therefore it can be used to modify further settings depending on the language.

## Authors

* **François Rozet** - [Donshel](https://github.com/Donshel)
