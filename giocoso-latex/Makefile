TEXCC=latexmk
MASTER=master

all: build

build:
	$(TEXCC) -pdf $(MASTER).tex

clean:
	rm -f *.log
	rm -f *.toc
	rm -f *.aux
	rm -f *.fls
	rm -f *.out
	rm -f *.fdb_latexmk

dropbox: build clean
	mkdir -p dropbox
	tar -zcf dropbox/superdoc.tar.gz --exclude .git --exclude dropbox --exclude .gitignore .
	cp $(MASTER).pdf dropbox/superdoc.pdf
