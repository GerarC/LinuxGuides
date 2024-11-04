---
tags: 
- display_manager
- tui
---

# Ly
[Ly](https://github.com/fairyglade/ly) is a [TUI](glossary.md#TUI%20application) [Display manager](glossary.md#Display%20Manager), very simple and at the same time very pretty. It could be a light and fast alternative for lightdm or SDDM.

## Installation
You should verify if Ly is available in your current Distribution repositories. If it is, then install it with the [Package manager](glossary.md#Package%20Manager) your distro  use. For example, to install it in arch you can use `pacman -S ly`. If there's no version available, then you have to compile it from [source code](https://github.com/fairyglade/ly).

## Configuration
Once you have Ly installed you should enable it with your Daemon Manager. and when you restart the PC you will have Ly running. By default it comes without Background, but you can configure `doom` or `cmatrix` inside the */etc/ly/config.ini*.

### Systemd
If you use systemd you can enable the service using the next command:
~~~ bash
systemctl enable ly.service
~~~