# sra-tools docker container with bash

This is a repo that adds `bash` to ncbi/sra-tools.

The original repository can be found at [https://github.com/statgen/ruth](https://github.com/ncbi/sra-tools)

## Installation

To install the container, run the following using docker:

```bash
docker pull befh/sra-tools
```

or the following with singularity:

```bash
singularity pull --name sra-tools.sif docker://befh/sra-tools:latest
```

To use with Snakemake, you do not need to install. Just put the following in the Snakefile:

```
container: 'docker://befh/sra-tools:latest'
```

Then run with `snakemake --use-singularity` see https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html for more info.

## Usage

To run with docker, `docker run sra-tools [ARGS]`.

To run with singularity, `singularity run sra-tools.sif [ARGS]`.
