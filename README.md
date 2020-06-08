# firtz


*firtz - podcast publisher*
*Version 2.9.1 (Alpha)*

## Über firtz (RC2.9.1)

<pre>
Du hast offensichtlich den Drang, entweder diesen Kram hier auszuprobieren,
oder einen Podcast aus der Taufe zu heben. Was auch immer Dich dazu bewogen
hat firtz auszuprobieren: Gute Idee :)

Um einen Podcast zu veröffentlichen, reichen im Grunde zwei Dinge:
- Audiodateien im Web und irgendwo eine XML-Datei, die den Feed beschreibt.
- Alles andere ist Beiwerk, das mehr oder minder nötig und arbeitsintensiv ist.

Warum aber an vielen Stellen so viel Arbeit machen, so viel Ballast herumschleppen?
Wieso ein Wordpress, wenn man alle zwei Monate mal was veröffentlicht? Wieso eine
SQL-Datenbank für fünf Artikel in einem Jahr? Wieso sich den Kopf zerbrechen über
die Installation diverser Plugins, wenn es ein paar KByte XML tun?

Der firtz soll - wo möglich - dabei helfen, Podcasts den Druck zu nehmen, sich
um technische Details zu kümmern. Deshalb also firtz. Die 0.1 war das Ergebnis
von knapp einskommafünf Tagen "Arbeit", die ich eigentlich nur gemacht habe,
um mal wieder irgendwas zusammen zu schrauben, das halbwegs funktioniert.

Wie funktioniert das aber nun? Über Konfigurationsdateien. Eine für den Feed mit
allgemeinen Daten und einer Datei für jede Episode mit den Details eben jener.
Wer es ganz einfach haben möchte, verbündet sich mit Auphonic und überlässt alle
Daten, die dort anfallen dem firtz, der dann daraus einen oder mehrere Feeds erzeugt.
Einfacher wird's nur noch, wenn Auphonic selbst sowas anbietet ;)

-- eazy, 2013
</pre>

Change: M.C., 2019

## Voraussetzungen

Aber fangen wir vorne an. Was brauchst Du? Du brauchst irgendwo Platz im Web.
Das ist dann doch noch nötig. Dieser Platz im Web muss im Grunde nur eine
Bedingung erfüllen: **php ab Version 5.4.0** muss ausgeführt werden können.
Besser ist **php mit Version 7.3.x**. Datenbanken und anderen Kram braucht
es nicht, allerdings muss der ausführende Nutzer des Webservers in der Lage,
Verzeichnisse zu erzeugen und Dateien in diese hineinzuschreiben.

Sollte der firtz in einem Unterverzeichnis der genutzten Domain betrieben werden,
musst Du noch die .htaccess korrigieren und die RewriteBase von:
`RewriteBase /` auf `RewriteBase /UNTERORDNER` zu ändern.

Es gibt übrigens hier und dort Probleme mit dem Schreiben in das temporäre
Verzeichnis. Je nach Webhoster kann es nötig und hilfreich sein, den Handler
für php auf (fast-)cgi zu stellen. In der .htaccess geht das z.B. mit dieser
Zeile:  `AddHandler php5-cgi .php`

Das sollte allerdings wirklich nur passieren, wenn der firtz diesbezüglich
Fehlermeldungen auswirft.

Change: M.C., 2020

## Los geht's

Du besorgst Dir das [firtz-Archiv](https://github.com/Firtz-Designs/firtz3.0),
entpackst es in den Ordner, in dem Du das auf dem Webserver haben willst und
bewegst Dich darauf hin in den Unterordner `feeds/`. In diesem findest Du
ein Demo-Verzeichnis. Der Name dieses Ordners, ist der zukünftige Name
Deines Feeds. Im Demo-Ordner sind vier Typen von Dateien: `feed.cfg`,
`001.epi`, `001-banner.jpg` und `001-cover.png`. Letzere sind Banner und
(wenn Du es bevorzugst) Episoden Bild für jede Episode extra.

Die `feed.cfg` ist Deine Feed Datei mit allen Grunddaten die dein Podcast
benötigt. Die `001.epi` ist die Datei für eine Episode. Du solltest darauf
achten, das jede Datei **möglichst mit Zahl** abgebildet wird. Du kann auch
etwa so aussehen: `001-TolleEpisode.epi`


Das nicht syntaktisch zu nennende Prinzip dieser Dateien ist identisch:

`#: ist ein Kommentar nicht den ":" vergessen!`

Attribute werden wie folgt notiert:

<pre>
attribute:
value
</pre>

Achtet bitte darauf, dass die Attribut-Zeile alleine steht. Leerzeilen
werden ignoriert, es sei denn, es geht um eine Textfeld wie summary.
An's Ende der Konfiguration kannst Du in einer neuen Zeile ein

`---end---`

setzen, alles dahinter wird ignoriert. Du kannst da Notizen oder Müll
unterbringen. Ich werde das hier im Moment noch nicht weiter ausbreiten.
Schau in die Dateien und spiel damit rum.

**Wichtig ist, dass alle Konfigurationsdateien UTF8 sind, denn sonst gibt's
Müsli im Feed!**

Solltest Du [Auphonic](http://auphonic.com/) nutzen, bist Du ganz fein raus.
Aktiviere in den Ausgangsdateien dort die Production-Description,
sorge dafür, dass firtz sie im Dateisystem findet und schon erstellen
sich die Folgen fast von selbst anhand der von Auphonic weitergereichten
Metadaten. Weitere Informationen dazu finden sich in der weiterführenden
Dokumentation.

Nehmen wir an, Du hast das soweit fertig. Wie erreichst du den Feed?
Angenommen der URL zu Deinem Webserver wäre `http://tollerneuerpodcast.de/`.
Der Feed heißt ja noch `demo`, also wäre der URL zum RSS2-Feed:
`http://tollerneuerpodcast.de/demo`

Wenn Du mehrere Audioformate nutzt, kannst Du auch die URL je Format nutzen:
`http://tollerneuerpodcast.de/demo/mp3`.

Eine Webseite gibt es als Bonus automatisch dazu. Die kannst Du für dieses
Beispiel dann so erreichen: `http://tollerneuerpodcast.de/demo/show`

Für jede Episode gibt es einen eigenen [Podlove Webplayer](https://github.com/gerritvanaaken/podlove-web-player).

Einzelne Episoden sind auch verlinkbar, indem an den Pfad der Slug der
Episode (praktisch der Dateiname ohne Endung) angehangen wird:
`http://tollerneuerpodcst.de/demo/show/001`.

## Das Theme und Layout: QuorX 3

QuorX ist einfach veränderbar. Du findest die Einstellungen unter:
`/templates/default/template.cfg`. Ich habe Euch schon beschrieben, welche
Einstellungen Ihr machen könnt, um Teile des Designs zu verändern.

Hier also ein paar Beispiele.

### Breite des Themes (Box/Full)

**layout: box**

<img src="https://raw.githubusercontent.com/Firtz-Designs/firtz3.0/master/doc/img/screen1.png">

**layout: full**

<img src="https://raw.githubusercontent.com/Firtz-Designs/firtz3.0/master/doc/img/screen2.png">


### Farbe des Themes

Ich habe euch schon einige Farbthemen als Beispiele beigelegt.
Selbsterklärend, könnt Ihr so euer eigenes Farbschema entwerfen.

<pre>
color #31424b     (Player)
light #81b55e     (Buttons und Icons)
dark  #2c3b43     (Links & Hintergrund)
</pre>

<img src="https://raw.githubusercontent.com/Firtz-Designs/firtz3.0/master/doc/img/screen3.png">

Bitte achte darauf: Es sind diese Farbangaben auch in der feed.cfg
unter: `/feeds/<demo>/feed.cfg` möglich. Sind hier Angaben hinterlegt,
dann gelten diese immer als gesetzt.

Es gibt noch viele weitere Angaben zu entdecken die Du setzen kannst,
um dem Quorx3 Theme einen eigenen Look zu verpassen.

Viel Spaß dabei!

-- Stand: 08.06.2020 by McCouman


## Twitter Kontakte

- Developer: [@eazy](https://twitter.com/eazyliving)
- Developer: [@mccouman](https://twitter.com/mccouman)


## Links

- Theme: [QuorX 3](https://github.com/Firtz-Designs/QuorX-III)
- Framework: [fat free framework](https://github.com/bcosca/fatfree)
- Componense: [Podlove Webplayer](https://github.com/gerritvanaaken/podlove-web-player)
