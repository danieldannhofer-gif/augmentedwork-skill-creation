---
name: workflow-html-beschreibung
description: Dokumentiere den Entstehungsprozess eines Skills oder Workflows als strukturierte, valides HTML-Dokument mit klar gegliederten Phasen. Verwende bei "Workflow als HTML", "Prozess dokumentieren", "Phasen beschreiben", "Entstehungsprozess nachvollziehen" oder wenn Workflow-Schritte als HTML-Seite ausgegeben werden sollen.
---

# Workflow-Beschreibung als HTML

Du unterstützt den Skill Creator dabei, den Entstehungsprozess eines Skills nachvollziehbar zu dokumentieren. Beschreibe anhand der bereitgestellten Workflow-Schritte den gesamten Prozess strukturiert und verständlich.

## Eingabe

- Workflow-Schritte: Die Beschreibung der gewünschten Workflow-Schritte (vom Nutzer bereitzustellen). Fehlt sie, frage nach, bevor du arbeitest.

## Vorgehen

1. **Gliederung**: Teile den Prozess in klar benannte, chronologisch geordnete Phasen.
2. **Phasenbeschreibung**: Beschreibe zu jeder Phase Zweck, wichtigste Aktivitäten und Ergebnis/Output dieser Phase.
3. **Abhängigkeiten**: Hebe Abhängigkeiten zwischen den Phasen hervor, sofern vorhanden.
4. **Sprache**: Verwende eine klare, professionelle Sprache ohne unnötige Fachbegriffe.
5. **Vollständigkeit**: Erfinde keine zusätzlichen Prozessschritte oder Anforderungen, die nicht in den bereitgestellten Workflow-Schritten enthalten sind.

## Ausgabeformat

Gib das Ergebnis ausschließlich als valides HTML-Dokument aus (inkl. `<!DOCTYPE html>`, `<html>`, `<head>` und `<body>`). Nutze semantische HTML-Elemente:

- `<h1>`/`<h2>` für Phasenüberschriften
- `<p>` für Beschreibungstexte
- `<ol>`/`<ul>` für Aktivitätslisten

Gib ausschließlich den HTML-Code zurück - ohne zusätzlichen Fließtext davor oder danach.

## Qualitätskriterien

- Das Dokument ist ohne Anpassungen als eigenständige HTML-Seite darstellbar.
- Jede Phase enthält Zweck, Aktivitäten und Output.
- Die Phasenreihenfolge entspricht exakt den bereitgestellten Workflow-Schritten.
