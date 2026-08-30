# Developer Guide: Building & Installing ESPHome Firmware

## Clone this repo

```bash
git clone https://github.com/vt-vaio/rowi2.git
```

## Prepare esphome development environment

This project uses [uv](https://docs.astral.sh/uv/) to manage the Python virtual environment. Install it first if you don't already have it:

```bash
# see https://docs.astral.sh/uv/getting-started/installation/ for other options
curl -LsSf https://astral.sh/uv/install.sh | sh
```

```bash
# cd into checkout folder
cd rowi2

# check uv version
uv --version
```

# Create virtual environment and install esphome

The required Python version and esphome dependency are declared in [`pyproject.toml`][pyproject]. Running `uv sync` creates `.venv` with a matching Python version and installs esphome into it:

```bash
uv sync

# to update after new versions of esphome is released use
uv lock --upgrade-package esphome
uv sync
```

Once synced, run esphome commands with `uv run esphome ...` — this uses `.venv` automatically without needing to activate it.

## Build using esphome cli

To be able to deploy the factory image to a running instance you need to specify the manual_ip settings either in [factory.yaml][factory] or [plug.yaml][plug]


```yml
wifi:
  manual_ip:
    # Set this to the IP of the ESP
    static_ip: 192.168.x.x
    # Set this to the IP address of the router. Often ends with .1
    gateway: 192.168.x.1
    # The subnet of the network. 255.255.255.0 works for most home networks.
    subnet: 255.255.255.0
```

Compile the firmware without installing it (useful to check the build succeeds without a device connected):

```bash
uv run esphome compile rowi2-plug.factory.yaml
```

Build and install firmware on the device:

```bash
uv run esphome run rowi2-plug.factory.yaml
```

If the device is connected to the USB port, ESPHome will allow you to select the install type.

[factory]: ../rowi2-plug.factory.yaml
[plug]: ../rowi2-plug.yaml
[pyproject]: ../pyproject.toml