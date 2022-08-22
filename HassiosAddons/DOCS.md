# Hostpot wifi pour Raspberry avec RaspAP

![](https://i.imgur.com/xeKD93p.png)
[![Release 2.8.4](https://img.shields.io/badge/release-v2.8.4-green)](https://github.com/raspap/raspap-webgui/releases) [![Awesome](https://awesome.re/badge.svg)](https://github.com/thibmaek/awesome-raspberry-pi) [![Join Insiders](https://img.shields.io/static/v1?label=Join%20Insiders&message=%E2%9D%A4&logo=GitHub&color=ff69b4)](https://github.com/sponsors/RaspAP) ![https://travis-ci.com/github/raspap/raspap-webgui/](https://api.travis-ci.org/RaspAP/raspap-webgui.svg) [![Crowdin](https://badges.crowdin.net/raspap/localized.svg)](https://crowdin.com/project/raspap) [![Twitter URL](https://img.shields.io/twitter/url?label=%40RaspAP&logoColor=%23d8224c&url=https%3A%2F%2Ftwitter.com%2Frasp_ap)](https://twitter.com/rasp_ap) [![Subreddit subscribers](https://img.shields.io/reddit/subreddit-subscribers/RaspAP?style=social)](https://www.reddit.com/r/RaspAP/)

RaspAP is feature-rich wireless router software that _just works_ on many popular [Debian-based devices](#supported-operating-systems), including the Raspberry Pi. Our popular [Quick installer](#quick-installer) creates a known-good default configuration for all current Raspberry Pis with onboard wireless. A fully responsive, mobile-ready interface gives you control over the relevant services and networking options. Advanced DHCP settings, WireGuard and OpenVPN support, [SSL certificates](https://docs.raspap.com/ssl-quick/), security audits, [captive portal integration](https://docs.raspap.com/captive/), themes and [multilingual options](https://docs.raspap.com/translations/) are included.

RaspAP has been featured on sites such as [Instructables](http://www.instructables.com/id/Raspberry-Pi-As-Completely-Wireless-Router/), [Adafruit](https://blog.adafruit.com/2016/06/24/raspap-wifi-configuration-portal-piday-raspberrypi-raspberry_pi/), [Raspberry Pi Weekly](https://www.raspberrypi.org/weekly/commander/) and [Awesome Raspberry Pi](https://project-awesome.org/thibmaek/awesome-raspberry-pi) and implemented in countless projects.

We hope you enjoy using RaspAP as much as we do creating it. Tell us how you use this with [your own projects](https://github.com/raspap/raspap-awesome).

![](https://i.imgur.com/uhBFoOB.png)
![](https://i.imgur.com/EiIpdOS.gif)
![](https://i.imgur.com/eCjUS1H.gif)
![](https://i.imgur.com/5FT2BcS.gif)
![](https://i.imgur.com/RKaBFrZ.gif)

## Installation

Basic Intallation, You can config 80/tcp in configuration tab of this addon. (More configuration is on the web gui)

**YOU DO NOT NEAD SOME MORE INFORMATION FOR SOME CONFIG**, Yes sadly some Home Assistant config can't do some configuration (example the next paragraph like _Prerequisites_, _Updates_ or _Quick installation_...) 

Link of the [Official github](https://github.com/RaspAP/raspap-webgui).
Link of the first HA addon made by [ArminasTV](https://github.com/ArminasTV/Hassio-addons/) **OBSOLETE**.


## Prerequisites
Start with a clean install of the [latest release of Raspberry Pi OS (32-bit) Lite](https://www.raspberrypi.org/software/operating-systems/#raspberry-pi-os-32-bit). The Raspberry Pi OS desktop and 64-bit beta distros are unsupported.

1. Update Raspbian, including the kernel and firmware, followed by a reboot:
```
sudo apt-get update
sudo apt-get full-upgrade
sudo reboot
```
2. Set the "WLAN country" option in `raspi-config`'s **Localisation Options**: `sudo raspi-config`

3. If you have a device without an onboard wireless chipset, the [**Edimax Wireless 802.11b/g/n nano USB adapter**](https://www.edimax.com/edimax/merchandise/merchandise_detail/data/edimax/global/wireless_adapters_n150/ew-7811un) is an excellent option – it's small, cheap and has good driver support.

With the prerequisites done, you can proceed with either the Quick installer or Manual installation steps below.


## Quick installer in webgui settings
Install RaspAP from your device's shell prompt:
```sh
curl -sL https://install.raspap.com | bash
```
The [installer](https://docs.raspap.com/quick/) will complete the steps in the manual installation (below) for you.

After the reboot at the end of the installation the wireless network will be
configured as an access point as follows:
* IP address: 10.3.141.1
  * Username: admin
  * Password: secret
* DHCP range: 10.3.141.50 — 10.3.141.255
* SSID: `raspi-webgui`
* Password: ChangeMe

**Note:** As the name suggests, the Quick Installer is a great way to quickly setup a new AP. However, it does not automagically detect the unique configuration of your system. Best results are obtained by connecting to ethernet (`eth0`) or as a WiFi client, also known as managed mode, with `wlan0`. For the latter, refer to [this FAQ](https://docs.raspap.com/faq/#headless). Special instructions for the Pi Zero W are [available here](https://docs.raspap.com/ap-sta/).

Please [read this](https://docs.raspap.com/issues/) before reporting an issue.


## Configuration


TODO

## Changelog & Releases


Update at version 2.8.4

## Support


TODO

## Authors & contributors

L'add-on est réalisé par [ArminasTV][Youtube]. Retrouvez moi sur mon [Twitter][Twitter], [Facebook][Facebook] et [Instagram][Instagram].

For a full list of all authors and contributors,
check [the contributor's page][contributors].

## License

GNU GENERAL PUBLIC LICENSE

[Youtube]: https://www.youtube.com/c/ArminasTV
[Facebook]: https://www.facebook.com/ArminasTV
[Instagram]: https://www.instagram.com/arminas.stream/?hl=fr
[Twitter]: https://twitter.com/ArminasTV
