# Kurtosis guide

- Dependencies
    - [Docker](https://docs.docker.com/get-started/)
    - [Kurtosis](https://docs.kurtosis.com/install)

## Install

> Skip this section if docker and kurtosis are already installed

Check that docker is installed:

```bash
docker image ls
```

Install kurtosis (macOS)

```bash
brew install kurtosis-tech/tap/kurtosis-cli
```

Add Kurtosis CLI completions (zsh)

```bash
# Add Kurtosis command-line completion
source <(kurtosis completion zsh)
compdef _kurtosis kurtosis
```

