CDK Erigon RPC Methods – Postman Collections

🚀 This repository contains a curated set of Postman collections for testing and interacting with CDK Erigon RPC methods.
It is designed to help developers, DevOps engineers, and support teams quickly query blockchain data, debug nodes, and validate RPC endpoints without manually building requests.

```bash
Repository Structure
.
├── RPC-POSTMAN-COLLECTIONS/   # JSON Postman collections organized by category
├── .github/workflows/         # GitHub Actions CI/CD pipelines
│   ├── postman-tests.yml      # Runs all Postman collections with Newman
│   └── readme-lint.yml        # Lints README for formatting
└── README.md
```

🔧 Prerequisites

Postman
 (for local testing)

Newman
 (for CLI runs)

A valid RPC URL (injected via environment variable BASE_URL)

🚀 Usage
1. Run locally with Postman

Import a collection from RPC-POSTMAN-COLLECTIONS/ into Postman.

Create a Postman environment with:

BASE_URL → Your RPC endpoint (e.g., https://rpc.testnet.sentient.org).

Additional variables (like account addresses) if needed.

Execute requests directly from Postman.

2. Run in CI/CD

This repo includes a GitHub Actions workflow using Newman:

```bash
newman run RPC-POSTMAN-COLLECTIONS/<your_collection>.postman_collection.json \
  --env-var BASE_URL=<your_rpc_url>
```


CI ensures:

All collections run successfully against your configured endpoint.

Hardcoded URLs are blocked → all requests must use {{BASE_URL}}.

✅ Continuous Integration

Postman Tests Workflow
Runs all Postman collections automatically on pushes/PRs to main.
Fails if:

Any test fails in a collection.

A collection uses a hardcoded RPC URL instead of {{BASE_URL}}.

README Lint Workflow
Lints README.md with markdownlint whenever the file is updated.

🤝 Contributing

Fork the repo and create a feature branch:

```bash
git checkout -b feature/add-new-methods

```


Add or update Postman collections inside RPC-POSTMAN-COLLECTIONS/.

Make sure all requests use {{BASE_URL}} (no hardcoded URLs).

Test locally with Newman.

Commit and push your changes, then open a PR.