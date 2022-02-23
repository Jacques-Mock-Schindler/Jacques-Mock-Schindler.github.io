---
layout: post
title: "YAML-Header Vorlagen"
---

## Motivation

Ein YAML-Header vereinfacht die Transformation des .md-files in das
gewünschte Ausgabeformat. Angestrebt ist, dass im Terminal lediglich 
`pandoc mein_file.md --citeproc -o output.fte` ausgeführt werden muss.

## Header für kurze Texte

Für Texte wie kleine Rechtsfälle oder Essays reicht ein kurzer Header
mit Titel, Name des Autors und Angaben zur Bibliographie. Folgendes
Beispiel dürfte das wesentliche abdecken.

```yaml
---
# Angaben für das Deckblatt
title: Titel
author: Verfasser
date: 23.02.2022

# Angaben zum Inhalt und zur Darstellung der Bibliographie
bibliography: Bibliographie.yaml
csl: chicago-note-bibliography.csl

# Angaben zum Layout
output: 
    pdf_document:
        latex_engine: xelatex
    fontsize: 12pt
    papersize: a4
    lang: de-CH 
---
````

Der Header bietet die Möglichkeit, Kommentare einzufügen. Kommentare
helfen einem, die Funktion bestimmter Teile des Headers zu verstehen,
wenn man sich zu einem späteren Zeitpunkt wieder mit dem Text
beschäftigt.
Kommentare werden mit einer Raute gekennzeichnet.

Zu den Elementen des Headers im Einzelnen:

* *Angaben für das Deckblatt*: Diese Angaben sind wahrscheinlich
  selbsterklärend.
* *Angaben zum Inhalt und zur Darstellung der Bibliographie*: Der
  Eintrag `bibliography` gibt an, in welcher Datei die bibliographischen
  Angaben abgespeichert sind. Wie eine solche Datei erstellt wird, ist
  in einem separaten Beitrag dargestellt.

  Der Eintrag `csl` legt die Darstellung der Belege und des
  Literaturverzeichnisses fest. Entsprechende Vorlagen finden sich
  beispielsweise unter [https://www.zotero.org/styles].
* *Angaben zum Layout*: In diesem Block wird das Ausgabeformat
  gesteuert. Grundsätzlich bietet Pandoc die Möglichkeit, ganz
  unterschiedliche Textformate zu erstellen. Standardzielformat dürfte
  wohl jedoch ein PDF sein. Zum erstellen des PDF muss angegeben werden,
  mit welcher *latex_engine* das PDF erstellt werden soll (diese wird
  durch die lokale LaTEX-Installation zur Verfügung gestellt). Für das
  erstellen von deutschsprachigen Texten hat sich `xelatex` bewährt.
  Diese Engine kann gut mit den deutschen Umlauten umgehen.
  
  Mit der `fontsize` wird die Schriftgrösse in Punkt festgelegt. Die
  `papersize` gibt die Grösse des "Papiers" in der Ausgabe an.

  Der Eintrag `lang` legt die Sprache des Ausgabedokumentes fest. Dies
  ist wichtig für die Steuerung der Trennungen und für die Darstellung
  von Sonderzeichen.