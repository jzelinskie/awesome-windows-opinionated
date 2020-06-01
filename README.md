# Awesome Windows - Opinionated Edition

At some point, these "awesome" lists get too many entries for the same type of program which makes them no better than googling.
I'm not trying to give you all possible options, rather what I consider to be the best option for the respective fields.

If something you use isn't here, that's because you already know you need it.
By omitting things, I'm not saying you shouldn't install Spotify because I recommend foobar2000.

## Applications

### Audio

- [ASIO4ALL](http://www.asio4all.org/) - Likely, you _really_ don't need this, but if you want an ASIO driver, this is the one.
- [EAC](http://www.exactaudiocopy.de/) - This is how you should rip music if you still own any physical music.
- [EqualizerAPO](https://equalizerapo.com/) - This is a system-wide EQ tool. There are other projects that provide better GUIs for it, but this is the core EQ that they all share.
- [Foobar2000](http://www.foobar2000.org/) - This is the only native music player you should be using. Various plugins available for things like transcoding, tagging, replay gain, improving the UI, scrobbling, etc...

Everything here is for playback because Windows sucks at recording. Use a Mac if you need a DAW.

### Chat

- [IRCCloud](https://github.com/irccloud/irccloud-desktop/releases) - This is a paid service that's like an IRC bouncer on steroids. This client is just an electron app, but it's my preference for IRC. 
- [Riot.im](https://riot.im) - This is my preference for Matrix. You can use it to connect to IRC, but I find the gateways too laggy.

I only included these two because they're clients for open chat protocols. If you need a specific chat app to talk with someone, just use it. I cannot recommend any chat apps that try to support every protocol because they will always harm user experience.

### Developer

- [Visual Studio Code](https://code.visualstudio.com/) - Text Editor. This isn't 2005 anymore: forget Notepad++.
- [WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10) - Linux in Windows. Install your distro of choice and here's the rest of your dev tools. Why bother with native Windows dev tools?
- [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal-preview/9n0dx20hk701) - Official Microsoft Terminal Emulator. I would recommend ConEmu, but I'm going to lean first-party when that solution is good enough.

I'm not a Windows developer. As a result, when I do target Windows, I don't use their toolchains. It's just not how you make portable software, so I cannot recommend them in good faith. Microsoft themselves have seemingly admitted this by their recent efforts with WSL and supporting crossplatform development in general.

### Documents

- [Calibre](http://calibre-ebook.com/) - Slow af, but the best converter for ebook formats if you're trying to load something onto a Kindle or Remarkable.
- [LibreOffice](https://wwww.libreoffice.com/en/) - The open source office suite. But do you really need one? Google Drive or Office 365 is crossplatform, cloud hosted, and real-time collaborative.
- [Sumatra PDF](https://www.sumatrapdfreader.org/free-pdf-reader.html) - Lightning fast PDF reader. But do you really need one? Your browser also opens PDFs.

### Networking

- [NextDNS](https://nextdns.io) - Secure DNS with configurable adblocking. An alternative to [PiHole](https://pi-hole.net) if you want someone else to host it for you.
- [Viscosity](https://www.sparklabs.com/viscosity/) - Best all around OpenVPN client. I actually recommending using the client your provider recommends, because they often implement additional security features that are outside the OpenVPN standard.

If the Windows machine is a desktop in your home network, you should not install or change _anything_ related to the network because you should be inheriting a good configuration that you've made _at the network-level_. I even run multiple VPN connections that available to the local network via SOCKS/HTTP proxies so that any device can use them.

### Overclocking / Hardware Inspection

- [AIDA64](https://www.aida64.com/products/aida64-extreme) - The best stress-testing tool.
- [CrystalDiskInfo](https://crystalmark.info/en/download/) - Check the healthiness of installed storage devices. Has alternative versions that change no behavior but adds pictures of anime girls to the UI.
- [HWiNFO64](https://www.hwinfo.com/download/) - Inspects the installed hardware and sensors (voltages, temperature) of the current system. This is basically CPU-Z, GPU-Z, Speccy, and HWMonitor rolled into one.
- [MSI Afterburner](https://www.msi.com/page/afterburner/) - Create profiles that alter fan curves, voltages, clock speeds, etc... for your GPU. This does not require an MSI GPU.

### Privacy

I actually don't recommend running any of the tools that does sweeping changes across the whole system to disable telemetry. I just run through the exposed options in the Settings menu. Windows is full of crufty state that builds up over time; power users are familiar with the process of reinstalling the OS every so often. I avoid making changes to the OS that are more than skin deep to keep things simple, easily reproducible, and unlikely to break anything in the future.

### Security

- [1password](https://1password.com) - Password Manager

You really should only be using the built-in Windows components: Windows Defender (Firewall), MSE (AntiVirus), BitLocker (full disk encryption).

### Utilities

- [7-Zip](http://www.7-zip.org/) - Supports every major compression and archive format. No reason to use anything else or any additional software.
- [DisplayFusion](https://www.displayfusion.com/) - Various utilites for managing multiple displays. I normally use it to set up wallpapers and mostly disable the service, but the other utilities can be very useful.
- [EarTrumpet](https://github.com/File-New-Project/EarTrumpet) - Windows Volume Mixer replacement. I have no idea why the native Windows mixer doesn't look/function exactly like this.
- [PowerToys](https://github.com/microsoft/PowerToys/releases) - Various power user utilities written by Microsoft that should just be built into Windows. Alpha quality.
- [ShareX](https://getsharex.com/) - Windows Snipping Tool on steroids. What if pressing Printscreen uploaded to imgur and put the direct link in your clipboard?
- [WizTree](https://antibody-software.com/web/software/software/wiztree-finds-the-files-and-folders-using-the-most-disk-space-on-your-hard-drive/) - Visualize what's eating space on your harddrive. This uses metadata in the NTFS filesystem so that it can run orders of magnitude faster than the other tools. I have no idea why Microsoft doesn't use this strategy everywhere and abandon full-text indexing so that they can save thousands of cpu/disk hours, especially on laptops.

### Video

- [Davinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve/) - If you aren't already dedicated to a paid video editor, this by far the best free one and is entirely GPU accelerated so the previews are very performant.
- [Handbrake](https://handbrake.fr/) - Video transcoder. This is mostly useful for the default profiles that are web-optimized.
- [MPC-HC](https://github.com/clsid2/mpc-hc/releases) - The highest quality video player on any OS. The upstream project died, but one of the authors still maintains it. Some users have moved on to a completely different project, [mpv](https://mpv.io), but the GUIs for that suck.
  - [madVR](http://www.madvr.com/) - This is a DirectShow video renderer that is the only external filter you need for MPC-HC.
- [OBS](https://obsproject.com/) - Swiss army knife for streaming or recording video.
- [VLC](https://www.videolan.org/vlc/) - Backup video player that supports the most features. For example, you can set the Renderer to cast videos directly to your Chromecast.
