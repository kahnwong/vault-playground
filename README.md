# Vault Playground

## Setup
<https://developer.hashicorp.com/vault/tutorials/getting-started/getting-started-install#install-vault>

## Init

```bash
vault server -dev
```

Then set `.env`:
```bash
VAULT_ADDR=
VAULT_TOKEN=
```

## Usage

```bash
vault kv put -mount=secret $PATH $KEY=$VALUE
vault kv delete -mount=secret $PATH
```
