# CDK Erigon RPC Methods – Postman Collections

This repository contains a curated set of Postman
collections for testing and interacting with CDK Erigon RPC methods.
It is designed to help developers, DevOps engineers,
and support teams quickly query blockchain data, debug nodes,
and validate RPC endpoints without manually building requests.

## Prerequisites

Postman

Newman
 (for local testing)

A valid RPC URL (injected via environment variable BASE_URL)

## Usage

Clone repository and
import a collection from CDK-Erigon-Methods/ into Postman
workspace.

Create a Global Postman environment variable with:

BASE_URL → Your RPC endpoint.

Execute requests directly from Postman.

## Contributing

Fork the repo and create a feature branch:

```bash

git checkout -b <your-branch-name>

```

Add or update Postman collections inside CDK-Erigon-Methods/.

Make sure all requests use {{BASE_URL}} variable (no hardcoded URLs).

Test locally with Newman & make sure all tests passes.

```bash

newman run CDK-Erigon-Methods/<your_collection>.postman_collection.json \
  --env-var BASE_URL=<your_rpc_url>

```

If contribution was made to README.md file,
make sure changes are properly linted.

```bash

markdownlint CDK-Erigon-Methods/README.md

```

Commit and push your changes, then open a PR.

PR would merged be if all test cases pass on CI.
