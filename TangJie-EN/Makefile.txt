all:
	pdflatex cv_7
	bibtex cv_7
	pdflatex cv_7
#xelatex OLT.tex; bibtex OLT.aux; xelatex OLT.tex; xelatex OLT.tex

origin:
	latex cv_7
	-bibtex cv_7
	latex cv_7
	latex cv_7
	dvips -t a4 -o cv_7.ps cv_7

clean:
	rm *.log *.aux *.out