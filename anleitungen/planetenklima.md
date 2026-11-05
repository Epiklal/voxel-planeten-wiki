# Planetenklima, grüne Umlaufbahnen und Wasser

**Eine grüne Umlaufbahn ist derzeit keine Bewohnbarkeitsgarantie.** Sie zeigt nur einen vereinfachten Bestrahlungsbereich: Ein generierter Planet erhält im Mittel über seine Bahn 35–110 % des Sonnenlichts, das die Erde erhält. Auch ein Gasriese oder eine Welt ohne Wasser kann deshalb eine grüne Bahn haben. Es gibt keinen allein durch den Abstand bestimmten „perfekten“ Lebensort.

## Wie Abstand und Temperatur berechnet werden

Die thermische Sternleuchtkraft folgt aus `Radius² × Temperatur⁴`. Der Lichtanteil beim Planeten beträgt in Erd-Sonnenlicht-Einheiten `Leuchtkraft in Sonnen × (1 AE / Abstand)²`; bei mehreren Sternen werden die Beiträge addiert. Für das mittlere Licht werden 96 Stichproben verwendet. Um einen einzelnen Stern liegen die Grenzen der vereinfachten Lichtzone bei `sqrt(Leuchtkraft / 1,1)` und `sqrt(Leuchtkraft / 0,35)` AE.

Die angezeigte Temperatur ist eine **Gleichgewichtstemperatur ohne Treibhauseffekt**, mit pauschal 30 % reflektiertem Licht und gleichmäßiger Wärmeverteilung. Sie ist keine berechnete tatsächliche Oberflächentemperatur. Bei Erd-Sonnenlicht ergibt sie ungefähr 255 K (−18 °C). Die echte Erde hat durch ihre Atmosphäre im globalen Mittel etwa +15 °C. Die grüne Lichtzone ergibt mit der derzeitigen Formel ungefähr −77 bis −12 °C: Ohne zusätzliche Erwärmung kann Oberflächenwasser dort gefroren sein.

## Warum Wasser, Eis und Aussehen noch nicht zusammenpassen

Das erzeugte Aussehen ist noch eine grobe Modell-/Zufallsauswahl. Eine „Ozeanwelt“ kann bei geeigneter Masse bereits oberhalb von 200 K (−73 °C) gewählt werden; eine Eiswelt wird unterhalb von 200 K gewählt. Ozeanwelten verwenden ein Geländeprofil mit Wasser, Eiswelten ein eisiges Geländeprofil. Das ist **keine konsistente Berechnung des Aggregatzustands von Wasser**. Auch die Angaben zur Luft sind vereinfachte Atmosphärenvorlagen, kein Nachweis von atembarer Luft.

Wasservorrat, Oberflächendruck, Atmosphärenzusammensetzung, Treibhauseffekt, Albedo, lokale Temperaturen und gefährliche Sternstrahlung werden noch nicht gemeinsam zur Bewohnbarkeit ausgewertet. Eine grüne Bahn verspricht daher weder flüssiges Wasser noch Sauerstoff noch Leben ohne Schutzanzug. Ein gefrorener Planet könnte in Wirklichkeit einen flüssigen Ozean unter dem Eis besitzen; das wird hier nicht als Untereis-Ozeanmodell simuliert und würde auch keine frei bewohnbare Oberfläche bedeuten.

**Geplante Verbesserung, noch nicht implementiert:** Die Lichtzone getrennt von einer Eignungsbewertung darstellen. „Potenziell geeignet“ dürfte erst nach gemeinsamer Prüfung von Planetentyp, Wasser, Atmosphäre/Druck, Oberflächentemperatur und Strahlungsgefahren angezeigt werden.

## Pflanzenfarbe unter fremden Sternen

Pflanzen schlucken das Licht, das sie nutzen können, und werfen den Rest zurück. Deshalb haben sie unter anderen Sternen eine andere Farbe. Es gibt dafür keine neuen Texturen: Die vorhandenen grünen Bilder werden nur umgefärbt, das Muster bleibt, und Erde, Holz oder Blüten behalten ihre Farbe. Die Karte zeigt die Farbe eines fremden Planeten in der Zeile „Pflanzen“. Im Sonnensystem bleibt alles grün.

| Licht                                  | Pflanzen                                  |
| -------------------------------------- | ----------------------------------------- |
| G-Stern                                | grün                                      |
| K-Stern                                | orange                                    |
| F-Stern                                | violettrot                                |
| M-Stern                                | schwarz                                   |
| Mehrere Sterne, ähnliche Farben        | wie beim Einzelstern, etwas blasser       |
| Zwei Sterne, verschiedene Farben       | schwarz                                   |
| Drei oder mehr Sterne                  | fast schwarz                              |
| Nur Schwarzes Loch oder Neutronenstern | graubraun, tote Vegetation                |
| Stern und dunkler Rest                 | wie beim Stern, etwas blasser und dunkler |
| Schwacher Stern und dunkler Rest       | schwarz                                   |
| Mehrere Sterne und dunkler Rest        | fast schwarz                              |

Dichte Luft und viel UV (auch unter A-, B- und O-Sternen) machen die Pflanzen dunkler. Sauerstoffarme Luft verschiebt die Farbe: unter einem G-Stern nach Gelb, unter einem K-Stern nach Rosarot, unter einem F- oder M-Stern nach Violett. Ob die Luft dicht oder sauerstoffarm ist, wird fest aus dem Planeten abgeleitet.

Blau gibt es nur in einem Fall: ein einzelner, sehr heißer F-Stern und eine Luft, die Rot stark filtert, sodass Blau als Überschuss übrig bleibt.
