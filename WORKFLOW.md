# Digital notetaking workflow

## When to use

Use for short documentation of topics, lecture notes or exam preparation notes. For bigger reports either use one of the report templates or preferebly usea text editing software like word of libre-office.

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
