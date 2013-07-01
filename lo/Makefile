all: oxt

FILES=dictionaries.xcu description.xml icon.png package-description.txt

oxt: $(FILES) ../README ../bo.dic ../bo.aff META-INF/manifest.xml
	@echo "Making oxt file for LibreOffice..."
	@mkdir -p dictionaries && cp ../bo.dic ../bo.aff dictionaries
	@cp ../README .
	@zip -rq tibetan-spellchecker.oxt dictionaries $(FILES) META-INF README

clean:
	@rm -rf dictionaries README tibetan-spellchecker.oxt
