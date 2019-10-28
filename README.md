Bigstep Metalcloud Terraform Provider
==================
This is a terraform plugin for controlling Bigstep Metalcloud resources.

Maintainers
-----------

This provider plugin is maintained by the Bigstep Team.

Requirements
------------

-	[Terraform](https://www.terraform.io/downloads.html) 0.12.x
-	[Go](https://golang.org/doc/install) 1.11 (to build the provider plugin)

Usage
---------------------

```
# For example, restrict template version in 0.1.x
provider "template" {
  version = "~> 0.1"
}
```

Building The Provider
---------------------

Clone repository to: `$GOPATH/src/github.com/bigstepinc/terraform-provider-metalcloud`

```sh
$ mkdir -p $GOPATH/src/github.com/bigstepinc; cd $GOPATH/src/github.com/bigstepinc
$ git clone git@github.com/bigstepinc/terraform-provider-metalcloud
```

Enter the provider directory and build the provider

```sh
$ cd $GOPATH/src/github.com/bigstepinc/terraform-provider-metalcloud
$ make build
```

Using the provider
----------------------
## Fill in for each provider

Developing the Provider
---------------------------

If you wish to work on the provider, you'll first need [Go](http://www.golang.org) installed on your machine (version 1.11+ is *required*). You'll also need to correctly setup a [GOPATH](http://golang.org/doc/code.html#GOPATH), as well as adding `$GOPATH/bin` to your `$PATH`.

To compile the provider, run `make build`. This will build the provider and put the provider binary in the `$GOPATH/bin` directory.

```sh
$ make build
...
$ $GOPATH/bin/terraform-provider-metalcloud
...
```

In order to test the provider, you can simply run `make test`.

```sh
$ make test
```

In order to run the full suite of Acceptance tests, run `make testacc`.

*Note:* Acceptance tests create real resources, and often cost money to run.

```sh
$ make testacc
```
