# Fortgeschrittener Anki-Karteikarten-Generator (TestDaF)

Dieser Prompt erstellt hochwertige, akademische Vokabel-Karteikarten in einem Format, das für den direkten Import in Anki bereit ist. Er ist speziell für Lernende zugeschnitten, die sich auf die TestDaF-Prüfung vorbereiten.

---

## ✨ Hauptmerkmale

-   **100% Anki-kompatibel:** Verwendet das TAB-Trennzeichen und eine 3-Feld-Struktur für einen nahtlosen Import.
-   **Zweistufige Erklärungen:** Bietet sowohl eine einfache Alltagsanalogie (A1-Niveau) für das intuitive Verständnis als auch eine akademische Standarddefinition (B2/C1-Niveau) für die Tiefe.
-   **Intelligente Handhabung von Nomen-Verb-Verbindungen:** Analysiert Phrasen, um intelligent zu entscheiden, ob eine einzelne Karte für die gesamte Phrase oder separate Karten für ihre Bestandteile erstellt werden sollen.
-   **Umfassendes, automatisches Tagging:** Fügt automatisch Tags für das GER-Niveau, die thematische Kategorie, die Wortart und mehr hinzu, um dein Anki-Deck organisiert und durchsuchbar zu machen.
-   **Statistische Analyse:** Erstellt einen Abschlussbericht über die verarbeiteten Wörter, um die eigene Arbeit zu überprüfen und die Genauigkeit sicherzustellen.
-   **Keine Redundanz:** Garantiert, dass keine doppelten Wörter oder geringfügige grammatikalische Varianten in der finalen Ausgabe erscheinen.

---

## 🚀 Anwendung

1.  **Prompt kopieren:** Kopiere den gesamten Prompt-Text aus dem untenstehenden Code-Block.
2.  **Wörter hinzufügen:** Füge deine Liste mit deutschen Vokabeln ganz am Ende ein, wo `[Hier stehen die Wörter]` steht.
3.  **Generieren:** Füge den vollständigen Text (Prompt + deine Wörter) in ein KI-Modell wie GPT-4 ein.
4.  **Ausgabe kopieren:** Die KI generiert die Karteikartendaten in einem oder mehreren Code-Snippets. Kopiere den Inhalt dieser Snippets.
5.  **In Anki importieren:**
    -   Öffne einen Texteditor (z.B. Notepad, VS Code oder TextEdit) und füge die kopierten Daten ein.
    -   Speichere die Datei als `.txt`-Datei (z.B. `testdaf_vokabeln.txt`).
    -   Gehe in Anki zu `Datei > Importieren` und wähle deine `.txt`-Datei aus.
    -   Stelle sicher, dass die Feldzuordnung korrekt ist und dass "Felder getrennt durch: Tabulator" ausgewählt ist.
    -   Importieren!

---

## 📋 Der Prompt

```prompt
AUFGABE: Erstelle akademische Vokabeln im Format für Anki-Karten (3-Feld-Format), die den Anforderungen des TestDaF und der universitären Sprachkompetenz (Uni Sicher) entsprechen.

WICHTIGSTE REGELN (für Anki Import):

1. Format: Die gesamte Ausgabe muss als einfacher Text (Plain Text) erfolgen.
2. Code-Snippet: Jede Kategorie muss in einem eigenen Code-Snippet erscheinen, um leicht kopierbar zu sein.
3. Trenner: Verwende echte Tabulator-Zeichen (TAB) als Feldtrenner.
4. Inhalt: Jede Zeile ist eine eigenständige Anki-Karte und endet mit einem Zeilenumbruch (Enter).
5. KRITISCH FÜR REDUNDANZ: Jede Vokabel darf NUR EIN EINZIGES MAL im gesamten Output erscheinen. 
   - Führe ein PREPROCESSING durch und entferne alle Duplikate sowie grammatikalischen Varianten aus der Eingabeliste. Wähle in solchen Fällen die relevanteste oder geläufigste Form (z.B. den Infinitiv eines Verbs).
   - Verarbeite ausschließlich die bereinigte Liste einzigartiger Wörter.
6. REGEL ZUR GENERALISIERUNG: Definiere jedes Wort in seiner allgemeinsten akademischen Bedeutung, unabhängig vom Kontext der anderen Wörter in der Eingabeliste. Die Definition sollte in möglichst vielen Fachbereichen anwendbar sein. Vermeide eine übermäßig spezialisierte Definition, es sei denn, das Wort hat von Natur aus nur eine sehr spezifische Bedeutung.
7. SONDERREGEL FÜR NOMEN-VERB-VERBINDUNGEN (NVV): Wenn ein NVV (z.B. "eine Frage stellen") in der Eingabeliste steht, führe folgende Analyse durch:
   a. Prüfung auf Idiomatizität: Hat die Phrase eine eigenständige, übertragene Bedeutung, die sich nicht direkt aus den Einzelteilen ergibt (typisches Funktionsverbgefüge)?
   b. Fall 1 (Idiomatisch/Feste Wendung): Wenn ja, ODER wenn es sich um eine extrem häufige akademische Kollokation handelt, erstelle EINE EINZIGE Anki-Karte für die gesamte Phrase.
   c. Fall 2 (Wörtliche Bedeutung): Wenn die Bedeutung wörtlich ist, erstelle KEINE Karte für die Phrase. Stattdessen, erstelle zwei separate Karten: eine für das Nomen (mit Artikel/Plural) und eine für das Verb (im Infinitiv), sofern diese nicht bereits als separate Einträge in der bereinigten Liste vorhanden sind.

Vokabelkarten-Struktur (3-Feld-Format):

[Feld 1]	[Feld 2]	[Feld 3]

Feld 1 (Frontseite):
- Nur das deutsche Wort oder Redemittel. (Alle Nomen mit Artikel/Plural, Verben mit fester Präposition).

Feld 2 (Rückseite):
- Die Rückseite muss zwei Hauptteile haben, die ausschließlich durch ein einziges HTML-Tag <br> voneinander getrennt sind.
  1. Teil 1 (Analogie für Anfänger): STRENGE REGEL: Erkläre das Konzept durch eine einfache Analogie auf maximal A1-Niveau aus dem Alltag. Stelle dir vor, du sprichst mit jemandem, der fast kein Deutsch kann. Verwende KEINE abstrakten Begriffe. Der Unterschied in der Einfachheit zu Teil 2 muss extrem deutlich sein. Es geht nicht um eine Definition, sondern um ein Bild. Beispiel: Für "Veröffentlichung" -> "Das ist wie wenn ein Bäcker seinen Kuchen fertig backt und ihn allen Leuten zeigt."
  2. Teil 2 (Standard-Erklärung & mehr): Eine präzise Standard-Definition (A2–B2). Unmittelbar danach, füge optional (falls passend) ein relevantes Synonym (Syn.:) und/oder Antonym (Ant.:) hinzu. Schließe diesen Teil IMMER mit einem realistischen Beispielsatz ab.

Feld 3 (Tags):
- Füge alle relevanten Tags mit Leerzeichen getrennt hinzu.
  - Haupt-Tag (KRITISCH): Wähle einen oder mehrere passende Haupt-Tags aus der Liste (Studium, Wissen, Umwelt, Gesellschaft, Argument, Kommunikation). *Wenn das Wort thematisch zu mehreren Bereichen passt, füge bitte alle relevanten Haupt-Tags hinzu.* 
  - Wortart-Tag: Unbedingt hinzufügen (z.B. Nomen, Verb, Adjektiv, Redemittel).
  - Form-Tag: Nur wenn zutreffend (z.B. NomenVerb, Praeposition, Konnektor).
  - LEVEL-TAG: Füge den CEFR-Sprachniveau-Tag hinzu (z.B. B2, C1).
  - Subtags: PFLICHT – Füge für jede Karte mindestens einen Subtag hinzu (z. B. UniLeben, Forschung, Logik, Klima).

KATEGORISIERUNG (6 Hauptkategorien):

WICHTIG – Platzierung: Jede Vokabelkarte wird NUR EINMAL in dem einen Code-Snippet platziert, das am besten zu ihrer primären Bedeutung passt.  
Der Tag dieses Snippets muss als erster Tag im Feld 3 erscheinen.

1. Studium & Hochschule → Primär-Tag: Studium  
2. Wissenschaft & Forschung → Primär-Tag: Wissen  
3. Umwelt & Nachhaltigkeit → Primär-Tag: Umwelt  
4. Gesellschaft & Wirtschaft → Primär-Tag: Gesellschaft  
5. Argumentation & Textstruktur → Primär-Tag: Argument  
6. Kommunikation & Interaktion → Primär-Tag: Kommunikation  

---

SCHLUSSANALYSE UND STATISTIK:

Nach allen Code-Snippets erstelle eine einzige zusammenfassende Tabelle über die bereinigte Wortliste.  
Die gesamte Statistik bezieht sich ausschließlich auf die bereinigte Liste, nicht auf die ursprünglichen Eingabewörter.

1.  Gesamtanzahl der verarbeiteten Vokabeln:  
    → Nur die eindeutigen, bereinigten Einträge als reine Zahl, z.B. 71

2.  Verteilung nach Haupt-Kategorie (Platzierung):  
    → Anzahl der Karten, die physisch in jedem Code-Snippet platziert wurden, als Prozentsätze bezogen auf die Gesamtanzahl. Summe = genau 100%

3.  Verteilung nach Wortart:  
    → Ebenfalls in Prozent, Summe = 100%

4.  Verteilung nach CEFR-Niveau:  
    → In Prozent, Summe = 100%

5.  Durchschnittliches CEFR-Niveau:  
    → z. B. ≈ B2; berechnet aus der Verteilung

---

CHECKLISTE VOR DEM OUTPUT (MUSS von dir beachtet werden):
- [ ] Hast du alle Duplikate entfernt (auch Wortformen wie Nomen+Verb)?
- [ ] Erscheint jede Karte nur einmal und in nur einem Snippet?
- [ ] Stimmen die Prozentsummen in ALLEN Statistik-Tabellen (Kategorie/Wortart/CEFR)? Alle = 100%
- [ ] Passt die Anzahl der generierten Karten genau zur bereinigten Liste?

---

ZU VERARBEITENDE WÖRTER:

[Hier stehen die Wörter]
```
