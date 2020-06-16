DEST_DIR :=$(shell dirname $(realpath $(firstword $(MAKEFILE_LIST))))
SRC_DIR = themes/beamercolorthemeapertus.sty themes/beamerfontthemeapertus.sty themes/beamerinnerthemeapertus.sty themes/beamerthemeapertus.sty

all: phaseI_firstHalf.pdf

phaseI_firstHalf.pdf: phaseI_firstHalf.tex
	cp -f $(SRC_DIR) $(DEST_DIR)
	rubber -d $<

clean:
	rm -rf beamer* *.aux *.log *.nav *.out *.snm *.toc
