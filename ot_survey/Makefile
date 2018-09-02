PANDOC=/usr/bin/pandoc
PANDOC_OPTIONS=--standalone
PANDOC_PDF_OPTIONS=--template pdf.template --data-dir ./ -V geometry:margin=1in -V fontsize:12pt -V linestretch:1.25 --pdf-engine=xelatex
PANDOC_SLIDE_OPTIONS=-s --mathjax -i -t revealjs --template revealjs.template --data-dir ./ -V theme=white -V slideNumber='c/t' -V transition:convex

BDIR=build
RJSDIR=reveal.js

## Markdown extension (e.g. md, markdown, mdown).
MEXT = md

# All markdown files in the working directory
MAN_SRC = $(wildcard *_Manuscript.$(MEXT))
HAND_SRC = $(wildcard *_Handout.$(MEXT))
SLIDE_SRC = $(wildcard *_Slides.$(MEXT))

MANUSCRIPTS=$(MAN_SRC:.md=.pdf)
HANDOUTS=$(HAND_SRC:.md=.pdf)
SLIDES=$(SLIDE_SRC:.md=.html)

# I'm a MakeFile N00b so I'm documenting more than I need so I ensure I understand/can later remember what is going on.

# - Make, with no arguments, will execute the first target in the file (this is why we often put all first)
# - the files after the : in the target definition tell make that it should run if any of those change

# targets for all, manuscripts, handouts, slides
all: clean manuscripts handouts slides
manuscripts: $(MANUSCRIPTS)
handouts: $(HANDOUTS)
slides: $(SLIDES)

%.pdf : %.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/$@ $<

%.html : %.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_SLIDE_OPTIONS) -o $(BDIR)/$@ $<

.PHONY: clean

clean :
	rm -rf $(BDIR)
	mkdir -p $(BDIR)/
	cp -r $(RJSDIR) $(BDIR)/
