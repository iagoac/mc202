###############################################################################################
######################### Compilação com suporte a múltiplos arquivos #########################
###############################################################################################

.PHONY: build clean

PDF=1
LAB = 01
MAX_TST = 6

.PHONY: preparar_ambiente

# make preparar_ambiente PDF=2 LAB=02 MAX_TST=6
preparar_ambiente:
	mkdir -p $(LAB) ; \
	mkdir -p $(LAB)/testes ; \
	cat Patterns/makefile.txt >> $(LAB)/Makefile ; \
	cat Patterns/pattern.txt >> $(LAB)/lab$(LAB).c ; \

	curl "https://raw.githubusercontent.com/iagoac/mc202/master/exercicios_laboratorio/Lab_$(PDF)_202.pdf" --output $(LAB)/Lab_$(LAB).pdf ; \

	for i in $(shell seq -f "%02g" 1 $(MAX_TST)) ; do \
		echo "\033[1;34mBaixando arquivos de teste #$$i\033[0m" ; \
		for ext in .in .res ; do \
			url=https://susy.ic.unicamp.br:9999/mc202defg/$(LAB)/dados/arq$$i$$ext ; \
			echo "$(LAB)/dados/arq$$i$$ext" ; \
			curl -s -k "$$url" > $(LAB)/testes/arq$$i$$ext ; \
		done ; \
		echo "\033[1;32mConcluído!\033[0m" ; \
		echo ; \
	done
	atom ./$(LAB) ; \
