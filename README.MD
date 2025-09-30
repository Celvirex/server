# GitHub Codespace auto start and keep alive.

This method is a way to host a Minecraft server or any server every for how long on GitHub Codespaces, as I can't afford dedicated hosting.

---

## Getting Started

Follow these instructions to set up your own free Minecraft server hosting using GitHub Codespaces. **PLEASE GIVE ME CREDITS. I FOUND THIS METHOD ALL BY MY OWN RETARDS.**

### Instructions

1. **Clone or fork the repository**  
   ```sh
   git clone https://github.com/celvirex/server.git

2. **Add the following secret variables in your repository's** Secrets settings:
```sh
GH_TOKEN: ${{ secrets.CODESPACE_TOKEN }}

CODESPACE_NAME: example (replace example with your own Codespace name)
```
To find your Codespace name, use the GitHub CLI command: gh codespace list

4.**Create the .devcontainer devcontainer.json file**

You can either learn how to create this file yourself or use my example devcontainer.json file.

5. **You're done!**

Your Minecraft server or server should now be hosted on GitHub Codespaces. Just remember, it will restart every 4 hours.

***REMEMBER TO DO NOT MODIFY THE WORKFLOW CRON JOB TO AVOID RATE LIMITING.***
If you know what your doing and you want it your own cron job, I suggest don't lower it too much like a 1sec or 1min.
