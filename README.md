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

## Running with Docker

You can also run this bot using Docker for easier deployment and isolation.

### Prerequisites
* [Docker](https://docs.docker.com/get-docker/) installed on your machine.
* [Docker Compose](https://docs.docker.com/compose/install/) (optional, but recommended).

### Using Docker Compose (Recommended)

1. Create a `.env` file in the project root or copy the `.env.example` file to `.env`. Fill it with these details:
   ```bash
   DISCORD_TOKEN=your_bot_token_here
   ```
2. Start the bot:
   ```bash
   docker-compose up -d
   ```

### Using Docker CLI

1. Build the image:
   ```bash
   docker build -t tiktok-embed-bot .
   ```
2. Run the container:
   ```bash
   docker run -d \
     --name tiktok-bot \
     -e DISCORD_TOKEN=your_bot_token_here \
     --restart unless-stopped \
     tiktok-embed-bot
   ```

For support please reach out on Discord: https://discord.gg/qrcCHA9g
