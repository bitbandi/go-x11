go-x11 [![License](https://img.shields.io/badge/license-ISC-blue.svg)](https://github.com/bitbandi/go-x11/blob/master/license.md) [![godoc](https://img.shields.io/badge/go-documentation-blue.svg)](https://godoc.org/github.com/bitbandi/go-x11) [![Build Status](https://travis-ci.org/bitbandi/go-x11.svg?branch=master)](https://travis-ci.org/bitbandi/go-x11) [![Coverage Status](https://coveralls.io/repos/github/bitbandi/go-x11/badge.svg?branch=master)](https://coveralls.io/github/bitbandi/go-x11?branch=master)
======

Implements the x11 hash and required functions in go.


Usage
-----

```go
	package main

	import (
		"fmt"
		"github.com/bitbandi/go-x11"
	)

	func main() {
		hs, out := x11.New(), [32]byte{}
		hs.Hash([]byte("DASH"), out[:])
		fmt.Printf("%x \n", out[:])
	}
```


Notes
-----

Echo, Simd and Shavite do not have 100% test coverage, a full test on these
requires the test to hash a blob of bytes that is several gigabytes large.


License
-------

go-x11 is licensed under the [copyfree](http://copyfree.org) ISC license.
