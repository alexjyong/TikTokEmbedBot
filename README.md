The following are prerequisites:
  Python installed on your machine.
  A Bot Token from the Discord Developer Portal.
  The discord.py library: pip install discord.py
You will need a local instance or cloud instance running to host your code. Currently this runs on an oracle free instance running ubuntu server. You will need to install python and the discord python library.
You will need to create a service using nano sudo nano /etc/systemd/system/tiktokbot.service and there is a ini.toml included in the repo to make your python script run as a service. You will need to use the following commands to insure it starts with the machine and restarts on fail:
  sudo systemctl daemon-reload
  sudo systemctl enable tiktokbot
  sudo systemctl start tiktokbot
  
