# Rüstung

**Rüstung** wie in Minecraft: Helm, Harnisch, Beinschutz und Stiefel, im Inventar links auf ihre Plätze legen (oder mit Shift anklicken). Die Materialien verhalten sich wie in echt:

| Material  | Rüstung | Gewicht | Strom              | Strahlung    | Besonderes                                          |
| --------- | ------: | ------: | ------------------ | ------------ | --------------------------------------------------- |
| Gummi     |       7 |    6 kg | isoliert bis 30 kV | hält 10 % ab | Gummistiefel federn Stürze ab (60 % Schaden)        |
| Gold      |      11 |   75 kg | leitet             | hält 80 % ab | weich und sehr schwer, schirmt dicht wie Blei ab    |
| Eisen     |      15 |   25 kg | leitet             | hält 50 % ab | Plattenrüstung aus Eisenplatten                     |
| Diamant   |      20 |   12 kg | isoliert bis 20 kV | hält 40 % ab | das härteste Material, leicht                       |
| Titan     |      18 |   14 kg | leitet             | hält 30 % ab | fester als Eisen, gut halb so schwer (Mond, Merkur) |
| Raumanzug |      +1 |   35 kg | isoliert bis 20 kV | hält 40 % ab | luftdicht, kommt **über** die Rüstung               |

Jeder Rüstungspunkt hält 4 % von Schlägen und Kakteen ab (höchstens 80 %, die Punkte stehen als kleine Harnische über den Herzen). Strom: Isolierende Teile schützen den Teil des Körpers, den sie bedecken (Helm 15 %, Harnisch 40 %, Beinschutz 30 %, Stiefel 15 %), der Raumanzug den ganzen Körper – gegen 380 kV hilft nichts. **Raumanzug und Rüstung wirken zusammen**: Der Anzug allein hält 40 % der Strahlung ab, mit Eisenrüstung darunter 70 %, mit Diamant 64 %, mit Gold 88 %. Schwere Sachen machen langsamer (100 kg auf der Erde: halb so schnell, auf dem Mond wiegt alles nur ein Sechstel) und ziehen im Wasser nach unten. Was man anhat, sehen die anderen an der Figur – jedes Teil bewegt sich mit seinem Körperteil (Helm am Kopf, Harnisch an Körper und Oberarmen, Beinschutz an Hüfte und Beinen, Stiefel an den Füßen); unten im Inventar steht, was alles zusammen schützt.

**Tech-Rüstung** (wie in IndustrialCraft) braucht Strom. Jedes Teil speichert seinen eigenen (grüner Balken unter dem Bild, im Spiel rechts neben den Rüstungspunkten mit Blitz und Prozent); leer schützt sie nicht, und was sie abfängt, kostet Strom (10 kJ je Lebenspunkt):

| Art     | Punkte | Speicher je Teil | Strom                | Strahlung    | Besonderes                                                             |
| ------- | -----: | ---------------: | -------------------- | ------------ | ---------------------------------------------------------------------- |
| Nano    |     20 |            1 kWh | isoliert bis 30 kV   | hält 30 % ab | leicht (10 kg), Stiefel halbieren den Fallschaden                      |
| Quanten |     26 |           10 kWh | hält auch 380 kV aus | hält 90 % ab | Helm gibt Luft wie ein Raumanzug (50 W), Stiefel fangen jeden Sturz ab |

Aufladen:
- **Akkus** (1 kWh) und **Energiekristalle** (10 kWh) im Inventar laden die angezogene Rüstung von selbst nach (bis 50 kW).
- **An Kabeln**: wer an einem Kabelblock unter Spannung steht (auch isoliert), lädt mit 20 kW (10 kV) bzw. 100 kW (380 kV) – an blanken Kabeln nur mit isolierender Rüstung, sonst gibt es einen Stromschlag (Nano hält 10 kV aus, Quanten auch 380 kV).
- **Kabellos** an einer **Ladestation** (braucht 0,5 MW aus dem Stromnetz): alle in 8 m Umkreis mit 50 kW, dazu 4 Plätze, in die man Akkus oder Rüstung zum Laden legt.
- **Solar**: Nano- und Quantenhelm lassen sich mit einem Solarmodul aufrüsten (300 W in voller Sonne, im Weltall mehr, je näher an der Sonne desto mehr, nachts und unter einem Dach nichts).

Erst wird die Rüstung voll, dann die Akkus. **Jetpack**: Nano- und Quantenharnisch lassen sich mit einem Jetpack aufrüsten – in der Luft hält die Leertaste einen oben (steigt bis 6 m/s, 30 kW; 1 kWh reicht für 2 Minuten). Beim Aufrüsten (und wenn ein Akku in einem Rezept steckt) bleibt der Strom erhalten. Wer stirbt, wacht mit "Wiederbeleben" am Startpunkt der Welt auf. Was dabei mit dem Inventar passiert, hängt von der **Schwierigkeit** ab, die man beim Anlegen einer Welt wählt – und lässt sich daneben einzeln einstellen:

| Schwierigkeit | Schaden | Erholung        | Beim Tod (Vorschlag)   |
| ------------- | ------- | --------------- | ---------------------- |
| Leicht        | halb    | ½ Herz alle 2 s | Alles behalten         |
| Normal        | normal  | ½ Herz alle 4 s | Kiste am Todesort      |
| Schwer        | 1,5×    | ½ Herz alle 8 s | Nur Werkzeuge behalten |
| Hardcore      | 1,5×    | ½ Herz alle 8 s | Alles weg (fest)       |

"Kiste am Todesort": Alles, was man dabei hatte, liegt in einer Kiste (bei viel Zeug in zweien) dort, wo man gestorben ist. Ist dort kein Platz, behält man es. Wer tot das Spiel verlässt, bekommt beim nächsten Mal wieder den Knopf "Wiederbeleben". Welten von vorher sind "Normal" mit Kiste.
