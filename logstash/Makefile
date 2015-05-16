BASENAME=$(shell basename `pwd`)
IMAGE_TAG=$(BASENAME)

all: clean build

build: Dockerfile
	docker build -t $(IMAGE_TAG) .

clean:
	-docker rmi $(IMAGE_TAG)

.PHONY: build clean
