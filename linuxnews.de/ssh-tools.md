# ssh-tools - den Alltag mit OpenSSH bequemer machen.

OpenSSH, das Schweizer Taschenmesser des Admins
für den täglichen Remotezugriff.

Das Projekt liefert einzelne Tools mit,
die einfach zu benutzen sind und als sehr sicher gelten.

Man kann sie daher in die Kategorie
[1] "Keep It Simple and Secure" einordnen.

Das bedeutet aber nicht,
dass der Alltag damit auch immer bequem ist.

Wer kennt es nicht, der begehrte Server
steht hinter einem JumpHost
oder man muss erst durch einen VPN Tunnel.

Oder beides.

Nun muss der Weg dorthin angepasst werden,
z.B. die Umstellung des VPN Tunnels zum Kunden.

Ab hier fängt die mühsame Dauerschleife an:

Der Kunde meldet Vollzug auf seiner Seite
und selbst hat man seine VPN Config auch schon angepasst,
ein Login Versuch via SSH schlägt aber noch fehl:

- Eigene Firewall Regeln nochmal geändert.
- Der nächste manuelle Login Versuch.
- Geht immer noch nicht.
- Kunde anschreiben
- Kunde meldet sich irgendwann später. Nochmal probieren...
- Nächster manueller Loginversuch.
- Tut sich nix.
- ...

Einen normalen Ping nebenher in einem Terminal laufen lassen
um das Prozedere zu vereinfachen, ist hier leider nutzlos,
da ein JumpHost dazwischen steht.

Den ICMP Echo Request leitet dieser nicht weiter.
Außerdem wollen wir wissen, ob der SSH Zugriff geht - nicht ein Ping.
Ein Check auf Port 22 z.B. mit Netcat bleibt hier auch wirkungslos.

Hier kommen nun die [2] ssh-tools ins Spiel,
die das KISS Prinzip um [3] CISS erweitern.

Die ssh-tools sind Wrapper-Skripte um den OpenSSH Client,
die vieles bequemer machen.

Für das oben beschriebene Problem gibt es z.B. *ssh-ping*,
das prüft, ob ein SSH Server auch wirklich erreichbar ist.

Das funktioniert sogar durch JumpHosts hindurch,
vorrausgesetzt diese sind über die SSH Config eingerichtet.

Damit kann man sich nun in Ruhe auf seine VPN, Firewall oder SSH Config konzentrieren,
und parallel auf ssh-ping schauen, ob die Anpassungen fruchten.

## Weitere Tools

Neben ssh-ping gibt es noch weitere Tools,
die das Admin Leben versüßen:

1) ssh-version: Zeigt die Version des SSH Servers an

2) ssh-diff: Eine Datei über SSH diffen

3) ssh-facts: Basisinfo über das Remotesystem anzeigen

  ( z.b. Welche Distro ist installiert )

4) ssh-hostkeys: Die Fingerprints der HostKeys in verschiedenen Formaten ausgeben

5) ssh-keyinfo: SSH PublicKeys in verschiedenen Formaten ausgeben

   (alte SSH Server schreiben z.B. noch MD5 Fingerprints ins Syslog)

6) ssh-certinfo: Zeigt an, ob und wie lange SSH Zertifikate (nicht PublicKeys) noch gültig sind.

   (Damit kann man z.B. monitoren, ob SSH Zertifikate erneuert werden müssen.)

7) ssh-force-password: Erzwingt bei PubKey Authentifizierung die Passwort Abfrage

   (z.B. um Passwort Änderungen zu testen)

## Pakete

Die ssh-tools sind mittlerweile für die gängigen Distibutionen [4] paketiert,
können aber auch direkt von Github runtergeladen und ausgeführt werden.

## Links

[1] https://de.wikipedia.org/wiki/KISS-Prinzip  
[2] https://github.com/vaporup/ssh-tools  
[3] https://github.com/vaporup/CISS  
[4] https://repology.org/project/ssh-tools/versions  
