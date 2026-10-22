# X4 Tether builds

Builds of X4 Tether, a co-op multiplayer mod for X4: Foundations 9.00 (Windows, Steam). The source is not public.

**Download:** [x4tether.zip](https://github.com/h34tsink/x4tether-releases/releases/latest/download/x4tether.zip) from the [latest release](https://github.com/h34tsink/x4tether-releases/releases/latest). It is updated with every change.

1. Unzip it into a folder of its own (not Program Files).
2. Run `X4TetherLauncher.exe` with X4 closed. Click **Install / Update**, then turn Protected UI Mode off.
3. Start X4. In the main menu, choose **Multiplayer (X4 Tether)**. Create a character, then join the host's address.

The launcher checks this page for updates each time it starts.

## What's new

### Features

- **Persistent players.** Each player has a character that the host remembers by key. A returning character gets its faction membership and last ship back.
- **Starter ship choice.** Each character keeps a starter ship choice. A new player starts in a starter ship at the hub. A returning player respawns in the last ship.
- **Multiplayer lobby.** One screen in the game for the character (name, gender, model), hosting, joining and settings. Favorite servers and recent servers are saved.
- **Launcher changes.** Hosting and joining are now done in the game. The launcher installs and updates, sets Protected UI Mode, tests connections, adds the firewall rule, runs the test server and starts X4 (**Start X4**). It updates itself from this page.
- **New world.** Starts a co-op game directly with your character and a starter ship, in a random start sector with Mission 1.
- **F10 menu.** Split into Session, Admin and debug tabs. F10 is the default menu key.
- **Protocol 7.** The host sends the join spawn plan with the save. Hosts and clients must use the same build.

### Fixes

- The `~` key is no longer the menu key (X4 uses it for debug input). The save no longer sets the shared save-restriction bit that stopped the map from opening.
- A ship is recorded only after it is in the host's world, and only when it is uploaded after the save has loaded. A bad last ship loads as no ship.
- If the last ship cannot respawn, the player gets the chosen starter ship at the hub, then a place near the player.
- The host no longer loses saved players or factions that failed to load. It holds joins until the player registry has loaded, and ignores stale answers during a world load.
- A newer identity file is not overwritten, and every `.bad` copy is kept.
- A character's model must match its gender. The default model of the character's gender is used if it does not.
- Networking does not start at the title screen. Title-screen joins download the world.
- A world-load request waits until the world is loaded. Load world loads once on a double click, and New world can be retried.
- The starter ship keeps its software.
- `host.txt` and world-load retry spam are gone from the log.
- Adding a favorite asks for a name. The Host switch no longer saves host mode, and **Don't host** is available.
- The launcher updates itself in its own folder, not the running exe.

X4 Tether runs on [X4Native](https://github.com/eg3r/X4Native) by eg3r (MIT license, included in the zip). X4: Foundations is a game by Egosoft; this mod is unofficial.
