# depu

[![Go](https://github.com/kevwan/depu/workflows/Go/badge.svg?branch=main)](https://github.com/kevwan/depu/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/kevwan/depu)](https://goreportcard.com/report/github.com/kevwan/depu)
[![Release](https://img.shields.io/github/v/release/kevwan/depu.svg?style=flat-square)](https://github.com/kevwan/depu)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Why to write depu

When I maintain [go-zero](https://github.com/zeromicro/go-zero), I often need to check if any updates on my dependencies.

Some advantages on keeping up-to-date:
- get more features
- known bugs or security issues get fixed
- not breaking for deprecated usages on must upgrade

And `go list` lists all the dependent packages for both direct and indirect usages, and `Indirect` fields always telling true. For details, check this issue: https://github.com/golang/go/issues/40364

## Design ideas

- use `go list -u -m -json all` to get all the available updates for both direct and indirect usages.
- parse local `go.mod` to get directly required packages.
- only display the availabe updates for directly required packages.

## Installation

```shell
$ go install github.com/kevwan/depu@latest
```

## How to use

In the directory of `go.mod`, run the following command:

```shell
$ depu
```

Results look like:

<img width="800" alt="image" src="https://user-images.githubusercontent.com/1918356/169304283-1b09a434-0034-48c5-ab72-6c2c8d10e946.png">

## Give a Star! ⭐

If you like or are using this project, please give it a star. Thanks!
