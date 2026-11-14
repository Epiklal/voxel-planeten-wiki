# Mods und Plugins

Es gibt zwei Ordner, die das Spiel beim Start selbst anlegt – im Spielordner (Einzelspieler und „Für andere öffnen“) bzw. neben dem dedizierten Server:

- **`mods/`**: neue Blöcke, Gegenstände, Rezepte und Preise aus Textdateien (`mod.txt`). Mitspieler brauchen dieselben Mods.
- **`plugins/`**: kleine Programme, die nur auf dem Server laufen und auf das reagieren, was Spieler tun – z. B. eine Bestenliste. Mitspieler brauchen nichts. Der dedizierte Server nimmt mit `--plugins <ordner>` einen anderen Ordner.

Ein Plugin ist ein Ordner in `plugins/` mit `plugin.txt` (`name = …`, `version = …`, `autor = …`) und `main.rhai`, geschrieben in [Rhai](https://rhai.rs). Das Skript schreibt Funktionen mit festen Namen, die der Server aufruft:

| Funktion | Wann |
|---|---|
| `start()` | nach dem Laden |
| `jede_sekunde()` | jede Sekunde |
| `beitreten(spieler)`, `verlassen(spieler)` | jemand kommt oder geht |
| `abgebaut(spieler, block)`, `platziert(spieler, block)` | Block abgebaut bzw. gesetzt |
| `bewegt(spieler, art, meter)` | jede Sekunde; `art`: gelaufen, geflogen, gesteuert (Schiff), mitgefahren |
| `gereist(spieler, koerper)` | auf einem anderen Himmelskörper angekommen |
| `gehandelt(spieler, art, ding, anzahl, cr)` | gekauft, verkauft oder bestellt (Terminal, Drohne, Händler) |
| `entdeckt(spieler, ding, als_erster)` | etwas entdeckt |
| `hergestellt(spieler, ding, anzahl)` | etwas hergestellt |
| `besiegt(spieler, wesen)`, `gestorben(spieler, ursache)` | Wesen besiegt bzw. gestorben |
| `auftrag(spieler, belohnung)` | Funk-Auftrag erledigt |
| `befehl(spieler, befehl, woerter)` | ein angemeldeter Chat-Befehl |
| `taste(spieler)` | Plugin-Taste (**Tab**) gedrückt |

In jeder Funktion ist `this` der Speicher des Plugins (eine Map); der Server speichert ihn mit der Welt in `plugins/<ordner>.json`. Aufrufen kann ein Skript: `befehl_anmelden(name, hilfe)`, `nachricht(spieler, text)`, `an_alle(text)`, `fenster(spieler, #{ titel, seiten: [#{ name, text, spalten, zeilen, markiert }] })` (ein Fenster mit Reitern und Tabelle), `online()`, `konto(spieler)`, `alle_konten()`, `bargeld(spieler)`, `entdeckungen(spieler)`, `erstentdeckungen(spieler)`, `ist_admin(spieler)`, `zahl(n)`, `meter(m)`, `dauer(sekunden)`, `jetzt()` und `print(text)` (ins Server-Log).

Ein kleines Beispiel, das abgebaute Blöcke zählt:

```text
fn start() { befehl_anmelden("abbau", "Wie viel habe ich abgebaut?"); }

fn abgebaut(spieler, block) {
    if this.abbau == () { this.abbau = #{}; }
    this.abbau[spieler] = (this.abbau[spieler] ?? 0) + 1;
}

fn befehl(spieler, befehl, woerter) {
    nachricht(spieler, `Abgebaut: ${zahl(this.abbau[spieler] ?? 0)} Blöcke`);
}
```

`/plugins` zeigt, welche Plugins laufen; `/hilfe` listet ihre Befehle mit. Plugins dürfen keine Dateien lesen, jeder Aufruf hat eine Höchstzahl an Schritten (eine Endlosschleife hält den Server nicht auf), und ein Plugin mit zu vielen Fehlern wird abgeschaltet.
