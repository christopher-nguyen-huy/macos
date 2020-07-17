Install
	Homebrew
	Firefox
	Firefox Dev
	Kitty
	Alacrity
		brew cask install alacritty
	ITerm2
	Sublime
	Atom
	Pycharm CE
		Install java first
	Xcode
		Otherwise `cd /Applications && touch Xcode.app` to clear Spotlight search results
	python3
	Transmission
	Insomnia
		brew cask install insomnia
	Redis
		brew install redis
		To have launchd start redis now and restart at login:
			brew services start redis
		Or, if you don't want/need a background service you can just run:
			redis-server /usr/local/etc/redis.conf
	MariaDB
		https://mariadb.com/kb/en/library/installing-mariadb-on-macos-using-homebrew/
	Navicat
	FastoReids
Generate SSH keys
TextEdit
	uncheck everything
	save as utf-8
	Set tabs spacing
		terminal: defaults write com.apple.TextEdit "TabWidth" '4'
Dock
	Remove everything from dock
Notifications
	Remove everything
Finders
	Show these items on the Desktop: Uncheck Hard Disk
	New Finder Window: Home
	Sidebar: Airdrop, Applications, Downloads, Home
	Locations: Uncheck
	Tags: Uncheck
	Show all Filename Ext
	Uncheck show warning before changing file extension
	Uncheck show warning before removing from icloud
	Search: The current folder

Settings
General
	Dark
	small icons
	always scrollbars
	jump to scrollbar click
	default browser: firefox dev
	recent items: None
	uncheck handoff mac & icloud
Desktop & Screen Saver
	Black BG
	Screen Saver start after: Never
Mission Control
	Uncheck Everything
	Check group windows by application
	Dashboard: Off
	Hot Corners
		Remove All hot corners
Dock
	Size: Small
	Magnification: On
	Position: Left
	Minimize Using: Scale effect
	Uncheck: Animate Opening applications
	Uncheck: Show recent applications
Security
	Set require password after 1h
Spotlight
	Keep only:
	Applications
	Calculator
	Conversion
	Folders
	System Preferences
	Uncheck Allow spotlight in Look up
Display
	Scaled: More Space
	Uncheck Auto Brightness
	Airplay Display: off
	Nightshift: Off
Energy Saver
	Uncheck Automatically Switch graphics
Keyboard
	Keyboard
		Repeat rate: 8/8
		Delay until repeat: 5/6
		Check turn backlight off after 30s
		Uncheck emoji bar
		Check Use f1, f2
	Text
		Clear replacements
		Uncheck first 3 (4 if touchbar)
	Shortcuts
Trackpad
	Uncheck Look up & data detectors
	Check Secondary
	Check Tap to click
	Tracking Speed: 6/10
	Uncheck rotate
	Uncheck everything under More Gestures except
		first
		3 fingers up for mission control
		3 fingers down for app expose
Software Updates
	Advanced
		Check of updates: disable
Sharing
	Change Hostname
Users & Groups
	Change Icon
Siri
	Disable Siri
Date & Time
	Timezone: NY
	Clock: 24H
	Show Date
Accessibility
	General
		Disable Sticky Keys


Installing API requirements
- Install redis
- Install mysql
	- create user
	- mysql < dump.sql
- Install python 3.6
- Create venv
- Install Dependencies
	- Mysql client
	- brew install cmake
	- brew install mysql-client
	- export LIBRARY_PATH="$LIBRARY_PATH:/usr/local/opt/openssl/lib/"
	- export PATH="/usr/local/opt/mysql-client/bin:$PATH"
- Create logging file in ‘~/var/log/fallback.log’
- Tweak settings in settings.py

Resetting SMC https://support.apple.com/en-us/HT201295
- Power down
- Shift-Ctrl-Alt-Power for 10 seconds
- Release
- Power