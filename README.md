# docker-bionic-rust

Rust on Ubuntu 18.04 (bionic) for multi-stage docker image build.

Dockerfile [ci-and-cd/docker-bionic-rust on Github](https://github.com/ci-and-cd/docker-bionic-rust)

[cirepo/rust on Docker Hub](https://hub.docker.com/r/cirepo/rust/)


## Use this image as a “stage” in multi-stage builds

```dockerfile

FROM cirepo/nix:2.2.1-bionic
COPY --from=cirepo/rust:1.33.0-bionic-archive /data/root /

```
