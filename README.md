# SMP-Mathe
Der Matheunterricht der 1ere & Te SMP auf Deutsch in digital und in vereinheitlicht. Das Ganze als hübsches PDF geschmückt.


## Bearbeitung:
Das Dokument besteht aus der ```main.tex``` Datei, und einer weiteren ```kap*.tex``` Datei pro Kapitel. Dort befindet sich der tatsächliche Inhalt.


## Struktur:
### Titel:
Befindet sich in ```/MAIN/title.tex```

### Visuelle Anpasssungen:
Als LaTex-Stylesheet: ```/STYLE.sty```

### Inhalt:
1 Kapitel pro Ordner (bzw. 1 Ordner pro Kapitel).

Der Inhalt des Kapitels sowie zugehörige Dateien (z.B. Grafiken) sollten sich im jeweiligen Ordner befinden.
Achtung: absolute Pfade verwenden (das Bild im Ordner kap1 ist nur über ``` \includegraphics{../kap1/bild}``` zu erreichen.

Jedes Kapitel muss folgendermaßen strukturiert sein:
```latex
\documentclass[../MAIN/main.tex]{subfiles}                   %MAIN.tex als übergeordnete Datei
\begin{document}
\chapter{Wahrscheinlichkeitstheorie}                        %Kapitelname, der auch im Hauptdokument erscheint
%%%%%%%%%%%
% INHALT  %
%%%%%%%%%%%
\end{document}
```

### Hauptdokument:
Wird über ```/MAIN/main.tex``` kompiliert. Enthält alle Kapitel, sowie ein detailliertes Inhaltsverzeichnis.


## Export
Das Hauptdokument sollte regelmäßig kompiliert werden, damit das Dokument als gesamtes immer aktuell bleibt.
