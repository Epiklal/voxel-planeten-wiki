# Speichern und Mehrspieler

Gespielt wird immer über einen Server – im Einzelspieler läuft er unsichtbar im
selben Programm. Er speichert alle 30 Sekunden und beim Beenden (Fenster
schließen oder Strg+C im Terminal).

- **Einzelspieler** zeigt alle Welten wie in Minecraft: zuletzt gespielte oben, mit
  "vor 5 Minuten" bzw. "gestern" und Spielmodus; Mausrad, Leiste oder Pfeiltasten
  zum Blättern, oben ein Suchfeld. Anklicken wählt aus, **Doppelklick** oder Enter
  spielt. Darunter: Spielen, Neue Welt erstellen (eigene Seite mit Name, Seed,
  Welttyp, Spielmodus, Schwierigkeit, Regel beim Tod, PvP), **Umbenennen**, **Löschen** (mit
  Rückfrage; die Welt kommt in den Ordner `welten-geloescht` daneben – wer sich
  vertan hat, schiebt sie von dort zurück nach `welten`).
- Spielstände liegen unter `~/.local/share/voxel-planeten/welten/<Name>`
  (Windows: `%APPDATA%\voxel-planeten\welten\<Name>`).
- Gespeichert wird nur, was Spieler verändert haben, dazu Positionen und Spielzeit.
  Das Gelände selbst entsteht aus dem Seed jedes Mal wieder genau gleich.
- Eine neue Welt bekommt einen zufälligen Seed (`--seed 42` für einen bestimmten).
- **Welttyp** (wie in Minecraft beim Erstellen wählbar, bleibt der Welt für immer):
  - **Realistisch** (Standard im Menü): Kontinente mit klaren Küsten (Strand,
    flacher Schelf, dann Tiefsee) statt eines Gewirrs aus Seen und Inseln, etwa
    halb Land, halb Meer; Gebirgsketten mit verschneiten Gipfeln, Hochländer;
    Flüsse, die zum Meer hin breiter werden und im Hügelland entspringen;
    Unterwasserhöhlen an den Küsten.
  - **Klassisch**: die erste Fassung (viel Meer, Inseln und Seen). Welten von vor
    dem Welttyp sind klassisch.
  - Monde und andere Planeten sehen bei beiden gleich aus.
  - Die Erde von oben als Bild: `cargo run --release -p voxel_common --example
    weltkarte -- realistisch 1337 karten/` (ganze Erde, Höhenkarte und
    Ausschnitte von 2000 km bis 2 km).
- Beim nächsten Start ist man wieder dort, wo man aufgehört hat. Mit `--planet`
  startet man stattdessen neu auf diesem Himmelskörper.

**Mit Freunden spielen** (im selben Netzwerk, also am selben Router/WLAN):

1. Gastgeber: eigene Welt starten, im Spiel **Esc → "Für andere öffnen"**. Das
   Pause-Menü zeigt danach die Adresse(n), unter denen die Welt erreichbar ist.
   (Oder gleich im Hauptmenü: Mehrspieler → "Eigene Welt öffnen".)
2. Mitspieler: Hauptmenü → **Mehrspieler**. Offene Spiele im Netzwerk erscheinen
   nach 1–2 Sekunden in der Liste – anklicken. Taucht nichts auf: die Adresse
   aus dem Pause-Menü des Gastgebers eintippen → "Beitreten".

Jeder Name kann nur einmal gleichzeitig spielen (Name im Mehrspieler-Menü).
Ohne Menü geht es auch: `--host` öffnet die eigene Welt, `--connect 192.168.1.20
--name Kim` tritt bei.

**Minecraft-Spieler** (Java Edition **1.20.1**) können mitspielen – mit ganz
normalem Minecraft, ohne Mod: Sobald eine Welt fürs Netzwerk offen ist (Esc → "Für
andere öffnen" oder der eigene Server), wartet sie auch auf dem Minecraft-Port
**25565**. In Minecraft: Mehrspieler → Server hinzufügen → die Adresse aus dem
Pause-Menü (ohne Port) → beitreten. In der Serverliste steht "Voxel-Planeten: …".

- Für unseren Server ist ein Minecraft-Spieler ein Spieler wie alle: dieselben
  Regeln (Überleben, Abbauen mit dem richtigen Werkzeug, Inventar, Lebenspunkte,
  Tod und Wiederbeleben, Befehle wie /wegpunkt, Ränge), alle sehen sich gegenseitig
  als Figuren, der Chat geht in beide Richtungen, die Tageszeit ist die des Planeten.
- Die Welt: Eine Würfelseite des Himmelskörpers ist für ihn eine flache
  Minecraft-Welt (x, z = Lage auf der Seite, y = Höhe von −128 bis 384); an ihrem
  Rand ist die Weltgrenze. `/tp` bringt ihn auch auf andere Seiten und Himmelskörper.
- Unsere Blöcke sieht er als ähnliche Minecraft-Blöcke (Regolith als hellgrauer
  Trockenbeton, Bauwerke als Eisenblöcke …), unsere Gegenstände als ähnliche
  Minecraft-Gegenstände mit **unserem Namen** (z. B. Papier namens "Graphen").
- Angemeldet wird ohne Mojang-Konto (wie ein Minecraft-Server im "offline-mode"):
  Jeder Name geht einmal gleichzeitig. Darum nur im eigenen Netzwerk öffnen.
- **Herstellen**: `/herstellen` (von Hand) oder Rechtsklick auf eine Werkbank öffnet
  ein Fenster mit den Rezepten (grün: geht, darunter die Zutaten und wie viele man
  hat; Klick stellt her, Shift-Klick 5×; Blättern und "nur herstellbare" unten).
- **Bauwerke**: mit dem Gegenstand in der Hand per Rechtsklick aufstellen (Ausrichtung
  wie bei uns), Linksklick baut sie als Ganzes ab. Rechtsklick öffnet Ofen, Kiste,
  Kraftwerk, Maschinen: oben die beschrifteten Plätze, darunter Strom, Fortschritt,
  Brennstoff, Fördermenge und das Rezept (Klick: anderes wählen), bei einer
  rausgeflogenen Sicherung der Knopf zum Zurücksetzen. Geduckt wird gebaut statt geöffnet.
- **Unsere Bilder**: Beim Beitreten bietet der Server ein Ressourcenpaket an
  (annehmen empfohlen). Damit sehen unsere Blöcke in Minecraft aus wie bei uns
  (Regolith wie Regolith, Erze, Steine, Glas …) und alle Gegenstände haben ihr eigenes
  Bildchen. Das Paket gilt nur auf unserem Server. Es liegt in
  `ressourcen/minecraft/voxel-planeten.zip` und kommt über Port **25566**; wer
  Texturen im Ressourcen-Ordner ändert, baut es neu mit
  `voxel_client --minecraft-paket` (bzw. `Voxel-Planeten.exe --minecraft-paket`).
- **Ohne Mod** zeigt Minecraft auch: Luft als Luftblasen (im Weltall, über 8 km,
  unter Wasser), Strahlung und das Laden der Tech-Rüstung in der Leiste über der
  Schnellleiste, eigene Entdeckungen groß in der Mitte und mit allen Eigenschaften
  im Chat, was andere entdecken, im Chat.
- **Mit unserer Fabric-Mod** (Extra, für noch mehr): oben links, auf welchem
  Himmelskörper und welcher Würfelseite man ist, Strahlung (Sv/h und Dosis, grün bis
  rot) und Laden der Rüstung; Entdeckungen als Tafel mit Eigenschaften und Erklärung
  (mit Ton), auch die der anderen; alle eigenen und geteilten **Wegpunkte im Bild**
  als Raute mit Name und Entfernung (außerhalb des Bildes am Rand, in ihrer Richtung).
  So kommt sie ins Spiel: [Fabric Loader](https://fabricmc.net/use/) für 1.20.1
  installieren (Fabric API braucht es nicht) und `voxel-planeten-mod.jar` in den
  Ordner `mods` legen. Der Server bietet sie an: Wer ohne Mod beitritt, bekommt nach
  ein paar Sekunden im Chat einen Link zum Anklicken
  (`http://<Server>:25566/voxel-planeten-mod.jar`); sie liegt auch in
  `ressourcen/minecraft/`. Auf anderen Servern tut die Mod nichts.
  Quelltext im Ordner `minecraft-mod/`, neu bauen mit
  `./werkzeuge/minecraft-mod-bauen.sh` (braucht Java 17 oder neuer).

Die Zuordnung der Blöcke und die Minecraft-Daten erzeugt `werkzeuge/minecraft_daten.py`
aus Minecrafts eigenem Datengenerator (Anleitung oben in der Datei).

**Klappt es nicht?**

| Meldung / Problem                                  | Ursache und Abhilfe                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Verbindung abgelehnt"                             | Der Gastgeber hat seine Welt nicht geöffnet (Esc → "Für andere öffnen") oder die Adresse gehört zu einem anderen Rechner.                                                                                                                                                                                                                                                                                                                                       |
| "Keine Antwort" / Zeitüberschreitung               | Meist die Firewall beim Gastgeber. Windows: beim ersten Öffnen "Zugriff zulassen" klicken. Wurde das abgelehnt: Windows-Sicherheit → Firewall- und Netzwerkschutz → "Zugriff von App durch Firewall zulassen" → Voxel-Planeten bei "Privat" anhaken. Das Netzwerk sollte in Windows als "Privat" eingestellt sein, nicht "Öffentlich". Linux mit Firewall: TCP 25600 und UDP 25601 freigeben (z. B. `sudo ufw allow 25600/tcp` und `sudo ufw allow 25601/udp`). |
| Spiel fehlt in der Liste, Adresse eintippen klappt | Der Router leitet die Suche (UDP-Broadcast) nicht weiter – kein Problem.                                                                                                                                                                                                                                                                                                                                                                                        |
| Gar nichts geht                                    | Gäste-WLAN oder "AP-Isolation" am Router trennt die Geräte voneinander.                                                                                                                                                                                                                                                                                                                                                                                         |
| "andere Spielversion"                              | Beide brauchen denselben Stand des Spiels.                                                                                                                                                                                                                                                                                                                                                                                                                      |

Ports: TCP 25600 (Spiel), UDP 25601 (Spielsuche). Übers Internet: Am Router TCP
25600 zum Gastgeber weiterleiten oder ein virtuelles Netz wie ZeroTier oder
Tailscale benutzen (dann funktioniert auch die Spielsuche).

**Dedizierter Server** (ohne Fenster, z. B. auf einem zweiten Rechner):

```bash
cargo run --release -p voxel_server -- --world server-welt --port 25600 [--seed 42]
# neue Welt mit Schwierigkeit und Regel beim Tod (alles, kiste, werkzeuge, nichts):
cargo run --release -p voxel_server -- --world harte-welt --schwierigkeit schwer --beim-tod kiste
# Welttyp einer neuen Welt (Standard: realistisch):
cargo run --release -p voxel_server -- --world alte-art --welttyp klassisch
```

In der Server-Konsole gehen alle Chat-Befehle (ohne `/`, die Konsole darf alles),
dazu `stop` (speichern und beenden); Strg+C speichert auch. Zum Beispiel: `liste`,
`speichern`, `zeit 100` (Zeitraffer ×100; `zeit 0` hält an, `zeit 0,5` halb so
schnell), `zeit jetzt` (echte Zeit), `zeit vor 24` (Stunden), `setzerang Kim
moderator`, `kick Max Spam`, `ban Max`. Wie früher geht auch `admin Kim`,
`admin weg Kim` und `admins`; eine alte `admins.txt` wird übernommen.
Mitspieler finden den Server im Mehrspieler-Menü (`--name` legt fest, wie er dort heißt).

Was übers Netz geht: Jeder Client erzeugt das Gelände selbst aus dem Seed. Der
Server schickt nur veränderte Chunks (pro Region von 512 × 512 m, sobald man in
die Nähe kommt), Blockänderungen, die Spielzeit und 20-mal pro Sekunde die
Positionen der anderen. Die Bewegung rechnet jeder Client selbst;
Blockänderungen prüft der Server (Reichweite, Grundgestein, Platz frei).
