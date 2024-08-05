# Python-CUDA-Devcontainers

A collection of Docker files to set up Python CUDA devcontainer images.

## Usage

1. Decide on a Python version (the `PY_VER`, e.g. `3.9`, `3.10`).
2. Decide on the Debian version (the `OS_VER`, e.g. `bookworm`, `bullseye`).
3. Find the appropriate Dockerfile.
4. Run

```bash
docker build . -t devcontainers/cuda-python:[PY_VER]-[OS_VER] -f [DOCKERFILE_PATH]
```

For example,

```bash
docker build . -t devcontainers/cuda-python:3.10-bullseye -f 3.10/11.bullseye.Dockerfile
```

will create an image with the tag `devcontainers/cuda-python:3.10-bullseye` using Python 3.10 in the `bullseye` Debian version (i.e., Debian 11).


## Attribution

Dockerfiles were largely adapted from [the NVIDIA container `Dockerfile`](https://gitlab.com/nvidia/container-images/cuda/-/blob/a819e795/dist/12.2.2/ubuntu2204/base/Dockerfile).
