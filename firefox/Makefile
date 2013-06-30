all: xpi

xpi: install.rdf ../bo.dic ../bo.aff icon.png ../README
	@echo "Making xpi file for firefox..."
	@mkdir -p dictionaries && cp ../bo.dic ../bo.aff dictionaries
	@cp ../README .
	@zip -rq tibetan-spellchecker.xpi install.rdf icon.png dictionaries README
	@rm -rf dictionaries README
