# LUKSO CLI monitoring &middot; [![PR Welcome Badge](https://badgen.net/https/pr-welcome-badge.vercel.app/api/badge/Hugoo/lukso-cli-monitoring)](https://github.com/Hugoo/lukso-cli-monitoring/issues?q=archived:false+is:issue+is:open+sort:updated-desc+label%3A%22help%20wanted%22%2C%22good%20first%20issue%22)

This repo is provided "as is". It suggests a simple way to monitor a LUKSO node using the [LUKSO CLI](https://github.com/lukso-network/tools-lukso-cli) by using [docker compose](https://docs.docker.com/compose/). Depending on your configuration, you might need to adjust it.

PR welcome 🤗

## Requirements

- For local setup with GUI: [Docker Desktop](https://www.docker.com/products/docker-desktop/)

or

- For remote/server/no GUI setups: docker compose ([tutorial for Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-22-04))

Tested on macOS Intel.

## Instructions

1. Install the [`lukso-cli`](https://github.com/lukso-network/tools-lukso-cli).
2. Follow the CLI instructions and start the LUKSO CLI.

NOTE: this setup has only been tested with prysm.
NOTE: if you use erigon client, you need to enable metrics with: `--erigon-metrics` flag:

```bash
# Erigon
lukso start --validator --transaction-fee-recipient "0x123..." --erigon-metrics

# Geth
lukso start --validator --transaction-fee-recipient "0x123..." --geth-metrics
```

3. Run: `docker compose up` (you can use `-d` to run it in the background).
4. Wait for all services to start.
5. Go to: <http://localhost:3000/> and login with user: `admin`, password: `admin`.

> 💡 Note: if you run the LUKSO CLI on a remote node with no GUI, you might need to use [SSH port-forwarding](https://unix.stackexchange.com/a/115906) to view the dashboards.

6. You can find the dashboard from the [dashboard menu](http://localhost:3000/dashboards) in the General folder.

You can check on the [Prometheus dashboard](http://localhost:9090/) if the [targets](http://localhost:9090/targets?search=) are green.

## Inspired by

- <https://github.com/metanull-operator/eth2-grafana>
- <https://github.com/ledgerwatch/erigon/tree/devel/cmd/prometheus>
- <https://grafana.com/grafana/dashboards/14053-geth-overview/>

## References

- [LUKSO Docs](https://docs.lukso.tech)
- GitHub: [lukso-network/network-configs](https://github.com/lukso-network/network-configs)
- <https://docs.prylabs.network/docs/prysm-usage/monitoring/grafana-dashboard>
