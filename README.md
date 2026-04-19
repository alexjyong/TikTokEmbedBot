# TikTok Discord Bot

This bot allows you to embed TikTok videos directly into Discord. Currently, this project is hosted on an **Oracle Free Instance** running **Ubuntu Server**.

## Prerequisites

To run this bot, you will need the following:
* **Python:** Ensure Python 3.x is installed on your machine.
* **Discord Bot Token:** Obtain this from the [Discord Developer Portal](https://discord.com/developers/applications).
* **discord.py Library:** Install it via pip:
  ```bash
  pip install discord.py
  
## Running as a service
You will need to create a service using nano
```bash
sudo nano /etc/systemd/system/tiktokbot.service
```
There is a ini.toml included in the repo to make your python script run as a service. You will need to use the following commands to insure it starts with the machine and restarts on fail:
```bash
  sudo systemctl daemon-reload
  sudo systemctl enable tiktokbot
  sudo systemctl start tiktokbot
```  
For support please reach out on Discord: https://discord.gg/qrcCHA9g
