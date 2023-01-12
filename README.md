# rhasspy-ha-kodi
Files to control kodi via rhasspy using homeassistant

# Assumptions
I assume, that you already have integrated Kodi into homeassistant and allowed the JSONRPC Protocol

# Structure
rhasspy contains all relevant rhasspy files which live under profile/en/
the entities script is a modified version of the one provided by homeassistant, it includes:
	- new domain: kodi
	- media_player only shows music assistant players
	- sanitizing of names to prevent rhasspy errors

homeassistant contains the relevant scripts and intend configuration

There are also some intends and scripts, which are not relevant to kodi, but you might find them usefule nontheless

Some intends handle kodi via mass (Musicassistant), either configure the addon in Homeassistant or adapt the intents as neccessery

Contributions are welcome, I hope we can create a nice library of intents and voicecommands


Have fun :D


# Longer explanation of setup

If you want to use my files without much editing, here is what is used:

Homeassistant:
	- Musicassistant with spotify
	- Kodi integration

Kodi:
	- Jsonrpc enabled, see kodi wiki
	- playrandom addon https://github.com/rmrector/script.playrandomvideos
	- southpark addon https://github.com/wargio/plugin.video.southpark_unofficial
	- local movies and shows
	- If you have multiple kodi instances, I strongly recommend to setup a shared database and store your files on a NAS, since the scripts have no errorhandling
