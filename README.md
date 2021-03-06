go-gitconfig [![GoDoc](https://godoc.org/github.com/tcnksm/go-gitconfig?status.svg)](https://godoc.org/github.com/tcnksm/go-gitconfig) [![Build Status](http://drone.io/github.com/tcnksm/go-gitconfig/status.png)](https://drone.io/github.com/tcnksm/go-gitconfig/latest) [![Coverage Status](http://coveralls.io/repos/tcnksm/go-gitconfig/badge.png)](https://coveralls.io/r/tcnksm/go-gitconfig)
====

Use `gitconfig` values in Golang.

## Usage

If you want to use git user name defined in `~/.gitconfig`: 

```go
username, err := gitconfig.Username()
```

Or git user email defined in `~/.gitconfig`: 

```go
email, err := gitconfig.Email()
```

Or, if you want to extract origin url of current project (from `.git/config`):

```go
url, err := gitconfig.OriginURL()
```

You can also extract value by key:

```go
editor, err := gitconfig.Global("core.editor")
```

```go
remote, err := gitconfig.Local("branch.master.remote")
```

See more details in document at [https://godoc.org/github.com/tcnksm/go-gitconfig](https://godoc.org/github.com/tcnksm/go-gitconfig). 

## Install

To install, use `go get`:

```bash
$ go get -d github.com/tcnksm/go-gitconfig
```

## VS.

- [speedata/gogit](https://github.com/speedata/gogit)
- [libgit2/git2go](https://github.com/libgit2/git2go)

These packages have many features to use git from golang. `go-gitconfig` is very simple alternative and focus to extract information from gitconfig. `go-gitconfig` is used in [tcnksm/ghr](https://github.com/tcnksm/ghr). 

## Contribution

1. Fork ([https://github.com/tcnksm/go-gitconfig/fork](https://github.com/tcnksm/go-gitconfig/fork))
1. Create a feature branch
1. Commit your changes
1. Rebase your local changes against the master branch
1. Run test suite with the `go test ./...` command and confirm that it passes
1. Run `gofmt -s`
1. Create new Pull Request

## LICENCE

[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/tcnksm/go-gitconfig/blob/master/LICENCE)

## Author

[tcnksm](https://github.com/tcnksm)
