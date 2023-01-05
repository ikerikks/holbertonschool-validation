build: ## Generate a website
	@hugo

clean: ## Remove the dist directory
	@rm -r dist/*

post: ## Create a new post
	@hugo new posts/$(POST_NAME).md
	@sed -i 's/title: .*/title:"$(POST_TITLE)"/' content/posts/$(POST_NAME).md

help: ## Show list of target's usage
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'
