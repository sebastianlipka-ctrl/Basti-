# Amtliche Baupreis-Dokumentationen deutscher Straßenbauverwaltungen (außer M-V 2024/2025)

> Stand der Recherche: 15.11.2026. Ziel war, Quellen wie die „Preisdokumentation“ der Straßenbauverwaltung M-V (Mittel der 5 günstigsten Bieter je STLK-Position) für alle anderen Länder, Bund, WSV und Kommunen zu finden und alle Positionen zu extrahieren.
> **Wichtige Einschränkung:** Diese Sitzung lässt nur wenige Hosts zu (Allowlist). Mit curl erreichbar waren nur **www.strassen-mv.de**, www.destatis.de, www-genesis.destatis.de, www.sirados.de, www.bki.de und www.gesetze-bayern.de. **Alle Websites der übrigen Straßenbauverwaltungen sowie web.archive.org waren gesperrt** (Proxy: „CONNECT tunnel failed, response 403“; WebFetch: „getaddrinfo ENOTFOUND“). Es wurde nichts umgangen. Aussagen zu anderen Ländern beruhen deshalb nur auf Suchergebnis-Snippets, die PDFs selbst wurden nicht geöffnet.

## Welche frei herunterladbaren amtlichen Einheitspreis-Dokumentationen gibt es, und welche ließen sich extrahieren?

### Takeaway
Die einzige gefundene und extrahierte amtliche Einheitspreis-Dokumentation nach dem M-V-Muster sind **ältere M-V-Jahrgänge 2021 und 2022**. Sie liegen noch auf strassen-mv.de, sind aber nicht mehr auf der Downloadseite verlinkt. Daraus stammen **5.941 Positionen** in `amtliche_preise_weitere.csv`. Für andere Länder fand sich keine vergleichbare öffentliche Preisdokumentation. Laut Bundesrechnungshof hatten die meisten Auftragsverwaltungen gar keine Preisdatenbank.

### Cited Findings

**Quelle 1: Preisdokumentation M-V, Alt-Jahrgänge 2021 und 2022 (extrahiert)**
- Herausgeber: Landesamt für Straßenbau und Verkehr Mecklenburg-Vorpommern, Rostock. Es gibt 3 Preislisten je Jahr (Straßenbau, Straßen-Brückenbau, Landschaftsbau). Auswertezeitraum ist jeweils der 01.01. bis 31.12. Die PDFs für 2021 wurden am 28.06.2022 erstellt, die für 2022 am 12.06.2023 — [SB 2021](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202021.pdf), [SB 2022](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202022.pdf)
- Methode laut Vorwort 2022: Bei Wechsel in die Auftragsphase wird je OZ das arithmetische Mittel der Einheitspreise der 5 billigsten Bieter gebildet. Bedingungen: mindestens 3 Bieter, nur STL-Positionen (auch Pauschal und teilfreie Textergänzungen), keine Freitextpositionen, Ausreißertest nach GRUBBS, Programmsystem iTWO. Die Listen weisen AM und GM (MEP/MEPi) je Position aus — [SB 2022](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202022.pdf)
- Dateien und Umfang (Seiten / extrahierte Positionen):
  - Straßenbau 2021: 455 S. / 2.222
  - Straßenbau 2022: 455 S. / 2.395
  - Brückenbau 2021: 101 S. / 531 — [BB 2021](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202021.pdf)
  - Brückenbau 2022: 35 S. / 155 — [BB 2022](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Br%C3%BCckenbau%202022.pdf)
  - Landschaftsbau 2021: 113 S. / 404 — [LB 2021](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Landschaftsbau%202021.pdf)
  - Landschaftsbau 2022: 59 S. / 234 — [LB 2022](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Landschaftsbau%202022.pdf)
  - **Summe: 5.941 Positionen**
- Stichprobe: STLK 18.101 107 21 „Baustelle einrichten, Dies. LV-Abschn., Zufahrt vorh.“ 2022 = 10.441,35 € Psch (AM = GM, 1 Vergabe), so in PDF und CSV — [SB 2022](https://www.strassen-mv.de/static/LSBV/Dateien/Downloads/Preisdokumentation/Preisdokumentation%20MV%20Stra%C3%9Fenbau%202022.pdf)
- In der CSV steht in `preis_eur` der AM (MEP/MEPi). GM, STLK-Nr., Anzahl der Vergabe-Einträge und Listenseite stehen in `leistung`. Ob die Preise netto oder brutto sind, sagt die Quelle nicht ausdrücklich. Wie beim bestehenden M-V-Datensatz ist die Spalte als „netto (Inferenz)“ markiert.
- Für 2023 sowie 2015–2020 wurden verschiedene Dateinamen-Varianten auf strassen-mv.de geprüft. Alle ergaben HTTP 404, das Verzeichnis-Listing ergab 403. Ein **Jahrgang 2023 ist auf dem Server nicht auffindbar** — eigene Prüfung per curl
- Seriosität: hoch (amtliche Primärquelle, dokumentierte Methode). Einschränkungen: Bei n=1–2 Vergaben sind die Werte wenig belastbar. Bei rund 315 Positionen mit langen Freitext-Ergänzungen konnte die Einheit nicht ausgelesen werden (Eintrag „k.A. (siehe PDF)“).

**Ältere M-V-Jahrgänge, nur über Drittseiten auffindbar (gesperrt, nicht extrahiert)**
- Brückenbau 2015 auf tragwerk-und-statik.de; Ausgaben 2015–2018 („Preisliste Straßen-Brückenbau“, u. a. 2018) auf docplayer.org — [tragwerk-und-statik.de](https://tragwerk-und-statik.de/dokument/Preisdokumentation_Mecklenburg-Vorpommern_Brueckenbau_2015-1_1559939745_6029.pdf), [docplayer 130435524](https://docplayer.org/130435524-preisdokumentation-mecklenburg-vorpommern-preisliste-strassen-brueckenbau-in-euro.html), [docplayer 41339610](http://docplayer.org/41339610-preisdokumentation-mecklenburg-vorpommern-preisliste-strassen-brueckenbau-in-euro.html), [docplayer 167819029](https://docplayer.org/167819029-preisdokumentation-mecklenburg-vorpommern-preisliste-strassen-brueckenbau-in-euro.html)
- web.archive.org war gesperrt, Archivfassungen der M-V-Downloadseite ließen sich deshalb nicht prüfen.

**Bundesrechnungshof (Kontext, warum es kaum Vergleichbares gibt)**
- Laut Gutachten des Bundesbeauftragten für Wirtschaftlichkeit „Kostenmanagement im Bundesfernstraßenbau“ hatten die meisten Auftragsverwaltungen der Länder keine Preisdatenbanken für einzelne Gewerke und Positionen. Empfohlen wurden regionale Preisdatenbanken auf Basis abgeschlossener Vergaben (Inhalt laut Snippet, PDF nicht geöffnet, Host gesperrt) — [Bundesrechnungshof](https://www.bundesrechnungshof.de/SharedDocs/Downloads/DE/Berichte/BWV-Veroeffentlichung/kostenmanagement-im-bundesfernstrassenbau-volltext.pdf?__blob=publicationFile&v=1)

**Prüfergebnis je Verwaltung (nur Websuche, Hosts gesperrt)**
- Brandenburg (LS): Keine Preisdokumentation gefunden. Im Netz stehen Geschäftsberichte 2008–2024, Produktlisten natürlicher Baustoffe und ein Leistungs- und Entgeltverzeichnis der Ausbildungsstätte, aber keine EP-Listen. Über die Vergabeplattform sind einzelne Kurztext-/Preis-Verzeichnisse von Projekten auffindbar (Einzel-LV, keine Statistik) — [LS Geschäftsbericht 2024](https://www.ls.brandenburg.de/sixcms/media.php/9/2026-04-29_broschur_ls_gesch%C3%A4ftsbericht-2024.pdf), [LS-Vergabeplattform](https://www.ausschreibungen.ls.brandenburg.de/NetServer//TenderingProcedureDetails?function=_DownloadTenderDocument&documentOID=54321-SpecificationVersion-16054078cfb-c6f389d334349f9&Document=S1BWX0gyLnBkZg)
- Sachsen (LASuV): Nichts gefunden. SIB Sachsen (Hochbau) hat nur eine Prüfanlage zur Angemessenheit von EP, ohne Preise — [SIB](https://www.sib.sachsen.de/download/Anlage_zur_techn_u_wirtschaftl_Pruefung_und_zur_Pruefung_der_Angemessenheit_der_Einheitspreise_Stand_2023-02.pdf)
- Sachsen-Anhalt (LSBB): Nichts gefunden. Es gibt nur ZTV-StB LSBB ST 21 und Arbeitshilfen — [LSBB ZTV](https://lsbb.sachsen-anhalt.de/fileadmin/Bibliothek/Politik_und_Verwaltung/Landesbetriebe/LSBB/Service/Bautechnik_Info/ZTV-StB_LSBB_ST_21/ZTV-StB_LSBB_ST_21_Gesamtausgabe.pdf)
- Thüringen (TLBV): Nichts gefunden. Das Faltblatt „Bauleistungspreise in Thüringen“ des TLS (Ausgaben 2024–2026) enthält nur Preisindizes, keine €-Einheitspreise — [TLS 2026](https://statistik.thueringen.de/webshop/pdf/2026/80129_2026_00.pdf)
- Schleswig-Holstein (LBV.SH): Nichts gefunden. Es gibt nur Rundverfügungen, z. B. zur Stoffpreisgleitklausel (2022) — [aik-sh.de](https://www.aik-sh.de/wp-content/uploads/2023/08/II_2.10-059-RdVfG_15.09.2022_-Stoffpreisgleitklausel-Verlaengerung.pdf)
- Niedersachsen (NLStBV): Nichts gefunden. TED-Bekanntmachungen nennen nur die Prüfung auffälliger EP (Urkalkulation).
- Hessen Mobil: Nichts gefunden. Es gibt Handbücher (Ingenieurbau, Versorgungsleitungen) ohne Kostentabellen — [Handbuch Ingenieurbau](https://mobil.hessen.de/sites/mobil.hessen.de/files/2026-06/handbuch_ingenieurbau_1.3.1.pdf)
- NRW (Straßen.NRW): Nichts gefunden. Im Haushalt steht die Kennzahl „Kosten Bau Straßen / 1 Mio Bauvolumen“ ohne Werte. IT.NRW veröffentlicht nur Indizes — [Landtag NRW Haushalt](https://www.landtag.nrw.de/web/WWW/haushalt/cd-fm-0316/daten/pdf/2015/hh09/kap150W.pdf)
- Rheinland-Pfalz (LBM): Nichts gefunden. Es gibt nur STLK-Einführungsrundschreiben und Berichte des Rechnungshofs RLP zur Straßenerhaltung (2024) — [RH RLP 2024](https://rechnungshof.rlp.de/fileadmin/rechnungshof/Jahresberichte/2024/Jahresbericht_2024_Nr._09_Erhaltung_des_Landesstrassennetzes.pdf)
- Saarland (LfS): Nichts gefunden. Die LfS-Website hat die Rubrik „Vergebene Aufträge“ (Auftragsbekanntmachungen, keine EP) — [LfS](https://www.saarland.de/landesbetrieb_strassenbau.htm)
- Baden-Württemberg: Nichts gefunden. Das Statistische Landesamt BW veröffentlicht nur den Baupreisindex.
- Bayern: Keine EP-Datenbank gefunden. Die AKVS 2014 (Methodik) und der Leitfaden „Kostenbewusstes Planen und Bauen“ 2021 enthalten nach Snippets keine EP-Listen. „sub_2018.pdf“ ist die Broschüre „Straßen und Brücken in Bayern“, keine Submissionsstatistik — [AKVS 2014](https://www.gesetze-bayern.de/Content/Document/BayVV_912_I_1198/true), [sub_2018](https://www.bauministerium.bayern.de/assets/stmi/vum/strasse/sub_2018.pdf)
- Berlin: Es gibt eine Rundschreiben-Reihe „Projektvorbereitung und -prüfung Tiefbau, Richtwerte und Standards“ (aktuell SenStadt VI MH Nr. 01/2026, Anlage z. B. rsvibc_012011_anl1.pdf). Ob darin €-Kostenkennwerte stehen, ist **unbestätigt** (berlin.de gesperrt) — [Berlin Richtwerte Tiefbau](https://www.berlin.de/sen/sbw/service/rundschreiben/projekte-tiefbau-richtwerte-und-standards/), [Anlage 2011](https://berlin.de/sen/sbw/_assets/service/rundschreiben/projekte-tiefbau/rsvibc_012011_anl1.pdf)
- Hamburg (LSBG): Nichts gefunden. Im Transparenzportal liegen geschwärzte Unterlagen zu Einzelverträgen.
- Bremen (ASV): Nichts gefunden. Es gibt Vorgaben für Aufgrabungen (2020), eine „Dauerausschreibung“ und die AKVS-Fassung 2015 auf finanzen.bremen.de — [ASV Aufgrabungen](https://www.asv.bremen.de/sixcms/media.php/13/2020-09-11%20Vorgaben%20bei%20Aufgrabungen%20in%20Verkehrsfl%C3%A4chen%20der%20Freien%20Hansestadt.pdf), [ASV Dauerausschreibung](https://www.asv.bremen.de/sixcms/media.php/13/Dauerausschreibung.pdf)
- Autobahn GmbH / DEGES / BASt: Keine öffentliche EP-Liste gefunden. Das ARS 29/2020 nennt eine neue AKVS-Fassung im Zusammenhang mit der Autobahn GmbH (Methodik). BASt-Berichte stehen frei im ELBA-Archiv (bast.opus.hbz-nrw.de, gesperrt), ein EP-Katalog war nicht auffindbar — [BMV ARS 29/2020](https://www.bmv.de/SharedDocs/DE/Artikel/StB/allgemeines-rundschreiben-strassenbau-29-2020-vom-23-12-2020.html)
- WSV/BAW: Keine Preisdatenbank oder Kostenkennwerte gefunden.
- Kommunen: Keine EP-Statistiken gefunden. Treffer: Waldshut-Tiengen „Aufgrabungen in Verkehrsflächen – Oberfläche Asphalt“ (vermutlich Wiederherstellungssätze, nicht geprüft) sowie Aufbruchrichtlinien von Frankfurt (2015) und Nauen (ohne Preise laut Snippet) — [Waldshut-Tiengen](https://www.waldshut-tiengen.de/fileadmin/Dateien/Neue_Dateien/Stadtentwicklung/Tiefbauamt-Eigenbetrieb_Abwasser/Aufgrabungen_in_Verkehrsflaechen-_Oberflaeche_Asphalt.pdf), [Frankfurt](https://frankfurt.de/-/media/frankfurtde/service-und-rathaus/verwaltung/aemter-und-institutionen/amt-fuer-strassenbau-und-erschliessung/pdf/aufbruchrichtlinie_stand_2015.pdf)

### Inferences
- M-V ist offenbar die einzige Straßenbauverwaltung, die ihre iTWO-Preisdatenbank als Jahresliste veröffentlicht. Der Bundesrechnungshof-Befund (keine Preisdatenbanken in den meisten Ländern) passt dazu.
- Ältere M-V-Dateien bleiben auf dem Server, auch wenn sie nicht mehr verlinkt sind. 2023 fehlt vermutlich, weil es dort unter einem anderen Namen liegt oder gelöscht wurde.
- Wegen der gesperrten Hosts ist „nichts gefunden“ für die anderen Länder ein Ergebnis der Websuche, keine geprüfte Abwesenheit.

### Gaps
- M-V 2023 sowie 2015–2020 nicht extrahiert (2023 nicht gefunden; 2015–2018 nur auf gesperrten Drittseiten; web.archive.org gesperrt).
- Inhalt der Berliner Tiefbau-Richtwerte, der Waldshut-Tiengen-Liste und des Bundesrechnungshof-Gutachtens nicht geprüft (Hosts gesperrt).

## Gesperrte Hosts und nicht frei zugängliche Quellen

### Takeaway
Fast alle relevanten Hosts waren gesperrt. Kommerzielle oder interne Preisdatenbanken existieren zwar, sind aber nicht frei zugänglich.

### Cited Findings
- **Gesperrte Hosts** (curl: „CONNECT tunnel failed, response 403“, bzw. WebFetch: ENOTFOUND), exakt so getestet:
  - web.archive.org, archive.org
  - ls.brandenburg.de, www.ls.brandenburg.de (über Links), www.ausschreibungen.ls.brandenburg.de, bravors.brandenburg.de
  - www.lasuv.sachsen.de, www.sib.sachsen.de, www.statistik.sachsen.de
  - lsbb.sachsen-anhalt.de, izg.sachsen-anhalt.de, statistik.sachsen-anhalt.de
  - bau.thueringen.de, statistik.thueringen.de, www.friedrichroda.info
  - www.schleswig-holstein.de, www.aik-sh.de
  - www.strassenbau.niedersachsen.de
  - mobil.hessen.de
  - www.strassen.nrw.de, e-pflicht.ub.uni-duesseldorf.de
  - lbm.rlp.de, www.lbm.rlp.de, rechnungshof.rlp.de
  - www.lfs.saarland.de
  - www.svv-bw.de, www.statistik-bw.de, bauwirtschaft-bw.de
  - www.baysis.bayern.de, www.stmb.bayern.de, www.bauministerium.bayern.de, www.verkehrsministerium.bayern.de, mobilitaet.bayern.de, www.verkuendung-bayern.de
  - www.berlin.de, www.stadtentwicklung.berlin.de, www.statistik-berlin-brandenburg.de
  - www.hamburg.de, lsbg.hamburg.de
  - www.bauumwelt.bremen.de, www.finanzen.bremen.de
  - www.autobahn.de, www.bast.de, bast.opus.hbz-nrw.de, opus4.hbz-nrw.de, www.deges.de
  - www.gdws.wsv.bund.de, www.wsv.de, www.baw.de, izw.baw.de
  - www.bmv.de, www.bmdv.bund.de, www.bbr.bund.de, www.bbsr.bund.de, www.bundesrechnungshof.de, dserver.bundestag.de
  - www.landtag-mv.de, www.regierung-mv.de, www.laiv-mv.de
  - tragwerk-und-statik.de, docplayer.org
  - www.statistischebibliothek.de, ted.europa.eu, www.evergabe.de, www.dtvp.de, www.evergabe-online.de, www.subreport.de
  - www.waldshut-tiengen.de, frankfurt.de, www.nauen.de, www.wien.gv.at, www.muenchen.de, www.stadt-koeln.de, www.leipzig.de, www.dresden.de, www1.muelheim-ruhr.de
  - www-ecm-pu.deutschebahn.com, www.dbu.de, fib-bund.de, www.stlb-bau.de, www.fgsv-verlag.de, www.bauindustrie.de, vergabeblog.de, kleineanfragen.de, media.frag-den-staat.de, fragdenstaat.de, www.bundesanzeiger.de, www.forschungsinformationssystem.de, elib.bast.de, www.baupreise.de, www.bau.de, www.google.com, duckduckgo.com
- **Erreichbar:** www.strassen-mv.de, www.destatis.de, www-genesis.destatis.de, www.sirados.de, www.bki.de, www.gesetze-bayern.de.
- **Existierende, aber nicht frei zugängliche Quellen:**
  - Interne iTWO- bzw. Preisdatenbanken der Straßenbauverwaltungen. Die meisten Länder hatten laut Bundesrechnungshof keine, und die vorhandenen werden nicht veröffentlicht — [Bundesrechnungshof](https://www.bundesrechnungshof.de/SharedDocs/Downloads/DE/Berichte/BWV-Veroeffentlichung/kostenmanagement-im-bundesfernstrassenbau-volltext.pdf?__blob=publicationFile&v=1)
  - DB StaKoPläne (Deutsche Bahn): Standard-Kostenpläne mit EP aus abgerechneten Projekten in iTWO. Sie sind intern, öffentlich ist nur eine Bedienungsanleitung — [DB](https://www-ecm-pu.deutschebahn.com/resource/blob/9560702/9d7894e512ff7fcee6541a77e66c515d/20220126-Bedienungsanleitung-StaKoPla-ne-BK-in-iTWO_V2-0-data.pdf)
  - Kommerziell: DBD-VergabepreisSpeicher und phase0-Preisdatenbank — [DBD](https://www.dbd-center.de/vergabepreisspeicher), [phase0](https://www.phase0.com/preisdatenbank)
  - Tirol (AT, nicht DE): Interne Preisdatenbank der Landesstraßenverwaltung mit den EP der Bestbieter, beschrieben im Bericht des Landesrechnungshofs — [LRH Tirol](https://www.tirol.gv.at/fileadmin/landtag/landesrechnungshof/downloads/berichte/Bauliche_Erhaltung_von_Landesstrassen.pdf)

### Inferences
- Mehr Daten wären am ehesten zu bekommen, wenn web.archive.org, docplayer.org und tragwerk-und-statik.de (M-V 2015–2018) sowie www.berlin.de (Tiefbau-Richtwerte) in den Netzwerkeinstellungen freigeschaltet würden.

### Gaps
- Für keine andere Landesverwaltung ließ sich direkt auf der Website prüfen, ob es nicht verlinkte Preislisten gibt.
