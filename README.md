# QPunishments
QPunishments is a punishment system designed and developed by Quapi for maximum staff efficiency, offering a full all-in-one system including a built-in history and proof system.
<br /> <br />
The system is currently developed on top of BungeeCord 1.18 and a sister Velocity 3.1.x version is in the works and will be released at some point in the future
<br /> <br />
Please Note: For those who will choose to use this system instead of other older systems, as this is currently in alpha state, the chances of you encountering a lot of bugs potentially system breaking are quite high, it is possible that there aren't many bugs or risks, at least security-wise, although watch out for them and if you encounter one, report it immediately in the issues tab.

## Features

* History and proofing system for easy tracking on players
* A full lookup system allowing for checking a player's punishment history, comments, first and last login and his name history
* Fully working per-server / global punishment system
* 99% of messages customizable (System-critical messages are non-changable currently)<br>
* Redis & MySQL support

## Commands and usages
####   Command arguments explanation:
* [-is] = Silent punishment, removal
* [duration] = The duration of the punishment, for example 7m (minutes), 7h (7 hours), 7d (7 days)
* [server:<**?**>] = A specific server to provide the punishment, for example (server is case-sensitive): 
/qban Quapi server:ExampleServer
* [reason] = The reason for the given punishment.
* [-debug] = Debug argument will show you the comment id, only works on comment module
* [module] = A specific type of punishment to lookup. Currently available: ban, mute, kick, comment
* [limit] = The amount of the entries the lookup will return, only works modules
##### History command:
The **command** argument is crucial and may be one of the following:
> editcomment, removecomment, removepunishment, getcomment
#### Commands
> * qpunishments.command.ban - /qban <**playerName**> [-s] [duration] [server:<**?**>] [reason]
> * qpunishments.command.mute - /qmute <**playerName**> [-s] [duration] [server:<**?**>] [reason]
> * qpunishments.command.kick - /qkick <**playerName**> [-s] [reason]
> * qpunishments.command.ipban - /qipban <**playerName**> [-s] [duration] [server:<**?**>] [reason]
> * qpunishments.command.ipmute - /qipmute <**playerName**> [-s] [duration] [server:<**?**>] [reason]
> * qpunishments.command.unban - /qunban [-s] <**playerName**>
> * qpunishments.command.unban - /qunipban [-s] <**playerName**>
> * qpunishments.command.unban - /qunmute [-s] <**playerName**>
> * qpunishments.command.unban - /qunipmute [-s] <**playerName**>
> * qpunishments.command.lookup - /lookup [-debug] <**playerName**> [module] [limit]
> * qpunishments.command.lookupip - /lookupip [-debug] <**playerName or IP**> [module] [limit]
> * qpunishments.command.comment - /comment <**playerName**> <**text**>
> * qpunishments.admin - /reloadmessages (Reloads all plugin messages without restarting proxy)
> * qpunishments.command.history - /historyadmin <**command**> <**id**> [<**content**>] (History management for less sql tinkering incase of mistakes)
> * qpunishments.command.staffchat - /staffchat <**text**> (Can be replaced by a character, check config) (Private chat for staff)
> * qpunishments.command.find - /find <**playerName**> (Locates the server a player is connected to)

## Disclaimer
This plugin uses BStats for data collection, if you do not want to participate you can disable BStats in the BStats folder at /plugins/
