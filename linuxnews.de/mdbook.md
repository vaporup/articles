# mdBook - Pragmatisch Bücher in Markdown erstellen

Nicht selten will man etwas dokumentieren das größer ist als ein paar Befehle, Listen oder Notizen.  
Vielleicht eine REST API, HOWTOs, Tutorials oder sogar ein (kleines) Büchlein.

Optimalerweise das Ganze in Markdown,
das sich neben all den anderen **Lightweight** Markup Sprachen
sehr gut verbreitet hat.

Den Inhalt einfach in verschiedene Ordner
und Markdown Dateien auf Github pfeffern funktioniert, ist aber nicht besonders schick.

Da gibt es Lösungen wie Gitbook, Bookdown, selbst-gestrickte Pandoc Lösungen und vieles mehr,
doch mit mdBook erhält man ein Tool, das **out of the box** die wichtigsten Dinge mitbringt,
ohne überladen zu wirken. Eine Nische zwischen den kleinen und den sehr großen Lösungen.

Wer seinen Blog/Webseite mit Hugo betreibt,
wird mdBook vielleicht ebenfalls lieb gewinnen.

- Die Software ist schnell installiert, da einzelne Binary.
- Die Doku ist schnell überblickt und man kann zeitnah loslegen.
- Ein integrierter Webserver kann die Daten direkt im Browser rendern
  bevor man sie auf seinen eigenen Webserver oder Github/Gitlab Pages hochlädt
- Es stehen verschiedene Themes zu Verfügung (auch ein Dark Mode)
- Eine Suche zum Durchsuchen der Inhalte ist ebenfalls mit an Bord.

## Beispiele

mdBook kommt vom Rust Projekt um dessen Doku damit zu erstellen.

- https://doc.rust-lang.org/book/

Die Doku zu mdBook ebenfalls

- https://rust-lang.github.io/mdBook/

Ein Liste mit anderen Büchern

- https://github.com/softprops/awesome-mdbook

## Plugins

Gerendert wird zu HTML, es gibt jedoch verschiedene Plugins und Backends,
die man nutzen kann wie z.B. Manpages oder PDF statt HTML zu erzeugen.
Ein experimentelles Backend für EPUB gibt es ebenfalls.

- https://github.com/rust-lang/mdBook/wiki/Third-party-plugins

## Video Vortrag

- https://skillsmatter.com/skillscasts/15024-project-documentation-with-rust-and-mdbook
