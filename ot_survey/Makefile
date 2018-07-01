PANDOC=/usr/bin/pandoc
PANDOC_OPTIONS=--smart --standalone
PANDOC_PDF_OPTIONS=-V geometry:margin=1in

# Targets and dependencies
.PHONY: clean homework

all : clean homework

clean :
	- $(RM) $(EXPORTED_DOCS)

class01 :
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o Class_01.pdf Class_01_Handout.md

