<img src="https://kladde-dev.github.io/static/logo.svg" alt="kladde logo" width="80" align="right">

# Kladde

**Durable data structures: mutate in memory, and it's on disk.**
A cross-language file format and durability protocol with crash-safety guarantees, and libraries for building durable data types on top of it.

Founded and currently maintained by [Robert Bamler](https://robamler.github.io/).

Kladde is becoming a system for *durable data structures*: containers (strings, vectors, hash maps, trees, ...) and user-defined types that behave like their ordinary in-memory counterparts, but whose every mutation is durably recorded to a file as it happens, in a way that is optimized for disk I/O.
Unlike serialization formats like JSON or XML, there is no save step and no serialization pass.
Unlike sqlite, there is no SQL and no object-relational layer.
You open a kladde file containing some value (typically in some complex nested application-defined data type), you mutate some parts of the value in (almost) the same way you would mutate any other value, and each one of your changes is immediately and efficiently applied to the file.
The research literature calls the idea *orthogonal persistence*.

- **[Documentation](https://kladde-dev.github.io/)**, also as [one PDF](https://kladde-dev.github.io/kladde.pdf): the language-independent specification, the reference algorithms, the Rust implementation's design and tutorial, and measurements.
  Its source is [kladde-docs](https://github.com/kladde-dev/kladde-docs).
- **[kladde-rs](https://github.com/kladde-dev/kladde-rs)**: the Rust implementation, a proof of concept that tests the specification.

Early and moving: the file format is not frozen, and more implementations are meant to follow.
