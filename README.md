[![Build Status](https://travis-ci.org/JesusIslam/shash.svg?branch=master)](https://travis-ci.org/JesusIslam/shash)
[![Coverage Status](https://coveralls.io/repos/github/JesusIslam/shash/badge.svg?branch=master)](https://coveralls.io/github/JesusIslam/shash?branch=master)
[![GoDoc](https://godoc.org/github.com/JesusIslam/shash?status.svg)](https://godoc.org/github.com/JesusIslam/shash)
[![Go Report Card](https://goreportcard.com/badge/github.com/JesusIslam/shash)](https://goreportcard.com/report/github.com/JesusIslam/shash)

# Shash
### A no-nonsense golang package for creating random string

This package is very simple, just do

```
	package main

	import (
		"fmt"
		"github.com/JesusIslam/shash"
	)

	func main() {
		h := shash.New(10)
		r, _ := h.Generate()
		fmt.Println(r)
	}
```

The example will generate a base62 random string with length of 5 (default).

For the documentation see [here](http://godoc.org/github.com/JesusIslam/shash).

To test, just run `go test`, but you need to have [gomega](http://github.com/onsi/gomega) and [ginkgo](http://github.com/onsi/ginkgo) installed.

To install `go get github.com/JesusIslam/shash`.

### Benchmark
On i3-3217U @1.8GHz with `go test -bench . -benchtime=5s -cpu 4`

```
BenchmarkGenerate5-4 	  500000	     15130 ns/op
BenchmarkGenerate16-4	  200000	     48357 ns/op
BenchmarkGenerate32-4	  100000	     98319 ns/op
```
