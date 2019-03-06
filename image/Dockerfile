
FROM cirepo/nix:2.2.1-bionic


ARG IMAGE_ARG_RUST_CHANNEL


## install rust for current user
RUN curl https://sh.rustup.rs -o rustup-init.sh \
    && chmod +x ./rustup-init.sh \
    && sh ./rustup-init.sh --default-toolchain ${IMAGE_ARG_RUST_CHANNEL:-stable} -y \
    && . ~/.cargo/env \
    && rustup default ${IMAGE_ARG_RUST_CHANNEL:-stable} \
    && rm -f ./rustup-init.sh \
    && rustup target add aarch64-apple-ios \
    && rustup target add aarch64-linux-android \
    && rustup target add arm-linux-androideabi \
    && rustup target add armv7-apple-ios \
    && rustup target add armv7-linux-androideabi \
    && rustup target add armv7s-apple-ios \
    && rustup target add i386-apple-ios \
    && rustup target add i686-apple-darwin \
    && rustup target add i686-linux-android \
    && rustup target add thumbv7neon-linux-androideabi \
    && rustup target add x86_64-apple-darwin \
    && rustup target add x86_64-apple-ios \
    && rustup target add x86_64-linux-android
