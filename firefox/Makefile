all: xpi

xpi: install.rdf ../bo.dic ../bo.aff icon.png
	@echo "Making xpi file for firefox..."
	@mkdir -p dictionaries && cp ../bo.dic ../bo.aff dictionaries
	@zip -rq tibetan-spellchecker.xpi install.rdf icon.png dictionaries
	@rm -rf dictionaries README
