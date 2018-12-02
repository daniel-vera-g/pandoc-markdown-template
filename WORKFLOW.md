# Digital notetaking workflow

## Features

* Use templates
* Latex for formatting and math options
* Markdown for handy use

## CI

* linting(Markdownlint)
* Grammar and spelling check
* pandoc to convert markdown files into pdf
	* `make`(local) or `docker` to automate conerting workflow

## Other

* Use Autokey or other text expander to insert fast images and other latex formating.

## Workflow

1. Write notes in latex(formating & math) and markdown(simple markup)
2. Convert them local to pdf using `make` and `pandoc`
3. Before pushing, use pre-push: markdownlint + grammarlint & spellinglint
4. On repository run CL with docker:	
	* Check if every file can be converted(with `make`) without errors
	* Optional check spelling, grammar and linting
