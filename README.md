# Ethereum Stealer

[![GoDoc](https://godoc.org/github.com/hexoul/ether-stealer?status.svg)](https://godoc.org/github.com/hexoul/ether-stealer)

## Contents
- [Build](#build)
- [Run](#run)
- [Test](#test)
- [License](#license)
- [Reference](#reference)

## Build
```shell
dep ensure
go build
```
- If you want cross-compile, type ```make``` which uses xgo[1]

## Run
```shell
go run main.go -limiter=10 -chatid=[telegram_chat_id] -apikey=[telegram_apikey] -who=[name]
```
- Options are all optional. No need to put all

## Test
1. Move each module directory
2. Run testunit
```shell
go test -v
```

## Add ERC tokens
1. Get code at etherscan.io and put into contract/sol
2. Run abigen
```shell
abigen -sol contract/sol/[target].sol -pkg [target] -out contract/abigen/[target].go
```
3. Implement interface in contract package following sample

## License
MIT

## Reference
[1] https://github.com/karalabe/xgo