# Himmelskörper

Sonne, 8 Planeten, 9 Zwergplaneten und alle 466 bekannten Monde – vom Erdmond bis zu Brocken von 700 m Durchmesser. Alle Größen, Bahnen, Umlaufzeiten, Massen und Drehachsen sind echt; wo ein Körper am 1. Januar 2000 stand, steht er auch zu Spielbeginn. **Schwerkraft** ist im Verhältnis zur Erde angegeben; die **Sprunghöhe** gilt im Spiel (dort ist die Schwerkraft überall 2,45-mal so stark wie echt, damit sich Springen auf der Erde wie in Blockspielen anfühlt).

## Planeten

| Name    |     Radius | Abstand zur Sonne | Schwerkraft |                     Drehung | Im Spiel                                         |
| ------- | ---------: | ----------------: | ----------: | --------------------------: | ------------------------------------------------ |
| Sonne   | 696 340 km |                 – |     28-fach |                     25 Tage | keine Blöcke, man kann nicht landen              |
| Merkur  |   2 440 km |        58 Mio. km |        38 % |                     59 Tage | grauer Staub, Basalt, kein Himmel                |
| Venus   |   6 052 km |       108 Mio. km |        90 % |         243 Tage, rückwärts | gelbes Schwefelgestein, dichter gelber Dunst     |
| Erde    |   6 371 km |       150 Mio. km |       100 % |                 23 h 56 min | Kontinente, Ozeane, Wälder, Wüsten, Eis (Biome)  |
| Mars    |   3 390 km |       228 Mio. km |        38 % |                 24 h 37 min | roter Sand, Eis-Polkappen, butterfarbener Himmel |
| Jupiter |  69 911 km |       778 Mio. km |       253 % |                  9 h 56 min | Wolkenstreifen (begehbare Wolkenblöcke)          |
| Saturn  |  58 232 km |       1,4 Mrd. km |       106 % |                 10 h 39 min | cremefarbene Wolken, **Ringe** (siehe unten)     |
| Uranus  |  25 362 km |       2,9 Mrd. km |        89 % | 17 h 14 min, um 98° gekippt | türkise Wolken                                   |
| Neptun  |  24 622 km |       4,5 Mrd. km |       114 % |                  16 h 6 min | blaue Wolken                                     |
 
## Karte des Planeten

Oben rechts ist immer eine **kleine Karte** (Taste K blendet sie aus): Norden oben, man selbst als roter Pfeil in Blickrichtung, dazu Bauwerke, Mitspieler, Todesorte und Markierungen; je höher man ist, desto weiter reicht sie. Mit **M** öffnet sich die **große Karte**: Ziehen verschiebt, das Mausrad zoomt – von einzelnen Blöcken bis zur ganzen Kugel. Das Gelände kommt aus dem Weltgenerator: Meere (tiefes Wasser dunkler), Strände, Wüsten, Steppen, Wälder, Gebirge mit Schatten, Eis und Schnee.

**Zu sehen ist nur, wo man schon war**: am Boden ein paar hundert Meter um einen herum, je höher man fliegt, desto mehr (aus dem Orbit ein großes Stück des Planeten); der Rest ist dunkel. Im Kreativ- und Zuschauermodus sieht man alles. Was man aufgedeckt hat, merkt sich der Client je Welt (`karten/<seed>.txt` neben den Einstellungen).

Zoomt man ganz hinaus und dreht das Mausrad weiter, wird daraus die **Weltall-Karte** (wenn man darf, siehe unten) – und umgekehrt: Zoomt man in der Weltall-Karte an einen Planeten oder Mond heran, wird er zur Kugel mit seinem Gelände und ganz nah zu genau derselben Karte.

## Wegpunkte

Benannte Stellen auf einem Planeten oder Mond – im Bild als Fähnchen mit Name und Entfernung (auch durch Wände und über den Horizont), auf der kleinen und der großen Karte in ihrer Farbe. Gespeichert werden sie **auf dem Server beim Spieler** (je Welt, mit dem Himmelskörper): Wer auf einem Server spielt, hat sie auf jedem Rechner.

- **Setzen**: in der großen Karte (M) links einen Namen eintippen und Enter bzw. "Hier" (wo man steht) – oder **Rechtsklick auf die Karte** (dort, auf dem Boden). Oder im Chat `/wegpunkt setzen <Name>`.
- **Liste je Planet**: Links in der Karte stehen die Wegpunkte des Himmelskörpers, auf dem man ist (ein Klick auf den Namen fährt hin), darunter, wie viele auf anderen Körpern liegen; `/wegpunkt liste` zeigt alle, nach Himmelskörper.
- **an/aus**: im Bild zeigen oder nicht (auf der Karte bleibt er), **x** löscht.
- **Teilen**: "teilen" schickt ihn an das eigene Team (ohne Team: an alle), oder `/wegpunkt teilen <Name> <Spieler|team|alle>`. Bei den anderen steht er dann mit "(von …)" in der Liste; noch einmal geteilt, ersetzt er den alten.
- `/wegpunkt umbenennen <Name> <Neu>`, `/wegpunkt löschen <Name>` – Leerzeichen im Namen schreibt man in Befehlen als `_`.

## Planetenkarte (Weltall-Karte)

Ein Gegenstand (Werkbank: 2 Eisenplatten, 4 Kupferdraht, 1 Quarzkristall), der das Sonnensystem in 3D zeigt – in echtem Maßstab, mit allen Bahnen und wo jeder Körper gerade steht. **Ziehen** (linke Maustaste) dreht die Ansicht um die Mitte, mit der **rechten Maustaste** verschiebt man sie; "Von oben" bzw. "Schräg" oben rechts springt zurück. Planeten und Zwergplaneten stehen auf dünnen Stielen zur Ebene der Erdbahn – so sieht man, wie weit z. B. Pluto darüber oder darunter ist. Rot markiert: wo man selbst ist. Rechts stehen alle Planeten und Zwergplaneten mit ihrer Entfernung von einem; ein Klick auf einen Namen fährt hin und zoomt so weit, dass man seine großen Monde sieht. Dazu öffnet sich links ein **Fenster** mit allem über ihn: Entfernung, wie lange Licht bis dorthin braucht, Radius, Abstand zur Sonne bzw. zum Planeten, Umlaufzeit, wie lange ein Tag dauert, Schwerkraft, etwas zum Staunen und darunter **alle seine Monde** mit Radius (das Mausrad scrollt im Fenster). Ein Klick auf einen Mond zeigt seine Angaben, „Mond von …“ führt zurück zum Planeten, X schließt das Fenster. **Zu mir** (unten rechts) springt zurück zum Himmelskörper, auf dem man gerade ist. Entfernungen stehen in km, Mio. km, Mrd. km und Bio. km. Der Tag geht von Sonnenaufgang zu Sonnenaufgang und ist darum nicht ganz gleich der Drehung in den Tabellen: Die Erde dreht sich in 23 h 56 min, ein Tag dauert 24 h; auf der Venus 117 Tage statt 243, auf dem Mond 29,5 Tage. Mausrad zoomt (vom ganzen Sonnensystem bis zu einzelnen Monden), ein Klick auf einen Punkt wählt ihn aus (die Karte dreht sich dann um ihn). Ein roter Pfeil an der eigenen Position zeigt, wohin man gerade schaut.

Solange man die Karte **in der Hand** hält, stehen im Bild Wegweiser: wo am Himmel Sonne, Planeten, Zwergplaneten und die großen Monde in der Nähe sind, mit Name und Entfernung – so weiß man, wohin man fliegen muss. Was außerhalb des Bildes liegt, zeigt ein Punkt am Rand in seiner Richtung; was hinter dem eigenen Planeten liegt (unter dem Horizont), ist blasser. Mit **P** (umbelegbar) schaltet man dieselben Wegweiser dauerhaft an und aus – das geht im Kreativmodus, wenn man die Karte irgendwo im Inventar hat, oder im Cockpit eines Schiffs.

Im **Kreativmodus** bringt der Knopf „Hinreisen“ einen sofort zum ausgewählten Körper – auf den Boden, wo dort gerade Vormittag ist (zur Sonne: in sicherem Abstand). Kreativ-Spieler haben die Karte von Anfang an in der Schnellleiste.

## Teleskop

Ein **Teleskop** (Werkbank: 3 Kupferbarren + 2 Glas) in der Hand: **rechte Maustaste halten** zoomt weich heran, das **Mausrad** stellt die Vergrößerung ein (2× bis 1000×, Start 8×), Loslassen zoomt zurück. Rundherum ein schwarzer Rand wie beim echten Fernrohr, die Maus dreht entsprechend langsamer. Die Landschaft im Bild wird beim Zoomen feiner berechnet – bei 12× sieht man auf einem Berghang in 2 km Entfernung einzelne Kakteen und Erzflecken; Mond und Planeten werden bis zur vollen Vergrößerung feiner (auf dem eigenen Himmelskörper höchstens 6-mal, sonst würde auch alles hinter Bergen fein berechnet). Geht auch als Zuschauer.

## Saturns Ringe

Eine flache Scheibe in Saturns Äquatorebene, 66 900–141 000 km vom Mittelpunkt, mit echtem Aufbau: der fast undurchsichtige, cremefarbene **B-Ring**, außen der **A-Ring** mit der Encke- und der Keeler-Lücke, dazwischen die dunkle **Cassini-Teilung**, innen der dünne graue **C-Ring** (durch ihn sieht man Sterne), ganz außen der schmale **F-Ring**. Der Saturn wirft seinen Schatten auf die Ringe, die Ringe werfen Schattenbänder auf den Saturn. Von der beleuchteten Seite leuchten die dichten Ringe hell; von der anderen Seite scheint Licht nur durch die dünnen Stellen. Vom Saturn aus spannen sie sich als Bogen über den Himmel (am Tag blass, nachts hell). Man kann durch sie hindurchfliegen – sie bestehen (noch) nicht aus Brocken, aus der Nähe sind sie eine flache Fläche.

## Zwergplaneten

| Name     |   Radius | Abstand zur Sonne |       Umlauf |   Drehung | Monde                                  | Im Spiel                                                       |
| -------- | -------: | ----------------: | -----------: | --------: | -------------------------------------- | -------------------------------------------------------------- |
| Ceres    |   470 km |   380–450 Mio. km |    4,6 Jahre | 9 h 4 min | –                                      | größter Körper im Asteroidengürtel: dunkler Staub              |
| Pluto    | 1 188 km |   4,4–7,4 Mrd. km |    248 Jahre |  6,4 Tage | 5 (Charon, Nix, Hydra, Kerberos, Styx) | rotbraune Tholine, helles Stickstoffeis an den Polen           |
| Eris     | 1 163 km |  5,7–14,6 Mrd. km |    560 Jahre | 15,8 Tage | Dysnomia                               | hell wie frischer Schnee                                       |
| Haumea   |   780 km |   5,2–7,7 Mrd. km |    283 Jahre |     3,9 h | Hiʻiaka, Namaka                        | Wassereis (in Wirklichkeit eiförmig)                           |
| Makemake |   715 km |   5,7–7,9 Mrd. km |    308 Jahre |    22,8 h | MK2                                    | rötliches Methaneis                                            |
| Gonggong |   615 km |  4,9–15,1 Mrd. km |    547 Jahre |    22,4 h | Xiangliu                               | sehr rot                                                       |
| Quaoar   |   545 km |   6,3–6,7 Mrd. km |    284 Jahre |    17,7 h | Weywot                                 | rötlich                                                        |
| Sedna    |   497 km |    11–150 Mrd. km | 12 700 Jahre |    10,3 h | –                                      | einer der rötesten Körper; braucht für eine Runde 12 700 Jahre |
| Orcus    |   455 km |   4,6–7,2 Mrd. km |    247 Jahre |    13,2 h | Vanth                                  | graues Wassereis                                               |

## Monde

| Planet        | Monde | davon groß (> 100 km Durchmesser)                                                          |
| ------------- | ----: | ------------------------------------------------------------------------------------------ |
| Erde          |     1 | Mond                                                                                       |
| Mars          |     2 | – (Phobos und Deimos sind kleiner)                                                         |
| Jupiter       |   115 | Io, Europa, Ganymed, Kallisto, Amalthea, Himalia                                           |
| Saturn        |   291 | Titan, Rhea, Iapetus, Dione, Tethys, Enceladus, Mimas, Hyperion, Phoebe, Janus, Epimetheus |
| Uranus        |    29 | Titania, Oberon, Umbriel, Ariel, Miranda, Puck, Portia, Sycorax                            |
| Neptun        |    16 | Triton, Proteus, Nereid, Larissa, Galatea, Despina                                         |
| Pluto         |     5 | Charon                                                                                     |
| Zwergplaneten |     7 | Dysnomia, Hiʻiaka, Vanth                                                                   |

Die meisten kleinen Monde sind dunkle, eingefangene Brocken auf weiten, schrägen und oft rückläufigen Bahnen; ihre Größe ist aus ihrer Helligkeit geschätzt. Die großen Monde und ihr Aussehen im Spiel:

Fast alle Monde sind gebunden rotierend: Sie zeigen ihrem Planeten immer dieselbe Seite, ein Tag dauert dort so lange wie ein Umlauf. Wo nicht anders angegeben, kreisen sie in der Äquatorebene ihres Planeten.

| Mond       | Planet  |   Radius | Abstand zum Planeten | Schwerkraft | Sprung | Im Spiel                                                                                       |
| ---------- | ------- | -------: | -------------------: | ----------: | -----: | ---------------------------------------------------------------------------------------------- |
| Mond       | Erde    | 1 737 km |           384 400 km |        17 % |  7,6 m | grauer Staub, schwarzer Himmel, die Erde am Himmel                                             |
| Phobos     | Mars    |    11 km |             9 376 km |      0,06 % | 2,1 km | dunkler Staub; Mars füllt einen großen Teil des Himmels                                        |
| Deimos     | Mars    |     6 km |            23 463 km |      0,03 % | 4,9 km | dunkel und glatt – der kleinste Körper im Spiel                                                |
| Io         | Jupiter | 1 822 km |           421 700 km |        18 % |  6,8 m | gelber Schwefel, rötliche Pole, Basaltklippen                                                  |
| Europa     | Jupiter | 1 561 km |           671 034 km |        13 % |  9,3 m | glattes Eis                                                                                    |
| Ganymed    | Jupiter | 2 634 km |         1,07 Mio. km |        15 % |  8,6 m | größter Mond: schmutziges Eis, helle Polkappen                                                 |
| Kallisto   | Jupiter | 2 410 km |         1,88 Mio. km |        13 % |  9,9 m | dunkler Staub, helle Eisklippen                                                                |
| Amalthea   | Jupiter |    84 km |           181 366 km |       0,2 % |  620 m | der rötlichste Körper im Sonnensystem                                                          |
| Himalia    | Jupiter |    70 km |         11,5 Mio. km |       0,6 % |  210 m | dunkler, eingefangener Brocken, schräge Bahn, dreht sich in 7,8 h                              |
| Mimas      | Saturn  |   198 km |           185 539 km |       0,6 % |  190 m | graues Eis                                                                                     |
| Enceladus  | Saturn  |   252 km |           237 948 km |       1,2 % |  110 m | schneeweiß – heller als jeder andere Körper                                                    |
| Tethys     | Saturn  |   531 km |           294 619 km |       1,5 % |   84 m | graues Eis                                                                                     |
| Dione      | Saturn  |   561 km |           377 396 km |       2,4 % |   53 m | graues Eis, helle Klippen                                                                      |
| Rhea       | Saturn  |   764 km |           527 108 km |       2,7 % |   47 m | graues Eis                                                                                     |
| Titan      | Saturn  | 2 575 km |         1,22 Mio. km |        14 % |  9,1 m | **orangefarbener Dunsthimmel**, dunkle Dünen auf Eis – der einzige Mond mit dichter Atmosphäre |
| Hyperion   | Saturn  |   135 km |         1,48 Mio. km |       0,2 % |  600 m | schwammartig; taumelt in Wirklichkeit chaotisch                                                |
| Iapetus    | Saturn  |   735 km |         3,56 Mio. km |       2,3 % |   55 m | dunkel mit hellen Polen, stark geneigte Bahn                                                   |
| Phoebe     | Saturn  |   107 km |         13,0 Mio. km |       0,5 % |  250 m | dunkel, kreist rückwärts                                                                       |
| Janus      | Saturn  |    90 km |           151 460 km |      0,16 % |  780 m | teilt sich fast dieselbe Bahn mit Epimetheus                                                   |
| Epimetheus | Saturn  |    58 km |           151 410 km |       0,1 % | 1,2 km | graues Eis                                                                                     |
| Miranda    | Uranus  |   236 km |           129 390 km |       0,8 % |  160 m | zerklüftet, hohe Klippen                                                                       |
| Ariel      | Uranus  |   579 km |           190 900 km |       2,5 % |   49 m | helles Eis                                                                                     |
| Umbriel    | Uranus  |   585 km |           266 000 km |       2,5 % |   49 m | der dunkelste große Uranusmond                                                                 |
| Titania    | Uranus  |   788 km |           435 910 km |       3,7 % |   34 m | größter Uranusmond                                                                             |
| Oberon     | Uranus  |   761 km |           583 520 km |       3,6 % |   35 m | schmutziges Eis, rötliche Klippen                                                              |
| Puck       | Uranus  |    81 km |            86 004 km |       0,2 % |  630 m | dunkler Brocken                                                                                |
| Portia     | Uranus  |    68 km |            66 097 km |      0,25 % |  490 m | dunkler Brocken                                                                                |
| Sycorax    | Uranus  |    79 km |         12,2 Mio. km |      0,25 % |  490 m | rötlich, kreist rückwärts weit draußen                                                         |
| Triton     | Neptun  | 1 353 km |           354 759 km |       7,9 % |   16 m | kreist rückwärts (eingefangen), rosa Stickstoff-Polkappen                                      |
| Proteus    | Neptun  |   210 km |           117 647 km |       0,7 % |  180 m | dunkler Brocken                                                                                |
| Nereid     | Neptun  |   170 km |         5,51 Mio. km |       0,7 % |  170 m | graues Eis, sehr weite Bahn                                                                    |
| Larissa    | Neptun  |    97 km |            73 548 km |       0,3 % |  410 m | dunkler Brocken                                                                                |
| Galatea    | Neptun  |    88 km |            61 953 km |      0,19 % |  670 m | dunkler Brocken                                                                                |
| Despina    | Neptun  |    75 km |            52 526 km |      0,25 % |  490 m | dunkler Brocken                                                                                |
   
Die Uranusmonde kreisen um den um 98° gekippten Äquator des Uranus, also fast senkrecht zu seiner Bahn um die Sonne.
