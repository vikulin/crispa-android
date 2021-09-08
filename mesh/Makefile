GOPATH=$(shell go env GOPATH)
export GO111MODULE=off
all:
	-go get -u github.com/RiV-chain/RiV-mesh-go;
	-cd $(GOPATH)/src/github.com/RiV-chain/RiV-mesh-go; \
		go get -v -d ./...; \
		go get -u github.com/RiV-chain/RiV-mesh-extras; \
		ANDROID=true ./build;
	mv -f $(GOPATH)/src/github.com/RiV-chain/RiV-mesh/mesh.aar mesh.aar;
	mv -f $(GOPATH)/src/github.com/RiV-chain/RiV-mesh/mesh-sources.jar mesh-sources.jar;
