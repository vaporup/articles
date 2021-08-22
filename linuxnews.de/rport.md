# rport - Der TCP Tunnelbauer

Möchte man komplette Netze verbinden,
nimmt man in der Regel eine VPN Lösung,  
für einzelne Systeme oder Ports, ein Forwarding.

Für Letzteres z.B. den Router oder ein Werkzeug wie SSH,  
wobei OpenSSH schon seit längerem auch komplette Netze tunneln kann...

Ein Port Fowarding im Router möchte oder kann man vielleicht nicht einrichten,  
ein VPN für ein oder zwei Systeme wäre Overkill oder macht potentiell zuviel des eigenen Netzes erreichbar.

Für den spontanten Zugriff strickt sich der versierte Anwender  
mal kurz was mit SSH zurecht.
Soll das aber dauerhaft und robust laufen, muss man zu Tools wie [autossh](https://www.harding.motd.ca/autossh/) oder [sidedoor](https://github.com/daradib/sidedoor) greifen  
oder baut sich mit systemd Hausmitteln selbst etwas.

Diese funktionieren für ihren Anwendungs-Bereich sehr passabel, haben jedoch alle ihre kleineren Einschränkungen.

## Einschränkungen

- mehrere Tunnel nicht möglich oder umständlich einzurichten
- kein komfortables Management der Tunnel  
- keine Übersicht der Tunnel und deren Zustände  
- nicht für alle Betriebssysteme verfügbar ( systemd z.B. Linux-only )  

# Eine heterogene Lösung

Hier tritt nun [rport](https://oss.rport.io/) auf den Plan und möchte dies auf das nächste Level heben.  

Die Entwickler von rport haben erkannt (wie auch die PowerShell Macher),  
dass heutzutage heterogene statt Insel Lösungen gebraucht werden.

rport wurde daher bewusst in Go geschrieben damit eine Binärdatei hinten rausfällt,  
die auf so vielen Platformen wie möglich einfach gestartet werden kann.  

# Konzept

rport besteht aus folgenden Komponenten:

- Server
- Client
- API - mit CLI oder Webinterface nutzbar (optional)

Verwendet wird das Port Forwarding Konzept aus SSH,  
genutzt wird dazu aber nicht der lokale SSH Client sondern die SSH Library in Go.

Der Server ist die zentrale Anlaufstelle für die Clients, die auch hinter Routern stehen können.  
Diese bauen über HTTP eine Verbindung auf, über die dann SSH gesprochen wird.  
Über diese SSH Verbindung kann der Server den Client dann steuern,  
beispielsweise welcher Port wohin weitergeleitet werden soll.

Es lassen sich aber auch CLI Programme oder Skripte ausführen falls das Zielsystem dies unterstützt.  
Für Windows Systeme kann sogar die PowerShell verwendet werden.

# Management

Der Server beinhaltet eine API, die auch vom eingebauten Webinterface genutzt wird,  
in dem man eine Übersicht aller Clients, den Tunneln sowie weitere Metadaten vorfindet.

Das Webinterface unterstützt den Anwender auch damit,  
sich bequem auf dem Remotesystem einzuloggen.
Hier wird dann der lokale SSH, RDP oder VNC CLient gestartet.

Zusätzlich gibt es [rport-cli](https://github.com/cloudradar-monitoring/rportcli) um sich z.B. auch von der Shell aus eine Übersicht zu verschaffen  
oder automatisiert Tunnel zu erstellen.

# Sicherheit

Das Projekt bietet einige Mechanismen an um die Tunnel abzusichern.  
z.B. lassen sich ACLs setzen, damit auf ein Zielsystem nur bestimmte Clients dürfen,  
über Gruppen den Zugriff einschränken oder auch Befehle filtern, die auf Zielsystemen ausgeführt werden dürfen.

# Dokumentation

Mehr Info und Möglichkeiten findet man in der Dokumentation

- https://oss.rport.io/docs/
- https://kb.rport.io/

# Ausblick

In der [Vorstellung](https://programm.froscon.de/2021/events/2667.html) des Projektes
auf der [FroSCon](https://linuxnews.de/2021/08/konferenzen-froscon-am-21-und-22-august/)
wurde erwähnt, dass man Features wie das Fernsteuern wie von Teamviewer gewohnt
oder eine Art Ansible Framework zukünftig mitliefern will, damit man etwas mehr als nur Befehle oder Skripte ausführen kann.









