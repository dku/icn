XML2RFC=xml2rfc

DRAFTTXT=draft-icnrg-challenges.txt
SRC=draft-icnrg-challenges.xml
CURRENTVERSION=draft-kutscher-icnrg-challenges-01.txt

all: $(DRAFTTXT)

release: $(CURRENTVERSION)

$(CURRENTVERSION): $(DRAFTTXT)
	cp -f $< $@

$(DRAFTTXT): $(SRC)
	xml2rfc $(SRC) $(DRAFTTXT)
#	$(XML2RFC) xml2rfc draft-netinf-proto.xml $(DRAFTTXT)
#	$(XML2RFC) draft-netinf-proto




clean:
	rm -f $(DRAFTTXT) *~


