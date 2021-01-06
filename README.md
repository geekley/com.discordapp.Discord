# Discord

Discord is a free all-in-one messaging, voice and video client that's available on your computer and phone.

This repo hosts the flatpak wrapper for [Discord](https://discord.com/), available at [Flathub](https://flathub.org/apps/details/com.discordapp.Discord).

```sh
flatpak install flathub com.discordapp.Discord
flatpak run com.discordapp.Discord
```


## Differences in flatpak version

The flatpak version runs in a sandbox to provide better safety and privacy for users (see [this privacy report](https://spyware.neocities.org/articles/discord.html)).

However, this sandboxing prevents the following features from working:

- **Game Activity**: This flatpak version of Discord cannot scan running processes to detect running games.  
  There is currently no workaround or solution for this limitation.
- **Unrestricted File Access**: Default sandbox permissions limit Discord to only certain directories, so you can't access your entire Home directory. This limits which file directories you can attach files from and impacts drag and drop functionality. You can change sandbox permissions of installed flatpak applications (for example, with [Flatseal](https://flathub.org/apps/details/com.github.tchx84.Flatseal)) to give Discord broader file system access, allowing file attachments from more locations.
- **Rich Presence**: See [this page](https://github.com/flathub/com.discordapp.Discord/wiki/Rich-Precense-(discord-rpc)) if you want to expose Discord's rich presence interface for other applications.


## Legal

The Discord app itself is **proprietary** (closed source).

This wrapper is not verified by, affiliated with, or supported by Discord Inc.
