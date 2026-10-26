# Speichern und Mehrspieler

Gespielt wird immer über einen Server – im Einzelspieler läuft er unsichtbar im selben Programm. Er speichert alle 30 Sekunden und beim Beenden (Fenster schließen oder Strg+C im Terminal).

- **Einzelspieler** zeigt alle Welten: zuletzt gespielte oben, mit "vor 5 Minuten" bzw. "gestern" und Spielmodus; Mausrad, Leiste oder Pfeiltasten zum Blättern, oben ein Suchfeld. Anklicken wählt aus, **Doppelklick** oder Enter spielt. Darunter: Spielen, Neue Welt erstellen (eigene Seite mit Name, Seed, Welttyp, Spielmodus, Schwierigkeit, Regel beim Tod, PvP), **Umbenennen**, **Löschen** (mit Rückfrage; die Welt kommt in den Ordner `welten-geloescht` daneben – wer sich vertan hat, schiebt sie von dort zurück nach `welten`).
- Spielstände liegen unter `~/.local/share/voxel-planeten/welten/<Name>` (Windows: `%APPDATA%\voxel-planeten\welten\<Name>`).
- Gespeichert wird nur, was Spieler verändert haben, dazu Positionen und Spielzeit. Das Gelände selbst entsteht aus dem Seed jedes Mal wieder genau gleich.
- **Welttyp** (beim Erstellen wählbar, bleibt der Welt für immer):
  - **Realistisch** (Standard im Menü): Kontinente mit klaren Küsten (Strand, flacher Schelf, dann Tiefsee) statt eines Gewirrs aus Seen und Inseln, etwa halb Land, halb Meer; Gebirgsketten mit verschneiten Gipfeln, Hochländer; **Flüsse wie in echt**: Sie entspringen dort, wo genug Regen zusammenkommt (auch im Gebirge), fließen immer bergab zum Meer, kleine münden in größere (danach so breit wie beide), Wüsten haben wenige, feuchte Gegenden viele; große Ströme werden mehrere hundert Meter breit und schlängeln sich in Mäandern. Sie liegen in eigenen Tälern mit Flussebene, im Gebirge in engen Tälern; ihr Wasser steht auf der Höhe des Landes (nicht auf Meereshöhe) und fällt flussabwärts in kleinen Stufen, an denen es ein Stück weit überfließt wie eine Stromschnelle, im Kalten ist es oben gefroren. Das Bett ist aus Sand und Kies. Unterwasserhöhlen an den Küsten. Auch **Monde und Gesteinsplaneten** haben hier ihr echtes Gelände, an der echten Stelle und in echter Größe: Krater in allen Größen (der Mond, Merkur, Kallisto und Rhea übersät, Venus, Io und Europa fast ohne), die dunklen Mare des Mondes mit Tycho, Copernicus und dem Südpol-Aitken-Becken; auf dem Mars Olympus Mons, die Tharsis-Vulkane, Valles Marineris, Hellas, Argyre und das nördliche Tiefland; Caloris auf Merkur, Ishtar Terra, Maxwell Montes und Maat Mons auf der Venus; auf Io dunkle Vulkansenken und der rote Ring um Pele; Europas Risse; Ganymeds Rillen und dunkle Regionen; Valhallas Ringe auf Kallisto; Herschel auf Mimas; die Tigerstreifen von Enceladus; Titans Dünen und Seen; Iapetus mit dunkler Vorderseite und Äquatorgrat; Plutos Herz aus Stickstoffeis mit Eisbergen; Charons rote Polkappe; Occator und Ahuna Mons auf Ceres. Alles in **echter Höhe**: Olympus Mons ist 21 km hoch, der Everest knapp 9 km, das Meer im Schnitt 3,7 km tief, Krater so tief wie in echt (Tycho fast 5 km) – siehe die Tabelle "Höhen, Bauhöhe und Grabtiefe" bei den Himmelskörpern. Auf der Erde wird es nach oben hin kälter: Wald, darüber Tundra, ab etwa 3 km Schnee (in den Tropen erst ab 6 km).
  - **Klassisch**: die erste Fassung (viel Meer, Inseln und Seen; Monde und Planeten mit sanften Hügeln). Welten von vor dem Welttyp sind klassisch.
  - **Realistisch (flach)**: So waren realistische Welten bis Oktober 2026 – alle Höhen gestaucht auf −112 bis 360 m. Nicht mehr wählbar; solche Welten bleiben, wie sie sind.
- Beim nächsten Start ist man wieder dort, wo man aufgehört hat.

**Mit Freunden spielen** (im selben Netzwerk, also am selben Router/WLAN):

1. Gastgeber: eigene Welt starten, im Spiel **Esc → "Für andere öffnen"**. Das Pause-Menü zeigt danach die Adresse(n), unter denen die Welt erreichbar ist. (Oder gleich im Hauptmenü: Mehrspieler → "Eigene Welt öffnen".)
2. Mitspieler: Hauptmenü → **Mehrspieler**. Offene Spiele im Netzwerk erscheinen nach 1–2 Sekunden in der Liste – anklicken. Taucht nichts auf: die Adresse aus dem Pause-Menü des Gastgebers eintippen → "Beitreten".

Jeder Name kann nur einmal gleichzeitig spielen (Name im Mehrspieler-Menü).

**Klappt es nicht?**

| Meldung / Problem                                                | Ursache und Abhilfe                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Windows: "Die Firewall hat einige Features dieser App blockiert" | Kommt nur beim Gastgeber, wenn er seine Welt öffnet (bzw. beim Server): Das Spiel will Verbindungen von Mitspielern annehmen. "Zulassen" klicken. Fremder Code läuft dabei nicht – übers Netz kommen nur Spieldaten (Blöcke, Positionen, Chat). Mitspieler fragt Windows nicht (die Spielsuche lauscht auf keinem Port).                                                                                                                                          |
| "Verbindung abgelehnt"                                           | Der Gastgeber hat seine Welt nicht geöffnet (Esc → "Für andere öffnen") oder die Adresse gehört zu einem anderen Rechner.                                                                                                                                                                                                                                                                                                                                         |
| "Keine Antwort" / Zeitüberschreitung                             | Meist die Firewall beim Gastgeber. Windows: beim ersten Öffnen "Zugriff zulassen" klicken. Wurde das abgelehnt: Windows-Sicherheit → Firewall- und Netzwerkschutz → "Zugriff von App durch Firewall zulassen" → ExoGrid Industry bei "Privat" anhaken. Das Netzwerk sollte in Windows als "Privat" eingestellt sein, nicht "Öffentlich". Linux mit Firewall: TCP 25600 und UDP 25601 freigeben (z. B. `sudo ufw allow 25600/tcp` und `sudo ufw allow 25601/udp`). |
| Spiel fehlt in der Liste, Adresse eintippen klappt               | Der Router leitet die Suche (UDP-Broadcast) nicht weiter – kein Problem.                                                                                                                                                                                                                                                                                                                                                                                          |
| Gar nichts geht                                                  | Gäste-WLAN oder "AP-Isolation" am Router trennt die Geräte voneinander.                                                                                                                                                                                                                                                                                                                                                                                           |
| "andere Spielversion"                                            | Beide brauchen denselben Stand des Spiels.                                                                                                                                                                                                                                                                                                                                                                                                                        |

Ports: TCP 25600 (Spiel), UDP 25601 (Spielsuche). Übers Internet: Am Router TCP 25600 zum Gastgeber weiterleiten oder ein virtuelles Netz wie ZeroTier oder Tailscale benutzen (dann funktioniert auch die Spielsuche).

**Dedizierter Server** (ohne Fenster, z. B. auf einem zweiten Rechner):

```bash
./ExoGrid-Industry-Server --world server-welt --port 25600 [--seed 42]
# neue Welt mit Schwierigkeit und Regel beim Tod (alles, kiste, werkzeuge, nichts):
./ExoGrid-Industry-Server --world harte-welt --schwierigkeit schwer --beim-tod kiste
# Welttyp einer neuen Welt (Standard: realistisch):
./ExoGrid-Industry-Server --world alte-art --welttyp klassisch
```

In der Server-Konsole gehen alle Chat-Befehle (ohne `/`, die Konsole darf alles), dazu `stop` (speichern und beenden); Strg+C speichert auch. Zum Beispiel: `liste`, `speichern`, `zeit 100` (Zeitraffer ×100; `zeit 0` hält an, `zeit 0,5` halb so schnell), `zeit jetzt` (echte Zeit), `zeit vor 24` (Stunden), `setzerang Kim moderator`, `kick Max Spam`, `ban Max`. Wie früher geht auch `admin Kim`, `admin weg Kim` und `admins`; eine alte `admins.txt` wird übernommen. Mitspieler finden den Server im Mehrspieler-Menü (`--name` legt fest, wie er dort heißt).

## Server-Verwalter mit Dashboard im Browser

Das Dashboard bleibt erreichbar, auch wenn der Server gerade aus ist.

- **Status**: läuft/aus, Welt, Spielzeit, Spieler online, Abstürze; Starten, Stoppen, Neustarten.
- **Konsole**: die Ausgabe des Servers live, Befehle eingeben wie in der Konsole.
- **Spieler**: wer online ist und auf welchem Himmelskörper (Erde, Mars, Mond …) mit Breite, Länge und Höhe, Verwarnungen je Spieler (vom Spiel automatisch oder von Moderatoren), Sperren und Ränge.
- **Karte**: die Geländekarte eines Himmelskörpers (Norden oben, Raster 30°) mit allen Spielern darauf. Oben je ein Knopf für jeden Körper mit Spielern, daneben eine Liste mit allen anderen; „◎ Körper“ in der Spielertabelle springt zur Karte dieses Spielers. Die Karte rechnet der Server beim ersten Aufruf aus (ein paar Sekunden), danach bleibt sie bis zum nächsten Serverstart.
- **Welten**: alle Welten, neue anlegen, wechseln, löschen (gelöschte Welten landen im Ordner `welten-papierkorb`).
- **Sicherungen**: von Hand oder automatisch (Standard: alle 60 Minuten, die letzten 10 automatischen bleiben), zurückspielen.
- **Einstellungen**: Servername, Spiel-Port, Autostart, Neustart nach Absturz, Sicherungen, Dashboard-Zugriff und Passwort.

Wer den Server aufmacht, entscheidet, wer das Dashboard sieht. Beim ersten Start im Terminal fragt der Verwalter danach und man **muss ein Passwort vergeben** (mindestens 6 Zeichen, die Eingabe bleibt unsichtbar, zweimal eintippen):

```
  Wer soll das Dashboard öffnen dürfen?
    1) lokal       – nur dieser Rechner
    2) LAN         – alle Rechner im Heimnetz
    3) öffentlich  – übers Internet (Port 25610 am Router freigeben)
  Auswahl [1–3, Enter = 1]:
```

| Zugriff      | Wer kommt drauf              | Passwort                    |
| ------------ | ---------------------------- | --------------------------- |
| `lokal`      | nur dieser Rechner           | nötig                       |
| `lan`        | alle im Heimnetz             | nötig                       |
| `öffentlich` | alle, die den Port erreichen | nötig, dazu HTTPS empfohlen |

Bei „öffentlich“ fragt er noch, ob HTTPS an sein soll (Standard: ja; ohne eigenes Zertifikat erzeugt der Verwalter eines selbst, der Browser warnt dann einmal – „Erweitert → trotzdem öffnen“). Die Adresse beginnt dann mit `https://`; wer `http://` eintippt, wird umgeleitet. Die Felder „Zertifikat“ und „Schlüssel“ in den Einstellungen sind **Dateipfade** zu einer eigenen PEM-Datei (z. B. von Let's Encrypt) – leer lassen fürs selbst unterschriebene, dort gehört kein Passwort hinein. Passt der Pfad nicht, nimmt der Verwalter mit einer Warnung das selbst unterschriebene. HTTPS an/aus wirkt erst nach einem Neustart des Verwalters. Später ändern: `ExoGrid-Industry-Verwalter --einrichten` oder im Dashboard unter Einstellungen. Ohne Terminal (z. B. als Dienst) wird nichts gefragt; dann gibt man es auf der Befehlszeile an:

```bash
ExoGrid-Industry-Verwalter --zugriff lan --passwort geheim123
ExoGrid-Industry-Verwalter --zugriff öffentlich --passwort geheim123 --https
```

Diese Angaben merkt sich der Verwalter in `verwalter.json` (auch `--web-port`, `--kein-https`); nur für diesen Start gelten `--einrichten`, `--ordner` (Datenordner), `--server` (anderes Server-Programm) und `--kein-browser`. Ohne Passwort ist das Dashboard nur auf dem eigenen Rechner erreichbar. `--help` zeigt alles. Daten liegen unter `~/.local/share/voxel-planeten/server-verwalter` (Windows: `%APPDATA%\voxel-planeten\server-verwalter`) mit `welten/` und `sicherungen/`. Strg+C speichert die Welt, stoppt den Server und beendet den Verwalter (zweimal Strg+C: sofort). Ports: TCP 25610 fürs Dashboard, dazu wie oben TCP 25600 fürs Spiel.

Was übers Netz geht: Jeder Client erzeugt das Gelände selbst aus dem Seed. Der Server schickt nur veränderte Chunks (pro Region von 512 × 512 m, sobald man in die Nähe kommt), Blockänderungen, die Spielzeit und 20-mal pro Sekunde die Positionen der anderen. Die Bewegung rechnet jeder Client selbst; Blockänderungen prüft der Server (Reichweite, Grundgestein, Platz frei).
