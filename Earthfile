VERSION 0.7

PROJECT applied-knowledge-systems/terraphim-platform

main-pipeline:
  PIPELINE --push 
  TRIGGER push main 
  TRIGGER pr main 

all:
    BUILD ./terraphim-cloud-fastapi/+build-fastapi
    BUILD ./terraphim-cloud-fastapi/+release 
    BUILD ./terraphim-firecracker/+bionic-terraphim
    BUILD ./terraphim-firecracker/+terraphim-python