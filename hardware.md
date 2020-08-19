# Hardware

## HDMI port outputting yCBR instead of RGB
[Sometimes](https://forums.macrumors.com/threads/hdmi-color-issue-on-mac-mini.2219029/) apple thinks that we plugged in a TV and will give bad colors

- Must disable SIP (System integrity protection)
	- reboot mac
	- hold `cmd-r` down, bootup should slow down, enters recovery mode
	- Utilities -> Terminal
	- `csrutils disable`
	- reboot
- Must disable _read-only_ system partition
	```shell
	$ sudo mount -uw /
	$ killall Finder
	```

- Download, `chmod +x` and run [patch-edid.rb](https://gist.github.com/adaugherity/7435890)
- It creates a `DisplayVendorID-xxxx` folder
- Copy that folder into `/System/Library/Displays/Contents/Resources/Overrides`
	- If the same folder name already exists, back it up

### Ressources
- https://www.youtube.com/watch?v=cDNvpYGIl_4
- https://www.mathewinkson.com/2013/03/force-rgb-mode-in-mac-os-x-to-fix-the-picture-quality-of-an-external-monitor
- https://redd.it/caiue5