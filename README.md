# Raft

A Rust implementation of the [Raft consensus algorithm](https://raft.github.io/), focused on:

- Correctness and readability. The core implementation is [written](src/core.rs) alongside the [original Raft TLA+
  specification](https://github.com/ongardie/raft.tla) to aid auditability.
- Simplicity. Some optional features described in Diego Ongaro's [Raft
  thesis](http://web.stanford.edu/~ouster/cgi-bin/papers/OngaroPhD.pdf) such as pre-voting, membership changes, and
  snapshots are currently not implemented.
- Usability. A primary goal of the API to be simple and not error-prone.

This crate is `no_std`, but depends on the `alloc` crate.

[API Documentation](https://simple-raft-rs.github.io/raft-rs/raft)  
[Examples](examples)

## Crate Features

This crate has the following optional features:

- `prost` enables optional protobuf serialization of Raft messages. A corresponding [protobuf file](src/raft.proto) is
  also provided.

## License

Copyright (C) 2019 Open Whisper Systems  
Copyright (C) 2021 jessa0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
