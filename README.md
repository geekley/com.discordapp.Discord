# Discord

Discord is a free all-in-one messaging, voice and video client that's available on your computer and phone.

This repo hosts the flatpak wrapper for [Discord](https://discord.com/), available at [Flathub](https://flathub.org/apps/details/com.discordapp.Discord).

```sh
flatpak install flathub com.discordapp.Discord
flatpak run com.discordapp.Discord
```


## Differences in flatpak version

The flatpak version runs in a sandbox to provide better safety and privacy for users.

However, this sandboxing prevents the following features from working:

- **Game Activity**: This flatpak version of Discord cannot scan running processes to detect running games.  
  There is currently no workaround or solution for this limitation.
- **Drag and Drop Files**: To work around this now, you can change sandbox permissions of installed flatpak applications to give Discord file system access:

```sh
flatpak override --user --filesystem=home:ro com.discordapp.Discord```
- **Rich Presence**: See [this page](https://github.com/flathub/com.discordapp.Discord/wiki/Rich-Precense-(discord-rpc)) if you want to expose Discord's rich presence interface for other applications.


## Legal

The Discord app itself is **proprietary** (closed source).

This wrapper is not verified by, affiliated with, or supported by Discord Inc.
