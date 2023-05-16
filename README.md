# LUKSO CLI monitoring &middot; [![PR Welcome Badge](https://badgen.net/https/pr-welcome-badge.vercel.app/api/badge/Hugoo/lukso-cli-monitoring)](https://github.com/Hugoo/lukso-cli-monitoring/issues?q=archived:false+is:issue+is:open+sort:updated-desc+label%3A%22help%20wanted%22%2C%22good%20first%20issue%22)

This repo provides a simple example of docker configuration to monitor a LUKSO node using the [LUKSO CLI](https://github.com/lukso-network/tools-lukso-cli). Depending on your configuration, you might need to adjust it. For instance, if you run the LUKSO CLI on a remote node with no GUI, you might need to use [SSH port-forwarding](https://unix.stackexchange.com/a/115906) to view the dashboards.

PR welcome 🤗

## Requirements

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)

Tested on macOS Intel.

## Instructions

1. Install the [`lukso-cli`](https://github.com/lukso-network/tools-lukso-cli).
2. Follow the CLI instructions and start the LUKSO CLI.

NOTE: this setup has only been tested with prysm.

3. `docker compose up`
4. Wait for all services to start.
5. Go to: <http://localhost:3000/>
   User: `admin`, password: `admin`
6. You can find the dashboard from the [dashboard menu](http://localhost:3000/dashboards) in the General folder.

You can check on the [Prometheus dashboard](http://localhost:9090/) if the [targets](http://localhost:9090/targets?search=) are green.

## Inspired by

- <https://github.com/metanull-operator/eth2-grafana>

## References

- [LUKSO Docs](https://docs.lukso.tech)
- [lukso-network/network-configs](https://github.com/lukso-network/network-configs)
- <https://docs.prylabs.network/docs/prysm-usage/monitoring/grafana-dashboard>
