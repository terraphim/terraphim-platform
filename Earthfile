VERSION 0.7

PROJECT applied-knowledge-systems/terraphim-platform

main-pipeline:
  PIPELINE --push 
  TRIGGER push main 
  TRIGGER pr main 
  BUILD +all

all:
    BUILD ./terraphim-cloud-fastapi/+build-fastapi
    BUILD ./terraphim-cloud-fastapi/+release 
    BUILD ./terraphim-firecracker/+bionic-terraphim
    BUILD ./terraphim-firecracker/+terraphim-python

docker:
	FROM earthly/dind:alpine
	WITH DOCKER
		RUN --no-cache --secret DOCKERHUB_USER=std/registry/registry-1.docker.io/username \
        --secret DOCKERHUB_PASS=std/registry/registry-1.docker.io/password \
		docker login --username "$DOCKERHUB_USER" --password "$DOCKERHUB_PASS"
	END