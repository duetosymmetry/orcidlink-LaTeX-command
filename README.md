# orcidlink-LaTeX-command
LaTeX style file to add a macro for inserting a linked ORCiD logo

This LaTeX style file just defines a single macro, `\orcidlink`.  The code is from [this TeX.SE answer](https://tex.stackexchange.com/a/445583/34063).  My only contribution was wrapping it into a style file.

Usage
-----

Just copy [orcidlink.sty](orcidlink.sty) into the same directory as your LaTeX source.  Then in your preamble, add:
```latex
\usepackage{orcidlink}
```
When you want to insert the hyperlinked ORCiD logo, use `\orcidlink{0000-0000-0000-0000}`, replacing the digits with your ORCiD (just the digits, not your whole URL).  This is most common in the author list.  For example, in a revtex article, you would write e.g.
```latex
\author{Emmy Noether\,\orcidlink{0000-0000-0000-0000}}
...
```
This will appear as a clickable hyperlink, and will look like this:
![Author LaTeX render preview image](https://raw.githubusercontent.com/duetosymmetry/orcidlink-LaTeX-command/f03c85cd9fe3e40bec5f51b1319b0e9ab30c2e09/preview.png)

Dependancies
------------

This package relies on the following packages:
- [hyperref](https://www.ctan.org/pkg/hyperref)
- [scalerel](https://www.ctan.org/pkg/scalerel)
- [tikz](https://www.ctan.org/pkg/pgf)

All of these packages are included in the popular [TeX Live](https://www.tug.org/texlive/) distribution, so most users should not have to install anything new.
