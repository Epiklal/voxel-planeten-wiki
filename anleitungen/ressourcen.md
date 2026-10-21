# Eigene Texturen, Geräusche und Musik

Alle Texturen, Geräusche und Lieder liegen im Ordner **`ressourcen/`** neben dem Spiel (`ExoGrid-Industry.exe` bzw. `ExoGrid-Industry`) – zum Selbstbemalen und Austauschen. Einstellungen → Credits → "Ressourcen-Ordner öffnen" zeigt ihn. Fehlende Dateien legt das Spiel beim Start an; `LIESMICH.txt` darin listet jeden Dateinamen auf.

**Blender-Modell der Batterie**: `3d/batblock.blend` ist die Blender-Quelldatei; das Spiel zeichnet den platzierten Batterieblock (`Schiffsbatterie`) mit `3d/batblock.glb`, einschließlich seiner eingebetteten PNG-Textur. Das gilt auf Schiffen und im Gelände. In Blender nur die Modellobjekte auswählen und als **glTF 2.0 / GLB** mit **Ausgewählte Objekte** exportieren. Normalen und UV-Koordinaten mit exportieren; Texturen müssen in der GLB-Datei stecken. Die gesamte Modellgeometrie wird unter Beibehaltung der Proportionen auf höchstens einen Block skaliert, horizontal zentriert und auf den Boden gesetzt. Die GLB-Datei wird beim Bauen eingebettet: Nach einem neuen Export das Spiel neu bauen und starten. Die Batterie behält ihre bisherige Blockkollision, Speicherkapazität und Stromfunktion. Inventar-/Handdarstellung bleiben unverändert. Der erste Modellimport unterstützt statische Dreiecksnetze, Materialgrundfarben und PNG-Basisfarbtexturen, noch keine Animationen, transparenten Materialien oder vollständige PBR-Effekte.

    ressourcen/
      LIESMICH.txt          alle Namen (schreibt das Spiel bei jedem Start neu)
      texturen/bloecke/     ein PNG pro Block: stein.png, gras_oben.png, gras_seite.png …
      texturen/items/       ein PNG pro Gegenstand: akku_1074.png …
      geraeusche/           ein Geräusch pro Datei: klick.wav, abbauen_stein.wav …
      musik/                beliebig viele Lieder, zufällige Reihenfolge

**Texturen**: Beim ersten Start schreibt das Spiel sein eingebautes Aussehen als PNG hinein (16 × 16 Pixel); ändern und speichern, fertig. In einer geöffneten Welt prüft das Spiel jede Sekunde auf Änderungen und lädt sie automatisch nach, einschließlich Inventar, Hand und fallengelassener Gegenstände. Fehlerhafte oder noch unvollständige PNGs werden im Log gemeldet; die bisherigen Texturen bleiben erhalten. Item-Dateien tragen den deutschen Gegenstandsnamen und zur Eindeutigkeit die Item-Nummer; `LIESMICH.txt` listet die Zuordnung. Größere Bilder (32, 64 …) gehen auch – dann werden alle auf die größte Größe gebracht. Blöcke mit verschiedenen Seiten haben `name_oben.png`, `name_seite.png`, `name_unten.png`, alle anderen `name.png` (eine einzelne Seite kann man trotzdem extra machen, z. B. `stein_oben.png`).

**Alle sechs Blockseiten einzeln bemalen**: Eine vorhandene PNG kopieren und mit einer dieser Endungen im selben Blocktextur-Ordner speichern:

| Datei (Beispiel Stein) | Seite im lokalen Blockraster |
| ---------------------- | ---------------------------- |
| `stein_vorne.png`      | vorne (−Z)                   |
| `stein_hinten.png`     | hinten (+Z)                  |
| `stein_links.png`      | links (−X)                   |
| `stein_rechts.png`     | rechts (+X)                  |
| `stein_oben.png`       | oben (+Y)                    |
| `stein_unten.png`      | unten (−Y)                   |

Eigene Seitendateien haben Vorrang vor `name_seite.png` und `name.png`. **Englische Dateinamen funktionieren ebenfalls**, unabhängig von der eingestellten Sprache: `stone.png`, `stone_side.png`, `stone_front.png`, `stone_back.png`, `stone_left.png`, `stone_right.png`, `stone_top.png`, `stone_bottom.png`. Auch gemischt geht es, beispielsweise `stein_front.png`. Die Endungen sind `front`/`vorne`, `back`/`hinten`, `left`/`links`, `right`/`rechts`, `top`/`oben`, `bottom`/`unten` und `side`/`seite`. Die Dateien zum Bemalen liegen unter **`ressourcen/texturen/bloecke/`**, nicht im Item-Ordner. `ressourcen/LIESMICH.txt` listet pro Block die vorhandenen Dateinamen und den englischen Dateistamm unter `EN` auf. Eine PNG kopieren oder umbenennen, um eine englische Variante anzulegen; das Spiel erzeugt bewusst keine doppelten Sprachversionen. Bei doppelten Dateien gilt: Einzelne Seite vor Sammelbild, innerhalb derselben Stufe englischer Blockname vor deutschem, dann englische Endung vor deutscher. Nur die bevorzugte Datei bearbeiten oder doppelte Varianten entfernen.

Fehlende Seiten behalten ihr bisheriges Aussehen; optionale Seitendateien legt das Spiel bewusst nicht automatisch an, damit die Grunddatei weiterhin wirkt. Gerichtete Blöcke drehen die Seiten mit. Normale Würfel verwenden dieselben Texturen im Gelände, auf Schiffen, in der Hand, als fallengelassene Gegenstände und für das dreidimensionale Inventarbild. Änderungen werden auch dort live übernommen. Bei Blöcken, die keine Würfel sind, ersetzen die sechs Seitendateien keine Geometrie. Sondermodelle wie die GLB-Batterie nutzen weiterhin ihre eingebetteten Materialien, keine Würfelseiten-PNGs.

**Kabeltexturen**: Auch Materialkabel einschließlich Supraleitern besitzen bearbeitbare PNGs unter `ressourcen/texturen/bloecke/`, beispielsweise `kupferkabel.png` und `niob_supraleiter.png`. Die Zuordnung samt englischen Namen steht in `ressourcen/LIESMICH.txt`. Diese Bilder gelten für verlegte Kabel, deren Verbindungen, Kabel auf Schiffen und die Kabeldarstellung in der Hand bzw. als Drop. Alle Dicken desselben Materials teilen ein Bild. Die Inventar-Itembilder unter `texturen/items/` bleiben separat bearbeitbar. Normale Blöcke in der eigenen Hand stehen mit ihrer Oberseite nach oben, unabhängig von Armneigung und Blickhöhe; ihre Texturen bleiben pixelgenau statt weichgefiltert.

Durchsichtige Pixel sind bei Blättern Löcher und bei Glas durchsichtig – auch für die Raytracing-Schatten. Die Farbe in der Ferne (Landschaft, Karte) ist der Durchschnitt des Bildes. Gelöschte Dateien legt das Spiel beim nächsten Start wieder an.

**Geräusche**: Auch die eingebauten Geräusche legt das Spiel als WAV-Dateien hinein (48000 Hz, Mono). Formate: OGG, MP3, WAV, FLAC. Eine eigene Datei mit anderer Endung neben der WAV (`klick.ogg` neben `klick.wav`) gilt vor der WAV. Gelesen beim Start des Spiels.

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

`…` ist das Material: `stein` (Stein, Erz, Metall), `holz`, `erde` (Erde, Gras), `sand` (Sand, Kies, Schnee), `weich` (Blätter) – also 15 Dateien von `abbauen_stein` bis `schritt_weich`.

**Musik**: beliebig viele Lieder (OGG, MP3, WAV, FLAC, jeder Name), auch 100 und mehr. Sie laufen in zufälliger Reihenfolge – jedes einmal, dann neu gemischt, nie zweimal dasselbe hintereinander – mit 20–60 Sekunden Pause dazwischen. Das Lied wird beim Abspielen Stück für Stück gelesen (braucht kaum Speicher), neue Lieder kommen bei der nächsten Runde ohne Neustart dazu. Ist der Ordner beim Start leer, spielt die eingebaute Musik. Ideen für die ersten zehn:

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
