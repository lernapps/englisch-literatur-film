---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: { checks-pass: 1 }
---

# Plan: englisch-literatur-film, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-24. Explore, Plan, Code, Commit.*

## Goal

Lernende ab Klasse 9 untersuchen Kurzgeschichten, ein Gedicht, eine Dramenszene und einen kurzen Film mit Fachbegriffen und belegen ihre Deutung mit Zeilenangaben. Ein Analyse-Werkzeugkasten (toolkit) aus Karten (Fachbegriff, Leitfrage, Satzanfang) trägt die App und wächst Seite für Seite.

## Key decisions

- Archetyp `explainer`, Format 2, Einheiten-App (`subject: englisch`, `explainerFocus: competency`): Seiten mit Lesestück, Erklärung und Übungen; nichts davon ist ein Spiel oder Trainer.
- Auftrag steht in Issue 483 (Orchestrator-Session in der Rolle der Ersteller:in); das ersetzt die Interviewfragen Goal, Learners, Content, Amount.
- Sprache der Seiten Deutsch (`languages: [de]`), englische Texte und Beispiele, britisches Englisch, Anrede du.
- Fall statt Figuren (Stufe 9-10): die Lernenden stellen eine Lese- und Sehliste für Year 10 zusammen und begründen jede Wahl mit dem Werkzeugkasten; keine erfundenen Kinder, keine Szenenbilder mit Figuren, Sophie (15-16) höchstens als einzelne Stimme (guess).
- Alle Lesestücke sind eigene Texte (CC BY 4.0); kein Gutenberg, keine fremden Gedichte, Songtexte, Filmdialoge oder Standbilder. Der Film der Seite 9 ist ein erfundener Kurzfilm, beschrieben als Szenenliste (guess).
- `scope` ja (offene Aufgaben: der Tutor beurteilt nach dem Scope), in `src/app.yaml` mit `out`, auf jeder Seite.
- Zeilenangaben: Lesestücke stehen als Tabelle [Zeile, Text] mit nummerierten Zeilen, damit Belege „(l. 4)“ möglich sind (guess, auf der Musterseite prüfen).

## Notes

**Fach/Strang:** Englisch, Einheiten-App über die Stränge `texte` und `wortschatz`; Stufe 9-10; alle neun Bausteine sind Lücken der Karte (`practisedBy` leer, Stand 2026-11-24 aus `https://lernapps.net/apps/map/englisch.json`).

**Kapitel und Bausteine (Karten-Ids, „Ich kann“ der Karte):**
1. `kurzgeschichten` · Kurzgeschichten untersuchen: `text-fachbegriffe` (Schritt 1, öffnet 5) → `kurzgeschichte` (Schritt 2) → `erzaehlperspektive` (Schritt 3) · `charakterisierung` (Schritt 1) · `inhaltsangabe` (Schritt 1). Recap am Kapitelanfang: `englisch/figuren-ort-handlung`, `englisch/zusammenfassung`, `englisch/simple-present`, `englisch/personen-orte-beschreiben` (story map aus #479, Steckbrief aus #477).
2. `gedicht-szene-film` · Gedicht, Szene und Film: `stilmittel` (Schritt 2) → `gedicht-analysieren` (Schritt 3) · `drama-szene` (Schritt 1) · `film-analysieren` (Schritt 1). Recap: `englisch/gedichte-reime`, `englisch/dialog-schreiben`, `englisch/figuren-ort-handlung`.
Reihenfolge der Seiten in Kapitel 1: text-fachbegriffe, kurzgeschichte, erzaehlperspektive, charakterisierung, inhaltsangabe; in Kapitel 2: stilmittel, gedicht-analysieren, drama-szene, film-analysieren. Elf Seiten (neun Bausteine, zwei Recaps).

**Werkzeugkasten:** je Karte `note` „Werkzeugkarte · <Begriff>“ mit Fachbegriff, Leitfrage und Satzanfang. Kapitel 1: narrator, character, setting, plot (Seite 1), dazu Merkmale der Kurzgeschichte, narrative perspective, characterisation, summary. Kapitel 2: metaphor, simile, repetition, rhetorical question; stanza, rhyme scheme; stage direction; shot types (long shot, medium shot, close-up) und camera angle. `stilmittel` wird in #486 und #487 wieder aufgenommen: hier einführen.

**Seitenaufbau (Stufe 9-10):** Vorwissen-Frage, Lesestück 300-600 Wörter in Abschnitten mit `vocabulary` als Randglossar, Aufgaben in drei Stufen (Verstehen, Belegen mit Zeile, Meinung), Erklärkasten und Werkzeugkarte, Schreibauftrag (`open-task` mit Punkten und Musterlösung), kurze Hörsätze (Diktat, Nachsprechen); Szene: Rollen sprechen (`speaking-task`). Höchstens etwa 25 Items, 350 Wörter Erklärtext je Seite.

**Üben:** Begriff erkennen (single-choice, matching), Stelle belegen (Zeile wählen, Beleg zuordnen, language-task `gap`), Wirkung beschreiben (Satzanfang wählen, `choice`), Inhaltsangabe: Sätze ordnen und im present tense schreiben (`language-task` write mit Cue), freie Aufgabe mit Punkten. Typische Fehler mit eigener Meldung: Autor und Erzähler verwechselt, Handlung nacherzählt statt analysiert, Inhaltsangabe im past tense oder mit Zitat und Meinung, Charakterzug behauptet ohne Beleg, Reim nach Schreibung statt nach Klang, Regieanweisung mit Dialog verwechselt, Kameraeinstellung mit Kamerawinkel verwechselt.

**Umfang:** drin: neun Bausteine, ein Lesestück je Seite, Audio kurz (`bf_emma`). Nicht drin: Bewertung offener Texte oder der Aussprache durch die App, Analyse echter Filme und geschützter Gedichte (nur Fakten), Zeitungstexte (#486), Werbung (#487), Zeitformen selbst (#472), Erörterung. Daten: Zeilenzahlen und Strophen der eigenen Texte.

**Quellen (geöffnet am 2026-11-24, nur Fakten):** en.wikipedia.org Rhyme scheme, Stanza, Shot (filmmaking), Close-up, Camera angle, Metaphor, Rhetorical question, Narration (Einleitung gelesen). Nicht geprüft: Short story (Abfrage lieferte keinen Text). Karte und Grundwortschatz von lernapps.net. Alle Texte und Zeichnungen eigen.

**Offene Fragen:** keine; Annahmen sind oben mit (guess) markiert.

## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [x] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [x] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [x] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [x] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [x] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [x] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [x] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [x] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [x] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [x] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [x] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [x] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.
      Creator: Orchestrator (Rolle der Ersteller:in): Recherche bestätigt; Annahmen 1 und 2 ja; Musterseite kurzgeschichten/text-fachbegriffe ja; Lesestücke mit nummerierten Zeilen wie in den Schwesterapps lösen; Textmengen-Hinweis ist bekannt.

### Answers

<!-- The interview: per topic the creator's answer, in their words. Keep the topics. -->

- Goal: Issue 483, Leitidee: „Ich kann Kurzgeschichten, Gedichte, Dramenszenen und Filme mit Fachbegriffen untersuchen und meine Deutung am Text belegen.“ (Orchestrator-Session in der Rolle der Ersteller:in, Auftrag).
- Learners: Issue 483: Englisch, Stufe 9-10; Vorwissen aus #479 (story map), #477 (Steckbrief), #472 (simple present).
- Model and focus: Issue 483: Analyse-Werkzeugkasten (toolkit) trägt den Explainer; Vorgänger englisch-geschichten, englisch-alltag, englisch-klang-schrift, englisch-saetze-verbinden als Muster.
- Hurdles: Issue 483 nennt keine; Annahmen unter Notes (Autor/Erzähler, Nacherzählen statt Analyse, past statt present in der Inhaltsangabe) (guess).
- Content: Startnachricht: eigene Texte oder gemeinfrei mit belegter Quelle; keine geschützten Werke; Quellen nur Fakten.
- Amount: Startnachricht: der ganze Explainer, 2 Kapitel, 9 Bausteine, nur Stufe 9-10.
- Languages: Deutsch mit englischen Beispielen (Konventionen §4).
- Look and feel: fixed by the archetype.
- Terms: Werkzeugkasten (toolkit), Werkzeugkarte, Lesestück, Beleg; Fachbegriffe englisch.
- Finding the app: Annahme (guess): Kurzgeschichte analysieren Englisch, Gedichtanalyse, Charakterisierung, Inhaltsangabe, Filmanalyse, Klasse 9 und 10.

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [x] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [x] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [x] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [x] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [x] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [x] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: Orchestrator (Rolle der Ersteller:in): Plan und Inhaltsmethode bestätigt; Musterseite kurzgeschichten/text-fachbegriffe mit Lerner-Check, danach ohne Rückfragen den Rest; Texte sachlich, keine Gewalt- oder Verstörungsthemen.

### Content method

**Karte → Archetyp:** zwei Kapitel, elf Seiten (neun Bausteine, zwei Recaps), `src/app.yaml` mit `subject: englisch`, `languages: [de]`, `scope` mit `out`. Kapitel-Ids `kurzgeschichten`, `gedicht-szene-film`; Seiten-Ids siehe Notes. Keine Komponenten, keine Datendateien (`prefer-built-in-block`): Zeichnungen sind SVG in `src/images/`.

**Seitenaufbau (Muster aus den Schwesterapps, Stufe 9-10):** Abschnitte `einstieg` (Vorwissens-Frage als `single-choice` mit Begründung, „Das kannst du danach“), `lesestueck` (zuerst `vocabulary` „Wörter zum Text“ als Randglossar, dann der Text in `text`-Blöcken mit nummerierten Zeilen „**[1]** …“, 300-600 Wörter, eigener Text; neutraler Titel), `neu` (Erklärung, Werkzeugkarte als `note` „Werkzeugkarte · <Begriff>“ mit Fachbegriff, Leitfrage, Satzanfang; Merke), `uebung` (drei Stufen: Verstehen, Belegen mit Zeile, Meinung), `anwenden` (`open-task` mit Punkten und Musterlösung, `speaking-task`, Diktat), `weiter` (Eintrag für die Lese- und Sehliste der Year 10, Ausblick). Kein Satz des Lesestücks steht wörtlich in Merke, Karte oder Einstieg. Eine Figur wird nicht eingeführt; kein Datum und keine Altersangabe im Fließtext.

**Fall (Entscheidung):** Die Lernenden stellen die Lese- und Sehliste für Year 10 zusammen. Jede Seite endet mit einem Listeneintrag (ein bis zwei Sätze mit Satzanfang der Werkzeugkarte und einer Zeilenangabe). Die letzte Seite (`film-analysieren`) fragt, welchen der untersuchten Texte oder Filme sie empfehlen, mit zwei belegten Gründen; mehrere Antworten sind richtig, die Musterlösung zeigt nur eine Sichtweise. Keine erfundenen Kinder; Sophie kommt nicht vor.

**Muster je Baustein (Name: Art, Form, Beispiel):**
- Begriff erkennen: `matching` Fachbegriff ↔ Textstelle, `single-choice` mit `info` je Option (narrator oder author, setting oder plot).
- Belegen mit Zeile: `multiple-choice` „In welchen Zeilen steht …?“ und `language-task` (`mode: gap`) „The narrator … (l. 3)“; Zeilenangaben haben die Form `(l. 4)` und `(ll. 2-5)`.
- Wirkung beschreiben: `language-task` `mode: choice` Satzanfang (The metaphor … shows …) mit Distraktoren, die echte Lernerfehler sind (nacherzählen statt deuten).
- Ordnen: `ordering` Inhaltsangabe-Sätze; Station der Handlung (Einleitung, Wendepunkt, offenes Ende).
- Schreiben: `language-task` `mode: write` mit Cue (`narrator · tell · story · first person`), `form: { punctuation: ok, case: hint }`; `open-task` mit 2-5 Punkten und Musterlösung („Die App bewertet den Text nicht.“).
- Hören und Sprechen: je Seite 3 Diktatsätze und 3 Nachsprechsätze (`speaking-task`), kurz, nicht aus dem Lesestück und nicht aus Merke oder Karte; Szene: `speaking-task` mit den Textzeilen der Rollen (kurz).
- Selbsteinschätzung: je Kapitel 2-3 Übungen je Seite ohne Material der Seite.

**Typische Fehler (je eine Meldung):** Autor = Erzähler; „I“ heißt immer die Autorin; Handlung nacherzählt statt analysiert; Inhaltsangabe im past tense, mit wörtlicher Rede, Zitat oder Meinung; Charakterzug ohne Beleg; direkte und indirekte Charakterisierung vertauscht; Metapher mit Vergleich (like, as) verwechselt; Reimschema nach Schreibung statt Klang; Regieanweisung als Dialog gesprochen; close-up und high angle vertauscht.

**Bilder:** eigene SVG, CC-BY-4.0, #f4efe2, Schrift ab 16 im 480er viewBox: Werkzeugkasten (Kartenreihe, Kapitel 1 und 2 je eine Fassung), story map zur Inhaltsangabe (Farben who #2c6fd8, where #138d75, when #d35400, what #c0392b wie in #479), Gedichtform (Strophen, Reimbuchstaben), Bühnenplan, Kameraeinstellungen (long shot, medium shot, close-up als Strichzeichnung, high und low angle). Ein Zeichenskript im Scratchpad, die SVG sind die Quelle.

**Audio:** `bf_emma`, `regen_audio.py` aus dem Inhaltsführer von #479, Hörliste im Inhaltsführer, `audio-texte.json`, Prüfskript `pruefen.py` (Hörsätze gegen die Seite; Wörter gegen die Karte).

**Wörter:** Grundwortschatz A1/A2 plus Fachbegriffe der Karte; Wörter ab B1 im `vocabulary`-Block der Seite erklärt und im Inhaltsführer gelistet.

**Engagement je Seite (Opening · Change · Reward · Story):** Immer so: Opening = Vorwissens-Frage mit Begründung; Change = lesen, markieren, Karte anlegen, schreiben, sprechen im Wechsel (nie mehr als vier Textblöcke hintereinander); Reward = die neue Werkzeugkarte im Kasten und ein eigener Listeneintrag; Story = Lese- und Sehliste für Year 10, jede Seite fügt einen Eintrag hinzu.
- `text-fachbegriffe`: Opening: Wer erzählt hier? (Text ohne Fachwort). Change: vier Karten anlegen. Reward: Kasten mit vier Karten. Story: erster Eintrag zur Nachtschicht-Geschichte.
- `kurzgeschichte`: Opening: Was fehlt am Ende? Change: Merkmale an Zeilen belegen. Reward: Karte plot wird genauer (Wendepunkt, offenes Ende). Story: Eintrag „Platform Two“.
- `erzaehlperspektive`: Opening: dieselbe Szene, zwei Stimmen. Change: Ich- und Er/Sie-Fassung umschreiben. Reward: Karte narrator mit Perspektive. Story: Eintrag zur Wahl der Perspektive.
- `charakterisierung`: Opening: Steckbrief einer Figur aus Zeilen füllen. Change: Steckbrief wird Absatz mit Belegen. Reward: Karte character mit direkt und indirekt. Story: Eintrag zur Figur.
- `inhaltsangabe`: Opening: story map füllen. Change: Sätze ordnen, im present tense schreiben. Reward: eine eigene Inhaltsangabe, geprüft an Punkten. Story: Kapitelrückblick, die vier Einträge im Überblick.
- `stilmittel`: Opening: Welche Wörter wirken in der Rede? Change: Stilmittel finden, Wirkung wählen. Reward: Karten metaphor, simile, repetition, rhetorical question. Story: Eintrag zur Rede.
- `gedicht-analysieren`: Opening: Gedicht hören (Nachsprechen), Reim finden. Change: Strophen und Reimschema eintragen. Reward: Karten stanza, rhyme scheme. Story: Eintrag Gedicht und Song.
- `drama-szene`: Opening: Regieanweisung oder Dialog? Change: lesen, Rollen sprechen. Reward: Karte stage direction, gesprochene Szene. Story: Eintrag Szene.
- `film-analysieren`: Opening: Welche Einstellung zeigt Angst? Change: Szenenliste lesen, Einstellungen zuordnen. Reward: Karten shot und camera angle, ganzer Kasten. Story: Entscheidung: Welchen Text oder Film empfiehlst du? Zwei belegte Gründe.

**Neue Kapitel später:** Inhaltsführer „Adding a chapter or round“.
<!-- An explainer: per figure, model and component its learning action in two to four sentences
(`explainer-representation-explained`); per page its prerequisites the app does not practise, and which get a recap
page, which a link. -->

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [x] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [x] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [x] Load skill `lernapps-explainer`.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Baue die Musterseite kurzgeschichten/text-fachbegriffe: Lesestück mit nummerierten Zeilen, Werkzeugkarten narrator, character, setting, plot, Übungen in drei Stufen, Schreibauftrag, Hörsätze und Nachsprechen, Zeichnung des Werkzeugkastens; baut die App, den Inhaltsführer-Eintrag, Kapitelrahmen und das Audio-Gerüst mit, und committet.
<!-- tasks: pattern (1 added): the one page or screen that is the pattern for the others -->
- [x] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
      Creator: Orchestrator (Rolle der Ersteller:in): Muster bestätigt, übrige Seiten ohne Rückfragen; Lizenz-Badge: unten Platz im Bild lassen; Hörurteil bestätigt.
- [x] Kapitel 1: Recap-Seite kurzgeschichten/das-brauchst-du und Seite kurzgeschichte (Merkmale, Lesestück mit offenem Ende).
- [x] Kapitel 1: Seite erzaehlperspektive (Lesestück in zwei Fassungen, Autor oder Erzähler).
- [x] Kapitel 1: Seite charakterisierung (Steckbrief wird Charakterisierung mit Belegen).
- [x] Kapitel 1: Seite inhaltsangabe (story map wird Inhaltsangabe im present tense), Kapitelrückblick und Selbsteinschätzung.
- [x] Kapitel 2: Recap-Seite gedicht-szene-film/das-brauchst-du und Seite stilmittel (Rede als Lesestück, Karten metaphor, simile, repetition, rhetorical question).
- [x] Kapitel 2: Seite gedicht-analysieren (eigenes Gedicht und Songtext, Strophe, Reimschema, Zeichnung der Gedichtform).
- [x] Kapitel 2: Seite drama-szene (Szene mit Regieanweisungen, Bühnenplan, Rollen sprechen).
- [x] Kapitel 2: Seite film-analysieren (Szenenliste eines erfundenen Kurzfilms, Zeichnung der Kameraeinstellungen, Entscheidung für die Liste), Kapitelrückblick und Selbsteinschätzung.
- [x] Inhaltsführer, Hörliste, Quellen, Wörterdatei und Prüfskript pflegen; Hörsätze erzeugen (bf_emma, regen_audio.py) und über alle Seiten prüfen.
<!-- tasks: pages (9 added): the other pages or screens, after the pattern -->
- [x] Update the content guide so that it describes the app as built (`app-content-matches`).
- [x] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [ ] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [ ] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
