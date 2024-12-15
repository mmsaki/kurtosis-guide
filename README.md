# Kurtosis guide

- Dependencies
    - [Docker](https://docs.docker.com/get-started/)
    - [Kurtosis](https://docs.kurtosis.com/install)

## Install

> [!NOTE]
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
kurtosis run --enclave my-testnet github.com/ethpandaops/ethereum-package --args-file custom.yaml
```

> [!TIP]
> ### Creating custom configuration
> 
> Create `custom.yaml` from examples:
> - [Ethpandaops configs examples](https://github.com/ethpandaops/ethereum-package/blob/main/.github/tests/)
> - [Documented configuration setup guide](https://github.com/ethpandaops/ethereum-package/blob/main/README.md#configuration)


## Kurtosis commands :shipit:

Checking enclaves

```sh
kurtosis enclave ls
```

Get more details about an enclave

```sh
kurtosis enclave inspect my-testnet
```

Check some file

```sh
kurtosis files inspect my-testnet el_cl_genesis_data
kurtosis files inspect my-testnet el_cl_genesis_data ./config.yaml
```

Enclave dump

```sh
kurtosis enclave dump my-testnet
```

Logs

```sh
kurtosis service logs -f my-testnet
# checke additional services
kurtosis service logs -f my-testnet dora
```

Removing enclace

```sh
# Stop kurtosis then remove enclave
kurtosis enclave stop my-testnet
kurtosis enclave rm my-testnet
# or force remove
kurtosis enclave rm -f my-testnet
```

Checking engine status

```sh
kurtosis engine status
kurtosis engine restart
```

Cleanup everything, including enclaves

```sh
kurtosis clean -a
```

