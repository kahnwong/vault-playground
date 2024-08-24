# Vault Playground

## Setup
<https://developer.hashicorp.com/vault/tutorials/getting-started/getting-started-install#install-vault>

## Init

```bash
vault server -dev
```

Then set `.env`:
```bash
VAULT_ADDR=http://127.0.0.1:8200
VAULT_TOKEN=
```

## Usage

```bash
vault kv put -mount=secret $PATH $KEY=$VALUE
vault kv delete -mount=secret $PATH
```

## Configurations

```bash
mkdir -p ./vault/data # raft dir
vault server -config=config.hcl

# init
vault operator init
```

To auto unseal a vault: <https://developer.hashicorp.com/vault/docs/configuration/seal/gcpckms>
