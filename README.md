Find it on the [Docker Hub](https://hub.docker.com/r/rustlang/rust/).

For typical use cases, see the [official image](https://hub.docker.com/_/rust/).

This image has two tags, `nightly` and `nightly-slim`, which are updated every
day to match the current Rust nightly.  The `nightly` tag is configured
identically to that of the `latest` tag of the official image, except that the
nightly toolchain is selected via rustup.  The `nightly-slim` tag is configured
identically to that of the `slim` tag of the official image, except that the
nightly toolchain is selected via rustup.
