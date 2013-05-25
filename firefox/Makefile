all: xpi

xpi:
	@echo "Making xpi file for firefox..."
	@mkdir -p dictionaries && cp ../bo*.dic ../bo*.aff dictionaries
	@zip -rq tibetan-spellchecker.xpi install.rdf dictionaries
	@rm -rf dictionaries
