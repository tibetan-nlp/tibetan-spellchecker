all: oxt

FILES=dictionaries.xcu description.xml package-description.txt

oxt: $(FILES) ../README.md ../bo.dic ../bo.aff META-INF/manifest.xml
	@echo "Making oxt file for LibreOffice..."
	@mkdir -p dictionaries && cp ../bo.dic ../bo.aff dictionaries
	@cp ../README.md .
	@zip -rq tibetan-spellchecker.oxt dictionaries $(FILES) META-INF README.md

clean:
	@rm -rf dictionaries README.md tibetan-spellchecker.oxt
