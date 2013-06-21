all: xpi

FILES=dictionaries.xcu description.xml icon.png package-description.txt

xpi: $(FILES) ../bo.dic ../bo.aff META-INF/manifest.xml
	@echo "Making oxt file for LibreOffice..."
	@mkdir -p dictionaries && cp ../bo.dic ../bo.aff dictionaries
	@zip -rq tibetan-spellchecker.oxt dictionaries $(FILES) META-INF
	@rm -rf dictionaries
