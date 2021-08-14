# glow - Der pfiffige CLI Markdown Viewer

Wer z.B. viel mit Markdown Dateien auf Github/Gitlab arbeitet,  
möchte nicht immer zuerst Pushen um zu merken,  
dass die Änderungen nicht so aussehen, wie man sich das gedacht hat.

Grafische Markdown Viewer und Editoren gibt es mittlerweile viele.  
Für die CLI fällt die Auswahl schon etwas geringer aus.

Neben [grip](https://github.com/joeyespo/grip) und [mdless](https://github.com/ttscoff/mdless)
gibt es noch das pfiffige [glow](https://github.com/charmbracelet/glow)
das dem Ganzen noch einen schicken [Charm](https://charm.sh) verleiht.

## Features

- Schicke Darstellung von Markdown im Terminal
- Findet alle Markdown Dateien automatisch
- Speichern von Dateien in der Charm Cloud (Stashing)
  - Dateien werden mit dem lokalen SSH PublicKey verschlüsselt

## Benutzung

### Markdown anschauen

```
glow README.md
````

### Markdown anschauen (mit Pager)

```
glow -p README.md
````

### Interaktiv (TUI)

```
glow
````

## Installation

Für einige Distros gibt es schon [Pakete](https://repology.org/project/glow/versions), glow lässt sich aber einfach [runterladen](https://github.com/charmbracelet/glow/releases),  
da es (wie von Go und Rust gewohnt) nur eine einzige Binärdatei ist.  

Das Github Repo hat auch fertige Distro Pakete (Deb, rpm, apk),  
die man nutzen kann um seinem Paketmanager treu zu bleiben.

