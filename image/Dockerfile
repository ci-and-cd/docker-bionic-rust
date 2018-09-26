
FROM cirepo/nix:2.1.1-bionic


ARG IMAGE_ARG_RUST_CHANNEL


## install rust for current user
RUN curl https://sh.rustup.rs -o rustup-init.sh \
    && chmod +x ./rustup-init.sh \
    && sh ./rustup-init.sh --default-toolchain ${IMAGE_ARG_RUST_CHANNEL:-stable} -y \
    && . ~/.cargo/env \
    && rustup default ${IMAGE_ARG_RUST_CHANNEL:-stable} \
    && rm -f ./rustup-init.sh
