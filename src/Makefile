###
### Makefile for building and pushing site
###

GITHUB_PAGES_BRANCH=gh-pages
THEME = csfor

MARKDOWN = python3 -m markdown

html:
	hugo --theme=$(THEME)

develop:
	sleep 1 && echo "Opening local browser..." &&  open http://localhost:1313 &
	hugo server --theme=$(THEME) --buildDrafts --watch

github: html
	cp -r ./public/* ../
	cp -r docs ../docs
	cp -r assets/images/ ../images/
	rm -r ./public
	git add -A :/; git commit -m "Rebuilt site" ; git push

.PHONY: html clean develop
