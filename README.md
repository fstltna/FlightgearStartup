# Flightgear Startup Scripts (1.0.0)
Startup scripts for the Flightgear server software - uses the "screen" command to manage session. This also restarts the Flightgear server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/FlightgearStartup)

---

These start up the Flightgear server at boot time with a "screen" process.

1. Copy **flightgear** into **/home/flightgear/bin** - make sure it is executable
2. Copy **startflightgear** into **/home/flightgear/local** - make sure it is executable
3. Add "**@reboot /home/flightgear/bin/flightgear start**" to the crontab

When you want to view the Flightgear console, just enter "**screen -r**" in your shell.

To disconnect from the Flightgear console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /home/flightgear/server-data/nostart**". To reenable it type "**rm /home/flightgear/server-data/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
