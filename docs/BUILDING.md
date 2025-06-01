# Developer Guide: Building & Installing ESPHome Firmware

## Clone this repo

```bash
git clone https://github.com/vt-vaio/rowi2.git
```

## Prepare esphome development environment

```bash
# cd into checkout folder
cd rowi2

# check python version
python3 --version
```
# Create virtual environment

## using standard python way
```bash
python3 -m venv .venv

# to activate venv
source .venv/bin/activate
```
## using python oh-my-zsh plugin
```bash
mkv
# to activate afterwards
vrun
```

# install esphome
```bash
pip install --upgrade pip
pip install esphome

# to update after new versions of esphome is released use
pip install --upgrade esphome
```

## Build using esphome cli

To be able to deploy the factory image to a running instance you need to specify the manual_ip settings in [factory.yaml][factory]


```yml
wifi:
  manual_ip:
    # Set this to the IP of the ESP
    static_ip: 192.168.x.x
    # Set this to the IP address of the router. Often ends with .1
    gateway: 192.168.x.1
    # The subnet of the network. 255.255.255.0 works for most home networks.
    subnet: 255.255.255.0
  on_connect:
    - delay: 5s
    - ble.disable:
    - lambda: id(improv_ble_in_progress) = false;
  on_disconnect:
    - ble.enable:
```

Build and install firmware on the device:

```bash
esphome run rowi2-plug.factory.yaml
```

If the device is connected to the USB port, ESPHome will allow you to select the install type.

[factory]: ../rowi2-plug.factory.yaml