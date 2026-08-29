# SysMon — System Monitoring Dashboard

A lightweight, web-based system monitoring dashboard for Omarchy and Arch Linux. Real-time metrics accessible from any device on the network.

## What is it?

A Python web application that reads system metrics (CPU, memory, disk, network, temperatures, battery) via psutil and serves them through a clean web interface. Designed for local network monitoring of Linux machines — no cloud, no accounts, no external dependencies.

## What does it do?

- **Real-time metrics**: CPU (per-core + total), memory, disk usage, network I/O
- **Process monitoring** (planned): top processes by CPU/RAM
- **Hardware sensors**: Temperatures and fan speeds (when available via psutil)
- **Battery status**: For laptops (capacity, charging state, time remaining)
- **Customizable widgets**: Enable/disable metrics, rearrange layout
- **Lightweight and fast**: Minimal overhead, runs as a simple Python service
- **Network accessible**: Access via browser on any device on the same network
- **No database**: In-memory metrics, no persistence needed

## Technologies

Python 3.x, psutil, built-in http.server (or FastAPI for extended version)

## Installation

### Dependencies

- Python 3.x
- psutil (install via `pacman -S python-psutil`)

### Install from source

```bash
git clone https://github.com/ThorrijaDEV/sysmon-dashboard
cd sysmon-dashboard
make install
```

## Usage

Run the dashboard:

```bash
sysmon
```

By default, the dashboard will be available at http://localhost:8080

You can specify a different host and port:

```bash
sysmon --host 0.0.0.0 --port 8080
```

## Configuration

The dashboard can be configured by editing the source code or by creating a config file (future feature).

## Status

**Functional / Maintenance**

Core metrics working: CPU, memory, disk, network, temperatures, battery. Web interface accessible locally and over LAN. Process monitoring planned.

## Repository Note

This repository contains documentation only. The implementation is private code.

## License

MIT