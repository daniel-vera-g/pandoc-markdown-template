# Pandoc Markdown template

This repository is a small collection of personal Markdown templates for Pandoc.

Each directory contains a working template and example PDF output.

## Requirements

Be sure to have LaTeX ([Windows](http://miktex.org/), [OS X](https://tug.org/mactex/),
[Linux](http://latex-project.org/)) and Pandoc installed.

On macOS, Pandoc can be installed with Homebrew: `brew install pandoc`.

For typesetting you can either use the `Makefile`s with `make` or just use `pandoc`.

For the `report-bib` you will need `pandoc-citeproc` too. On macOS that is easily installed with
`brew install pandoc-citeproc`.

## Customization

If you want to see what Pandoc allows for customization you can use `pandoc -D latex` to get the
default LaTeX template. You can set variables with `-V/--variable` when using `pandoc` or preferably
put them into a [YAML front matter](http://assemble.io/docs/YAML-front-matter.html).

## TODO

* Fix make scripts
* Customize Templates
* Create pre-commit linting for markdown files || Travis CI to test pandoc convertion 
	* Check for grammar errrors
	* convert to pdf
	* Markdown linting
	* Latex linting ...
* Customize Templates
* report and report-lib


### TO-CHECK

* `pandoc: Could not parse YAML header: mapping values are not allowed in this context "source" (line 4, column 6) -> When adding `\usepackage[margin=0.5in]{geometry}`to the YAML header
* Documentclass article in template for report
* % Fix \tightlist error
\def\tightlist{} -> In template
* \usepackage{graphicx} -> In template for images
* \begin{figure}[H]
  \includegraphics[width=\linewidth]{./img/Vektoren_2.jpg}
\end{figure} -> for right aligned immages
* Script create pdf -> pandoc -o vektorielle-geometrie-new.pdf vektorielle-geometrie-new.md --template=template.tex --latex-engine=xelatex

