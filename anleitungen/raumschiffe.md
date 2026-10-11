# Raumschiffe bauen und fliegen

**Fliegen** (der Server rechnet es wie in echt): Jeder Block hat ein Gewicht (Rumpfblöcke sind leicht, volle Gesteinsblöcke 2,6 t), daraus folgen Masse, Schwerpunkt und wie schwer sich das Schiff dreht. Bauteile:

| Bauteil          |  Gewicht | Was es tut                                                                      |
| ---------------- | -------: | ------------------------------------------------------------------------------- |
| Cockpit          |   800 kg | Rechtsklick: einsteigen. Zeigt beim Setzen in Blickrichtung (vorne)             |
| Raketentriebwerk | 1 200 kg | 400 kN Schub; schiebt in die Richtung, in die man beim Setzen schaut            |
| Ionentriebwerk   |   500 kg | 25 kN Schub – für den Weltall, auf der Erde zu schwach                          |
| Kreisel          |   600 kg | dreht das Schiff (400 kNm), ohne Kreisel dreht es sich nur durch schiefen Schub |
| Leichter Rumpf   |   150 kg | Aluminiumblech                                                                  |
| Schwerer Rumpf   |   400 kg | Titanplatten                                                                    |

Ist der Schub nach oben kleiner als das Gewicht, hebt das Schiff nicht ab. Ein Triebwerk, das nicht unter dem Schwerpunkt sitzt, dreht das Schiff (die Kreisel halten dagegen, so gut sie können). Im Cockpit: W/S vor/zurück, A/D seitwärts, Leertaste/Shift hoch/runter, Maus und Q/R lenken, X schaltet die **Trägheitsdämpfer** (an: wo man nicht steuert, bremst das Schiff ab und hält sich gegen die Schwerkraft in der Luft; aus: es fliegt weiter, wie es fliegt). H schaltet **Horizont halten** (am Anfang an): Die Kreisel halten das Schiff waagerecht, die Maus dreht es nur nach links und rechts, hoch und runter schaut man nur – so fliegt es sich wie ein Hubschrauber. Aus (und fern von allem, wo es keine Schwerkraft gibt) neigt die Maus das Schiff, Q/R rollen. Rechts oben stehen Masse, Tempo, Höhe und Schub im Vergleich zum Gewicht. F oder Rechtsklick steigt aus (oben aufs Cockpit oder an den nächsten freien Platz). Ohne Pilot fällt ein Schiff, landet auf seiner Außenhaut (mit Reibung) und bleibt liegen. Feuernde Triebwerke haben eine Flamme. **An Bord** fährt man mit und spürt, wie das Schiff beschleunigt: am Boden die Schwerkraft, beim Gasgeben wird man nach hinten gedrückt, im freien Fall (Umlaufbahn) ist man schwerelos. **Reiseflug**: Ab 100 km von der nächsten Oberfläche schieben die Triebwerke immer stärker (mit dem Quadrat des Abstands), und das Schiff darf so schnell sein, dass es in 4 s dort wäre – höchstens Lichtgeschwindigkeit. Nähert man sich einem Körper, wird man dadurch von selbst langsamer.

**Treibstoff und Strom**: Bauteile, die sich berühren (oder über Leitungen verbunden sind), bilden ein Netz. Ein Triebwerk schiebt nur, wenn sein Netz etwas hat – ein Tank am anderen Ende des Schiffs nützt ohne Leitung nichts. Treibstoff ist schwer (das Schiff wird beim Fliegen leichter).

| Bauteil           | Netz               | Was es tut                                                                  |
| ----------------- | ------------------ | --------------------------------------------------------------------------- |
| Treibstofftank    | Treibstoff         | hält 500 kg; Rechtsklick mit Raketentreibstoff in der Hand füllt das Netz   |
| Treibstoffleitung | Treibstoff         | verbindet (dünnes Rohr)                                                     |
| Raketentriebwerk  | Treibstoff         | verbrennt bei vollem Schub 20 kg/s                                          |
| Schiffsgenerator  | Treibstoff → Strom | macht aus Treibstoff 5 MW, solange die Batterien nicht voll sind            |
| Schiffsbatterie   | Strom              | speichert 55 kWh                                                            |
| Solarzellen       | Strom              | 20 kW in voller Sonne (weiter weg weniger, im Schatten des Planeten nichts) |
| Schiffskabel      | Strom              | verbindet (dünn)                                                            |
| Ionentriebwerk    | Strom              | braucht bei vollem Schub 1 MW                                               |

Raketentreibstoff: Ölschiefer (Erde, große Lager in mittlerer Tiefe) im Ofen zu Erdöl, 2 Erdöl → 1 Raketentreibstoff (50 kg); auf Eiswelten (Pluto, Triton …) 3 Methaneis → 2 Raketentreibstoff, so wie die Methan-Raketen von SpaceX. Mit /schiff gebaute Schiffe kommen vollgetankt. Im Cockpit stehen Treibstoff und Strom in der Anzeige.

**Plasma**: Ein **Fusionsreaktor** verschmilzt Helium-3 (aus Mondstaub: 16 Regolith an der Werkbank – der Sonnenwind hat es über Milliarden Jahre hineingeweht) und liefert 200 MW Plasma, dazu 50 MW Strom fürs Stromnetz. Ein Stück Helium-3 reicht eine Stunde volle Leistung, in einen Reaktor passen 10 (Rechtsklick mit Helium-3 in der Hand). **Plasmaröhren** leiten das Plasma zu den **Plasmatriebwerken** (1,5 MN Schub, 2 500 kg, brauchen 100 MW): Ein Reaktor reicht für zwei auf voller Kraft – feuern mehr aus einem Netz gleichzeitig, schieben alle entsprechend schwächer. Plasmatriebwerke haben eine violette Flamme. Der Bauplan **Plasmakreuzer** zeigt, wie es geht.

**Künstliche Schwerkraft**: Ein **Schwerkraftkern** (braucht 2 MW aus dem Stromnetz) zieht an Bord wie auf der Erde zum Boden des Schiffs – egal, wie das Schiff fliegt. Ohne ihn spürt man, was das Schiff tut (Schub, Bremsen, freier Fall). **Dreht sich ein Schiff** (Dämpfer aus und mit Maus oder Q/R anwerfen – es dreht sich dann von selbst weiter), drückt die Fliehkraft nach außen, weg von der Drehachse (ω²r), dazu die Corioliskraft wie in echt: So entsteht in einem Drehring Schwerkraft. Man steht dabei immer auf der Seite, die am besten nach "unten" zeigt – auch an den "Wänden" eines Rings oder auf einem umgekippten Schiff.

**Warpantrieb**: Hängt er am Plasmanetz, springt das Schiff zu einem gewählten Himmelskörper – fast sofort. Im Cockpit öffnet M die Planetenkarte (eingebaut); rechts den Körper anklicken, dann "Warpsprung". Das kostet 100-mal so viel, wie die Strecke mit Lichtgeschwindigkeit kosten würde, dazu das Hochfahren des Warpfelds; bezahlt wird mit dem Helium-3 der Reaktoren in den Netzen mit Warpantrieb. Für kurze Strecken lohnt es sich also nicht (der Reiseflug ist dort kaum langsamer und kostet fast nichts). Beispiel Plasmakreuzer (57 t): zum Mond 0,05 Helium-3, zum Mars gut 5, zum Jupiter etwa 45 (dafür braucht er mehr Reaktoren). Warpen geht nur im Weltall (über der Luft, mindestens 100 km hoch). Beim Start gibt es eine blaue Explosion, an Bord einen gleißenden Blitz und Sterne, die vorbeiziehen; am Ziel strömen Lichtteilchen zusammen. Das Schiff kommt ruhend in sicherem Abstand an (auf der Seite, aus der es kam), alle an Bord kommen mit.

**Mitfliegen:** Im All bewegt man sich immer mit dem Himmelskörper mit, dessen Oberfläche am nächsten ist. Lässt man die Tasten los, bleibt er also gleich groß – auch wenn er in Wirklichkeit mit 30 km/s um die Sonne rast. Auf halber Strecke zu einem anderen Körper wechselt man zu dessen Bewegung.
