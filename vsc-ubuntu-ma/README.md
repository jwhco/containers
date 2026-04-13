---
platform: Docker Hub
permalink: https://hub.docker.com/repository/docker/hittjw/vsc-ubuntu-ma/general
---

# A Multiple Architecture Ubuntu Editorial Environment

## Overview

A Ubuntu 22.04-based Visual Studio Code environment with Python, Pandoc, LaTeX, Node.js, and NPM. Runs on AMD64 and ARM64 for a mixed Kubernetes cluster.

To support technical writing in Python development and Markdown writing environments. A basic environment for Text Analysis and Natural Language Processing.

This image currently supports GitHub storage of Obsidian, LogSeq, Zettlr, FOAM, and VIM remote note-taking environments.

## Purpose

- Multi-arch Ubuntu Editing Environment. Works with Visual Studio Code, plus basic text analysis and Pandoc compile.

## Package

- `vsc-ubuntu-ma.yml` pulls image from repository, already built with vscode, pandoc, and text analysis support.


## Instruction

### Local Kubernetes Cluster Has Multiple Architectures

- There are four Raspberry Pi 4 Model B nodes.  There are two x86_64 Generic nodes.
- The philosophy of this Kubernetes cluster is bare-bones commodity systems.

### How to Build the Multiple Architecture Image

To build the image in Docker, then upload to repository.

```bash
docker buildx create --use --name multi-arch-builder
docker buildx build --platform linux/amd64,linux/arm64 --tag hittjw/vsc-ubuntu-ma:latest --push .
docker push hittjw/vsc-ubuntu-ma:latest
```

The build takes about 10 minutes, it will need a docker environment with a little horsepower.


## Docker Hub

- Description (100) = A Ubuntu VSCode Multi-Arch ENV with Python, Pandoc, LaTeX, Node.js, and NPM.
- Category = Developer Tools

/EOF/