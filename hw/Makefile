TEXINPUTS:=.

CLASS_HW=\
	pdf/2023-01-25-class.pdf \
	pdf/2023-01-27-class.pdf

HW=$(CLASS_HW)

.PHONY: all copy
all: $(HW)

pdf/%.pdf: tex/%.tex
	xelatex -output-dir pdf $<
	xelatex -output-dir pdf $<

clean:
	rm -f pdf/*.aux pdf/*.log pdf/*.out
	rm -f pdf/*.nav pdf/*.snm pdf/*.toc 
	rm -f pdf/*.vrb

distclean: clean
	rm -f pdf/*.pdf

copy:
	mkdir -p ../web/hw
	cp $(HW) ../web/hw
