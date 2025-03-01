#Time-stamp: <2008-10-23 23:39:09 hamada>
TARGET = hpcasia
TEX = platex



all : $(TARGET).ps


$(TARGET).dvi : $(TARGET).tex
	platex $(TARGET).tex
	platex $(TARGET).tex
	platex $(TARGET).tex

$(TARGET).ps : $(TARGET).dvi
	pdvips $(TARGET).dvi


$(TARGET).pdf: $(TARGET).ps
	ps2pdf $(TARGET).ps
	cp $(TARGET).pdf ~/

s : $(TARGET).dvi
	pxdvi $(TARGET).dvi &

p : $(TARGET).ps
	kghostview $(TARGET).ps

pdf: $(TARGET).pdf
	cp $(TARGET).pdf ~/

#	xdvi $(TARGET).dvi &

c : clean


clean:
	rm -f $(TARGET).{ps,pdf,dvi,aux,log,bbl,blg} *~ .*~


