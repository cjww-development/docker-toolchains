# docker-toolchains

This repository contains a set of `Dockerfile` that can be used as build agents in CI/CD pipelines.

## Scala toolchain
The scala toolchain image is for building scala based projects with SBT. 

This image contains the following tools

- Java 11
- Scala 2.13.7
- SBT 1.6.2
- Docker (Docker CLI available with Docker engine as a volume mount)
- AWS CLI

License
=======
This code is open sourced licensed under the MIT License