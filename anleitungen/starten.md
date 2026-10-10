# Starten

```bash
cargo run --release                      # Hauptmenü: Einzelspieler, Mehrspieler, Einstellungen
cargo run --release -- --world welt      # ohne Menü gleich in die Welt "welt"
cargo run --release -- --world zweite --seed 42   # andere Welt, neue Welten mit festem Seed
cargo run --release -- --world bau --modus kreativ # neue Welt im Kreativmodus (Standard: überleben)
cargo run --release -- --world echt --welttyp realistisch  # neue Welt mit realistischer Erde (Standard hier: klassisch)
cargo run --release -- --planet mars     # auf einem anderen Himmelskörper starten (titan, io, phobos, …)
cargo run --release -- --planet io --height 400000   # 400 km über Io starten (fliegend)
cargo run --release -- --grafik niedrig  # Grafikstufe retro / niedrig / mittel / hoch / ultra (sonst passend zur Grafikkarte)
cargo run --release -- --view 24         # größere Sichtweite der Blöcke (Chunks)
cargo run --release -- --api gl          # Grafik-Schnittstelle erzwingen: vulkan, dx12, gl
cargo run --release -- --screenshot a.png --time 12  # Bild ohne Fenster + Benchmark (12 h nach Spielbeginn)
VOXEL_FIGUREN=1 cargo run --release -- --screenshot a.png  # dazu vier Spielerfiguren mit Rüstung vor der Kamera
VOXEL_HAND=0.4 cargo run --release -- --screenshot a.png   # die eigene Hand mit Schwert, mitten im Schlag (0–1)
cargo test --workspace                   # Tests
```
