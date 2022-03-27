# Home Assistant Windows Portable (HassWP) CTM FORKED

This forked fixes the TIMEZONE issue faced on certain windows. **If you face any issue in this forked please use AlexxIT version as its is more stable**

Portable version of Home Assistant for Windows.

Minimum requirements: **Windows 8+ 64-bit**. *If you need Windows 7 or 32-bit support - use [old version] from AlexxIT (https://github.com/AlexxIT/HassWP/releases/tag/v2021.12.10).*
TESTED on: **Windows Server 2016 Standard**


Preinstalled:

- [WinPython](https://winpython.github.io/) v3.9.10 64-bit
- [Home Assistant](https://www.home-assistant.io/) v2022.2.9
- [HACS](https://hacs.xyz/) v1.22.0
- [SonoffLAN](https://github.com/AlexxIT/SonoffLAN) v2.4.6
- [XiaomiGateway3](https://github.com/AlexxIT/XiaomiGateway3) v1.6.5
- [YandexStation](https://github.com/AlexxIT/YandexStation) v3.8.0
- [StartTime](https://github.com/AlexxIT/StartTime) v1.1.6


**Attention:** Direct works in Windows is not tested by the core developers of Home Assistant. So some components/integrations may not work at all.

# HOW TO USE

1. Download [CTMHomeAssistant2022-3-7.rar](https://github.com/ctmaqil/HassWP/releases/latest)
2. Unpack in a folder
3. Run hass.cmd
4. Press any key to start.

Useful files:

- `hass.cmd` - run Home Assistant and default Browser
- `web.url` - open default Browser with http://localhost:8123/
- `config/reset.cmd` - reset Home Assistant but don't touch config files

# Supervisor and Addons

HassWP **don't have and can't have supervisor** and any Hass.io addons. Supervisor can be installed only over Docker. Nativelly Docker works only on Linux core. In any other OS it will use virtualization.

If you really needs Hass.io addons on Windows - use [virtualization](https://www.home-assistant.io/installation/windows).

# Move config

You can transfer your configuration to another Hass installation at any time. In another HassWP, venv, docker, hass.io, etc. Windows or Linux, it doesn't matter. Just move the contents of the `config` folder to a new location. Remember about `config/.storage` folder, it is also important. The `config/deps` folder may not be moved, but if you do, it's not a problem.

Before any movement - stop the old and new Home Assistant!

# Problems

1. If you have this problem:

   ```
   File "C:\HassWP\python-3.8.7\lib\socket.py", line 49, in <module>
       import _socket
   ImportError: DLL load failed while importing _socket
   ```
   
   Install Windows update: **KB2533623**.
