
# Example PureScript project using Pulp

This is an example PureScript project that uses Pulp as its build tool.  It is
built to accompany the blog post [here][cbt].

[cbt]: http://www.arow.info/blog/posts/2015-12-17-purescript-intro.html#compiler-and-build-tools

## Installing necessary build tools.

In order to play around with this code, you need to install [`node` and
`npm`](https://nodejs.org/en/download/package-manager/).

After installing `npm`, run the following command:

```sh
$ npm install
```

This installs all the dependencies listed in `packages.json` to the
`node_modules/` directory.  This includes the PureScript compiler, Bower, and
Pulp.

Next, use Bower to install required PureScript libraries:

```sh
$ node_modules/.bin/bower install
```

This reads the dependencies from `bower.json` and installs them to the
`bower_components/` directory.

## Building the code

This code can be built with Pulp:

```sh
$ node_modules/.bin/pulp build
```

This command puts the compiled code in the `output/` directory.

## Running tests

```sh
$ node_modules/.bin/pulp test
```

## Looking at the code in a browser

Try running the following command and opening up [`index.html`](http://localhost:1337/) in a browser:

```sh
$ node_modules/.bin/pulp server
```
