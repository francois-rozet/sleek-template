# Sleek Template

Sleek Template is a collection of LaTeX packages and settings that ease the writing of beautiful documents.

All packages, settings, environments, commands and macros are explained and illustrated in the [wiki](https://github.com/Donshel/sleek-template/wiki). There is also a bunch of cool stuff like LaTeX tutorials and examples. Have a look !

## Options

The `sleek` package has three options :

* `parindent` restores the indentation of paragraphs' first line.
* `noheader` removes the document header.
* `french` changes the decimal sign and some captions.

```latex
\usepackage[parindent, french]{sleek}
```

## Title page

The title page is included as first command in the `document` environment.

```latex
\begin{document}
\maketitle
...
\end{document}
```

Sleek Template offers a modified title page in the package `sleek-title`. The title page presents the following informations :

```latex
\logo{}
\institute{}
\faculty{}
\department{}
\title{}
\subtitle{}
\author{}
\supervisor{}
\context{}
\date{}
```

Among these, only `\title{}`, `\author{}` and `\date{}` have to be filled. However, none of these should stay empty. Prefer deleting or commenting the line if so.

## Author

* **François Rozet** - [francois-rozet](https://github.com/francois-rozet)
