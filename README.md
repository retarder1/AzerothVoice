# AzerothVoice

**Proximity Voice für World of Warcraft.** Du hörst andere Spieler, je nachdem, wie nah sie sind. In Dungeons und Raids hörst du alle in der Instanz.

> **Testphase.** Nicht von Blizzard freigegeben, Nutzung auf eigenes Risiko.
> AzerothVoice liest **keinen** Spielspeicher, greift **nicht** ins Spiel ein und drückt **niemals** Tasten. Es liest nur ein paar Bildpunkte aus dem WoW-Fenster, wie eine Bildschirmaufnahme.

## Download

Unter **[Releases](../../releases/latest)** die Datei **`azeroth-voice.exe`** herunterladen. Es gibt nichts zu installieren, einfach starten.

Windows warnt beim ersten Start eventuell („Der Computer wurde durch Windows geschützt“), weil das Programm noch nicht signiert ist. Dann auf **„Weitere Informationen“ → „Trotzdem ausführen“** klicken.

## Loslegen

1. **`azeroth-voice.exe` starten.** Das Programm sucht beim Start selbst nach Updates und installiert bzw. aktualisiert das WoW-Addon automatisch. Wird WoW nicht gefunden: **„WoW-Ordner wählen“**.
2. **Einladung laden:** Die Datei `azeroth-voice-server.ini` bekommst du vom Gastgeber. Leg sie neben die exe oder klick auf **„Einladung laden …“**.
3. **„1. Mumble installieren“**, falls noch nicht vorhanden. Der offizielle Installer wird geladen und seine Signatur geprüft.
4. **„2. Mumble einrichten“** (Mumble muss dafür geschlossen sein). Das schaltet Positional Audio und die Spielanbindung ein.
5. **Namen eintragen → „3. Verbinden“.**
6. WoW im Modus **„Fenster (Vollbild)“** spielen. Im Programm steht unter „Live“, ob alles ankommt.

Im Spiel zeigt **`/av`** den Status des Addons.

## Probleme

| Anzeige | Lösung |
|---|---|
| „Kein Streifen gefunden“ | Addon in der WoW-Addon-Liste aktiv? Ggf. „Veraltete AddOns laden“ anhaken, `/reload` |
| „WoW-Fenster nicht gefunden“ | WoW starten, Modus „Fenster (Vollbild)“ |
| Stimmen kommen von der falschen Seite | Im Programm unter „Erweitert“ → „Links/rechts spiegeln“ |
| Alle sind immer gleich laut | In Mumble muss unter Einstellungen → Plugins „Link“ aktiv sein. Mumble schließen und „2. Mumble einrichten“ wiederholen |
