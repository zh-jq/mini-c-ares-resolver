# mini-c-ares-resolver

A fork of [c-ares-resolver](https://github.com/dimbleby/c-ares-resolver), which use
[mini-c-ares](https://github.com/zh-jq/mini-c-ares) instead of [c-ares](https://github.com/dimbleby/rust-c-ares/).
, for asynchronous DNS requests.

This crate provides three resolver types - the `Resolver`, the `FutureResolver`,
and the `BlockingResolver`:

- The `Resolver` is the thinnest wrapper around the underlying `c-ares` library.
  It returns answers via callbacks. The other resolvers are built on top of
  this.
- The `FutureResolver` returns answers as `std::future::Future`s.
- The `BlockingResolver` isn't asynchronous at all - as the name suggests, it
  blocks until the lookup completes.

## Documentation

API documentation is [here](https://docs.rs/mini-c-ares-resolver).

## Contributing

Contributions should be sent to [c-ares-resolver](https://github.com/dimbleby/c-ares-resolver).
