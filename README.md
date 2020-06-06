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

## Running a binary

After running the setting up commands, you can check that it works by running:

```
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
