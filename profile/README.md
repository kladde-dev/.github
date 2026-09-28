# Kladde

**Durable data structures: mutate in memory, and it's on disk.**
A cross-language file format with implementations.

Founded and currently maintained by [Robert Bamler](https://robamler.github.io/).

Kladde is a system for *durable data structures*: containers and user-defined types that behave like their ordinary in-memory counterparts, but whose every mutation is durably recorded to a file as it happens.
There is no save step, no serialization pass, and no object-relational layer; reads never touch the file.
The research literature calls the idea *orthogonal persistence*.

- **[Documentation](https://kladde-dev.github.io/)**, also as [one PDF](https://kladde-dev.github.io/kladde.pdf): the language-independent specification, the reference algorithms, the Rust implementation's design and tutorial, and measurements.
  Its source is [kladde-docs](https://github.com/kladde-dev/kladde-docs).
- **[kladde-rs](https://github.com/kladde-dev/kladde-rs)**: the Rust implementation, a proof of concept that tests the specification.

Early and moving: the file format is not frozen, and more implementations are meant to follow.
