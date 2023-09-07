# Setup Guides

Some guides for setting up computing resources.

1. [Fermilab LPC](fermilab-lpc.md)
2. [Google Cloud](google-cloud.md)

- [Setup Guides](#setup-guides)
  - [General conda / mamba set-up:](#general-conda--mamba-set-up)
  - [Recommendations](#recommendations)


## General conda / mamba set-up:

```bash
# Download the setup bash file from here https://github.com/conda-forge/miniforge#mambaforge
# e.g. wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh
# Install: (the mamba directory can end up taking O(1-10GB) so make sure the directory you're using allows that quota)
./Mambaforge-Linux-x86_64.sh  # follow instructions in the installation
mamba create -n my-env python=3.10
mamba activate my-env
mamba install ...
```


## Recommendations

This repository has a lot of useful unix and Python tips: https://github.com/klieret/everything-you-didnt-now-you-needed.