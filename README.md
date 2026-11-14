<p align="center"><img src="assets/azerothvoice.png" width="128" alt="AzerothVoice"></p>

# AzerothVoice

**Proximity voice chat for World of Warcraft.** You hear other players depending on how close they are. In dungeons and raids you hear everyone in the instance.

🇩🇪 [Deutsche Anleitung](README.de.md)

> **Test phase.** Not approved by Blizzard, use at your own risk.
> AzerothVoice does **not** read game memory, does **not** interfere with the game and **never** presses keys. It only reads a few pixels from the WoW window, like a screen recording. The addon only uses official addon functions.

## Download

Download **`azeroth-voice.exe`** from **[Releases](../../releases/latest)**. There is nothing to install, just run it.

Windows may warn you on the first start ("Windows protected your PC") because the program is not signed yet. Click **"More info" → "Run anyway"**.

## Getting started

1. **Run `azeroth-voice.exe`.** The program checks for updates by itself and installs or updates the WoW addon automatically. If WoW is not found: **"Choose WoW folder …"**.
2. **Load the invitation:** you get the file `azeroth-voice-server.ini` from the host. Put it next to the exe or click **"Load invitation …"**.
3. **"1. Install Mumble".** The program downloads the official Mumble installer, checks its signature and unpacks a **private copy** (no installation, no Windows prompt). **All game plugins are deleted** from this copy (including Mumble's own WoW plugin, which reads game memory), and so is the **overlay**. Only the AzerothVoice plugin is added. A normally installed Mumble is not used and must be closed while you play.
4. **"2. Set up Mumble".** Turns on positional audio and push-to-talk and turns off Mumble updates.
5. **"3. Connect".** Your character name is used as your name.
6. Play WoW in **"Windowed (Fullscreen)"** mode. The **Live** section of the program shows whether everything arrives.
7. **Bind the talk key** in WoW: Options → Keybindings → AddOns → AzerothVoice → "Talk (push-to-talk)". You only transmit while you hold it and WoW is in the foreground.

You don't need the Mumble window at all: everything is set in AzerothVoice.

## In the game

- A **speech bubble** shows who is talking: on nameplates in the open world, on party and raid frames in dungeons and raids.
- The **"Talking now"** list shows everyone who is talking. `/av unlock` lets you move it, `/av lock` fixes it, `/av list` turns it on or off.
- **Mute** someone: right-click the player → **"AzerothVoice: Mute"** or `/av mute Name`. It takes effect immediately. `/av unmute Name` undoes it.
- **`/av`** shows the addon status.

## Microphone & sound

All in the AzerothVoice window, section **"Microphone & sound"**:

- **Microphone** and **playback** device, **noise suppression** (RNNoise recommended). "Apply" restarts Mumble and reconnects.
- **Level** meter, **microphone volume** and **overall volume** (take effect immediately).
- **Test microphone:** records 3 seconds and plays them back to you (needs a connected Mumble).
- **Music protection:** anyone who transmits non-stop for longer than the set time (default 30 s) is turned down.

## Safety

AzerothVoice uses its own cleaned Mumble copy with exactly one plugin, its own. A **guard** checks every 2 seconds that:
- no file of the copy was added or changed,
- Mumble has loaded no other plugin,
- the AzerothVoice plugin in Mumble answers (handshake).

If something is wrong, talking is blocked and Mumble is closed. The status is shown under **Live → Guard**.

## Troubleshooting

| Message | Fix |
|---|---|
| "No strip found" | Is the addon enabled in the WoW addon list? Tick "Load out of date AddOns" if needed, `/reload` |
| "WoW window not found" | Start WoW, mode "Windowed (Fullscreen)" |
| Voices come from the wrong side | In the program under "Advanced" → "Mirror left/right" |
| Everyone is always equally loud | Close Mumble and repeat "2. Set up Mumble" |
| "Another Mumble is running" | Close the regular Mumble (also in the system tray at the bottom right), then "3. Connect" |
| Guard: "plugin does not answer" | Restart Mumble with "3. Connect" |
| No level / microphone test silent | Is Mumble connected? Right microphone selected? |
