## sp

[![GoDoc](https://godoc.org/bitbucket.org/gdamore/sp?status.png)](https://godoc.org/bitbucket.org/gdamore/sp)

Package sp is an implementation in pure Go of the SP ("Scalable Protocols")
protocols.  This makes heavy use of go channels, internally, but it can
operate on systems that lack support for cgo.  It has no external dependencies.

The reference implementation of the SP protocols is available as [nanomsg](http://www.nanomsg.org)
 
The design is intended to make it easy to add new transports with almost
trivial effort, as well as new topologies ("protocols" in SP terminology.)

At present, only Req/Rep over TCP and IPC are supported, but that will probably
change very quickly.

Basic interoperability with nanomsg has been tested with nanocat.

Consider this a work-in-progress, and use at your own risk.

If you find this useful, I would appreciate knowing about it.  I can be reached
via my email address, garrett -at- damore -dot- org

## Installing

### Using *go get*

    $ go get bitbucket.org/gdamore/sp

After this command *sp* is ready to use. Its source will be in:

    $GOROOT/src/pkg/bitbucket.org/gdamore/sp

You can use `go get -u -a` to update all installed packages.

## Documentation

For docs, see http://godoc.org/bitbucket.org/gdamore/sp or run:

    $ godoc bitbucket.org/gdamore/sp

## Testing

This package supports internal self tests, which can be run in
the idiomatic Go way:

    $ go test bitbucket.org/gdamore/sp

