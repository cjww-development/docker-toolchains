# docker-toolchains

This repository contains a set of `Dockerfile` that can be built and used as build agents in CI/CD pipelines.

## Scala toolchain
The scala toolchain image is for building scala based projects with SBT. 

This image contains the following tools

- Java 11
- Scala 2.13.7
- SBT 1.6.2
- Docker (Docker CLI available with Docker engine as a volume mount)
- Docker compose
- AWS CLI

## NodeJS & AWS
The NodeJS toolchain image is for building JS/TS based projects with yarn and deployment to AWS.

This image contains the following tools

- NodeJS
- NPM
- Yarn
- aws-cli
- zip
- jq

## Basic tools
The Basic tools toolchain runs an Alpine image and basic linux commands are installed and extended as necessary.

This image contains the following tools

- curl

License
=======
This code is open sourced licensed under the MIT License