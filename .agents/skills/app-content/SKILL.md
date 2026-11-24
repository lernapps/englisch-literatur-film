---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

„Literatur und Film untersuchen“: Explainer (Einheiten-App `subject: englisch`, Format 2, Sprache Deutsch, englische Texte) für Stufe 9-10. Ein Analyse-Werkzeugkasten (toolkit) aus Werkzeugkarten trägt die App: Kapitel 1 führt narrator, character, setting und plot ein, Kapitel 2 erweitert ihn um Stilmittel, Strophe und Reimschema, Regieanweisung und Kameraeinstellung. Auftrag: Issue lernapps/apps#483 (Epic lernapps/apps#489, Konventionen dort, Abschnitt 8 Höhere Stufen). Die erste Version hat nur Stufe 9-10.

## Curriculum

Englisch als erste Fremdsprache, Klasse 9-10 (Stufe 9-10 der Karte). Kein Lehrplan: Reihenfolge und Bausteine kommen aus der Lernlandkarte `https://lernapps.net/apps/map/englisch.json` (Fokus `competency`; Einheiten-App über die Stränge `texte` und `wortschatz`). Vorwissen aus anderen Explainern (Wiederholungsseiten): `figuren-ort-handlung`, `zusammenfassung`, `gedichte-reime`, `dialog-schreiben` (#479), `personen-orte-beschreiben` (#477), `simple-present` (#472). Nicht hier: Zeitformen selbst (#472), Zeitungstexte (#486), Werbung und Meinung (#487), Erörterung.

## Competencies

Alle neun sind Lücken der Karte, Band 9-10. Eine Seite je Baustein, Reihenfolge nach `requires`; die Id steht in `competencies:` der Seite, die Ich-kann-Sätze sind die der Karte (nicht umformulieren).

1. Kapitel `kurzgeschichten` („Kurzgeschichten untersuchen“)
   - Wiederholung `recap: [englisch/figuren-ort-handlung, englisch/zusammenfassung, englisch/simple-present, englisch/personen-orte-beschreiben]` → `kurzgeschichten/das-brauchst-du`
   - `text-fachbegriffe` → `kurzgeschichten/text-fachbegriffe` (Musterseite): „Ich kann Fachbegriffe zum Sprechen über Texte verwenden, zum Beispiel narrator, character, setting, plot und stanza.“
   - `kurzgeschichte` → `kurzgeschichten/kurzgeschichte`: „Ich kann typische Merkmale einer Kurzgeschichte nennen und an einem Beispiel zeigen.“
   - `erzaehlperspektive` → `kurzgeschichten/erzaehlperspektive`: „Ich kann Ich-Erzähler und Er/Sie-Erzähler unterscheiden und Autor und Erzähler auseinanderhalten.“
   - `charakterisierung` → `kurzgeschichten/charakterisierung`: „Ich kann eine Figur charakterisieren und meine Aussagen mit Textstellen belegen.“
   - `inhaltsangabe` → `kurzgeschichten/inhaltsangabe`: „Ich kann eine Inhaltsangabe schreiben: mit Einleitungssatz, im present tense, ohne Zitate und ohne eigene Meinung.“
2. Kapitel `gedicht-szene-film` („Gedicht, Szene und Film“)
   - Wiederholung `recap: [englisch/gedichte-reime, englisch/dialog-schreiben]` → `gedicht-szene-film/das-brauchst-du`
   - `stilmittel` → `gedicht-szene-film/stilmittel`: „Ich kann häufige Stilmittel wie Wiederholung, rhetorische Frage, Vergleich und Metapher erkennen und ihre Wirkung beschreiben.“
   - `gedicht-analysieren` → `gedicht-szene-film/gedicht-analysieren`: „Ich kann ein Gedicht oder einen Songtext untersuchen: Strophen, Reimschema, Bilder und Wirkung.“
   - `drama-szene` → `gedicht-szene-film/drama-szene`: „Ich kann eine Dramenszene lesen, Regieanweisungen verstehen und die Szene vorspielen.“
   - `film-analysieren` → `gedicht-szene-film/film-analysieren`: „Ich kann filmische Mittel wie Kameraeinstellung, Schnitt und Musik erkennen und ihre Wirkung beschreiben.“

Übungs-IDs: Präfix = Seite (`fachbegriffe-…`), Diktat `<präfix>-hoeren`, Nachsprechen `<präfix>-nachsprechen`, offene Aufgabe `<präfix>-schreiben`.

## Content structure

- Pfad: `src/<kapitel>/chapter.yaml`, Seiten `src/<kapitel>/<seite>.yaml`, Bilder `src/images/`, Audio `src/audio/`.
- Jede Seite (außer den Wiederholungsseiten) hat die Abschnitts-IDs `einstieg` (Vorwissens-Frage als `single-choice`, „Das kannst du danach“), `lesestueck` (zuerst ein `vocabulary` „Wörter zum Text“ als Randglossar, dann der Text in `text`-Blöcken mit nummerierten Zeilen „**[1]** …“, 300 bis 600 Wörter, Titel neutral), `neu` (Erklärung, Werkzeugkarte, Merke), `uebung` (drei Stufen: Verstehen, Belegen mit Zeile, Meinung; mindestens vier Übungen), `anwenden` (`open-task` mit `points` und `solution`, dazu `speaking-task`) und `weiter` (Eintrag für die Lese- und Sehliste, Ausblick). Titel sagen, was der Abschnitt tut. Die Wiederholungsseiten haben nur Text, keine oder höchstens zwei Übungen.
- Werkzeugkarte = `note` mit Titel „Werkzeugkarte · <Begriff>“ und drei Zeilen: Fachbegriff (englisch, mit deutscher Bedeutung), **Leitfrage** (englisch, ein Satz) und **Satzanfang** (englisch, „The narrator …“). Der Werkzeugkasten wächst: jede Seite legt höchstens ein bis vier neue Karten an; das Wort „Kasten“ meint die Karten bisher.
- Zeilen: ein `text`-Block hat höchstens drei bis fünf nummerierte Zeilen; Belege stehen als `(l. 4)` oder `(ll. 2-5)`. Gedichte und Szenen: jede Verszeile oder Sprechzeile eine Nummer.
- Länge: Erklärtext höchstens 350 Wörter, das Lesestück zählt nicht mit (Konventionen §8); der Hinweis `explainer-text-load` ist bei diesen Seiten bewusst. Höchstens etwa 25 Items und 10 Übungen.
- Fall: Die Lernenden stellen die Lese- und Sehliste für Year 10 zusammen. `weiter` jeder Seite fordert einen Listeneintrag (ein bis zwei Sätze, Satzanfang der Karte, Zeilenangabe); `film-analysieren` fragt nach der Empfehlung mit zwei Gründen. **Keine Figuren-Einführung im Seitentext**, keine erfundenen Kinder, keine Szenenbilder mit Figuren; Sophie kommt nicht vor. Die Figuren der Lesestücke sind Erwachsene.
- Anrede „du“. Texte sachlich, keine Gewalt- und Verstörungsthemen ohne Not.

## Terminology

- Werkzeugkasten (englisch toolkit), Werkzeugkarte, Lesestück, Beleg, Zeile (l.), Listeneintrag. „Ausdruck“ (fester Ausdruck), nie „Wendung“. Fachbegriffe englisch: narrator, character, setting, plot, stanza, rhyme scheme, metaphor, simile, repetition, rhetorical question, stage direction, shot, close-up, camera angle, summary, present tense.
- Karten und Fachbegriffe heißen überall gleich: Karten `narrator`, `character`, `setting`, `plot`; Kapitel 2: `metaphor`, `simile`, `repetition`, `rhetorical question`, `stanza`, `rhyme scheme`, `stage direction`, `shot`, `camera angle`.
- Britisches Englisch (favourite, colour). Englische Aufgaben enthalten kein deutsches Wort; der deutsche Hinweis steht in `source` oder in der Frage.
- Aussprache: keine Lautschrift; die Hörsätze zeigen sie.
- Wörter: Grundwortschatz A1/A2 aus `https://lernapps.net/apps/map/englisch/grundwortschatz/`; Fachwörter und Wörter ab B1 stehen im `vocabulary`-Block der Seite (Kopf: Wort, Bedeutung) und unten unter „Sources“.

## Exercise patterns

Aufbau leicht → schwer, drei Stufen je Seite. Je Übung `mistakes` mit eigener Meldung je typischem Fehler; gleichwertige Antworten als Gruppe `(a|b)` im `target`; `form: { punctuation: ok }`.

- Begriff erkennen: `matching` (Fachbegriff ↔ Textstelle), `single-choice` mit `info` je Option.
- Belegen mit Zeile: `multiple-choice` „In welchen Zeilen steht …?“, `language-task` `mode: gap` für `(l. 4)`, `single-choice` „Welche Zeile belegt …?“.
- Wirkung beschreiben: `language-task` `mode: choice` mit Satzanfang der Werkzeugkarte und Distraktoren, die echte Lernerfehler sind (nacherzählen statt deuten).
- Ordnen: `ordering` für Sätze einer Inhaltsangabe oder Stationen.
- Schreiben: `language-task` `mode: write` mit englischem `cue`.
- Hören und Sprechen: je Seite drei Diktatsätze (`language-task` mit `audio`) und drei Nachsprechsätze (`speaking-task`), neue Sätze, nicht im Lesestück, in Merke, Karte oder Einstieg. Anwenden (`open-task`): immer `points` und eine Musterlösung; die App bewertet den Text nicht.
- Typische Fehler (jeweils `mistakes`): Autor = Erzähler, „I“ ist immer die Autorin, Handlung nacherzählt statt analysiert, Inhaltsangabe im past tense oder mit Zitat und Meinung, Charakterzug ohne Beleg, direkte und indirekte Charakterisierung vertauscht, Metapher mit Vergleich verwechselt, Reimschema nach Schreibung statt Klang, Regieanweisung als Dialog gesprochen, shot und camera angle vertauscht.
- Jede Seite hat eine andere Mischung von Übungsarten (`explainer-page-variety`). Keine Komponenten, keine Datendateien.

## Figures

- Eigene Zeichnungen als SVG in `src/images/`, `CC-BY-4.0`, Quelle `eigene Zeichnung`, Hintergrund #f4efe2, Schrift mindestens 16 im 480er viewBox, Beschriftung innerhalb des `viewBox`. Keine Fotos, keine Figuren aus Büchern, Filmen oder Marken, keine Standbilder. `alt` sagt, was die Zeichnung zeigt, nie die Lösung; Bildunterschrift nennt, was zu sehen ist.
- Geplant: `werkzeugkasten-<seite>.svg` (Kartenreihe, wächst), `story-map-inhaltsangabe.svg` (Farben who #2c6fd8, where #138d75, when #d35400, what #c0392b wie in #479; diese Farben bedeuten nur diese Felder), `gedichtform.svg` (Strophen und Reimbuchstaben), `kameraeinstellungen.svg` (long shot, medium shot, close-up, high angle, low angle als Strichzeichnung). Die SVG-Dateien sind die Quelle, das kleine Zeichenskript liegt im Scratchpad, nicht im Repository.
- Das Bild zeigt nie dieselben Wörter oder Zeilen wie die erste Aufgabe darunter.

## Built (Stand)

Noch nichts gebaut; dieser Abschnitt wird nach jedem Baustein ergänzt (Seiten, Übungs-IDs, Hörsätze).

## Sources

Karte `https://lernapps.net/apps/map/englisch.json` und Baustein-Seiten `https://lernapps.net/apps/map/englisch/c/<id>/`; Grundwortschatz (A1/A2). Fakten (keine Sätze), Wikipedia (CC BY-SA), geöffnet am 2026-11-24: Rhyme scheme, Stanza, Shot (filmmaking), Close-up, Camera angle, Metaphor, Rhetorical question, Narration. Nicht geprüft: Short story (die Abfrage lieferte keinen Text). Alle Lesestücke, Gedichte, Songtexte, Szenen und Filmbeschreibungen sind eigene Texte (CC BY 4.0), alle Zeichnungen eigen; keine fremden Texte, Songtexte, Filmdialoge oder Standbilder. Audio: KI-Stimme `bf_emma` (britisch, weiblich), mit Skill `lernapps-audio` erzeugt und als KI-generiert markiert. Material der Ersteller:in: keines. Prüfskript: `python3 -I .agents/skills/app-content/scripts/pruefen.py` (Hörsätze gegen den Text derselben Seite, Wörter gegen die Liste der Karte; Meldungen zu deutschen Wörtern in englischen Feldern sind Rauschen). Wörter außerhalb des Grundwortschatzes, auf der Seite erklärt: Datei `.agents/skills/app-content/scripts/woerter-erklaert.json`.

## Hörliste (Sätze, die die Ersteller:in gezielt abhört)

Hörsätze bleiben natürlich: kein Name wird nur wegen des Klangs angehängt. `regen_audio.py` schneidet das Ausklingen ab; Sätze, die auf ein einsilbiges Wort enden, stehen hier zum gezielten Abhören. Noch keine.

## Adding a chapter or round

1. Baustein der Karte wählen; die Voraussetzungen müssen auf früheren Seiten stehen oder eine Wiederholungsseite bekommen.
2. Seite `src/<kapitel>/<seite>.yaml` mit den Abschnitten `einstieg`, `lesestueck`, `neu`, `uebung`, `anwenden`, `weiter`, in `chapter.yaml` eintragen, Competency-Id setzen.
3. Lesestück: eigener Text, nummerierte Zeilen, Vokabelblock davor; Werkzeugkarte um das Neue; Zeichnung ergänzen.
4. Übungen aus den Mustern oben, je mit `mistakes` und `hint`; 2 bis 3 davon in `selfAssessment` des Kapitels (Skill `lernapps-explainer-self-assessment`).
5. Hörtexte: `src/audio/<satz>.mp3`, Eintrag in `.agents/skills/app-content/scripts/audio-texte.json` (Datei → Satz), erzeugt mit `~/.cache/lernapps/audio/venv/bin/python .agents/skills/app-content/scripts/regen_audio.py .agents/skills/app-content/scripts/audio-texte.json "<Satz>"`; anhören lassen; einsilbig endende Sätze in die Hörliste.
6. Wörter gegen den Grundwortschatz und Hörsätze gegen die Seite prüfen (`pruefen.py`); `npx --no -- lernapps check`; committen.

## Rules learned from mistakes

Aus den Vorgängern (#470 bis #482) und den Konventionen übernommen:
- Jede Übung fragt nur Wörter ab, die vorher auf der Seite stehen. Eine Tabelle oder Karte, die eine Übung beantwortet, steht nicht direkt über ihr; Karte, Merke, Einstieg und Bild nennen andere Beispielsätze als die Übungen.
- Englische Aufgaben enthalten kein deutsches Wort; gleichwertige Antworten als Gruppe `(a|b)`; `punctuation: ok`; das Feld `accepted` wirkt nicht.
- Als Auswahl nur echte Lernerfehler, keine Unwörter; jeder Distraktor eine eigene Meldung; ein Einstiegs-`single-choice` hat mindestens drei Optionen; Optionstexte enden ohne Punkt.
- Hörsätze: neue Sätze (kein Hörsatz wörtlich oder fast wörtlich auf derselben Seite), Ausklingen abschneiden, keine Namen für den Klang anhängen.
- Ein Doppelpunkt in einem Hinweis, einer Meldung oder einer `explanation` lässt das YAML scheitern: in Anführungszeichen setzen.
- Offene Aufgaben: immer `points` und Musterlösung, mit dem Hinweis, dass die App den Text nicht bewertet.
- Keine Figuren-Einführung im Seitentext, keine erfundenen Kinder (Stufe 9-10); Titel der Lesestücke neutral.
- Bilder: Beschriftungen innerhalb des `viewBox`, `alt` verrät nie die Lösung.
- Ein Lesestück je Seite; Vokabelblock statt Wörter-Tabellen; „Ding“ steht nur für Gegenstände.
