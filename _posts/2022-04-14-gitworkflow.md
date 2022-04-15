---
layout: post
title: "Gemeinsame Textredaktion mit Github"
---

## Motivation

Die gemeinsame Redaktion von Texten wird immer wichtiger. Anbieter wie
Google und Microsoft haben dies verstanden und bieten die Möglichkeit
an, in Echtzeit gemeinsam an einem Dokument zu arbeiten. Dabei besteht
auch die Möglichkeit die Änderungen im Text nachzuverfolgen. Allerdings
wird der Änderungsverlauf bei mehreren Überarbeitungen sehr schnell
unübersichtlich.

Aus diesem Grund soll hier eine Variante mit Hilfe von Github
beschrieben werden.

Git ist ein Versionskontrollsystem, das ursprünglich für die
Versionierung von Computerprogrammen konzipiert wurde. Wenn man
bezüglich der Arbeitsumgebung für die Textredaktion bereit ist,
Konzessionen zu machen, dann kann diese Versionskontrolle auch für die
gemeinschaftliche Redaktion von Texten nutzbar gemacht werden. Die
Versionskontrolle kann dabei ausschliesslich lokal durchgeführt werden
oder man kann sie im Zusammenspiel mit einem entfernten Server
verwenden. Für die Zusammenarbeit in einer Gruppe muss ein entfernter
Server verwendet werden. Dafür gibt es verschiedene mögliche Lösungen.
Hier wird die Lösung mit Hilfe von Github beschrieben.

## Voraussetzungen

Damit Git bzw. Github für die Versionierung von Texten verwendet werden
kann, muss der entsprechende Text als reiner Text abgespeichert werden.
Mögliche Formate dafür sind beispielsweise LaTEX oder Markdown.

Ich beschreibe hier den Workflow unter Verwendung von Visual Studio Code
mit den entsprechenden Erweiterungen als Texteditor. Das heisst, auf dem
Computer muss Visual Studio Code installiert sein. Zusätzlich braucht es
eine lokale Installation von Git. Ausserdem braucht man ein Github
Konto.

## Charakteristik des Github Workflows

In Github wird nicht nur die Version des Textes kontrolliert, es können
darüber hinaus auch Varianten des Textes erstellt werden. Der
Git-Begriff für solche Varianten ist *Branch*.

Wenn ein neues Github Repository erstellt wird, richtet Github
automatisch den *Branch* `main` ein. In diesem *Branch* liegt der Text
als Original vor. Wenn eine Variante des Originals erstellt werden soll,
kann ein neuer *Branch* erstellt werden. Der Name dieses *Branches* kann
dabei frei gewählt werden. Für die Redaktion der Textvariante wird nun
in diesem *Branch* gearbeitet. Wenn die Textvariante fertig ist, kann
Sie mit dem Original verglichen werden und dann ganz oder Teilweise
übernommen werden.