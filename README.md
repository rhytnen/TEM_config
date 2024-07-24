# TEM Config

This repository contains configuration files for the TEM acquisition system. It uses [Pigeon Config](https://pypi.org/project/pigeon-config/) (installable using `pip install pigeon-config`) to manage configurations for multiple systems.

## Usage

1. Compile the desired configuration using `pigeon-config`. For example, to compile the configuration for `T3`, run `pigeon-config config/T3`.
2. Run `docker compose`.

## Example

Install Pigeon Config:

```bash
pip install pigeon-config
```

Compile the configuration for creating a graph of the [PyTEM](https://github.com/AllenInstitute/PyTEM) state machine:

```bash
pigeon-config config/graph
```

Pull the necessary Docker containers from the compiled Docker compose file (must be connected to Allen Institute network or VPN):

```bash
sudo docker compose pull
```

Run the compiled Docker compose file:

```bash
sudo docker compose up
```

The graph should be saved to a file `graph.png`.
