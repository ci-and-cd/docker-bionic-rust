# docker-bionic-rust

Rust on Ubuntu 18.04 (bionic) for multi-stage docker image build.

Dockerfile [ci-and-cd/docker-bionic-rust on Github](https://github.com/ci-and-cd/docker-bionic-rust)

[cirepo/bionic-rust on Docker Hub](https://hub.docker.com/r/cirepo/bionic-rust/)


## Use this image as a “stage” in multi-stage builds

```dockerfile

FROM alpine:3.7
COPY --from=cirepo/bionic-rust:stable-archive /data/root /

```
