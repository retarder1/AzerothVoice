<p align="center"><img src="assets/azerothvoice-512.png" width="160" alt="AzerothVoice"></p>

# AzerothVoice

**Proximity Voice für World of Warcraft.** Du hörst andere Spieler, je nachdem, wie nah sie sind. In Dungeons und Raids hörst du alle in der Instanz.

🇬🇧 [English guide](README.md)

> **Testphase.** Nicht von Blizzard freigegeben, Nutzung auf eigenes Risiko.
> AzerothVoice liest **keinen** Spielspeicher, greift **nicht** ins Spiel ein und drückt **niemals** Tasten. Es liest nur ein paar Bildpunkte aus dem WoW-Fenster, wie eine Bildschirmaufnahme. Das Addon nutzt nur offizielle Addon-Funktionen.

## Download

Unter **[Releases](../../releases/latest)** die Datei **`azeroth-voice.exe`** herunterladen. Es gibt nichts zu installieren, einfach starten.

Windows warnt beim ersten Start eventuell („Der Computer wurde durch Windows geschützt“), weil das Programm noch nicht signiert ist. Dann auf **„Weitere Informationen“ → „Trotzdem ausführen“** klicken.

## Loslegen

1. **`azeroth-voice.exe` starten.** Das Programm sucht beim Start selbst nach Updates und installiert bzw. aktualisiert das WoW-Addon automatisch. Wird WoW nicht gefunden: **„WoW-Ordner wählen“**.
2. **Einladung laden:** Die Datei `azeroth-voice-server.ini` bekommst du vom Gastgeber. Leg sie neben die exe oder klick auf **„Einladung laden …“**.
3. **Mumble wird automatisch eingerichtet.** Das Programm lädt den offiziellen Mumble-Installer, prüft die Signatur und entpackt daraus eine **eigene Kopie** (keine Installation, keine Windows-Abfrage). Aus dieser Kopie werden **alle Spiel-Plugins gelöscht** (auch Mumbles eigenes WoW-Plugin, das den Spielspeicher liest) und das **Overlay**. Dazu kommt nur das AzerothVoice-Plugin. Ein normal installiertes Mumble wird nicht benutzt und muss während des Spielens geschlossen sein.
4. Sonst gibt es nichts zu klicken: Positional Audio, Push-to-Talk und das Server-Zertifikat werden automatisch eingerichtet, Mumble-Updates sind aus.
5. **In WoW einloggen.** Sobald ein Charakter im Spiel ist, verbindet AzerothVoice automatisch mit dessen Namen. Charakter wechseln: verbindet neu mit dem neuen Namen. Ausloggen: trennt.
6. WoW im Modus **„Fenster (Vollbild)“** spielen. Im Programm steht unter „Live“, ob alles ankommt.
7. **Sprechtaste** in WoW belegen: Optionen → Tastaturbelegung → AddOns → AzerothVoice → „Sprechen (Push-to-Talk)“. Gesendet wird nur, solange du sie hältst und WoW im Vordergrund ist.

Mumble läuft unsichtbar im Infobereich, sein Fenster brauchst du nie.

## Im Spiel

- Eine **Sprechblase** zeigt, wer spricht: an der Namensplakette in der offenen Welt, an den Gruppen- und Schlachtzugsrahmen in Dungeons und Raids.
- Die Liste **„Spricht gerade“** zeigt alle, die gerade sprechen. `/av unlock` macht sie verschiebbar, `/av lock` fixiert sie, `/av list` schaltet sie ein oder aus.
- **Stummschalten:** Rechtsklick auf den Spieler → **„AzerothVoice: Stummschalten“** oder `/av mute Name`. Wirkt sofort. `/av unmute Name` hebt es auf.
- **`/av`** zeigt den Status des Addons.

## Mikrofon & Ton

**Im Spiel:** Optionen → AddOns → **AzerothVoice** oder `/av options`:

- **Mikrofon-Lautstärke**, **Gesamtlautstärke** und **Rauschunterdrückung** (RNNoise empfohlen).
- **Musikschutz:** wer länger als die eingestellte Zeit (Standard 30 s) am Stück sendet, wird leiser.
- **Mikrofon testen:** nimmt 3 Sekunden auf und spielt sie dir vor.
- Auch als Befehle: `/av mic 120`, `/av vol 80`, `/av music 30` oder `/av music off`, `/av noise rnn`, `/av test`.

Nur **Mikrofon und Wiedergabegerät** wählst du im AzerothVoice-Fenster (Standard: das Windows-Standardgerät). Dort gibt es auch eine Pegelanzeige.

## Sicherheit

AzerothVoice nutzt eine eigene, bereinigte Mumble-Kopie mit genau einem Plugin, dem eigenen. Ein **Wächter** prüft alle 2 Sekunden, dass:
- keine Datei der Kopie hinzugekommen oder verändert ist,
- Mumble kein anderes Plugin geladen hat,
- das AzerothVoice-Plugin in Mumble antwortet (Handshake).

Stimmt etwas nicht, wird Sprechen gesperrt und Mumble beendet. Der Zustand steht unter **Live → Wächter**.

## Probleme

| Anzeige | Lösung |
|---|---|
| „Kein Streifen gefunden“ | Addon in der WoW-Addon-Liste aktiv? Ggf. „Veraltete AddOns laden“ anhaken, `/reload` |
| „WoW-Fenster nicht gefunden“ | WoW starten, Modus „Fenster (Vollbild)“ |
| Stimmen kommen von der falschen Seite | Im Programm unter „Erweitert“ → „Links/rechts spiegeln“ |
| Alle sind immer gleich laut | Mumble schließen und „2. Mumble einrichten“ wiederholen |
| „Ein anderes Mumble läuft“ | Normales Mumble schließen (auch unten rechts im Infobereich), dann AzerothVoice neu starten |
| Wächter: „Plugin antwortet nicht“ | In AzerothVoice „Neu verbinden“ klicken |
| Kein Pegel / Mikrofontest stumm | Ist Mumble verbunden? Richtiges Mikrofon gewählt? |
