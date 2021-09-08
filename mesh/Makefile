GOPATH=$(shell go env GOPATH)
export GO111MODULE=off
all:
	-go get -u github.com/mesh-network/mesh-go;
	-cd $(GOPATH)/src/github.com/mesh-network/mesh-go; \
		go get -v -d ./...; \
		go get -u github.com/mesh-network/mesh-extras; \
		ANDROID=true ./build;
	mv -f $(GOPATH)/src/github.com/mesh-network/mesh-go/mesh.aar mesh.aar;
	mv -f $(GOPATH)/src/github.com/mesh-network/mesh-go/mesh-sources.jar mesh-sources.jar;
