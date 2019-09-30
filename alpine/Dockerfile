FROM alpine:3.10

ENV RUSTUP_HOME=/usr/local/rustup \
    CARGO_HOME=/usr/local/cargo \
    PATH=/usr/local/cargo/bin:$PATH

RUN set -eux; \
    apk add --no-cache \
    ca-certificates \
    gcc; \
    \
    url="https://static.rust-lang.org/rustup/dist/x86_64-unknown-linux-musl/rustup-init"; \
    wget "$url"; \
    echo "b535be813cd89000044764806f569a8c1428417d4226f16ee9993867f0c4ea4e *rustup-init" | sha256sum -c -; \
    chmod +x rustup-init; \
    ./rustup-init -y --no-modify-path --default-toolchain nightly; \
    rm rustup-init; \
    chmod -R a+w $RUSTUP_HOME $CARGO_HOME; \
    rustup --version; \
    cargo --version; \
    rustc --version;
