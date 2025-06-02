Kontrollfragen zum Thema "Verlustbehaftete Bildkompression": (Potentielle Prüfungsfragen)
1. Was bringt mehr Speicherersparnis? Ein "UHD-1 4k" Bild anstatt in Farben (RGB) in Graustufen (Y) abzuspeichern oder das "UHD-1 4k" Bild auf ein
   "HD720" Bild herunter zu skalieren?
Herunterskalieren bringt sehr viel, das man so die Farben verringert und die Auflösung reduziert.


2. Kann man durch die Bildumwandlung vom RGB- in den YCbCr-Farbraum bereits Speicherplatz einsparen?
Nein, Anzahl Werte bleibt gleich, nur die Darstellung der Werte ändert sich.

3. Berechnen sie für folgendes Subsamplingvarianten die Speichereinsparung in % gegenüber dem Original: "4:4:4", "4:2:2", "4:1:1", "4:2:0".
   | Variante | Helligkeit (Y)                                                                 | Farbwerte (Cb & Cr)                                |
   |----------|---------------------------------------------------------------------------------|----------------------------------------------------|
   | 4:4:4    | Jeder Pixel hat eigene Helligkeit ✅                                            | ➤ Keine Ersparnis                                 |
   | 4:2:2    | Jeder Pixel hat Helligkeit ✅, aber immer 2 Pixel teilen sich 1 Farbinfo        | ➤ 50 % weniger Farbwerte                           |
   | 4:1:1    | Jeder Pixel hat Helligkeit ✅, aber 4 Pixel teilen sich 1 Farbinfo              | ➤ 75 % weniger Farbwerte                           |
   | 4:2:0    | Wie 4:2:2, aber auch in der Höhe halbiert → also nur 1 Farbe für 2×2 Pixel     | ➤ 75 % weniger Farbwerte                           |

4. Warum verschlechtert sich die Bildschärfe von 4:1:1-Subsampling gegenüber 4:4:4-Subsampling nicht?
Weil hier die Farben komprimiert werden und nicht die Helligkeit. Die Bildschärfe wird durch die Helligkeit des bildes und nicht durch die Farben bestimmt.

5. Warum bilden sich bei der JPG-Bildkompression (DCT) bei sehr starker Komprimierung sogenannte Block-Artefakte?
JPG teil das Bild in kleine 8x8 Pixel Blöcke auf und komprimiert diese einzeln.
Die benachbarten Blöcke unterscheiden sich so stärker und es werden Kanten zwischend den Blöcken sichtbar.

6. Was versteht man unter der Bezeichnung GOP25?
Group of Pictures mit 25 Bildern.
Um Speicher zu sparen, speichert man nicht jedes Bild einzeln, sonder:
- Ein Intra Frame (I-Frame) wird gespeichert, das ist ein vollständiges Bild.
- Darauf folgen 24 Differenzbilder (P-Frames / B-Frames), die nur die Unterschiede zum vorherigen Bild speichern.

7. A: In einer Heimatkundefilm-Sequenz wurde die unbewegte Kamera 20 Sekunden lang auf einen Kirchturm gerichtet.
   B: In einer Tierfilm-Sequenz verfolgt eine Handkamera aus einem bewegten Fahrzeug heraus 20 Sekunden lang einen Leoparden bei der Jagd.
   Welche der beiden Szenen A oder B bietet mehr Potential für eine speichersparende "Interframe Komprimierung"?
Szene A, da sich das Video nicht gross verändert und man so fast keine Veränderunge im Video hat.

8. Das Bild zeigt die GOP-Sequenz eines roten, wandernden Punktes. Pro Frame verschiebt sich der Punkt um eine Pixelstelle nach rechts.
   Zeichnen sie das erste Differenzbild.
   Rot und Weiss: Sichtbare Pixel
   Schwarz: Weggelassene Pixel
