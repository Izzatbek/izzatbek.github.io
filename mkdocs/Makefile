# pip install mkdocs
# [sudo] gem install gimli

all: pdf site

site:
	@mkdocs build
	@cp -R site/* ../
	@rm -rf site
	@echo Moved the content of directory site into root
	@echo Ready to commit and push

pdf:
	gimli -file docs/index.md -outputfilename ../cv
	gimli -file docs/cv_francais.md -outputfilename ../cv_francais
	@echo Updated CV