# 📈 Tracker

This repository contains the tracking server for analytics for our products. It's a single Node.js file, [`index.mjs`](./index.mjs) that runs a [Polka](https://github.com/lukeed/polka) server which sends data to AWS-managed ElasticSearch.

## ⭐ Getting started

1. Fork this repository
2. Add the required environment variables
3. Run the Node.js script with `node index.mjs`

## ⚙️ Configuration

The following environment variables are required:

- `AWS_ELASTIC_HOST` is the host endpoint without protocol, e.g., search-example.eu-central-1.es.amazonaws.com
- `AWS_ACCESS_KEY_ID` is the AWS access key
- `AWS_SECRET_ACCESS_KEY` is the AWS secret key
- `AWS_REGION` is the AWS region, e.g., "eu-central-1"

Locally, these environment variables are loaded from a `.env`.

This repository also uses CI/CD and triggers an endpoint for deployment from the `master` branch. Optionally, you may add the following as repository secrets (see [Creating and storing encrypted secrets](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets)):

- `CI_WEBHOOK`

## 📄 License

- Code: [MIT](./LICENSE) © [Koj](https://joinkoj.com)
- "ElasticSearch" is a trademark of Elastic NV
- "Amazon Web Services" and "AWS" are trademarks of Amazon.com, Inc.