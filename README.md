# Cost Reports
<a href='https://github.com/jpoles1/gopherbadger' target='_blank'>![gopherbadger-tag-do-not-edit](https://img.shields.io/badge/Go%20Coverage-76%25-brightgreen.svg?longCache=true&style=flat)</a>
[![Docker](https://github.com/empathyco/platform-cost-report/actions/workflows/docker.yml/badge.svg)](https://github.com/empathyco/platform-cost-report/actions/workflows/docker.yml)
[![Gosec](https://github.com/empathyco/platform-cost-report/actions/workflows/gosec.yaml/badge.svg)](https://github.com/empathyco/platform-cost-report/actions/workflows/gosec.yaml)
[![Reviewdog](https://github.com/empathyco/platform-cost-report/actions/workflows/reviewdog.yml/badge.svg)](https://github.com/empathyco/platform-cost-report/actions/workflows/reviewdog.yml)
## Architecture
![](docs/diagram.png)
## Requirements

```sh
brew install go
```

## Build

```sh
make build
## Docker 

For those who wants keep it simple and avoid install a lot of things:

```sh
docker build . -t cost-report
docker run -p 8080:8080 cost-report
```

## Usage

```sh

```
### Development
1. Add comments to your API source code, [See Declarative Comments Format](https://swaggo.github.io/swaggo.io/declarative_comments_format/).
2. Download [Swag](https://github.com/swaggo/swag) for Go by using:
```sh
$ go get -u github.com/swaggo/swag/cmd/swag
```

3. Run the [Swag](https://github.com/swaggo/swag) in your Go project root folder which contains `main.go` file, [Swag](https://github.com/swaggo/swag) will parse comments and generate required files(`docs` folder and `docs/doc.go`).
```sh
$ swag init
```
4. Run Cost Report API 
```sh 
$ go run main.go
```


5. Endpoints

- Metrics: localhost:8080/metrics
- Healthcheck: localhost:8080/health
