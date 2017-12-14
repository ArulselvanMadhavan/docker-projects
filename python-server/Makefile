PORT=8080
WWW_ROOT=/usr/src/app
PYTHON_SERVER_IMAGE_NAME=python-server
PYTHON_SERVER_CONTAINER_IMAGE_NAME=python-server

python-server-build:
	docker image build --build-arg UBUNTU_VERSION=18.04 -t $(PYTHON_SERVER_IMAGE_NAME) .

python-server-run: python-server-build
	docker run --rm -p $(PORT):$(PORT) python-server-build

python-server-volume-mount: python-server-build
	docker run --rm -v $(PWD)/www:$(WWW_ROOT) -p $(PORT):$(PORT) ${PYTHON_SERVER_IMAGE_NAME}
