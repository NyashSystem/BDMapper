BDMapper [BackDoorMapper]
<div align="center"> <h1>BDMapper</h1> <p><i>A powerful backdoor injector and telemetry system for Minecraft plugins.</i></p> </div><div align="center"> <img alt="Logo" src="logo.png"/> </div><div align="center"> <a href="https://github.com/VoxelHax/BDMapper/issues"><img alt="Open issues" src="https://img.shields.io/github/issues-raw/VoxelHax/BDMapper"/></a> <a href="https://github.com/Voxelhax/BDMapper/releases/latest"><img alt="GitHub downloads" src="https://img.shields.io/github/downloads/VoxelHax/BDMapper/total"/></a> <img alt="Code size" src="https://img.shields.io/github/languages/code-size/VoxelHax/BDMapper"/> <a href="https://www.codefactor.io/repository/github/voxelhax/BDMapper"><img alt="CodeFactor" src="https://www.codefactor.io/repository/github/voxelhax/BDMapper/badge"/></a> <a href="https://discord.gg/xtaktPTzYp"><img alt="Discord" src="https://img.shields.io/discord/928214827095175199"></a> </div><div align="center"> <a href="https://github.com/Voxelhax/BDMapper/releases/latest"><img alt="Download" src="https://img.shields.io/badge/-DOWNLOAD_LATEST_RELEASE_(CLICK)-blue?style=for-the-badge"/></a> </div><br>
Languages: English, Русский, Українська

BDMapper is a modern and powerful universal backdoor injector compatible with all Bukkit/Spigot/Paper plugins. Unlike traditional injectors, BDMapper allows you to integrate backdoors into any plugin without manually modifying the code every time. It features a powerful camouflage engine that makes your backdoor nearly impossible to detect without advanced tools.

BDMapper was developed by the VoxelHax team to test and secure Minecraft servers.

🚀 Features
Universal Compatibility: Works with all Bukkit forks on any Minecraft version.
Easy Patcher (.exe): A user-friendly way to patch plugins without touching the command line.
Telemetry System: Real-time data reporting via Discord Webhooks.
Powerful Camouflage: Hide your backdoor from players and optimization tools.
🛠 How to use (The Easy Way)
BDMapper now includes a dedicated .exe Patcher for a seamless experience:

Prepare the folder: Place both BDMapper.exe and the BDMapper.jar in the same folder.
Drag & Drop: Drag your desired plugin (.jar) onto the BDMapper.exe file.
Set Target Key: The program will prompt you to enter your Target Key.
Done! The patcher will process the plugin and generate a patched version automatically.
📊 Telemetry & Webhooks
One of BDMapper's strongest features is its Telemetry System. You can connect it to a Discord Webhook to receive real-time data about your server and players.

To set this up, simply provide your Discord Webhook URL when running the patcher/program.

🛰 Server Launch Information
Every time your patched plugin starts, BDMapper sends the following details to your webhook:

Core: (e.g., Spigot, Paper, Forge)
Patched Plugin: The name of the plugin being injected.
Bukkit Version: The version of the API.
Hosting Country: Where your server is located.
Server IP & Port: Your server's address.
Target Key: The specific key used for the backdoor.
Plugin List: A list of all active plugins.
👤 Player Join Information
Whenever a player joins, BDMapper sends:

Skin Face: Reference to the player's skin.
UUID: (e.g., 77bcc289-45dc-365d-b3fb-389dc20dbb98)
Client Type: (e.g., Fabric, Optifine, Vanilla)
Version: The Minecraft version the player is using.
Location: (e.g., `United
