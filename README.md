# orcidlink-LaTeX-command
LaTeX style file to add a macro for inserting a linked ORCiD logo

This LaTeX style file just defines a single macro, `\orcidlink`.  The code is from [this TeX.SE answer](https://tex.stackexchange.com/a/445583/34063).  My contribution was wrapping it into a style file (and improving the fragility of the command a bit).

Installation
------------

If `orcidlink` is already provided in your TeX distribution, skip this
section.  You should be able to install `orcidlink` [from the CTAN](https://www.ctan.org/pkg/orcidlink) via
your distribution's utility (e.g. the TeX Live Utility).
Alternatively, you can get the package from the [source repository on
GitHub](https://github.com/duetosymmetry/orcidlink-LaTeX-command).  If
you do not want to do a "full" installation, just copy
[orcidlink.sty](orcidlink.sty) into the same directory as your LaTeX
source.

Usage
-----

In your preamble, add:
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

Dependancies and Compatibility
------------------------------

This package relies on the following packages:
- [hyperref](https://www.ctan.org/pkg/hyperref)
- [tikz](https://www.ctan.org/pkg/pgf)

All of these packages are included in the popular [TeX Live](https://www.tug.org/texlive/) distribution, so most users should not have to install anything new.

If you want to pass options to either of these packages, load them
before you load `orcidlink`. Similarly, if you want to specify options
to e.g. `xcolor`, load `xcolor` before loading `tikz` or `orcidlink`.

Credits
-------

The original TikZ icon code was created by user [Milo on
TeX.SE](https://tex.stackexchange.com/users/128068/milo).
This package was created and is maintained by [Leo
C. Stein](http://duetosymmetry.com/), (c) 2019-2023.
This material is subject to the [LaTeX Project Public License
1.3c](https://www.ctan.org/license/lppl1.3).
