# modern-ocaml

Template for an ocaml project with modern tooling.

The setup should be installable as easily as possible.

For opam users:

```
opam switch create . 4.10.0 --no-install
opam install . --deps-only
```

For esy users:

```
esy
```

## Package manager

In an effort to take the best of all tools, both opam and esy are used.

Opam is used as the main package manager. As it is the most popular tool so
far. Using an opam file allows this repository to be consumed by any package
manager. It also enables publication in the opam repository.

Esy is configured as an overlay on top of the opam file. For those who want
to use it it can reduce compilation time. And it also allows for easier
pinning of development tools.

## Build system

The current goto build system in ocaml is dune. Version 2 or superior of the
dune lang should be used if possible. The base of the project has been
generated with `dune init project modern_ocaml`.

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
