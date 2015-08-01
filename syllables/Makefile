bo.dic:
	wc -l *.txt |grep total | cut -d' ' -f2 > bo.dic
	cat *.txt >> bo.dic

test: bo.dic
	@echo "All the following lines should be stars:"
	hunspell -d bo -a tests/pass.txt
	@echo "None the following lines should be stars:"
	hunspell -d bo -a tests/fail.txt
