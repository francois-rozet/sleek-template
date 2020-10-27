# Sleek Template

Sleek Template is a collection of [LaTeX](https://www.latex-project.org/) packages and settings that ease the writing of beautiful documents such as reports, articles, thesis, and more. It also features a fully automatic and modular title page (*e.g.* [`main.pdf`](main.pdf)).

All packages, settings, environments, commands and macros are explained and illustrated in the [wiki](https://github.com/Donshel/sleek-template/wiki). There is also a bunch of cool stuff like LaTeX tutorials and examples. Have a look!

## Overleaf :leaves:

Sleek Template is [Overleaf](https://www.overleaf.com/) ready!

1. Download the repository [archive](https://github.com/francois-rozet/sleek-template/archive/master.zip)
2. On your Overleaf project page, click **New Project** and choose **Upload Project**
3. Drag or select the downloaded archive
4. Remove the `README.md` and `main.pdf` files
5. Rename the project
6. Enjoy :ok_hand:

## Options

The [`sleek`](packages/sleek.sty) package has three options :

* `parindent` restores the indentation of paragraphs' first line.
* `noheader` removes the document header.
* `french` changes the decimal sign and some captions.

```latex
\usepackage[parindent, french]{packages/sleek}
```

## Title page

The title page is included as first command in the `document` environment.

```latex
\begin{document}
\maketitle
...
\end{document}
```

Sleek Template offers a modified title page in the package [`sleek-title`](packages/sleek-title.sty). The title page presents the following informations :

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
