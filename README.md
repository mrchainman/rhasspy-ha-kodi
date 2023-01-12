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
