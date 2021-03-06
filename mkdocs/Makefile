all: pdf site

# pip install mkdocs
# pip install mkdocs-bootswatch
site:
	@mkdocs build
	@cp -R site/* ../
	@rm -rf site
	@echo Moved the content of directory site into root
	@echo Ready to commit and push

# docker build -t walle/gimli:latest .
# See https://github.com/walle/gimli
pdf:
	docker run -v $(shell pwd):/tmp/gimli walle/gimli -f /tmp/gimli/docs/index.md -s /tmp/gimli/gimli.css -outputfilename /tmp/gimli/mukhanov-izzat-cv
	@mv -f mukhanov-izzat-cv.pdf ../mukhanov-izzat-cv.pdf
	@echo Updated CV
