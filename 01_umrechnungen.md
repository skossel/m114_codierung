# Tag 1

## Aufgabe 1
## 1. Umrechnung 11111111B in Dezimal
2 hoch 0 = 1
2 hoch 1 = 2
2 hoch 2 = 4
2 hoch 3 = 8
2 hoch 4 = 16
2 hoch 5 = 32
2 hoch 6 = 64
2 hoch 7 = 128

Summe davon = 255 D

## 2. Umrechnung 01001101B in Dezimal
1 + 4 + 8 + 64 = 77 D
Info: von rechts nach links zählen 1-64
## 3. Wieviele Bit werden benötigt, um 16 Bitkombinationen zu erstellen?
1 Bit kann 4 Binärzahlen abspeichern
16 / 4 = 4. -> es werden 4 Bit benötigt
4 Bit sind 1 Hex Ziffer
## 4. Umrechnung 11111111B in Hexadezimal
1 + 2 + 4 + 8 + 16 + 32 + 64 + 128 = 255
255 D = FF H
Auteilen: 1111 1111
F = 1111
1 + 2 + 4 + 8  = 15 -> F
## 5. Umrechnung 10110101B in Hexadezimal
## 6. Umrechnung FFH in Binär
## 7. Umrechnung E7H in Binär
## 8. Umrechnung 37D in Binär
## 9. Wieviele Bit werden mindestens benötigt, um 1000 Bitkombinationen darzustellen?

## Aufgabe 2
## 1. Addiere die beiden 4Bit Integer 0101B + 0011B
0101B
0011B
------
1000B

## 2. Addiere die beiden 4Bit Integer 1101B + 0110B
1101B
0110B
------
0001 0011B -> falsch
0011B -> richtig 1 Bit ist Data Overflow
## 3. Umrechnung -4D in Unsigned Integer mit Bitbreite 4

## 4. Umrechnung -18D in Unsigned Integer mit Bitbreite 8

## Aufgabe 3
### 1. Welche Speicherkapazität in kiB (Hinweis: 1kiB=1024B) besitzt ein Arbeitsspeicher
   mit 12-Bit-Adressbus und 16-Bit-Datenbus?
12Bit Adresse: 2^12 = 4'096 Speicherplätze
2 * 4'096 = 8'192 Bit
8'192/1'024 = 8kBi



### 2. Zwei Geräte sind mit einer seriellen Leitung und einer Leitung für das Taktsignal
   von 1MHz verbunden.
   a. Wie viele Bytes können pro Sekunde übertragen werden?
1MHz = 1'000'000 Hz
1'000'000 Hz = 1'000'000 Bit/Sekunde
   b. Wie viele Bytes pro Sekunde können übertragen werden, wenn die Verbindung
   der beiden Geräte nicht seriell, sondern 8 Bit-parallel wäre?


### Zwischenfrage
Wie viele Kombinationen sind mit 7 Bit möglich?
2^7 = 128

## Aufgabe 3
## Wo wird UTF8 eingesetzt, wo UTF-16?
UTF-8: JavaScript, HTML, Python, Linux, MacOS
UTF-16: Java, C#, Windows

## Was bedeutet die Byteorder bei UTF-16?
UTF-16 muss erkennen, ob zuerst grosses oder kleines Byte kommt:
Big Endian: 
- 12 34
- Zuerst das grosse Byte (von rechts aus betrachten)
- FE FF
Little Endian: 
- 34 12
- Zuerst das kleine Byte
- FF FE

## Was bedeutet «abwärtskompatibel» im Zusammenhang mit UTF-8? Existiert diese
«Abwärtskompatibilität» auch bei UTF-16?
UTF-8
- Abwärtskompativel zu ASCII, da erste 128 Zeichen gleich sind
- ASCII ist 7 Bit, UTF-8 ist 8 Bit
UTF-16
- Nicht abwärtskompatibel zu ASCII, da UTF-16 2 Byte pro Zeichen benötigt und ASCII nur 1 Byte
- UTF-16 ist 16 Bit, ASCII ist 7 Bit

## Wie beurteilen sie den Speicherbedarf von deutsch- oder englischsprachigem Text
bei ISO-8859-Codierung, UTF-8-Codierung und UTF-16-Codierung?
UTF-8:
- 1 Byte für ASCII(a-z, 0-9)
- 2 Byte für Umlaute ( ä, ö, ü)
UTF-16:
- 2 Byte pro Zeichen egal welches Zeichen

## Wann wird ein UTF-16-Code vier Byte lang?
UTF-16 braucht 4 Bytes, wenn das Zeichen ausserhalb der BMP (Basic Multilingual Plane) liegt, also:
Unicode-Codepoint ab U+10000

## Wie müssen sie vorgehen, wenn sie z.B. in Word ein Zeichen eingeben wollen, das sie auf der
Tastatur zwar nicht finden, dessen Unicode sie aber kennen? (z.B. das Eurozeichen)
U+20AC eingeben und danach ALT-C drücken

## Was wird das Problem sein, wenn sie auf dieselbe Weise wie in der vorangegangenen Aufgabe
das Unicode-Zeichen des Violinschlüssels (Musiknoten) in eine Wordtext einfügen wollen?
Gewählter Font-Satz wie z.B. Arial enthält Violinzeichen nicht.

## Aufgabe 4
Untersuchen sie den Textstring €URO. Beachten sie, dass es sich beim ersten Zeichen
nicht um ein E sondern um das Eurozeichen € handelt.
## 1. Wie lautet der ANSI-ASCII-Code für das Eurozeichen €?
0x80 hex -> Ox: zeigt Hexadezimal an
80 hex = 1000 0000 b

## 2. Wie lautet der Unicode für das Eurozeichen €?
U+20AC hex

U+ -> Unicode
20AC -> hexadezimaler Wert

## 3. Schreiben sie den ANSI-ASCII Text €URO in HEX und in Binär.
€ = 0x80
U = 0x55
R = 0x52
O = 0x4F
4F: 4 * 16 = 64, 15* 1 = 15

## 4. Schreiben sie den UTF-8 Text €URO in HEX und in Binär.
| Zeichen | UTF-8 (HEX) | UTF-8 (Binär)                          |
|---------|-------------|----------------------------------------|
| €       | E2 82 AC    | 11100010 10000010 10101100             |
| U       | 55          | 01010101                               |
| R       | 52          | 01010010                               |
| O       | 4F          | 01001111                               |

## 5. Schreiben sie den UTF-16-BE Text €URO in HEX und in Binär.
| Zeichen | UTF-16-BE (HEX) | UTF-16-BE (Binär) |
|---------|-----------------|-------------------|
| €       | 20 AC           | 00100000 10101100 |
| U       | 00 55           | 00000000 01010101 |
| R       | 00 52           | 00000000 01010010 |
| O       | 00 4F           | 00000000 01001111 |

## 6. Schreiben sie den UTF-16-LE Text €URO in HEX und in Binär.
| Zeichen | UTF-16-LE (HEX) | UTF-16-LE (Binär) |
|---------|-----------------|-------------------|
| €       | AC 20           | 10101100 00100000 |
| U       | 55 00           | 01010101 00000000 |
| R       | 52 00           | 01010010 00000000 |
| O       | 4F 00           | 01001111 00000000 |

## 7. Vergleichen sie die Resultate.
U, R, O sind immer 7 Bit und werden einfach mit Nullen aufgefüllt
