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

class04:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_04_Manuscript.pdf OT_Class_04_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_04_Handout.pdf OT_Class_04_Handout.md
	decktape -s 1024x768 webslides OT_Class_04_Slides.html build/OT_Class_04_Slides.pdf

class05:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_05_Manuscript.pdf OT_Class_05_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_05_Handout.pdf OT_Class_05_Handout.md
	decktape -s 1024x768 webslides OT_Class_05_Slides.html build/OT_Class_05_Slides.pdf

class06:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_06_Manuscript.pdf OT_Class_06_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_06_Handout.pdf OT_Class_06_Handout.md
	decktape -s 1024x768 webslides OT_Class_06_Slides.html build/OT_Class_06_Slides.pdf

class07:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_07_Manuscript.pdf OT_Class_07_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_07_Handout.pdf OT_Class_07_Handout.md
	decktape -s 1024x768 webslides OT_Class_07_Slides.html build/OT_Class_07_Slides.pdf

class08:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_08_Manuscript.pdf OT_Class_08_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_08_Handout.pdf OT_Class_08_Handout.md
	decktape -s 1024x768 webslides OT_Class_08_Slides.html build/OT_Class_08_Slides.pdf

class09:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_09_Manuscript.pdf OT_Class_09_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_09_Handout.pdf OT_Class_09_Handout.md
	decktape -s 1024x768 webslides OT_Class_09_Slides.html build/OT_Class_09_Slides.pdf

class10:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_10_Manuscript.pdf OT_Class_10_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_10_Handout.pdf OT_Class_10_Handout.md
	decktape -s 1024x768 webslides OT_Class_10_Slides.html build/OT_Class_10_Slides.pdf

class11:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_11_Manuscript.pdf OT_Class_11_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/OT_Class_11_Handout.pdf OT_Class_11_Handout.md
	decktape -s 1024x768 webslides OT_Class_11_Slides.html build/OT_Class_11_Slides.pdf

.PHONY: clean

clean :
	rm -rf $(BDIR)
	mkdir -p $(BDIR)/
	cp -r $(RJSDIR) $(BDIR)/
