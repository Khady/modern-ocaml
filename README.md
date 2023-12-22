# modern-ocaml

Template for an ocaml project with modern tooling.

The setup should be installable as easily as possible.

## Getting started

```sh
opam switch create . 5.1.1 --no-install
opam install . --deps-only
```

## Build system

The current goto build system in ocaml is dune. Version 3 or superior of the
dune lang should be used if possible. Unless the goal is to write a library
that must be compatible with legacy environements. The base of the project has
been generated with `dune init project modern_ocaml`.

## Continuous integration

The CI setup is relying on github actions. It is kept as simple as possible.
It checks for compilation of the project, tests, code formatting.

## Code formatting

This repository has ocamlformat enabled. With the default configuration. In a
modern editor setup, using it should be mostly transparent. It can also be
triggered with `dune build @fmt`.

## Editor tooling

Over the past year a very good implementation of a LSP server for ocaml has
been developed. It should be automatically installed during the setup of the
project.

## Running a binary

After running the setting up commands, you can check that it works by running:

```sh
$ dune build
$ dune exec bin/main.exe
Hello, World!
```

## License

This repository contains a AGPLv3+ license file. I made this choice because I
support free software and I believe that it is the best license to use for
personal projects. But this repository is meant to be used as a template. It
doesn't contain any original code by itself. So it can't be covered by a
license. Feel free to use this template for your projects and pick the
license you prefer. It is also totally fine to use it for a closed source
project.

If you need help selecting a license, the Free Software Foundation provides a
[short guide]( https://www.gnu.org/licenses/license-recommendations.html) for
picking a license.
