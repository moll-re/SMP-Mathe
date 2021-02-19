# SMP-Mathe
Der Matheunterricht der 1ere & Te SMP live und in Farbe, ähh auf Deutsch und in digital. Das Ganze als hübsches, einheitliches PDF. Enjoy!


## Bearbeitung:
Das Dokument besteht aus der ```main.tex``` Datei, und einer weiteren ```kap*.tex``` Datei pro Kapitel. Dort befindet sich der tatsächliche Inhalt.


## Struktur:

### Visuelle Anpasssungen:
Als LaTex-Stylesheet in ```/STYLE.sty```. Only touch if you know what you're doing.

### Inhalt:
Eine Datei pro Kapitel. Zugehörige Dateien werden bitte, zur Übersichtlichkeit, in den passenden Ordner geräumt. Beim Einbinden dieser Dateien muss logischerweise ein **absoluter** Pfad benutzt werden:

Beispiel - das Bild im Ordner kap1 ist nur über ``` \includegraphics{../kap1/bild}``` zu erreichen.

Jede Kapitel-Datei hat die folgende Strukur:
```latex
\documentclass[main.tex]{subfiles}
%MAIN.tex als übergeordnete Datei

\begin{document}
\chapter{Wahrscheinlichkeitstheorie}
%Kapitelname, der auch im Hauptdokument erscheint

%%%%%%%%%%%
% INHALT  %
%%%%%%%%%%%

\end{document}
```

## Hauptdokument:
Das Gesamtergebnis wird in ```main.tex``` kompiliert. Dieses PDF enthält alle Kapitel, sowie ein Inhaltsverzeichnis (und ein lexikograhisches Verzeichnis, falls jemand Bock hat das zu implementieren). 


## Export
Das Hauptdokument wird per GitHub-action bei jedem push kompiliert. Aktueller Status:

[![Compile main document](https://github.com/L0rd0fB0red0m/SMP-Mathe/actions/workflows/main.yml/badge.svg)](https://github.com/L0rd0fB0red0m/SMP-Mathe/actions/workflows/main.yml)