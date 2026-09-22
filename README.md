# augmentedwork-skill-creation

Eine wachsende Sammlung wiederverwendbarer Skills im **SKILL.md-Format** — kompatibel mit gängigen Agent-Tools wie Claude Skills, Mistral Vibe, Cursor und anderen, die Skills/Anweisungsdateien mit YAML-Frontmatter unterstützen. Jeder Skill liegt in einem eigenen Ordner mit einer `SKILL.md`.

## Enthaltene Skills

| Skill | Zweck | Wann verwenden? |
|---|---|---|
| [golden-example](golden-example/SKILL.md) | Synthetisiert aus mehreren Arbeitsergebnissen ein exemplarisches "Golden Example" als Referenzstandard | Wenn mehrere Varianten desselben Ergebnisses vorliegen und daraus eine verbindliche Vorlage werden soll |
| [workflow-html-beschreibung](workflow-html-beschreibung/SKILL.md) | Dokumentiert Workflow-Schritte als strukturiertes, valides HTML-Dokument mit Phasen | Wenn ein Prozess oder Entstehungsprozess nachvollziehbar als eigenständige HTML-Seite festgehalten werden soll |

## Wann verwende ich was?

Nicht jede Aufgabe braucht einen Skill. Diese Übersicht hilft bei der Einordnung:

| Situation | Passendes Werkzeug |
|---|---|
| Einmalige Aufgabe, die sich nicht wiederholt | Einfacher Prompt im Chat - kein Skill nötig |
| Aufgabe wiederholt sich, soll aber flexibel bleiben | Prompt-Vorlage, die du kopierst und anpasst |
| Aufgabe wiederholt sich immer gleich und soll zuverlässig funktionieren | **Skill** (feste Anweisungsdatei, die vom Agent automatisch geladen wird) |
| Verhalten, das bei *jeder* Konversation gelten soll | Globale Regel / Custom Instruction des Agent-Tools (z. B. bevorzugte Sprache, Ton) |

Kurz gesagt: **Ein Skill lohnt sich, wenn du dieselbe Anweisung zum dritten Mal tippst.** Er sorgt dafür, dass ein wiederkehrendes Ergebnis nicht vom Zufall oder von der Tagesform abhängt, sondern jedes Mal nach demselben Standard entsteht.

## Wie definiere ich das Ziel eines Skills?

Du musst kein Prozessexperte sein, um einen guten Skill zu definieren. Ein Skill ist nichts anderes als eine schriftliche Anweisung, die der Agent jedes Mal auf dieselbe Weise ausführt. Entscheidend ist nur, dass du klar sagen kannst, was am Ende dabei herauskommen soll.

Beantworte nacheinander diese vier Fragen - am besten in einfachen Worten, so wie du es einem Kollegen erzählen würdest:

1. **Wobei soll mir der Skill helfen?** ("Ich habe mehrere Entwürfe und will daraus die beste Version machen.")
2. **Was genau soll am Ende dastehen?** ("Ein einziges, fertiges Dokument, das ich direkt weiterverwenden kann.")
3. **Woran erkenne ich, dass es gut gelungen ist?** ("Keine Widersprüche, einheitlicher Ton, nichts Erfundenes.")
4. **Wann soll der Skill zum Einsatz kommen?** ("Immer wenn ich sage: Golden Example erstellen.")

Schreibe deine Antworten in ein bis zwei Sätzen auf. Das ist bereits die Zieldefinition deines Skills.

### Vom Ziel zur SKILL.md

Aus deinen Antworten ergibt sich die Struktur der Datei fast von selbst:

| Frage | Wird zu ... |
|---|---|
| 1 + 2 (Zweck + Endresultat) | Anweisungen: **Vorgehen** und **Ausgabe** |
| 3 (Erfolgskriterium) | **Qualitätskriterien** |
| 4 (Trigger) | `description` im YAML-Frontmatter - sie entscheidet, wann der Agent den Skill lädt |

Fehlt dir noch eine Antwort auf eine der Fragen, frage dich: "Was würde ich einem neuen Mitarbeiter erklären müssen, damit er diese Aufgabe ohne Rückfragen richtig macht?" Alles, was du dabei erklärst, gehört in den Skill.

## Aufbau einer SKILL.md

```markdown
---
name: mein-skill
description: Wann der Skill geladen werden soll (Trigger und Zweck).
---

# Mein Skill

## Eingabe
Was der Nutzer bereitstellen muss - und was nachgefragt werden soll, wenn es fehlt.

## Vorgehen
Die Schritte in der Reihenfolge, in der sie auszuführen sind.

## Ausgabe
Was am Ende dastehen soll - und in welchem Format.

## Qualitätskriterien
Woran man ein gelungenes Ergebnis erkennt.
```

Der Aufbau ist bewusst einfach gehalten und funktioniert in jedem Agent-Tool, das Markdown-Dateien als Anweisungen einliest.

## Skill hinzufügen

1. Neuen Ordner anlegen: `<name>/SKILL.md`
2. Datei nach dem Aufbau oben erstellen
3. In der Tabelle oben verlinken (inkl. "Wann verwenden?")
