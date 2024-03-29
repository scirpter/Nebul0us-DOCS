# Nebul0us

## Table of Contents

- [About](#about)
- [Command List](#command_list)
- [Useful Metas](#useful_metas)

## About <a name = "about" />

Nebul0us is a completely external, networked Nebulous.io cheat made from reverse engineering their UDP networking code.

## Command List <a name = "command_list" />

- `splasmaexploit` - Enables the plasma exploit to get over 300k plasma/hour. `y` for yes, `n` for no, followed by the instance type.
    ###### Example: `splasmaexploit y main` or `splasmaexploit y alt` or `splasmaexploit n main` or `splasmaexploit n alt`
    > **Note**
    > This is a paid feature. You can buy it by messaging the bot developer on Discord.

- `co` - (Re)connects the bots to the server.
    > **Note**
    > You only need to do this after using the `dc`/`d` command.

- `activate` - Activate/change your license key.
    ###### Example: `activate SIG 0x123456789`

- `jo` - Joins the lobby with the specified player ID or world name/password.
    ###### Example: `jo 12409385` or `jo goodapple123`

- `en` - Lets the bots start playing.

- `rj` - Rejoins the lobby.
    > **Note**
    > This only works if the `jo` command was used, otherwise use `dc` -> `co` to disconnect and reconnect instead.

- `dc` - Disconnects the bots from the server.

- `d` - Disconnects a single bot from the server.

- `fe` - Feeds a specified player ID or name.
    ###### Example: `fe 12409385` or `fe goodapple123` or `fe`
    > **Note**
    > If you pass no arguments, the bots will stop feeding. To feed multiple targets at once, just use the && separator, e.g. `fe 12409385 && fe goodapple123`. The player with the lowest mass will be prioritized.

- `sdndmaxmass` - Sets the maximum mass for all bots running on `dnd` by ejecting mass. **Set to 9e8 by default.**
    ###### Example: `sdndmaxmass 100000` or `sdndmaxmass 50000`
    > **Note**
    > All mass will be evenly distributed, which means that if e.g. the max is 50k, bot 1 has 25k and bot 2 has 30k, bot 2 will release 5k mass, bot 1 will release nothing.

- `ex` - Force exits the program.

- `smoddetection` - Sets whether or not the bots should detect moderators. `y` for yes, `n` for no. **Set to `y` by default.**
    ###### Example: `smoddetection y` or `smoddetection n`
    > **Note**
    > This only detects mods via chat and the player list. It does not detect mods that join the lobby invisibly, so this is unreliable.

- `fo` - Follows a player and chills next to them.
    ###### Example: `fo 12409385` or `fo goodapple123` or `fo`
    > **Note**
    > If you pass no arguments, the bots will stop following.

- `savoidalgo` - Sets whether or not the bots should avoid other players. `y` for yes, `n` for no. **Set to `y` by default.**
    ###### Example: `savoidalgo y` or `savoidalgo n`

- `ch` - Sends a chat message with the specified text.
    ###### Example: `ch Bye World.`

- `em` - Sends an emote with the specified index.
    ###### Example: `em 1` or `em 78`

- `rn` - Renames the bots.
    ###### Example: `rn badapple123`
    > **Note**
    > Max 15 characters.

- `semloop` - Sets whether or not the bots will loop emotes. `y` for yes, `n` for no, followed by the index.
    ###### Example: `semloop y 54` or `semloop n 12`
    > **Note**
    > You must still pass the index as an argument even if you set it to `n`. If you set the index to `0`, it will loop random emotes.

- `smassthreshold` - Sets the mass threshold for the bots to start actions like feeding a player. This is especially useful for trick mode, as they already spawn with mass and you can set it to 0. **Set to 250 by default.**
    ###### Example: `smassthreshold 0` or `smassthreshold 750`

- `sautorejoin` - Sets whether or not the bots will automatically reenter after death. `y` for yes, `n` for no. **Set to `y` by default.**
    ###### Example: `sautorejoin y` or `sautorejoin n`

- `slvlmeta` - Sets whether or not the bots will start farming holes. `y` for yes, `n` for no.
    ###### Example: `slvlmeta y` or `slvlmeta n`

- `splasmafarm` - Sets whether or not the bots will start farming plasma. `y` for yes, `n` for no.
    ###### Example: `splasmafarm y` or `splasmafarm n`
    > **Note**
    > If the bot is logged in and farming in a game mode that is not plasma hunt, it will automatically kill itself every 5-10 minutes to ensure that the plasma is saved to the account.

- `clear` - Clears the console.

- `splasmafor` - Remotely farms plasma for a specific player in plasma hunt. This is useful for farming plasma for a friend.
    ###### Example: `splasmafor 12409385` or `splasmafor goodapple123`
    > **Note**
    > You do not need to enable `splasmafarm` and `splasmafor` at the same time.

- `injecttoken` - Inject the token of your last logged in account into the specified bot index. For example, if you only have 1 bot, the index is 0. If you have 2 bots, the first bot has the index 0 and the second one has the index 1, ...
    ###### Example: `injecttoken 0` or `injecttoken 1` or `injecttoken 2`
    > **Warning**
    > This will kick you from the lobby. Also do NOT reconnect or the bot will be kicked. Instead, log out and/or use another account.

    > **Note**
    > To see what index a bot has specifically, look at the numbers at the end of the bot name in the player list, e.g. bot**0**, bot**1**, bot**2**, ...

- `gettoken` - Prints out the token of your last logged in account.
    ###### Example: `gettoken`
    > **Note**
    > You can list this token in your tokens.txt file and the bots will automatically sign in with it if you restart the script.

- `gettokens` - Prints out all saved tokens from your tokens.txt and their index.
    ###### Example: `gettokens`

- `addtoken` - Adds a token to your tokens.txt.
    ###### Example: `addtoken YOUR_TOKEN_HERE`

- `deletetoken` - Removes a token from your tokens.txt by index.
    ###### Example: `deletetoken 0` or `deletetoken 1` or `deletetoken 2`

- `resynctokens` - Resyncs the current tokens you have in your tokens.txt with the bots' tokens to submit changes you made to the tokens.txt without having to restart the software.

- `addproxy` - Adds a proxy to your proxies.txt.
    ###### Example: `addproxy 127.0.0.1:8080:username:password`
    > **Note**
    > Restart the script after adding a proxy to apply the changes.

- `deleteproxy` - Removes a proxy from your proxies.txt by index.
    ###### Example: `deleteproxy 0` or `deleteproxy 1` or `deleteproxy 2`
    > **Note**
    > Restart the script after adding a proxy to apply the changes.

- `getproxies` - Prints out all saved proxies from your proxies.txt and their index.
    ###### Example: `getproxies`

- `packetsearch` - Searches for a packet in the packet log, followed by the raw hex data of the specific packet segment. This only works if the *Trace packets* option is enabled.
    ###### Example: `packetsearch ffabcd` or `packetsearch bb58ac`
    > **Note**
    > You can use this to find specific packet data, such as the token of the current world. Useful for development purposes.

- `netstats` - Prints out the hexadecimal representation of the client connection tokens. Those tokens are necessary to identify a player in the current world. If you wish to only print out the tokens of the bots, use the command followed by the client index.
    ###### Example: `netstats` or `netstats 0` or `netstats 1` or `netstats 2`
    > **Note**
    > To see what index a bot has specifically, look at the numbers at the end of the bot name in the player list, e.g. bot**0**, bot**1**, bot**2**, ...

- `dnd` - Enables "Do Not Disturb" mode, followed by the corner direction. This will let the bot just run into a specific corner of the map and do nothing. Useful for farming XP without disturbance. `tr` for top right, `tl` for top left, `br` for bottom right, `bl` for bottom left. If you use no arguments, it will disable this mode.
    ###### Example: `dnd tr` or `dnd tl` or `dnd br` or `dnd bl` or `dnd`

## Useful Metas <a name = "useful_metas" />

- `Singular Bot Command` - If you have multiple bots, but only want one of them to have a command executed, you can start the command with the index of the bot you want to execute the command on. For example, if you have 2 bots, the first bot has the index 0 and the second one has the index 1, ...
    ###### Example: `0 ch Bye World.` or `1 rn badapple123`
    > **Note**
    > To see what index a bot has specifically, look at the numbers at the end of the bot name in the player list, e.g. bot**0**, bot**1**, bot**2**, ...

- `Trick Mode Hack` - Set the mass threshold to 0 and start splitrunning with another player. You will gain A LOT of trick points, catapulting you to the top global leaderboard.

- `XP Farm` - Set the mass threshold of 1 bot to 0 to not get blocked from gaining XP from holes, activate the LVL meta for the account you want to farm XP with and let the third bot sit around in watch mode (aka. dead) to prevent the holes from getting out of the farming bot's range of view.
    ###### Example procedure: `0 slvlmeta y` -> `1 smassthreshold 0` -> `2 sautorejoin n` -> `0 en` -> `1 en`

### Any suggestions? Feel free to join our [Discord](https://discord.gg/EAUwnjAZDw) and suggest them in one of our public channels.
