# rsync-sidekick - rsync's dufter Kumpel

Wenn es darum geht Daten zu synchronisieren,  
findet sich auch heute noch das bewährte rsync  
im Werkzeugkoffer der meisten Admins.

Doch bei der Menge von Daten heutzutage  
zeigt sich bei rsync das ein oder andere Manko besonders deutlich.

Ändert man z.B. einfach nur die Ordnerstruktur,  
ist das für rsync nicht direkt ersichtlich  
und es wird im schlimmsten Fall nochmal komplett alles übertragen.

Um dieses Problem zu lösen, gibt es in rsync selbst  
den **--fuzzy** Parameter, der jedoch nur bedingt gut funktioniert.

Projekte wie [casync](http://0pointer.net/blog/casync-a-tool-for-distributing-file-system-images.html) lösen ähnliche Probleme,  
können teilweise aber nicht, wie man es von rsync gewohnt ist, benutzt werden.

Ansetzen möchte hier das Projekt [rsync-sidekick](https://github.com/m-manu/rsync-sidekick).

Das Tool schaut sich alle Dateien in Quelle und Ziel an  
und versucht zu ermitteln, welche Dateien und Ordner verschoben  
bzw. umbenannt werden müssen damit der normale rsync Aufruf danach  
nur wenig Geradeziehen bzw. nur Daten, die wirklich fehlen, übertragen muss.

Dabei werden Daten nicht direkt verändert, sondern am Ende wird einfach nur ein Shellskript ausgespuckt,  
das man entweder manuell ausführt oder direkt von rsync-sidekick starten lassen kann.

Danach sollte man unbedingt nochmal rsync selbst drüberschlichten lassen  
um das ein oder andere Fältchen gerade zu bügeln...

Um das Vergleichen der Daten zu beschleunigen, wird nicht die komplette Datei,  
sondern nur einzelne Stellen darin gehashed (das Verfahren ähnelt dem von [OpenSubtitles](https://trac.opensubtitles.org/projects/opensubtitles/wiki/HashSourceCodes)).

Um rsync-sidekick zwischen Hosts zu nutzen,  
muss man sich [derzeit](https://github.com/m-manu/rsync-sidekick/issues/1) noch mit SSHFS o.ä. behelfen.
