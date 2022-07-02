# RNKM65 Gateway

## Stacks
- golang
- gRPC
- go-fiber

## Getting Start
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
- golang 1.18 or [later](https://go.dev)
- docker
- makefile
- go-swagger
- protoc

### Installing
1. Clone the project from [RNKM65 Gateway](https://github.com/isd-sgcu/rnkm65-gateway)
2. Import project
3. Copy `config.example.yaml` in `config` and paste it in the same location then remove `.example` from its name.
4. Download dependencies by `go mod download`

### Testing
1. Run `go test  -v -coverpkg ./... -coverprofile coverage.out -covermode count ./...` or `make test`

### Running
1. Run `docker-compose up -d` or `make compose-up`
2. Run `go run ./src/.` or `make server`

### Compile proto file
1. Run `make proto`

### Generate docs
1. Run `swag init -d ./src -o ./src/docs -md ./src/docs/markdown` or `make create-doc`
