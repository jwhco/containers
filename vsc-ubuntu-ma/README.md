# A Multiple Architecture Ubuntu Editorial Environment

## Purpose

- Multi-arch Ubuntu Editing Environment. Works with Visual Studio Code, plus basic text analysis and Pandoc compile.

## Package

- `vsc-ubuntu-ma.yml` pulls image from repository, already built with vscode, pandoc, and text analysis support.

## Local Kubernetes Cluster Has Multiple Architectures

- There are four Raspberry Pi 4 Model B nodes.  There are two x86_64 Generic nodes.
- The philosophy of this Kubernetes cluster is bare-bones commodity systems.

## Build Muli-Arch Image

To build the image in Docker, then upload to repository.

```bash
docker buildx create --use --name multi-arch-builder
docker buildx build --platform linux/amd64,linux/arm64 --tag hittjw/vsc-ubuntu-ma:latest --push .
docker push hittjw/vsc-ubuntu-ma:latest
```

The build takes about 10 minutes, it will need a docker environment with a little horsepower.


/EOF/