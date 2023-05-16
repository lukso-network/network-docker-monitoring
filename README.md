# LUKSO CLI monitoring &middot; [![PR Welcome Badge](https://badgen.net/https/pr-welcome-badge.vercel.app/api/badge/Hugoo/lukso-cli-monitoring)](https://github.com/Hugoo/lukso-cli-monitoring/issues?q=archived:false+is:issue+is:open+sort:updated-desc+label%3A%22help%20wanted%22%2C%22good%20first%20issue%22)

This repo provides a simple example of docker configuration to monitor LUKSO node using the [`lukso-cli`](https://github.com/lukso-network/tools-lukso-cli). PR welcome 🤗.

## Requirements

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)

Tested on macOS Intel.

## Instructions

1. Install the [`lukso-cli`](https://github.com/lukso-network/tools-lukso-cli).
2. Follow the CLI instructions and start the `lukso-cli` with prysm.

NOTE: this setup only works with prysm.

3. `docker compose up`
4. Wait for all services to start.
5. Go to: <http://localhost:3000/>
   User: `admin`, password: `admin`

You can check on the [Prometheus dashboard](http://localhost:9090/) if the [targets](http://localhost:9090/targets?search=) are green.

## Inspired by

- <https://github.com/metanull-operator/eth2-grafana>

## References

- [LUKSO Docs](https://docs.lukso.tech)
- [lukso-network/network-configs](https://github.com/lukso-network/network-configs)
