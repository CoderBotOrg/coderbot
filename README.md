# CoderBot

A RaspberryPI-based programmable robot for educational purposes. Check the [project website](https://www.coderbot.org) for more information.

For further information about development and technical documentation, see the [Wiki](https://github.com/CoderBotOrg/coderbot/wiki).

This repository contains the backend, along with some configuration applied on the base system image.

### Quickstart

Prerequisites:

```bash
sudo apt install python3 python3-venv
```

Be sure you have Python **3.6**. You may need to use `python3.6` and `python3.6-venv` packages on some repositories with python3 already pointing to **3.7** (e.g. debian unstable/sid).



```bash
git clone https://github.com/CoderBotOrg/coderbot.git
cd coderbot
python3 -m venv .
source bin/activate

# Install the basic requirements
pip3 install -r requirements_stub.txt
# Additional packages if you are running the real thing
pip3 install -r requirements.txt

# Start the backend in stub mode
PYTHONPATH=stub python3 init.py

# or, run the real thing if you're on a physical RPi
python3 init.py
```

The legacy API and frontend application is available at `localhost:5000`.

The new API is at `localhost:5000/v2`, while the new application is served at `localhost:5000/vue` (assuming the [vue-app](https://github.com/coderbotorg/vue-app) build is placed in the `dist/` folder).

To see the dynamic documentation of the new API, clone the [swagger-ui](https://github.com/coderbotorg/swagger-ui) repository inside the `coderbot/` folder and it'll be live at `localhost:5000/v2/ui/index.html`.

