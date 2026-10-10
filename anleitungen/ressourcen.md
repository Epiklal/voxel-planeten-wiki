# Eigene Texturen, Geräusche und Musik

Alle Texturen, Geräusche und Lieder liegen im Ordner **`ressourcen/`** im
Projektordner (gehört zum Quellcode, wird mit committet). Die Windows-ZIP hat ihn
neben `Voxel-Planeten.exe`. Das Spiel sucht ihn erst neben sich selbst, dann im
Quellcode-Ordner, zuletzt im Spielstand-Ordner (Einstellungen → Credits →
"Ressourcen-Ordner öffnen" zeigt, welcher gilt). Fehlende Dateien legt das Spiel
beim Start an; `LIESMICH.txt` darin listet jeden Dateinamen auf.

    ressourcen/
      LIESMICH.txt          alle Namen (schreibt das Spiel bei jedem Start neu)
      texturen/bloecke/     ein PNG pro Block: stein.png, gras_oben.png, gras_seite.png …
      geraeusche/           ein Geräusch pro Datei: klick.wav, abbauen_stein.wav …
      musik/                beliebig viele Lieder, zufällige Reihenfolge

**Texturen**: Beim ersten Start schreibt das Spiel sein eingebautes Aussehen als
PNG hinein (16 × 16 Pixel); ändern, Welt neu betreten, fertig. Größere Bilder
(32, 64 …) gehen auch – dann werden alle auf die größte Größe gebracht.
Blöcke mit verschiedenen Seiten haben `name_oben.png`, `name_seite.png`,
`name_unten.png`, alle anderen `name.png` (eine einzelne Seite kann man trotzdem
extra machen, z. B. `stein_oben.png`). Durchsichtige Pixel sind bei Blättern
Löcher und bei Glas durchsichtig – auch für die Raytracing-Schatten. Die Farbe
in der Ferne (Landschaft, Karte) ist der Durchschnitt des Bildes. Gelöschte
Dateien legt das Spiel beim nächsten Start wieder an.

**Geräusche**: Auch die eingebauten Geräusche legt das Spiel als WAV-Dateien
hinein (48000 Hz, Mono). Formate: OGG, MP3, WAV, FLAC. Eine eigene Datei mit
anderer Endung neben der WAV (`klick.ogg` neben `klick.wav`) gilt vor der WAV.
Gelesen beim Start des Spiels.

| Datei                                | Wann                                    |
| ------------------------------------ | --------------------------------------- |
| `klick`                              | Klick auf einen Knopf                   |
| `oeffnen`                            | Inventar oder Karte öffnen              |
| `nachricht`                          | Nachricht im Chat                       |
| `landen`                             | Aufkommen nach einem Sprung oder Fall   |
| `schaden`                            | Schaden nehmen                          |
| `warp_start`, `warp_ende`            | Warpsprung: Abflug (Knall) und Ankunft  |
| `explosion`, `sprudeln`              | Reaktionen mit Wasser                   |
| `triebwerk`                          | Triebwerke und Jetpack (läuft im Kreis) |
| `wind`                               | Wind (läuft im Kreis)                   |
| `abbauen_…`, `setzen_…`, `schritt_…` | Block abbauen, setzen, darauf laufen    |

`…` ist das Material: `stein` (Stein, Erz, Metall), `holz`, `erde` (Erde, Gras),
`sand` (Sand, Kies, Schnee), `weich` (Blätter) – also 15 Dateien von
`abbauen_stein` bis `schritt_weich`.

**Musik**: beliebig viele Lieder (OGG, MP3, WAV, FLAC, jeder Name), auch 100 und
mehr. Sie laufen in zufälliger Reihenfolge – jedes einmal, dann neu gemischt,
nie zweimal dasselbe hintereinander – mit 20–60 Sekunden Pause dazwischen. Das
Lied wird beim Abspielen Stück für Stück gelesen (braucht kaum Speicher), neue
Lieder kommen bei der nächsten Runde ohne Neustart dazu. Ist der Ordner beim
Start leer, spielt die eingebaute Musik. Ideen für die ersten zehn:

| Datei              | Stimmung                                              |
| ------------------ | ----------------------------------------------------- |
| `01_sonnenaufgang` | ruhiger Morgen auf der Erde, Vögel, warme Töne        |
| `02_wald`          | zwischen Bäumen, leise Gitarre oder Flöte             |
| `03_hoehle`        | tief unter der Erde, hallend, ein bisschen unheimlich |
| `04_fabrik`        | Bänder und Maschinen, gleichmäßiger Takt              |
| `05_start`         | Raketenstart, wird immer größer                       |
| `06_umlaufbahn`    | schwerelos über der Erde, weite Klangflächen          |
| `07_mond`          | grau und still, langsame Klaviertöne                  |
| `08_mars`          | rote Wüste, Wind, fremde Klänge                       |
| `09_warpsprung`    | schnell, glitzernd, aufregend                         |
| `10_heimkehr`      | zurück auf der Erde, freundlich und warm              |
