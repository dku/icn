XML2RFC=./xml2rfc

DRAFTTXT=draft-icnrg-challenges.txt
SRC=draft-icnrg-challenges.xml
CURRENTVERSION=draft-irtf-icnrg-challenges-06.txt
PDFVERSION=$(patsubst %.txt, %.pdf, $(CURRENTVERSION))

all: $(DRAFTTXT)

release: $(CURRENTVERSION)


pdf: $(PDFVERSION)

$(CURRENTVERSION): $(DRAFTTXT)
	cp -f $< $@

$(DRAFTTXT): $(SRC)
	$(XML2RFC) $(SRC) $(DRAFTTXT)
#	$(XML2RFC) xml2rfc draft-netinf-proto.xml $(DRAFTTXT)
#	$(XML2RFC) draft-netinf-proto




clean:
	rm -f $(DRAFTTXT) *~


%.pdf : %.txt
	a2ps -1 -B --borders=0 -M a4 -R -columns=1 -l 72 $< -o- | ps2pdf - $@

