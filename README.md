# transport-ingest-c

The ingest transport layer in C over picoquic, which terminates client connections; iceoryx2 is the intended hand-off to an interactor.

## What it is for

It holds no authority, runs no simulation and keeps no durable state, and it uses the same QUIC implementation (picoquic) as the client. The shared QUIC and WebTransport termination is here; the ingest process that will call it is not written, and [`ingest/README.md`](ingest/README.md) states its contract. RFD 2123 covers the WebTransport edge and its second implementation.

## Build

The repository has no top-level build, because the server program that will link this code is not written. Every dependency is vendored, so a clone needs no submodule fetch.

## Licence

MIT; see `LICENSE`. Vendored projects carry their own licences.
