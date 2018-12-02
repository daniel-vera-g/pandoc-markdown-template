.PHONY: typeset

typeset:
	pandoc                          \
	  --from         markdown       \
	  --to           latex          \
	  --template     template.tex   \
	  --out          assignment-toc.pdf \
	  --latex-engine   xelatex        \
	  assignment-toc.md
