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

class01:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_01_Manuscript.pdf NT_Class_01_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_01_Handout.pdf NT_Class_01_Handout.md
	#decktape -s 1024x768 webslides NT_Class_01_Slides.html build/NT_Class_01_Slides.pdf

class02:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_02_Manuscript.pdf NT_Class_02_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_02_Handout.pdf NT_Class_02_Handout.md
	#decktape -s 1024x768 webslides NT_Class_02_Slides.html build/NT_Class_02_Slides.pdf

class03:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_03_Manuscript.pdf NT_Class_03_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_03_Handout.pdf NT_Class_03_Handout.md
	#decktape -s 1024x768 webslides NT_Class_03_Slides.html build/NT_Class_03_Slides.pdf

class04:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_04_Manuscript.pdf NT_Class_04_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_04_Handout.pdf NT_Class_04_Handout.md
	#decktape -s 1024x768 webslides NT_Class_04_Slides.html build/NT_Class_04_Slides.pdf

class05:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_05_Manuscript.pdf NT_Class_05_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_05_Handout.pdf NT_Class_05_Handout.md
	#decktape -s 1024x768 webslides NT_Class_05_Slides.html build/NT_Class_05_Slides.pdf

class06:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_06_Manuscript.pdf NT_Class_06_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_06_Handout.pdf NT_Class_06_Handout.md
	#decktape -s 1024x768 webslides NT_Class_06_Slides.html build/NT_Class_06_Slides.pdf

class07:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_07_Manuscript.pdf NT_Class_07_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_07_Handout.pdf NT_Class_07_Handout.md
	#decktape -s 1024x768 webslides NT_Class_07_Slides.html build/NT_Class_07_Slides.pdf

class08:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_08_Manuscript.pdf NT_Class_08_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_08_Handout.pdf NT_Class_08_Handout.md
	#decktape -s 1024x768 webslides NT_Class_08_Slides.html build/NT_Class_08_Slides.pdf

class09:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_09_Manuscript.pdf NT_Class_09_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_09_Handout.pdf NT_Class_09_Handout.md
	#decktape -s 1024x768 webslides NT_Class_09_Slides.html build/NT_Class_09_Slides.pdf

class10:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_10_Manuscript.pdf NT_Class_10_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_10_Handout.pdf NT_Class_10_Handout.md
	#decktape -s 1024x768 webslides NT_Class_10_Slides.html build/NT_Class_10_Slides.pdf

class11:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_11_Manuscript.pdf NT_Class_11_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_11_Handout.pdf NT_Class_11_Handout.md
	#decktape -s 1024x768 webslides NT_Class_11_Slides.html build/NT_Class_11_Slides.pdf

class12:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_12_Manuscript.pdf NT_Class_12_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_12_Handout.pdf NT_Class_12_Handout.md
	#decktape -s 1024x768 webslides NT_Class_12_Slides.html build/NT_Class_12_Slides.pdf

class13:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_13_Manuscript.pdf NT_Class_13_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_13_Handout.pdf NT_Class_13_Handout.md
	#decktape -s 1024x768 webslides NT_Class_13_Slides.html build/NT_Class_13_Slides.pdf

class14:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_14_Manuscript.pdf NT_Class_14_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_14_Handout.pdf NT_Class_14_Handout.md
	#decktape -s 1024x768 webslides NT_Class_14_Slides.html build/NT_Class_14_Slides.pdf

class15:
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_15_Manuscript.pdf NT_Class_15_Manuscript.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $(BDIR)/NT_Class_15_Handout.pdf NT_Class_15_Handout.md
	#decktape -s 1024x768 webslides NT_Class_15_Slides.html build/NT_Class_15_Slides.pdf

.PHONY: clean

clean :
	rm -rf $(BDIR)
	mkdir -p $(BDIR)/
	cp -r $(RJSDIR) $(BDIR)/
