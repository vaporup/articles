# mcfly - Düsen durch die Shell History

Die Shell. Von vielen gefürchtet wie der Teufel das Weihwasser  
aber immer noch eins der effektivsten Werkzeuge heutzutage. 

Doch auch hier kann man wertvolle Zeit vergeuden z.B. beim Suchen alter Befehle.

Den ```history``` Befehl lernt man schnell kennen  
sowie das Zurückholen vorheriger Befehle mit der Pfeiltaste nach oben.

Sitzt man neben einem Kollegen, der in der Historie mit der Pfeiltaste sucht,  
kann dies schnell zum Geduldspiel werden  
und ein Tipp zu ```STRG + r``` wird nicht selten zur Heiligen Offenbarung.

Doch auch hier fühlt es sich manchmal an wie beim Drehen eines Glücksrades  
und schießt beim Suchen nicht selten übers Ziel hinaus.

Hier möchte nun [1]mcfly unterstützen damit man schneller findet statt sucht.

## Funktionsweise

Das Programm klinkt sich beim Drücken von STRG+r ein  
und ersetzt dadurch das bisherige Such-Interface der Shell.

Ein Suchergebnis kann direkt durch ENTER wieder ausgeführt  
bzw. beim Drücken der TAB Taste vorher nochmal editiert werden.

Suchergebnisse werden nach verschiedenen Kriterien priorisiert.  
Mit einberechnet werden z.b. der aktuelle Ordner in dem man sich befindet,  
wie oft man einen Befehl ausgeführt hat, etc...

Das History File der Shell wird weiter gepflegt,  
sodass man mcfly ohne kalten Entzug leicht wieder absetzen kann.

## Shell-Support

Unterstützt werden aktuell folgende Shells:

- Bash
- Zsh
- Fish

## Installation

Es gibt fertige [2]Binaries zum Runterladen  
und man entpackt sich das passende davon einfach in den Pfad.

mcfly erzeugt Shell Code für die jeweilige Shell,  
den man sich entweder selbst in die passende Config schreibt,  
oder via ```eval``` direkt ausführt.  
Letzteres ist zwar bequemer und vereinfacht auch das Updaten,  
jedoch sollte man sich vorher immer mal anschauen was man da ausführt.

### Anzeigen des Shell Codes

- Bash: ```mcfly init bash```
- Zsh:  ```mcfly init zsh```
- Fish: ```mcfly init fish```

### Aktivieren des Shell Codes


- Bash: ```eval "$(mcfly init bash)"```
- Zsh:  ```eval "$(mcfly init zsh)"```
- Fish: ```mcfly init fish | source```

Damit man dies nicht immer wieder eingeben muss,  
trägt man es in seine passende Shell Config ein.

Beispiel für Bash

```bash
#
# mcfly - init
#

eval "$(mcfly init bash)"
```

Im Falle von Bash sollte man sich jedoch noch einen zusätzlichen TRAP setzen  
ansonsten [3]müllt man sich /tmp/ über die Zeit voll

```bash
#
# mcfly - cleanup
#
# <https://github.com/cantino/mcfly/issues/71>

mcfly_cleanup() {
  if [ ! -z "${MCFLY_HISTORY}" ] && [[ -f "${MCFLY_HISTORY}" ]]; then
    rm "${MCFLY_HISTORY}"
  fi
}

trap mcfly_cleanup EXIT

```

Für Zsh und Fish wird das nicht gebraucht.  
Zsh räumt selbst auf und für Fish wird kein Tempfile verwendet.


## Konfiguration

Über Umgebungsvariablen kann man sich vieles anpassen wie z.B.

- Anzahl Suchergebnisse
- Farbschema
- Reihenfolge der Ergebnisse
- ...und einiges mehr

## Schmankerl

Der Name des Tools ist eine Anspielung auf die bekannten Szenen aus der [4]**Zurück in die Zukunft** Reihe

## Links

- [1] <https://github.com/cantino/mcfly>
- [2] <https://github.com/cantino/mcfly/releases>
- [3] <https://github.com/cantino/mcfly/issues/71>
- [4] <https://www.youtube.com/watch?v=AMsDYUi4LiU>
