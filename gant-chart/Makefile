NAME="proposal"

all: $(NAME)

$(NAME):
		pdflatex $(NAME); \
		bibtex $(NAME); \
		pdflatex $(NAME); \
		pdflatex $(NAME); \
                evince $(NAME).pdf;

clean:
		find . \( -name "*.toc" -o -name "*.fdb_latexmk" \
						         -o -name "*.pdfsync" \
						         -o -name "*.log" \
						         -o -name "*.fls" \
						         -o -name "*.aux" \
						         -o -name "*.bbl" \
						         -o -name "*.blg" \
						         -o -name "*.glo" \
						         -o -name "*.ist" \
						         -o -name "*.lof" \
						         -o -name "*.lot" \
						         -o -name "*.out" \
						         -o -name "*.toc" \
                                                         -o -name "*.dvi" \
                                                         -o -name "*-blx.bib" \
                                                         -o -name "*.run.xml" \
                                                         -o -name "*~" \
					\) -print0 | xargs -0 rm -f
