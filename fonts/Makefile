INSTALL = install -p

tfmpath = $(TEXMFHOME)/fonts/tfm/adobe/AGaramondPro
vfpath = $(TEXMFHOME)/fonts/vf/adobe/AGaramondPro
pfbpath = $(TEXMFHOME)/fonts/type1/adobe/AGaramondPro
mappath = $(TEXMFHOME)/fonts/map/dvips/adobe
encpath = $(TEXMFHOME)/fonts/enc/dvips/adobe
stypath = $(TEXMFHOME)/tex/latex/adobe

install:
	$(INSTALL) -d $(tfmpath)
	$(INSTALL) -d $(vfpath)
	$(INSTALL) -d $(pfbpath)
	$(INSTALL) -d $(mappath)
	$(INSTALL) -d $(encpath)
	$(INSTALL) -d $(stypath)
	$(INSTALL) AGaramondPro/LY1--AGaramondPro*.tfm $(tfmpath)
	$(INSTALL) AGaramondPro/LY1--AGaramondPro*.vf $(vfpath)
	$(INSTALL) AGaramondPro/AGaramondPro*.pfb $(pfbpath)
	$(INSTALL) AGaramondPro/AGaramondPro.map $(mappath)
	$(INSTALL) AGaramondPro/a_*.enc $(encpath)
	$(INSTALL) AGaramondPro/{AGaramondPro.sty,*AGaramondPro*.fd} $(stypath)
	texhash $(TEXMFHOME)
	updmap --enable Map=$(mappath)/AGaramondPro.map

uninstall:
	rm -f $(tfmpath)/LY1--AGaramondPro*.tfm
	rm -f $(vfpath)/LY1--AGaramondPro*.vf
	rm -f $(pfbpath)/AGaramondPro*.pfb
	rm -f $(mappath)/AGaramondPro.map
	rm -f $(encpath)/a_*.enc
	rm -f $(stypath)/{AGaramondPro.sty,*AGaramondPro*.fd}
	texhash $(TEXMFHOME)
	updmap --disable $(mappath)/AGaramondPro.map

