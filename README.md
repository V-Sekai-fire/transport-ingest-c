# transport-ingest-c

The ingest transport layer in C over picoquic, for terminating client connections and passing player input to an interactor over iceoryx2.

## What it is for

It holds no authority, runs no simulation and keeps no durable state, and it links the same QUIC and TLS libraries as the client so both ends of a connection run the same code. The shared QUIC and WebTransport termination is here; the ingest process that will call it is not written, and [`ingest/README.md`](ingest/README.md) states its contract. RFD 2123 covers the WebTransport edge and its second implementation.

## Build

The repository has no top-level build, because the server program that will link this code is not written. Every dependency is vendored, so a clone needs no submodule fetch.

## Licence

MIT; see `LICENSE`. Vendored projects carry their own licences.
