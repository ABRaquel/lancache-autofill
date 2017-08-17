# lancache-autofill
Automatically fill a Lancache with content.

# Requirements

* Ubuntu 16.04 x64

# Installation

* `git clone https://github.com/zeropingheroes/lancache-autofill.git`
* `cd lancache-autofill`
* `sudo ./install.sh`

# Usage

Set the default Steam account to be used when queueing apps for download:

`nano .env`

Log in to your Steam account to SteamCMD:

`/usr/games/steam/steamcmd.sh +login your-username-here`

Search for the apps you wish to download to find their app ID:

`./lancache-autofill steam:search-apps "team fortress 2"`

	440     Team Fortress 2
	[...]

Queue the app for download by ID:

`./lancache-autofill steam:queue-app 440`

Start downloading items in the download queue:

`./lancache-autofill steam:start-downloading`

View the download queue to see the status of the downloads:

`./lancache-autofill steam:show-queue`

Clear the temporary download location:

`./lancache-autofill app:initialise-downloads-directory`

# Reference

* [SteamCMD Reference](https://developer.valvesoftware.com/wiki/SteamCMD)
* [SteamCMD Commands and Variables](https://github.com/dgibbs64/SteamCMD-Commands-List/blob/master/steamcmdcommands.txt)
* [Laravel Query Builder](https://laravel.com/docs/5.4/queries)
* [Laravel Artisan Console](https://laravel.com/docs/5.4/artisan)
* [Symfony Process Component](http://symfony.com/doc/current/components/process.html)
