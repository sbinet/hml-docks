## higgsml/xgboost

.PHONY: all build

REPO := higgsml/xgboost
TAG ?= $(shell date +%Y%m%d)

all: build
	@echo "done"

build: Dockerfile
	docker build --rm --tag=$(REPO):$(TAG) .
	docker tag --force $(REPO):$(TAG) $(REPO):latest

upload: build
	docker push $(REPO):$(TAG)
	docker push $(REPO):latest



