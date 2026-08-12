# Yieldia Devnet Data

Public issuer and prospectus documents registered with Yieldia on Solana devnet.

## Layout

Every non-hidden directory at the repository root represents one issuer. The issuer metadata lives directly in that directory; every nested directory represents one prospectus.

```text
<issuer>/
├── issuer.json
└── <prospectus>/
    ├── prospectus.md
    └── proof-pack.json
```

Use lowercase kebab-case directory names. Keep the document filenames shown above so paths stay predictable.

## Create documents

```sh
mkdir -p <issuer>/<prospectus>
yieldia issuer create <issuer>/issuer.json
yieldia prospectus create <issuer>/<prospectus>/prospectus.md
yieldia proof-pack create <issuer>/<prospectus>/proof-pack.json
```

Complete every `REPLACE_ME` value and set the final public HTTP(S) URIs before validation.

## Validate documents

```sh
yieldia issuer validate <issuer>/issuer.json
yieldia proof-pack validate <issuer>/<prospectus>/proof-pack.json \
  --issuer-file <issuer>/issuer.json
yieldia prospectus validate <issuer>/<prospectus>/prospectus.md \
  --proof-pack-file <issuer>/<prospectus>/proof-pack.json
```

Commit and publish the exact validated bytes before registering them onchain. After registration, do not rewrite, move, or delete a registered prospectus or proof pack; create a new prospectus directory instead.

Never commit keypairs, seed phrases, private keys, or `.env` files to this repository.
