# Grafik und Einstellungen

**Einstellungen** gibt es im Hauptmenü und im Spiel im Pause-Menü (Esc) – dort gilt alles sofort. Oben wählt man den Bereich, ein Linksklick auf einen Knopf schaltet weiter, ein Rechtsklick zurück. **Zahlen sind Schieberegler** wie in Minecraft (anklicken und ziehen): Sichtweite (2–64 Chunks), Auflösung, Sichtfeld, Helligkeit, Bilder pro Sekunde, Threads, Maus, Lautstärken und die Chat-Werte. Unten steht, was der Knopf unter der Maus macht. Gespeichert in `einstellungen.txt` im Spielstand-Ordner, dort liegt auch `log.txt` (wird bei jedem Start neu geschrieben – bei Problemen mitschicken).

**Grafik** hat drei Seiten: **Allgemein**, **Bildqualität** und **Leistung**. Die **Grafikstufe** stellt die Werte links (auf beiden Seiten) auf einmal ein; jeden kann man danach einzeln ändern ("angepasst"):

| Stufe   | Auflösung der Welt | Pixel-Look | Sichtweite Blöcke | Landschaft | Lichtstreuung | Wolken  | Kantenglättung | Schärfe | Texturen      |
| ------- | -----------------: | ---------- | ----------------- | ---------- | ------------- | ------- | -------------- | ------- | ------------- |
| Minimal |               50 % | an         | 4 Chunks (64 m)   | Aus        | Einfach       | aus     | aus            | aus     | Pixel         |
| Retro   |               50 % | an         | 6 Chunks (96 m)   | Kurz       | Einfach       | aus     | aus            | aus     | Pixel         |
| Niedrig |               67 % | aus        | 8 Chunks (128 m)  | Mittel     | Niedrig       | Niedrig | FXAA           | aus     | Mipmaps       |
| Mittel  |              100 % | aus        | 12 Chunks (192 m) | Weit       | Mittel        | Mittel  | FXAA           | aus     | Anisotrop 4×  |
| Hoch    |              100 % | aus        | 16 Chunks (256 m) | Sehr weit  | Hoch          | Hoch    | TAA            | leicht  | Anisotrop 8×  |
| Ultra   |              100 % | aus        | 24 Chunks (384 m) | Extrem     | Ultra         | Ultra   | TAA            | leicht  | Anisotrop 16× |

- Auflösung: 25–200 % der Fenstergröße (Menüs und Schrift bleiben scharf). Unter 100 % schneller; mit TAA holt das Spiel über mehrere Bilder Details zurück (Hochskalieren wie FSR/DLSS). Über 100 % **Supersampling**: größer zeichnen und verkleinern – sehr glatt, aber teuer (200 % = viermal so viele Pixel)
- **Kantenglättung**: **FXAA** (schnell, sucht Kanten im fertigen Bild und glättet sie, etwas weich) oder **TAA** (jedes Bild wird um einen Bruchteil eines Pixels verschoben gezeichnet und mit den vorigen gemischt – die glattesten Kanten, kein Flimmern, kein Nachziehen dank Tiefe und Kamerabewegung)
- **Schärfe**: macht das Bild nach der Kantenglättung wieder knackiger (Aus, Leicht, Mittel, Stark), ohne helle Ränder an Kanten
- **Zwischenbilder** (Frame Generation, bei allen Stufen aus): Die Welt wird nur jedes zweite Bild neu gezeichnet; jedes gezeigte Bild wird auf die neueste Blickrichtung verschoben. Gemessen etwa 35–45 % mehr Bilder pro Sekunde, gleichmäßig verteilt; an Rändern, die bei schneller Bewegung neu ins Bild kommen, leichte Schlieren
- **Texturen**: Pixel (ohne Mipmaps – flimmert in der Ferne wie bei ganz alten Spielen), Mipmaps (in der Ferne weich), Anisotrop 4×/8×/16× (auch flach liegende Böden bleiben bis weit hinten scharf; nah bleiben die Texel trotzdem kantig)
- Pixel-Look: verkleinertes Bild mit großen, scharfen Pixeln wie bei alten Spielen
- Landschaft: wie weit und fein die vereinfachte Landschaft hinter den Blöcken reicht (Aus, Kurz … Extrem, **Maximal** für sehr starke Grafikkarten). **Gebautes ist darin auch in der Ferne zu sehen**: Häuser, Türme, Fabriken, Glas und Bäume, die Spieler gesetzt haben, als vereinfachte Klötze (Bauwerke betongrau) – auch aus der Luft, mit dem Teleskop und aus dem All (dort nur, was groß genug ist). Die Sichtweite der echten Blöcke geht bis 64 Chunks (1 km)
- Lichtstreuung: wie genau Himmel, Dunst und Abendrot gerechnet werden
- Wolken: aus bis Ultra (Wolken kosten viel Rechenzeit)
- Niederschlag: Regen und Schnee als Effekt auf dem Bildschirm (bis Mittel) oder als echte Tropfen und Flocken in der Welt – "Teilchen" (Hoch, 12 000) bzw. "Viele Teilchen" (Ultra, 30 000): unterschiedlich lang, schnell und hell, in Böen dichter, Schnee taumelt; Dächer und Bäume halten sie ab, Blöcke davor verdecken sie. Kostet kaum etwas (gut 0,3 ms je Bild)
- Blätter: durchsichtig (mit Löchern, man sieht in die Bäume hinein) oder undurchsichtig wie bei alten Spielen (schneller; Stufen Retro und Niedrig)
- **Raytracing** (nur auf Grafikkarten, die es können, z. B. Radeon RX 6000 und neuer, GeForce RTX, Intel Arc – sonst ausgegraut): **Schatten** – jeder Pixel schickt einen Strahl zur Sonne; Bäume, Berge, Häuser und Schiffe werfen echte Schatten (bis 160 m um dich herum, dahinter weich ausgeblendet). Durch die Löcher der Blätter fällt geflecktes Licht, farbiges Glas wirft farbiges Licht, klares Glas nur einen Hauch von Schatten – oder **Schatten + Spiegelungen**: Wasser spiegelt auch Ufer, Bäume und Bauwerke statt nur den Himmel. Stufe Ultra schaltet beides ein. Kostet auf einer RX 7900 XTX etwa 1 ms pro Bild.
- Rechts auf Allgemein: **Oberfläche** – wie groß Menüs, Schrift und Inventar sind. Automatisch: so groß, wie es ins Fenster passt (springt, wenn das Fenster etwas kleiner oder größer wird); fest 1×, 2×, 3× …: bleibt gleich (höchstens so groß, dass alles passt). Dazu Sichtfeld (30–110°), Helligkeit (50–200 %), **Animationen** (Alle / Wenige: ohne Blitze, weniger Lichtteilchen / Aus: Wolken stehen, keine Flammen, Sterne im Menü funkeln nicht) und Grafik-Schnittstelle (nach Neustart); auf Bildqualität: Bilder pro Sekunde (alle oder höchstens 20–245 – schont alte Rechner und Akkus) und VSync

**Leistung** (für schwache Prozessoren, dazu der Look ganz alter Spiele):

- **Nebel**: Die Welt verschwindet vor dem Ende der Sichtweite im Dunst – in genau der Farbe des Horizonts (auch abends). Ohne Landschaft füllt der Dunst auch den Boden dahinter, statt dort Leere zu zeigen. Höher, als die Blöcke reichen, blendet er aus und die Landschaft erscheint (sonst sähe man aus dem Flugzeug nichts)
- **Chunks pro Bild**: alle oder höchstens 32/16/8/4 – weniger ruckelt nicht beim Laden, die Welt baut sich aber langsamer auf
- **Farbtiefe**: Voll, 16 Bit (5-6-5 wie Grafikkarten der 90er) oder 8 Bit (3-3-2 = 256 Farben wie VGA), mit dem typischen Raster dazwischen
- **Threads**: wie viele Prozessor-Threads Chunks und Landschaft berechnen (automatisch oder 2–32; gilt beim nächsten Betreten einer Welt)

Dazu: Landschaft **Aus** (am Boden nur die echten Blöcke – spart viel Prozessor; aus der Höhe und dem All sieht man die Himmelskörper trotzdem), Texturen **Aus** (jede Seite einfarbig wie die ersten 3D-Spiele) und Sichtweite ab 2 Chunks.

Für sehr schwache Rechner (Dual-Core): Grafikstufe **Minimal** – halbe Auflösung, 4 Chunks Sicht mit Nebel, keine Landschaft dahinter, höchstens 8 Chunks pro Bild, 16 Bit Farben. Dazu Bilder pro Sekunde höchstens 30 und Animationen aus. Getestet mit 2 Prozessorkernen (`taskset -c 0,1`): wählt Minimal von selbst, 60 Bilder pro Sekunde. **Retro** sieht ähnlich alt aus, hat aber Landschaft und mehr Sichtweite.

**Steuerung**: alle Tasten frei belegen (Linksklick auf die Taste, dann die neue drücken; Esc bricht ab; schon belegt → getauscht), Maus-Empfindlichkeit (10–300 %), Maus umgekehrt, "Standard-Tasten". Gespeichert werden nur geänderte Tasten (`taste.vorwaerts = KeyQ Q` – Taste und was draufsteht).

**Ton**: Lautstärken für alles, Effekte (Abbauen, Bauen, Schritte, Landen, Schaden, Warpsprung), Umgebung (Wind, Triebwerke, Jetpack), Bedienung (Klicks, Inventar, Chat) und Musik (Standard 50 %). Die eingebauten Geräusche und die eingebaute Musik (ruhige Klänge) erzeugt das Spiel beim Start selbst; eigene Dateien im Ressourcen-Ordner ersetzen sie (siehe unten). Ohne Tongerät bleibt das Spiel einfach still.

**Figur**: wie dich die anderen sehen – Haut, Haare, Frisur (kurz, lang, Glatze, Mütze, Zopf, Irokese, Afro oder Dutt), Augen, Oberteil, Hose, Schuhe. Farben lassen sich aus Paletten wählen und mit RGB-Reglern frei mischen; rechts ist eine Vorschau. Dazu gibt es "Zufällig" und "Wie am Anfang" (aus dem Namen). Andere Spieler sind Figuren mit Armen und Beinen, die beim Laufen schwingen (nicht bei Animationen "Aus"). Wer schleicht, duckt sich: Oberkörper nach vorne gebeugt, Kopf tiefer – das sehen auch die anderen.

**Chat**: neue Zeilen zeigen oder nur im offenen Chat, Anzeigedauer (1–60 s), Anzahl Zeilen, Breite, Hintergrund (durchsichtig bis schwarz), große Schrift, "… ist im Spiel / hat das Spiel verlassen" an oder aus – mit Vorschau.

**Credits**: wer das Spiel gemacht hat und womit, dazu "Spielstand-Ordner öffnen" und "Ressourcen-Ordner öffnen".

"Automatisch" wählt nach Rechner: höchstens 2 Prozessor-Threads (Dual-Core ohne Hyperthreading) → Minimal; sonst nach Grafikkarte: eigene Grafikkarte → Hoch, alte Intel-Grafik (HD/UHD Graphics) und Software-Grafik → Niedrig, sonst Mittel.

Beim Start probiert das Spiel alle Grafikkarten und Schnittstellen der Reihe nach (Vulkan → DirectX 12 → OpenGL) und nimmt die erste, die alle Shader des Spiels übersetzen kann. Alte Intel-Grafik hat unter Windows z. B. kein Vulkan, läuft aber mit DirectX 12 oder OpenGL. Im Hauptmenü steht unten, was gerade benutzt wird.
