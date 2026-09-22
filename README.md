# augmentedwork-skill-creation

Wiederverwendbare Skills für Mistral Vibe im SKILL.md-Format. Jeder Skill liegt in einem eigenen Ordner mit einer `SKILL.md` (YAML-Frontmatter + Anweisungen).

## Skills

| Skill | Zweck |
|---|---|
| [golden-example](golden-example/SKILL.md) | Synthetisiert aus mehreren Arbeitsergebnissen ein exemplarisches "Golden Example" als Referenzstandard |
| [workflow-html-beschreibung](workflow-html-beschreibung/SKILL.md) | Dokumentiert Workflow-Schritte als strukturiertes, valides HTML-Dokument mit Phasen |

## Wie definiere ich das Ziel eines Skills?

Du musst kein Prozessexperte sein, um einen guten Skill zu definieren. Ein Skill ist nichts anderes als eine schriftliche Anweisung, die Vibe jedes Mal auf dieselbe Weise ausführt. Entscheidend ist nur, dass du klar sagen kannst, was am Ende dabei herauskommen soll.

Beantworte nacheinander diese vier Fragen - am besten in einfachen Worten, so wie du es einem Kollegen erzählen würdest:

1. **Wobei soll mir der Skill helfen?** ("Ich habe mehrere Entwürfe und will daraus die beste Version machen.")
2. **Was exactly soll am Ende dastehen?** ("Ein einziges, fertiges Dokument, das ich direkt weiterverwenden kann.")
3. **Woran erkenne ich, dass es gut gelungen ist?** ("Keine Widersprüche, einheitlicher Ton, nichts Erfundenes.")
4. **Wann soll der Skill zum Einsatz kommen?** ("Immer wenn ich sage: Golden Example erstellen.")

Schreibe deine Antworten in ein bis zwei Sätzen auf. Das ist bereits die Zieldefinition deines Skills.

### Vom Ziel zur SKILL.md

Aus deinen Antworten ergibt sich die Struktur der Datei fast von selbst:

- **Antwort 1 und 2** ergeben die Anweisungen (Vorgehen und Ausgabe).
- **Antwort 3** wird zu den Qualitätskriterien.
- **Antwort 4** landet in der `description` im YAML-Frontmatter - sie entscheidet, wann Vibe den Skill automatisch lädt.

Fehlt dir noch eine Antwort auf eine der Fragen, frage dich: "Was würde ich einem neuen Mitarbeiter erklären müssen, damit er diese Aufgabe ohne Rückfragen richtig macht?" Alles, was du dabei erklärst, gehört in den Skill.

## Aufbau einer SKILL.md

```markdown
---
name: mein-skill
description: Wann der Skill geladen werden soll (Trigger und Zweck).
---

# Mein Skill

## Eingabe
Was der Nutzer bereitstellen muss - und was du nachfragen sollst, wenn es fehlt.

## Vorgehen
Die Schritte in der Reihenfolge, in der sie auszuführen sind.

## Ausgabe
Was am Ende dastehen soll - und in welchem Format.

## Qualitätskriterien
Woran man ein gelungenes Ergebnis erkennt.
```

## Skill hinzufügen

1. Neuen Ordner anlegen: `skills/<name>/SKILL.md`
2. Datei nach dem Aufbau oben erstellen
3. In der Tabelle oben verlinken
