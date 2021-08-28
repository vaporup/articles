# Erfahrungsbericht: Reise zu GNU/Linux von Sven

## Anfänge

Meine Reise zu GNU/Linux begann, als mir meine Mutter einen [Schneider PC](https://retroport.de/schneider-cpc-serie/)
auf den Tisch stellte.  
Sie musste geahnt haben, dass hier ein SysAdmin-by-Nature heranwuchs.

Der PC kam mit einem gedruckten Handbuch, in dem u.a. BASIC Programme standen, die geometrische Figuren auf dem Bildschirm malten.
Hier machte ich die ersten Programmiererfahrungen durch Anpassen von Werten oder Anweisungen.
Leider musste man den ganzen Code manuell vom Buch abschreiben, konnte es aber nicht speichern.
Wenn der Computer aus war, durfte man wieder alles nochmal abtippen.

Spiele gab es auf Audio-Kassette, die jedoch sehr lange laden mussten :-)  
Die Kassette mit den besten Spielen hat mein Kumpel dann mal versehentlich beim Steinehüpfen
in den See entsorgt.  
War dafür aber der beste Wurf...

## Grundsteine

Nach kurzen Ausflügen über Amiga 500 und Commodore 64
kam dann der erste 486 PC mit MS-DOS ins Haus.  
Diesmal aber nicht für mich sondern meinen Vater.
Darauf lief seine Warenwirtschafts-Software (in Batch geschrieben).

Nachdem ich so mutig war und **command.com**, **autoexec.bat** sowie **config.sys**
mit dem Satz "Kenn ich net, weg damit..." entsorgt hatte,  
wurden damit die Grundsteine für das spätere Admin Leben gelegt,
da ich durch das Lesen des **guten** Handbuchs (RTFM: Read the **fine** manual)
erstmal verstanden habe, wofür diese Dateien da waren und sie dann wieder rekonstruieren konnte.

Hat zwar ein paar Tage gedauert, aber so lernte man, Systeme zu fixen...

### CLI

Die Kommandozeile hatte mich schon in MS-DOS sehr fasziniert
(vor allem die ganzen Komprimierungsprogramme wie ARJ und wie sie alle hießen)
und die Liebe zum Terminal war dann auch später der Einstieg zu Linux sowie der ersten Admin Stelle.

## Zwischenstationen

Während ich im ganzen Dorf jedem half seine DOS Start-Dateien zu optimieren
damit Spiele flüssiger laufen bzw. überhaupt starten,  
machte ich alle aufkommenden Windows Versionen ab 3.11 bis Windows 95 mit,
bis es Zeit wurde mir einen Ausbildungsplatz zu suchen.

Zu dem Zeitpunkt waren die Fachinformatiker Berufe gerade erst am entstehen,  
sodass ich erstmal eine Ausbildung zum Industrie-Mechaniker bei Daimler machte.

Parallel dazu natürlich weiter in der IT-Welt gewurschtelt
und vieles davon auch im Betrieb nutzen können.  
Während viele meiner Ausbildungskollegen an der CNC Maschine
noch Werkzeuge vermessten, liefen meine schon mit CNC Programmen
und hatte daher Zeit anderen Kollegen zu ihren PC Problemen zu beraten.

## Einstieg

Mittlerweile bei Windows XP angekommen, zog ein früherer Sport-Kollege gegenüber ein: "Der Linux Freak".

Selbst hatte ich schonmal SUSE 6.3 ausprobiert aber wieder entsorgt,  
da CD Brennen Arsch-lahm gegenüber Windows war (ich wusste noch nix von DMA und hdparm).

Der Nachbar meinte, ich soll Debian nehmen, also CD gebrannt und installiert.

Nach dem Booten blinkt mich aber nur ein Cursor an.  
Obwohl mir die CLI von DOS nicht fremd war, stand ich erstmal blöd da
mit den Worten:

"Kommt da keine grapische Oberfläche? Was nu?"."  

"Tz... Debian, das ist mir viel zu schwer", dachte ich mir dann nur.
Also auch erstmal links liegen lassen.

In der Zwischenzeit hatten ich und mein Kumpel uns dann
mit 1-Floppy Routern wie [fli4l](https://www.fli4l.de) und [anderen](http://www.fredshack.com/docs/floppyroutersfw.html) die Zeit vertrieben.  
Das war relativ einfach und konnte meist von Windows aus erledigt werden.

Einige Zeit später drückte mir der Debian Nachbar dann aber eine CD in die Hand  
mit der Aufschrift "Gentoo Linux" und meinte "probier das mal aus".

Im Nachhinein gesehen eigentlich nicht die optimale Einsteiger Distro  
aber Gentoo hat es damals geschafft durch sein sehr ausführliches Handbuch, dass ich ein laufendes System hinbekam.

Zwar erstmal alles nur abtippen ohne zu verstehen, was diese Befehle tun (erinnerte mich an die Schneider BASIC Zeiten)  
aber es bootete ein komplettes Linux System mit Enlightenment als Oberfläche und das war schon ein tolles Erfolgserlebnis.

## Fortschritte

Nach ca. 6 Monaten Gentoo sowie viel Lesen und Ausprobieren, ergab sich, wie es der Zufall so will,
eine Ausbildungstelle zum Fachinformatiker in der Firma des Debian Nachbarns.

Eigentlich wollte ich ja schon immer in der IT arbeiten, also: **Challenge accepted**

Während ich im Tagesgeschäft immer besser wurde, kaputte Windows Desktops und Server zu fixen (Danke [Mark Russinovich](https://docs.microsoft.com/de-de/sysinternals/downloads/sysinternals-suite)),  
oder Kunden half einen [VDR](https://de.wikipedia.org/wiki/Video_Disk_Recorder) zu Hause einzurichten,
lief nachts die Linux Weiterbildung im dunklen Keller des Nachbarn.

Zu der Zeit gab es noch kein Astaro, pfSense und wie sie alle heißen  
und daher wurde in vielen Nächten das eigene Router System für Kunden konzipiert.

Dazu musste aber erstmal viel gelesen und gewurschtelt werden.

Viele Nächte bestanden nur aus Man-Pages lesen wie z.B. IPTables oder in Mailinglisten zu wühlen wie man den [pppd](https://en.wikipedia.org/wiki/Point-to-Point_Protocol_daemon) robuster macht.  
Es ging sogar mal eine ganze Woche nur dafür drauf, dem qmail SMTP-AUTH beizubringen...

Hier hatte ich vieles zu Linux gelernt, aber auch wie wichtig Pragmatismus ist.  
Die übertriebenen Sicherheitsvorstellungen des Projektleiters waren für das Produkt leider sehr kontraproduktiv...

Parallel lernte ich nicht nur Linux sondern auch die komplette Geschichte dahinter  
und zwar die mit [Stallman](https://de.wikipedia.org/wiki/Richard_Stallman) (auch ihn traf ich später zufällig), [GNU](https://www.gnu.org/home.de.html), etc statt nur den kleinen Teil von Linus Torvalds.

Das bewegte mich auch dazu eine Linux User Group in der Nähe aufzusuchen.  
Den Gründer der LUG sollte ich später nochmal treffen.

Mittlerweile war ich in Debian relativ fit und Ubuntu erblickte das Licht der Welt.

Interessant war eine Video Reihe von Ubuntu Mitgliedern, eine Art FrOSCon, in dem sich einige persönlich vorstellten.  
Einer davon blieb mir sehr in Erinnerung, und auch ihn sollte ich später ebenfalls nochmal treffen.

## Zu den Profis

Der Arbeitskraftnehmer hat mich und alle anderen Azubis nach der Ausbildung dann entsorgt,  
sodass ich für kurze Zeit nochmal zu Daimler bin zum CNC-Fräsen.

In der Mittagspause las ich dann Bücher wie "Backup Tools for Linux"  
und Kollegen kommentierten dies nur mit rümpfender Nase: "Brauch man sowas?".

Mit der Antwort "Ich schon, da ich Admin werden will" konnte man nichts anfangen.

Während man mich an den Wochenenden verheizte, schrieb ich die ersten Bewerbungen für SysAdmin Stellen  
und bekam auch schon bald die ersten Einladungen.

Schließlich fand ich eine Firma, die einen Linux-Admin suchte und beim  Vorstellungsgespräch  
betrat dann das Zimmer zuerst der IT Leiter der Firma, der, **oha**, wie es der Zufall mal wieder wollte, der Gründer der Linux User Group war.

Er hatte mich ebenfalls erkannt und so entspannte sich das Bewerbungsgespräch sofort.

Der Team-Leiter, der dabei war, hat mir später noch gesagt, dass er mich eigentlich  
nur eingeladen hatte (damals kannte ich noch nicht "Das IT-Karrierehandbuch"),  
weil in der Bewerbung der Satz stand: "Kommandozeile bevorzugt" (er war auch ein Terminal Liebhaber).

## Hey, dich kenn ich doch

Nachdem mich die Firma einstellte, stand ein paar Monate später
jemand an meiner Büro-Tür und fragte nach dem Team-Leiter.

Als ich ihn anschaute, meinte ich nur "Hey, dich kenn ich doch. Du bist doch bei Ubuntu".

Wie es der Zufall mal wieder wollte, war es einer der Ubuntu Paket Maintainer,
den ich bei den Ubuntu Videos gesehen hatte.  
Hier in der Firma war er als Senior-SysAdmin eingestellt, in dessen Team in dann wechselte  
und von dem ich dann viel lernen durfte und dieses Wissen heute gerne weiter gebe (zumindest denen, die es interessiert).

## Komm doch vorbei

Irgendwann wollte ich selbst Paket-Maintainer für Debian werden am besten für ein GNU Projekt
und suchte noch eine Software, die noch nicht paketiert wurde und mich selbst auch interessierte.
Als ich eine [fand](https://www.gnu.org/software/recutils/), passte alles zusammen.
Das Projekt selbst gehörte zum GNU Projekt, der [Entwickler](http://www.jemarch.net/cv.html) ist der Gründer von GNU Spanien
und als ich ihm erzählte, dass ich ein Fan von Stallman und GNU bin, meinte er nur:

"Der kommt morgen zu mir zum Essen. Komm doch vorbei".

Und so war ich dann mit Stallman und ihm am Wochenende in einer Pizzeria in Frankfurt. 

## Heute

- Nach vielem Distro-Hopping verwende ich nun seit vielen Jahren nur noch Debian (das mir Anfangs zu schwer war :-) ).
- Windows habe ich eigentlich nur noch für ein paar Steam Spiele.
- GNU und Freier Software bin ich immer noch sehr nahe und versuche zurück zu geben, wo ich kann

## Tipp zum Schluss

Selbst habe ich keinen Informatik Abschluss, habe aber als Autodidakt trotzdem selbst viel **studiert** und **probiert**.  
und empfehle daher jedem Columbo's [Ratschlag](https://www.youtube.com/watch?v=OC-IxaEadns).
