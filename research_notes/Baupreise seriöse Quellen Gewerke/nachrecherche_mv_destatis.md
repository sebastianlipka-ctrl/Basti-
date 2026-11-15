# Nachrecherche: Amtliche Einheitspreise Straßen-/Brückenbau M-V (Preisdokumentation 2024/2025) und Destatis-Baupreisindizes (Stand Nov. 2026)

Hinweise zur Methode (gilt für alle M-V-Zahlen):
- Quelle: Download-Seite des Landesamts für Straßenbau und Verkehr M-V, Abschnitt „Preisdokumentation M-V 2024/2025“ — https://www.strassen-mv.de/de/downloads/ . Dort gibt es sechs PDFs: Straßenbau 2024 (613 S.), Straßenbau 2025 (712 S., erstellt am 12.02.2026), Straßen-Brückenbau 2024 (183 S.), Brückenbau 2025 (157 S.), Landschaftsbau 2024 (92 S.), Landschaftsbau 2025 (82 S.). Eine Ausgabe „Straßenbau 2022“ steht nicht mehr auf der Seite.
  - SB24: https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf
  - SB25: https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf
  - BB24: https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202024.pdf
  - BB25: https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202025.pdf
  - LB24/LB25: …/Preisdokumentation%20MV%20Landschaftsbau%202024.pdf bzw. …%202025.pdf (gleicher Pfad)
- Wie die Preise entstehen (SB25, S. A2–A7): Für jede Position (OZ) einer Ausschreibung wird das arithmetische Mittel der Einheitspreise der **5 billigsten Bieter** gebildet („MEP“). Bedingungen: mindestens 3 Bieter, nur Positionen aus dem STL-Katalog (Freitextpositionen werden nicht erfasst), Ausreißertest nach GRUBBS. Ausgewiesen werden pro STLK-Nr. **AM** (arithmetisches Mittel der MEP) und **GM** (nach Mengen gewogenes Mittel). Auswertezeitraum ist jeweils 01.01.–31.12. des Jahres. Erfasst sind die Straßenbauämter Neustrelitz, Schwerin und Stralsund sowie die SM Lübz.
- **Netto/brutto:** In den PDFs steht kein Hinweis zur Umsatzsteuer. Es sind Angebots-Einheitspreise aus öffentlichen LVs, die üblicherweise ohne USt angegeben werden. Die Angabe „netto“ ist deshalb eine Inferenz und nicht im Dokument belegt.
- „Seite“ meint unten die im Druck angegebene Listen-Seite („Seite: N“), nicht die PDF-Seite. Das „n“ in Klammern zählt die Vergabe-Einträge (Projekte bzw. VE-Typen) hinter dem Mittelwert. Bei n = 1 bis 2 sind die Werte wenig belastbar.
- **Vollständige Extraktion:** Alle 8.624 Positionen aus den sechs PDFs (je STLK-Nr. mit Kurztext, Einheit, AM, GM, n, Jahr, Seite) stehen in `/home/user/Basti-/research_notes/Baupreise seriöse Quellen Gewerke/mv_preisdoku_positionen.csv`. Format: Semikolon-getrennt, Dezimalkomma, preis_eur = AM. Bei 365 Positionen ist die Einheit maschinell nicht lesbar („k.A. (siehe PDF)“).

## Frage 1: Einheitspreise Straßen-/Brückenbau M-V (Preisdokumentation 2024/2025)

### Takeaway
Die Preisdokumentationen M-V 2024 und 2025 sind vollständig lesbar und wurden komplett extrahiert. Typische Werte (AM, netto) für 2025:
- Einfache Stahlschutzplanke (ESP, Profil B) herstellen: ca. 32–63 €/m, Eco-Safe ca. 28–54 €/m
- SE am äußeren Fahrbahnrand N2/W3–W4: ca. 28–42 €/m; auf Brücken H2: 159–225 €/m
- Schutzplanke abbauen: ca. 3–8 €/m
- Leitpfosten aufstellen: ca. 37–43 €/St
- Verkehrsschild anbringen: ca. 87 €/St
- Markierung 0,12 m (Kaltspritzplastik): ca. 0,90–1,50 €/m
- Asphalt fräsen auf großer Fläche: ca. 2 €/m², in Streifen/Zwickeln 6–16 €/m²
- AC 11 D S 4 cm: ca. 10–17 €/m²
- Baustelle einrichten (alle LV-Abschnitte), Straßenbau: ca. 12.900 €/psch

Eine eigene Position „Betonschutzwand“ und Lärmschutzwände kommen in den Listen nicht vor. Straßenbeleuchtung (Leuchten, Lichtmaste) ebenfalls nicht.

### Cited Findings

**Fahrzeug-Rückhaltesysteme / Stahlschutzplanke (LB 129) – Herstellen**
- 2025, 21.129 203 1211 11-- „SE herstellen, ESP, Profil B, Pf-Sigma L. 1900 mm, Pfostenabstand 4 m, HB 1“: AM 32,64 €/m, GM 32,64 (n=2; Einzelwerte 32,63 bzw. 32,65 €/m bei 300 m bzw. 700 m), S. 1102 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2025, 21.129 203 1212 11-- dto., Pfostenabstand 2 m: AM 62,70 / GM 31,48 €/m (n=3), S. 1102 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2025, 21.129 203 9291/9292/9293 „SE herstellen, Eco Safe, Profil B“, Pfostenabstand 4 m / 2 m / 1,33 m: AM 27,73 (GM 24,90; n=11) / AM 48,35 (GM 35,26; n=18) / AM 53,96 (GM 54,13; n=2) €/m, S. 1103–1106 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2024, dieselben Positionen: ESP Pf.-Abst. 4 m AM 40,65 / GM 38,85 €/m (n=3); ESP 2 m AM 46,01 / GM 46,94 (n=3); ESP Pf-Sigma 2500 mm, 1,33 m AM 55,95 (n=1); Eco Safe 4 m / 2 m / 1,33 m AM 34,42 / 55,46 / 66,65 €/m (n=6/13/3), S. 901–905 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- 2025, 21.129 103 … „SE am äußeren Fahrbahnrand herst., Stahl, N2, A“: W3 mit Abstand Unterl. 29,95 €/m (n=4); N2 W4 42,40 €/m (n=1); N2 W4 gestreckt 80,43 €/m (n=4); mit Motorradschutz W3 41,77 €/m; min. H1 W3 40,19 €/m, S. 1091–1094 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2025 Brückenbau-Liste: SE am äußeren Fahrbahnrand min. H1 W4: 55,23 €/m (n=2); min. H1 W5: 50,70 €/m; min. H2 W4: 88,91 €/m (n=2) bzw. 118,08 €/m (n=2); „SE auf Brücken und Stützw. herst.“ min. H1 W4 Außenkappe 118,14 €/m, min. H2 W4 158,93 €/m (AM; GM 167,82; n=3), mit Mitwirkung Geländer 225,47 €/m, Klasse max. B 194,09 €/m, S. 275–278 — [BB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202025.pdf)
- 2024 Brückenbau-Liste: SE auf Brücken min. H2 W4 Außenkappe 167,02 €/m (n=2); min. H2 W1 Mittelkappe 278,46 €/m; SE am äuß. Fahrbahnrand min. H2 W4 86,37 €/m, S. 328–329 — [BB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202024.pdf)
- 2025, 21.129 107 „SE im Mittelstreifen herstellen“ (Stahl, doppelseitig): AM 145,54 €/m; einseitig mit gemeinsamer Wirkung: 220,35 €/m (je n=2), S. 1094–1095 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2025 „AEK herstellen“ (Anfangs-/Endkonstruktion): Eco Safe Regelabsenkung 12 m 572,69 €/St (GM 596,19; n=11); ESP Profil B Pfosten Sigma 1.259,03 €/St (n=1); ESP Kurzabsenkung 4,37 m 440,25 €/St (n=3); EDSP 12 m 132,14 €/St (n=1), S. 1111–1115. Für 2024: ESP Profil B 695,80 €/St (n=2); ESP Regelabsenkung 12 m 731,99 €/St; Eco Safe 12 m 692,47 €/St (n=7); Terminal Primus P2 1.628,02 €/St, S. 908–912 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- 2025 „SE des AG aufstellen“ (Wiedereinbau von Material des AG): ESP Holm B Pfosten 4 m 7,56 €/m (n=4), 2 m 9,82 €/m (n=4), EDSP 1,33 m 12,51 €/m, DDSP 45,75 €/m, S. 1107–1110. 2024: ESP 4 m 10,19 €/m (n=2), S. 906 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2025 „FRS abbauen und herstellen“ (Umbau): 90,97–104,69 €/m (z. B. Freitext Profil B 100,32 €/m, n=5), S. 1121–1123 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- Pfosten: „Pfosten des FRS herstellen“ 2025: 35,06 €/St (Ersatzpfosten, n=2) bzw. 39,16 €/St (Eco-Safe-Pfosten C100, l=1700 mm, n=2), S. 1101/1119; 2024 ESP 47,81 €/St (n=2), S. 915 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Schutzplanke – Abbau**
- 2025 „SE aus Stahl abbauen, ESP Profil B, Pfostenabstand 4 m, HB 1, Teile verwerten“: AM 3,41 / GM 2,75 €/m (n=7); 1,33 m: 4,80 €/m (n=4); Teile zum Lagerplatz des AG: 4,08 €/m; ESP mit Teilen lagern: 79,22 €/m (n=1), S. 1066–1074 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2024 dto.: ESP 2 m 2,34 €/m; 1,33 m 2,82 €/m; EDSP 2 m 4,05 €/m; ESP 4 m 2,00 €/m (je n=2–3), S. 881–885 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- 2025 „AEK aus Stahl abbauen“ ESP Profil B Regelabs. 12 m: 104,08 €/St (n=8), S. 1076. „Schutzplanken-Pfosten abbauen“: 2,01 €/St (n=2) bzw. 4,57 €/St, S. 1082 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)

**Transportable Schutzeinrichtung (Baustelle, z. B. Betonleitwand)**
- 2025, 21.105 605 „Transp. Schutzeinrichtung aufbauen, Arb.st./ank. Verkehr, Aufhaltestufe H2, W2/W3, max. Baubreite 610 mm“: 241,09 €/m (n=1) bzw. 246,22 €/m (n=2), S. 278. „AEK f. transp. Schutzeinr. aufb.“: 904,85 €/St (n=2), S. 279 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2024 „Transp. Schutzeinrichtung umsetzen“: 17,96 €/m (n=1), S. 247 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Leitpfosten**
- 2025 „Leitpfosten aufstellen“, Eingrabpfosten ohne Auszug, Rohraussteifung 3 mm, 1 m, Typ R2: AM 42,68 / GM 44,54 €/St (n=3); Typ R1 RA2: 38,71 €/St (n=2); mit Rohraussteifung R1: 36,94 €/St; Profilaussteifung R2: 38,05 €/St, S. 1125–1129 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2024: Eingrabpfosten mit Auszug, Aussteifung 1,5 m: 50,50 €/St; Aufsatzleitpfosten (Kreuzprofil): 22,39–24,37 €/St; „Leitpfosten liefern“: 22,53 €/St, S. 918–923 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- „Leitpfosten abbauen“ (Eingrabpfosten, inkl. Erdarbeiten, verwerten): 2025 6,77 / GM 5,43 €/St (n=13), S. 1084; 2024 7,94 / GM 5,19 €/St (n=8), S. 893 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Verkehrszeichen / Schilder / Masten (LB 130)**
- 2025 „Verkehrsschild anbringen“, Größe 2, einseitig, Folie RA2, 2 mm, Rohrschelle, UK ab 2 m: AM 86,92 / GM 90,92 €/St (n=12), S. 1156. 2024 dto., 3 mm: 98,84 €/St (n=6), S. 975 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- „Verkehrsschild abbauen“ bis 1,1 m², Rohrpfosten bis 76,1, inkl. Fundament: 2025 28,43 €/St (n=5); 2024 28,73 €/St (n=5). Schild > 5–10 m² mit Mast bis 168,3: 441,37 €/St (2025), S. 1140/1147 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- „Verkehrsschild liefern“ 2024, Folie RA1, 2 mm: 28,29 €/St (n=6), S. 943 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- „Rohrpfosten aufstellen“ 2025: 3,5–4,0 m, Ø 76,1, Fundament Typ B: 121,93 €/St (n=4); 3,0–3,5 m, Ø 60,3, Fundament A: 107,76 €/St (n=3). 2024: 3,0–3,5 m, Ø 76,1, Ortbeton: 92,22 €/St (n=4); „Rohrpfosten liefern“ 2,25 m / 2,5 m Ø 60,3: 17,72 / 19,58 €/St, S. 951–985 bzw. 1167–1172 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Schildermasten 2025 „Mast aufstellen, Statik vorlegen, mit Fußplatte“: Ø 133/4,0, 4,0–4,5 m 663,57 €/St; Ø 152,4, 4,5–5 m 767,56; Ø 168,3 824,19; Ø 177,8 929,04; Ø 193,7, 5,5–6 m 1.091,45; Ø 219,1 1.376,17; Ø 244,5 1.725,66 €/St (jeweils Einzelvergabe), S. 1180–1181 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)

**Asphalt (LB 113)**
- Asphalt fräsen 2025: ADS Asphaltbeton, Tiefe 6–8 cm, Fahrbahn, Breite > 200 cm: 2,06 / GM 1,90 €/m² (n=9); Tiefe 2,5–4,5 cm, Breite 100–150 cm: 9,42 €/m² (n=6); Breite 50–100 cm: 16,21 €/m²; Breite 150–200 cm: 5,05 €/m²; Zwickel/Streifen: 6,04 / GM 3,62 €/m² (n=20); ATS 8–10 cm, Breite 50–100 cm: 14,36 €/m², S. 657–674 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- Asphalt fräsen 2024: Zwickel/Streifen 12,92 / GM 5,48 €/m² (n=33); ADS 2,5–4,5 cm Fahrbahn 1,70 €/m² (n=7); ABS 8–10 cm 2,10 €/m² (n=5); ATS 8 cm 1,18 €/m², S. 556–573 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Asphaltdeckschicht 2025: AC 11 D S, Bk3,2, 4 cm, 25/55-55A: 16,63 / GM 14,67 €/m² (n=3), mit Beschicker 10,13 €/m²; AC 11 D S nach Tonnen: 163,67 €/t bzw. 162,21 €/t; AC 11 D N, Bk1,8–0,3, 4 cm: 26,01 / GM 10,00 €/m² (n=8); MA 8 S Streifen/Rinnen: 77,57 / GM 42,35 €/m² (n=13), S. 786–816 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- Asphaltbinder 2025: AC 16 B S, Bk10, 8 cm, mit Beschicker: 21,48 €/m² (n=3); Bk3,2, 150 kg/m²: 17,90 €/m²; Schadstellen: 154,00 €/t; AC 16 B N Schadstellen: 240,58 / GM 190,07 €/t. Asphalttragschicht AC 22 T S, Bk10, 10 cm: 18,89–20,34 €/m², S. 758–784 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2024: AC 11 D S 4 cm, 50/70: 10,51 €/m² (n=5); AC 11 D S nach t: 151,63 / GM 129,27 €/t (n=4); SMA 11 S, Bk32, 4 cm: 19,46 €/m² (n=4); AC 16 B S nach t: 85,98 / GM 82,18 €/t (n=8); AC 22 B S, Bk32, 8 cm: 14,98 €/m²; AC 22 T S nach t: 60,73 €/t (Bk32, mehrschichtig oben), S. 646–683 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Fahrbahnmarkierung (LB 131)**
- 2025 Längsmarkierung Typ II, Kaltspritzplastik, 0,12 m: durchgehende Fahrbahnbegrenzung ohne Vormarkierung 0,90 / GM 0,87 €/m (n=24); mit Vormarkierung 1,50 €/m (n=17); Fahrstreifenbegrenzung 1,33 €/m; Leitlinie 1:2 1,45 €/m; Leitlinie 1:1 1,49 €/m; Blockmarkierung 0,25 m 7,44 €/m, S. 1238–1302 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- 2024: Fahrbahnbegrenzung mit Vormarkierung 1,74 €/m (n=15), ohne 0,97 €/m; Kaltplastik P7 0,12 m 5,00 €/m; Blockmarkierung Kaltplastik 0,25 m 13,35 €/m, S. 1055–1104 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Markierung entfernen (feinstfräsen) 0,12 m: 2025 2,37 €/m (n=16), 2024 2,73 €/m; Blockmarkierung 0,25 m: 6,30 bzw. 7,21 €/m — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Bankett**
- Bankett schälen 2025: 0,79–3,64 €/m (z. B. Breite bis 1,00 m, 5–10 cm, Abfräsen: 1,19 €/m). Bankett herstellen beim Hocheinbau (1,00 m): 1,19 €/m, S. 545–560. 2024: Bankett schälen 1,00–1,50 m 2,17–3,12 €/m; Hocheinbau 4,47 / GM 2,31 €/m (n=3) — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Erschwernis beim Bankettschälen durch Schilderpfosten: 17,20 €/St; bei Bankettherstellung: 19,78 €/St (2025), S. 587–588 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)

**Zäune, Tore (LB 128)**
- Wildschutzzaun herstellen 2025: H 1,6 m, Kunststoffpfosten D80, Knotengeflecht, Pfostenabstand 4 m: 23,20 €/m; Variante mit Metallanker: 13,66 €/m. 2024: H 2,0 m, Stahlpfosten D42: 42,46 €/m (jeweils n=1), S. 1059 bzw. Liste 2024 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Wildschutzzaun aufnehmen (Holzpfosten): 13,02 €/m (2025). Maschendrahtzaun herstellen H 1,50 m: 43,30–43,46 €/m; H 2,00 m: 51,66–52,42 €/m (2025), S. 1056–1063 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- Tore 2025: zweiflügeliges Tor für Stahlgitterzaun H 1,63 × B 4,00 m, Doppelstabmatte: 1.688,52 €/St; Tor für Stahlgitterzaun des AG (H 2,03 × B 4,00) herstellen: 553,52 €/St; Tür/Tor aufnehmen (B 2–4 m): 490,80 €/St. 2024: Tor einflügelig des AG 279,10 €/St, zweiflügelig 474,60 €/St — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Verkehrssicherung (LB 105)**
- 2025 „Verkehrssich. läng. Dauer vorhalten“ (wie Vorposition): AM 19,06 / GM 8,74 €/d (n=76); 2024: 23,11 / GM 23,93 €/d (n=39), S. 156 bzw. 145 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- 2025 Verkehrssicherung aufbauen nach RSA-Regelplan C I/5: 815,23 €/psch (n=6); abbauen: 327,51–896,04 €/psch; durchführen (Verkehrskonzept AG): 266,65 €/psch (n=7). 2024 „Verkehrssicherung umsetzen“: 1.074,15 €/psch (n=7) — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Transportable LSA (Baustellenampel): aufstellen Typ C 146,48 €/St (n=8, 2025) bzw. 155,50 €/St (2024); vorhalten Typ C 25,77 €/d; Typ C aufbauen und abbauen inkl. VTU 291,54–486,78 €/St; vorhalten „wie Vorposition“ 11,11 / GM 1,92 €/Std (n=23) — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- Absperrgerät/Warneinrichtung umsetzen: 15,44 €/St (2025, n=11); 8,05 €/St (2024, n=23); Absperrschranke umsetzen 16,16 €/St (2024); Vorwarn-Blinkleuchte aufbauen und abbauen 48,89–100,90 €/St — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)

**Baustelleneinrichtung (LB 101)**
- Straßenbau 2025: „Baustelle einrichten, sämtliche LV-Abschnitte, Zufahrt vorhanden“ 12.924,83 €/psch (n=37); Zufahrt durch AN herzustellen: 18.960,17 €/psch (n=4); für diesen LV-Abschnitt: 3.536,31 €/psch (n=26). „Baustelle räumen“ sämtliche Abschnitte: 2.036,18 €/psch (n=19), S. 93–99 — [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf)
- Straßenbau 2024: einrichten (sämtliche) 14.060,91 €/psch (n=37); dieser Abschnitt, Zufahrt AN: 10.559,58 (n=22); dieser Abschnitt, Zufahrt vorhanden: 4.235,95 (n=20); räumen: 1.952,58 €/psch (n=21), S. 77–81 — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf)
- Brückenbau: 2024 einrichten (sämtliche) 74.857,04 €/psch (n=4); 2025 einrichten (dieser Abschnitt) 159.138,72 €/psch, räumen 76.117,08 €/psch (n=4). Landschaftsbau 2025: 1.175,65 €/psch (n=8), 2024: 1.614,22 €/psch (n=13). SiGe-Koordinator: 7.231,26 €/psch (SB 2025), 3.014,71 €/psch (SB 2024) — [BB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202024.pdf), [BB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202025.pdf), [LB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Landschaftsbau%202025.pdf)

**Brückenbau-spezifisch**
- Betonstahl einbauen (BB25, Freitext): 767,74 / GM 558,14 €/t (n=38); Kappe 1.153,53 €/t; Fundament 1.499,66 €/t. BB24: 1.689,28 / GM 1.453,68 €/t (n=18); Kappe 1.603,47 €/t. Traggerüst: 42.134,33 €/psch (BB25) bzw. 41.824,28 €/psch (BB24). Kappenbeton C30/37 (Schalung gesondert): 769,85 €/m³ (BB24). Dichtungsschicht aus 1 Bitumenbahn, Teilflächen: 51,55 €/m² (BB24) — [BB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202025.pdf), [BB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202024.pdf)

**Elektro / Kabel / LSA (LB 132/134; Straßenbeleuchtung fehlt)**
- Kabelschutzrohr d110, liefern und einbauen: 13,95 €/m (PVC, 2025), 34,08 €/m (PE-HD, 2024); Kabel des AG verlegen: 14,62 €/m (2024); Kabel liefern und verlegen: 15,14 €/m (2025); Zähleranschlusssäule liefern und montieren: 4.718,08 €/St (BB25); Induktivschleife: 62,28 €/m; Signalgeber ab- und aufdecken: 66,79 €/St (2024) — [SB24](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202024.pdf), [SB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202025.pdf), [BB25](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202025.pdf)

### Inferenzen
- Die Werte schwanken stark: AM und GM liegen oft weit auseinander, und viele Positionen beruhen auf n=1–3. Für Kalkulationen sollte man den GM bei hohem n bevorzugen, also z. B. ESP Pfostenabstand 4 m mit ca. 25–40 €/m, Leitpfosten mit ca. 37–45 €/St, Markierung mit ca. 0,9–1,5 €/m.
- Die Preise beruhen auf den 5 günstigsten Angeboten und liegen damit tendenziell unter einem durchschnittlichen Marktpreis.
- Größere Flächen senken die €/m²-Preise deutlich (Fräsen 2 €/m² auf großer Fläche gegenüber 6–16 €/m² in Streifen).

### Lücken
- **Betonschutzwand (Ortbeton/Fertigteil, dauerhaft):** in keiner der sechs Listen als Position vorhanden. Es gibt nur die transportable SE (H2), 241–246 €/m.
- **Lärmschutzwand:** in keiner Liste als Position vorhanden. Der Begriff kommt nur als Freitext in einer Erdbauposition vor (BB24).
- **Straßenbeleuchtung (Leuchten, Lichtmaste):** keine Positionen gefunden. Vorhanden sind nur Kabel, Kabelschutzrohre, Zähleranschlusssäule, LSA-Teile und Leitungsgräben „für Beleuchtung“.
- **Anfahrschutz/Poller:** keine Position gefunden. Schranken nur als Absperrschranke der Baustellen-Verkehrssicherung.
- Preisdokumentation **Straßenbau 2022:** auf strassen-mv.de nicht mehr verlinkt, daher nicht ausgewertet.
- Netto/brutto ist in den PDFs nicht ausdrücklich angegeben (siehe Methode).

## Frage 2: Destatis-Baupreisindizes (2021 = 100), Stand Nov. 2026

### Takeaway
Der letzte veröffentlichte Berichtsmonat ist **August 2026** (Pressemitteilung Nr. 360 vom 9. Oktober 2026; der nächste Stand, November 2026, erscheint erst im Januar 2027). Indexstände konnte ich nur für Wohngebäude-Neubau und Straßenbau lesen: August 2026 Wohngebäude **141,7**, Straßenbau **149,3**. Für Ausbau, Instandhaltung, Büro- und Betriebsgebäude und die Gewerke liegen nur die Veränderungsraten aus den Pressemitteilungen vor. Alle Destatis-Werte sind **inkl. Mehrwertsteuer (brutto)**.

### Cited Findings
- Indexstände (2021 = 100) aus der Daten-CSV zur Grafik in PM 360. Die Datumsangaben der Grafik (01.01./01.04./01.07./01.10.) stehen für die Berichtsmonate Feb/Mai/Aug/Nov. Die Zuordnung ist mit den Raten der PM geprüft: 141,7/134,3 = +5,5 %, 149,3/139,7 = +6,9 % — [CSV PM 360](https://www.destatis.de/DE/Presse/Pressemitteilungen/Grafiken/Preise/Baupreise-Immobilienpreisindex/2026/_Interaktiv/_Daten/20261009-baupreise-wohngebaeude-strassenbau-index.csv?__blob=value)

| Berichtsmonat | Wohngebäude Neubau (konventionell) | Straßenbau |
|---|---|---|
| Aug 2021 | 102,1 | 100,8 |
| Aug 2022 | 118,9 | 119,0 |
| Aug 2024 | 130,3 | 135,0 |
| Aug 2025 | 134,3 | 139,7 |
| Nov 2025 | 135,0 | 140,3 |
| Feb 2026 | 137,0 | 142,9 |
| Mai 2026 | 140,3 | 147,8 |
| **Aug 2026** | **141,7** | **149,3** |

  (weitere Werte: Feb 2021 95,0/97,7; Mai 2021 98,7/99,0; Nov 2021 104,2/102,6; Feb 2022 108,8/107,2; Mai 2022 115,9/116,0; Nov 2022 121,7/122,0; Feb 2024 128,5/132,3; Mai 2024 129,4/133,3; Nov 2024 130,8/135,6; Feb 2025 132,6/137,8; Mai 2025 133,6/139,2)
- Veränderung zum Vorjahresmonat (Raten-CSV): Wohngebäude / Straßenbau Feb 2025 3,2/4,2; Mai 2025 3,2/4,4; Aug 2025 3,1/3,5; Nov 2025 3,2/3,5; Feb 2026 3,3/3,7; Mai 2026 5,0/6,2; Aug 2026 5,5/6,9 % — [Raten-CSV](https://www.destatis.de/DE/Presse/Pressemitteilungen/Grafiken/Preise/Baupreise-Immobilienpreisindex/2026/_Interaktiv/_Daten/20261009-baupreise-wohngebaeude-strassenbau-raten.csv?__blob=value)
- PM 360 (9.10.2026), August 2026 gegenüber August 2025: Wohngebäude +5,5 % (gegenüber Mai 2026 +1,0 %); Rohbau +5,4 %; Ausbau +5,7 %; Betonarbeiten +4,3 %; Mauerarbeiten +4,2 %; Dachdeckung +7,6 %; Zimmer-/Holzbau +7,2 %; Erdarbeiten +6,1 %; Heizanlagen/zentrale Wassererwärmung +5,2 %; **Metallbauarbeiten +5,0 %**; **Elektro-, Sicherheits- und Informationstechnische Anlagen +7,2 %**; WDVS +5,7 %; Instandhaltung Wohngebäude (ohne Schönheitsreparaturen) +6,0 %; Bürogebäude +5,7 %; gewerbliche Betriebsgebäude +5,5 %; Straßenbau +6,9 %. „Alle Preisangaben beziehen sich auf Bauleistungen am Bauwerk einschließlich Mehrwertsteuer.“ — [PM 360](https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_360_61261.html)
- PM 241 (10.7.2026, als KORREKTUR geführt), Mai 2026 gegenüber Mai 2025: Wohngebäude +5,0 % (gegenüber Feb 2026 +2,4 %); Rohbau +4,9 %; Beton +3,6 %; Mauer +3,8 %; Dachdeckung und Zimmerer je +7,3 %; Erdarbeiten +5,4 %; Ausbau +5,1 %; Heizanlagen +5,0 %; Metallbau +4,4 %; Elektro +6,4 %; WDVS +5,0 %; Instandhaltung +5,6 %; Büro +5,2 %; Betriebsgebäude +5,0 %; Straßenbau +6,2 % — [PM 241](https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/07/PD26_241_61261.html)
- Februar 2026: Wohngebäude +3,3 % zum Vorjahresmonat (Überschrift der PM vom 10.4.2026) — [Destatis Themenseite](https://www.destatis.de/DE/Themen/Wirtschaft/Preise/Baupreise-Immobilienpreisindex/_inhalt.html)
- Wohngebäude-Baupreise 2010–2025: +89 %; Verbraucherpreise im gleichen Zeitraum +38 % — [Destatis Themenseite](https://www.destatis.de/DE/Themen/Wirtschaft/Preise/Baupreise-Immobilienpreisindex/_inhalt.html)
- Detaillierte Reihen stehen in GENESIS-Online, Tabellen 61261-0001 bis 61261-0012 (u. a. 61261-0003 Ingenieurbau/Tiefbau, 61261-0005 Instandhaltung nach Gewerken) — [PM 360](https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_360_61261.html)

### Inferenzen
- Grobe Rückrechnung aus den Raten (nicht amtlich): Bürogebäude und Betriebsgebäude liegen in der Größenordnung des Wohngebäudeindex. Exakte Stände muss man in GENESIS 61261-0002 nachschlagen.
- Für das Fortschreiben der MV-Preise von 2025 auf 2026 passt der Straßenbauindex: Mittel 2025 nach den vier Quartalswerten ≈ (137,8+139,2+139,7+140,3)/4 ≈ 139,3, gegenüber 149,3 im August 2026, also ca. +7 %. Das ist eine Inferenz; wichtig ist, dass der Index brutto ist, die MV-Preise aber netto. Für Relativvergleiche spielt das keine Rolle.

### Lücken
- **Indexstände** für Ausbau, Instandhaltung, Bürogebäude, gewerbliche Betriebsgebäude, Brücken und alle Gewerke (Metallbau, Maler, Fliesen, Estrich, Heizung, Elektro/Beleuchtung) für Aug 2026/2025/2024/2022/2021 konnte ich **nicht lesen**. Sie stehen nur in GENESIS-Online (genesis.destatis.de bzw. GENESIS-API). Der Zugriff darauf wurde in dieser Umgebung nicht freigegeben; ein API-Login habe ich nicht verwendet. Die Destatis-Pressemitteilungen enthalten nur Raten, keine Indexstände.
- Raten für Maler-, Fliesen- und Estricharbeiten sowie für Brücken werden in den PMs 2026 nicht genannt.
- Eine Pressemitteilung für November 2026 gibt es noch nicht (Stand 15.11.2026; die PM zum Berichtsmonat November erscheint voraussichtlich im Januar 2027).
- haufe.de habe ich nicht gebraucht, weil die Primärquelle verfügbar war.
