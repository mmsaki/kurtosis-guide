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

## Run local Devnet

Use the [Ethereum Package](https://github.com/ethpandaops/ethereum-package) for kurtosis

```bash
kurtosis run --enclave my-testnet github.com/ethpandaops/ethereum-package
```

## Customize Devnet

Use a customized config

```bash
kurtosis run --enclave my-testnet github.com/ethpandaops/ethereum-package --args-file network_params.yaml
```

