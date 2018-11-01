# gobin

[![Build Status](https://img.shields.io/travis/leighmcculloch/gobin.svg)](https://travis-ci.org/leighmcculloch/gobin)

Gobin is a tool for installing Go packages containing binaries.

Binaries are installed to the directory specified by the `GOBIN` environment variable. By default `GOBIN` is set to `$GOPATH/bin` but change it by setting it to any absolute path by prefixing any gobin usage with `GOBIN=...`.

Works with all versions of Go 1.3+ and supports module versions in Go 1.11+.

## Usage

```
gobin <package[@version]>
```

## Examples

Get the latest:

```
gobin 4d63.com/tldr
```

Get a specific version (using Go 1.11 or later):

```
gobin 4d63.com/tldr@v1.0.0
```

Install to a specific location by setting `GOBIN`:

```
GOBIN=$HOME/bin gobin 4d63.com/tldr
```

## Install

Download `gobin` to somewhere in your path like `~/bin` or `/usr/local/bin`.

```
curl -sSL https://github.com/leighmcculloch/gobin/raw/master/gobin -o ~/bin/gobin && chmod +x ~/bin/gobin
```

## License

MIT
