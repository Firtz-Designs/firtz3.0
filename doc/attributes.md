# firtz RC 3.0 -  Attribute im Feed

#### Allgemeine Angaben

Die folgenden Attribute sind Angaben deines Feeds. Sie werden im Unterordner (in der Demo mit Namen
"demo" hinterlegt) des Hauptordners "/feeds" hinterlegt und in der feed.cfg eingetragen.

`z.B.: /feeds/demo/feed.cfg`

**title:**

Schlicht und einfach der Titel Deines Podcasts

**subtitle:**

Untertitel deines Podcasts

**description:**

Beschreibung trifft es wohl nicht ganz. Eigentlich ist das mehr ein kurzer Anreißer, worum es geht.
Wie zum Beispiel: "Der großartige Podcast aus Koblenz".

**summary:**

Jetzt kannst Du sicher ausführlicher werden als in der description. Übertreibe es aber auch nicht.

**formats:**

Sag dem firtz welche Formate Du in Deinem Podcast haben wirst.
Das erste angegebene Format ist das Standardformat, das genutzt wird, wenn kein explizites gewählt wird.

Hier folgt eine Liste der unterstützten Formate. Unterstützt heißt nun nicht, dass im Player auf der
Webseite alle diese Formate angezeigt oder abgespielt werden können. Das heißt an der Stelle nur,
dass der firtz weiß, dass es sich bei diesem Format um eines handelt, das einen Feed erzeugen kann.
Die Formate sind auch die slugs für alle Angaben z.B. im Feed.

Aber auch in den URLs werden Dir diese Slugs jedes mal wieder begegnen. In Klammern stelle ich
sicherheitshalber dahinter, ob es sich um Audio oder Video handelt. Ein paar Formate sind beides nicht...

* mp3 (audio)
* mpg (video)
* m4a (audio)
* m4v (video)
* oga (audio)
* ogg (audio)
* ogv (video)
* webma (audio)
* webm (video)
* flac (audio)
* opus (audio)
* mka (audio)
* mkv (video)
* epub (ebook)
* mobi (ebook)
* pdf
* png (image)
* jpg (image)
* torrent (und nochmal: bitte nicht mit der bitlove-Option verwechseln!)


**bitlove:**

Wenn Du bei [bitlove](http://bitlove.org) Deine Feeds torrentifizierst, kannst Du hier - allerdings ausschließlich für
das Webseitentemplate - Downloadlinks dafür konfigurieren.

Das Format sieht wie folgt aus (das "_" ist hier als Leerzeichen zu vetrstehen):
<br>`<format>_<user>_<feedname>`

Wenn Deine Torrents also ungefähr so heißen:
<br>`http://bitlove.org/supicast/supicast-m4a/sc001.m4a.torrent`,

Dann sieht die Konfigurationszeile so aus:
<pre>
bitlove:
m4a supicast supicast-m4a
</pre>

*Info:
<br>Es können beliebig viele Formate konfiguriert werden. Verwechselt das bitte nicht mit einem torrent-Feed.
Das geht auch, funktioniert allerdings genau so wie die normalen Formate.
Du müsstest dafür in die *format:* Konfiguration "torrent" hinzufügen und in jeder Episode den
vollständigen Link zu einem Torrentfile angeben. So wäre auch ein Feed ausschließlich mit
Torrentlinks denkbar.*


**language:**

Dies ist die Sprache, in der der Podcast veröffentlicht, Deutsch z.B. wäre "de-DE". Info zu den Sprachcodes finden sich [hier](http://www.rssboard.org/rss-language-codes)

**explicit:**

Hast Du Schweinkram auf der Zunge? Dann schütze die Kinder!!eins1ELF!



#### Lizenzangaben

**licensename:**

Gib hier an, wie die Lizenz heißt, unter der Du Deinen Podcast veröffentlichst. Schau Dich doch mal bei den [Creative Commons](http://creativecommons.org/) um. Da findest Du bestimmt etwas.

**licenseurl:**

Unter dieser URL findet sich eine Erklärung Deiner Lizenz.

**licenseimage:**

Einige Lizenzen bieten Logos an. CC hat sowas und sollte ein Bild vorliegen: her damit! Sieht besser aus.


#### Angaben zum Impressum

Diese Angaben sind in Deutschland Pflichtangaben für den Feed und das Impressum.
Optionale Angaben werden für das automatische generieren des Impressums benötigt und kannst Du
auch direkt in der Seite "Impressum.html" ändern. Du findes die Angaben unter:

`/templates/default/pages/Rechtliches/Impressum.html`

**author:**

Wie heißt Du? Diese Information ist sicherlich wichtig...

**email:**

Unter dieser Mailadresse bist Du zu erreichen. Denk dran, dass hier etwas erreichbares steht,
schließlich will Dich vielleicht Apple für ein Feature anschreiben! ;-)

**street: (optional)**

Straße deines Wohnortes.

**city: (optional)**

Stadt in der Du wohnhaft bist

**country: (optional)**

Ich denke das versteht sich von selbst :P

**phone: (optional)**

Telefonnummer von Dir.

**fax: (optional)**

Wer so etwas noch besitzt.

**tax: (optional)**

Wenn Du mit deinem Podcast einen Cent verdienst dann solltest Du eine Umsatzsteuer ID bekommen haben,
bzw. benötigst Du eine in Deutschland. Gebe diese unbedingt an um rechtliches Schritte zu verhindern.

Wir haben euch hiermit Informiert und sind damit fein aus der Sache raus :-P



#### Podcast Poster / Covers

**image:**

Das Logo Deines Podcasts sollte entweder im Format JPG oder PNG vorliegen. Ideal ist aktuell eine Größe von 1400x1400 Pixeln. Bedenke bei Deiner Wahl aber unbedingt, dass dieses Bild in allen möglichen Größen genutzt wird. Es gilt also wie für jede gute Logogestaltung: Es muss auch in 32x32 noch gut aussehen!

**imageCreator:**

Michael McCouman Jr.

**imageURL:**

http://wikibyte.org

**imageLicense:**

CC0


#### Kategorien und Keywords

**keywords:**

Gib hier ein paar sinnvolle, kommagetrennte Stichwörter zu Deinem Podcast an. Diese Stichwörter helfen, Deine Werke später in den Podcastverzeichnissen zu finden.

**category:**
Die Kategorien orientieren sich an den Vorgaben Apples für iTunes. Es gibt Hauptkategorien und jeweils mehrere Unterkategorien, die aber keine weiteren Kategorien unter sich haben. Um dies an dieser Stelle einigermaßen einfach konfigurieren zu können, wird entweder eine Hauptkategorie einzeln angegeben oder eine solche mit Unterkategorie durch -> verbunden:

<pre>
    Society & Culture -> Philosophy
    Technology
</pre>

Diese Konfiguration würde den Podcast sowohl in die Hauptkategorie *Society & Culture* ohne weitere Unterkategorie setzen und in die Unterkategorie *Podcasting* in der Kategorie *Technology*. Die einzelne Angabe der Hauptkategorie *Technology* ohne *Podcasting* ist in diesem Falle nicht nötig. 
Details zu den Kategorien finden sich [hier](https://help.apple.com/itc/podcasts_connect/#/itc9267a2f12).

Es ist nicht nötig (und erlaubt!) das "&" als `&amp;` zu kodieren!



#### Soziale Netzwerke

**twitter:**

Nur das Twitter-Handle angeben, nicht den vollen Pfad zu Twitter, ohne @.

**Mastodon:**

Wenn Du auch bei Mastodon zu finden bist, dann gebe hier die komplette URL an.

**Facebook:**

Niemand mag so komisch aussehende blaue und Ajax verseuchte Netzwerke. Vielleicht magst Du es doch?
Dann gebe einfach deine Seite oder das Handel dafür ein:

Bsp.: vorname.nachname

**github:**

Hack Hack, Du weist schon. Wenn Du willst, dann gebe einfach deinen Username an :D

**itunes:**

Ist der Podcast bereits bei iTunes erreichbar, steht hier der komplette Link zur iTunes-Seite.
Den findest Du irgendwo auf genau dieser... frag mich nicht!

**itunesblock:**

Möchtest Du iTunes blockieren? Weil Du gerade am Feed rumspielst? Oder weil iTunes doof ist? Dann schalte das hier auf `on` und Ruhe ist.



#### Einstellungen des firtz

**mediabaseurl:**

Gibst Du dann an, wenn Du allen Mediendateien einen festen URL voranstellen möchtest. Das macht im Grunde nur Sinn, wenn die Dateien anhand des Namens der .epi-Datei erkannt und gefunden werden sollen. Das wiederum benötigt dann auch den:

**mediabasepath:**

Das ist der Ordner, in dem sich die Mediendateien befinden. Das ist nur sinnvoll, wenn Du in den .epi-Dateien nicht explizit auf die Mediendaten hinweist, sondern anhand des Dateinamens (==slug) diese finden lassen möchtest.

**redirect:**

Es kann natürlich vorkommen, dass Du den Feed umziehen musst. Anderes System, andere Domain, was auch immer. Um Deine Abonnenten nicht mit einem toten (alten) Feed alleine zu lassen, erzählst Du dem firtz, wo denn der neue Feed zu finden ist. Der führt dann ein redirect (301) aus, was im Allgemeinen auch diverse Dienste wie z.B. iTunes auf den neuen Feed führen sollte.




#### Einstellungen Feed

**rfc5005:**

Kein Mensch kennt den rfc5005. Aber Du solltest ihn mit `on` einschalten, wenn Du absehen kannst, dass Dein Podcast viele Folgen bekommt. Der Sinn dahinter ist, im Feed nicht mehr alle Folgen zu haben, aber eine Verlinkung zu eine Feed mit älteren Folgen. Leider unterstützen viele Podcatcher dieses Feature nicht. Habe dennoch Mut!

**baseurl:**

Dieses Attribut benötigst Du nur, wenn Du in einer Installation des firtz mehrere Podcasts unter unterschiedlichen Domains veröffentlichen möchtest. Wenn dieser eine firtz dann mit einer bestimmten Domain angesprochen wird, muss er ja wissen, wo es langgeht. Bitte gib hier den vollen URL mit Schema (also http://) an.

**feedalias:**

`format feedname oldfeed`

Das Problem war bei vielen Migrationen, dass frei benannte Feedadressen auf die neue Notation (/slug/format) umgestellt werden müssen.
Wenn man z.B. von Wordpress kommt und der alte MP3-Feed nach *http://supicast.de/feed/mp3* ging, der neue aber *http://supicast.de/sc/mp3* lauten soll, trägt man in dieser Zeile

`mp3 sc /feed/mp3`

ein. Es gibt dann einen 301er redirect und alles bleibt "beim alten". Entsprechend gut programmierte Podcatcher werden die neue Adresse dann übernehmen.



#### Einstellungen für Auphonic

**auphonic-path:**

Ich erkläre den auphonic-Workflow genauer in der Gesamtdokumentation. Hier sei nur erwähnt, dass unter auphonic-path der Pfad auf Deinem Server gemeint ist, unter dem die .json-Dateien gefunden werden.

**auphonic-glob:**

Wenn im auphonic-path die jsons mehrere Podcasts liegen, kannst Du mit diesem Pattern die für diesen Podcast nötigen jsons selektieren. Wenn die z.B. fasel00X.json heißen, die eines anderen Podcasts bla00X.json, gibst Du hier `fasel*.json` an.

**auphonic-mode:**

full, exclusive, episode oder off. Genauere Infos in der vollen Dokumentation.


#### Einstellungen des Themes

**articles-per-page:**

Dieses Attribut beschränkt die Anzahl der Episoden auf der Webseite(!). Standard sind 3 Folgen.

**template:**

Wenn Du zusätzlich zum Standardtemplate ein weiteres, ein Child-Theme nutzen möchstest, musst Du dieses hier anmelden. Bitte gib nur den Namen des Ordners an, nicht den vollen Pfad.

**templatevars:**

Je nach Template kann es Variablen geben, die die Ausgabe und das Verhalten des Templates steuern.
Diese werden, entgegen der üblichen Sitte mit einer einfachen Notation nach:
`key value` angegeben.

Für die Variablen des QuorX 3 Templates, schaue bitte in die entsprechende Dokumentation.







# Attribute in der Episode

**title**

Muss ich nicht erklären, oder? Ok, für Dich: Dies ist der Titel der Episode.

**date**

Optional das Veröffentlichungsdatum der Episode in der Notation `YYYY-MM-DD HH:MM:SS`. Wird das Datum weggelassen, erzeugt sich das Veröffentlichungsdatum aus dem Datum der letzten Änderung der Konfigurationsdatei.

Wird ein Datum in der Zukunft (relativ zur Uhrzeit des Servers) gesetzt, wird die Episode ignoriert und erst nach Erreichen dieser Uhrzeit angezeigt.

**subtitle**

Fasse den Inhalt hier kurz zusammen. Kurz! 255 Zeichen maximal, sonst gibt's Ärger!

**summary**

Eine kurze aber knackige Zusammenfassung zu deiner Episode. Du kannst hier Markdown verwenden. 
Beachte die mindestanzahl von 4000 Zeichen.

**shownotes**

Und hier kannst Du dann ausführlicher werden. Aber übertreibe es auch wieder nicht und vor allem lass die Finger von HTML und Co. Hier gehört ausschließlich Markdown rein! Wie das funktioniert, erklärt Dir u.a. [Wikipedia](http://de.wikipedia.org/wiki/Markdown).

**keywords**

Gib hier eine sinnvolle, kommagetrennte Liste der Stichwörter für die Episode an. Der firtz hat übrigens eine Suchfunktion, die in diesen Stichwörtern sucht. Also sei schlau und nutze das sinnvoll.

**duration**

Gib hier die Dauer der Episode an. Nutze dafür bitte die Notation `HH:MM:SS`. Du kannst ggf. auch abkürzen mit `MM:SS`.

**chapters**

Kapitel. Du willst Kapitel! Egal was die anderen sagen. Und auf die Amis hörst Du schon gar nicht. DU - WILLST - KAPITEL! Außer natürlich, die Episode dauert nur zwei Minuten. Das Format sieht so aus:

`HH:MM:SS Kurze Beschreibung des Kapitels <optionaler link> <optional URL zu einem Kapitelbild>`


**contributors**

Hast Du die extension unter `ext\contributors` installiert kannst Du deiner Episode, hinterlegte Nutzer hinzufügen.
Die Erweiterung ist als Standard deklariert und bei einer Erstinstallation schon vorhanden. Weiteres findest Du auch direkt in der Readme Datei: https://github.com/Firtz-Designs/firtz3.0/blob/master/firtz-2.9/ext/contributors/README.md

Du kannst so ganz einfach deinen Mitwirkenden einbinden. Beachte die Lehrzeichen (ohne Komma!):

`maxi maximusterfrau maxmustermann`


**image**

Wenn Du möchstest, kannst Du der Episode ein Bild verpassen. Gib dazu den kompletten Link an. Gibst Du das nicht an, wird das Logo/Poster des Podcasts aus dem Feed genutzt.

`https://raw.githubusercontent.com/Firtz-Designs/firtz3.0/master/firtz-2.9/feeds/demo/001-cover.png`


**banner**

Ab der Version 2.9 (Beta) kannst Du nun auch einen Banner für jede Episode vergeben. Das macht deine Webseite interessanter.
Möchtest Du das nicht, dann lasse die Part einfach weg :)

`https://raw.githubusercontent.com/Firtz-Designs/firtz3.0/master/firtz-2.9/feeds/demo/001-banner.jpg`


**bannerLicense**

Ab der Version 2.9 (Beta) ist es möglich, einem verwendetem Banner auch eine Lizenzangabe zu geben. Dies macht nur Sinn, wenn Du natärlich einen Banner vergeben hast. Gebe hier den Namen der verwendeten Lizenz an, wenn Du nicht die Rechte besitzt, es jedoch unter einer Lizent verwenden darfst.

`Free for all`


**bannerPage**

Ab der Version 2.9 (Beta) ist es möglich, einem Banner für deine Episode zu verwenden. Gebe hier den Linknamen der angezeigt werden soll. Er wird direkt mit der bannderURL verbunden und kann später angeklickt werden. Damit kannst Du auf die Lizenz hinweisen.

`From www.Pexels.com by icon0.com`


**bannerURL**

Ab der Version 2.9 (Beta) ist es möglich, einem Banner für deine Episode zu verwenden. Gebe hier den Link zum Original an, um wo möglich rechtliche Probleme zu vermeiden.

`https://www.pexels.com/de-de/foto/aussicht-baume-draussen-felsen-719609/`


**intro** und **outro**

Ab der Version 2.9 (Beta) ist es möglich, auch Lizenzangaben für dein Intro oder outro zu vergeben. Dies kannst Du separiert angeben in der feed.cfg oder wenn Du jede Episode einen anderen Trailer oder Soundbeitrag verwendest.

<pre>
    1         2                   3            4                           5
SoundName, John Dow, https://www.domain.tld, CC BY, https://creativecommons.org/licenses/by/3.0/de/`

Infos:
1 = Angaben zum Namen des Sounds
2 = MacherIn/ProduzentIn des Sounds
3 = Website Link zur Person oder Sounds
4 = Linzenz der Verwendung des Sounds
5 = Angaben als Link zur verwendeten Lizenz
</pre>


**noaudio**

Vielleicht passiert es einmal, dass Du einen Artikel auf der Webseite haben möchtest, der keine Episode Deines Podcasts ist. Du möchstest z.B. eine Urlaubspause verkünden. Dann gib hier `on` an, damit die entsprechende .epi-Datei nicht ignoriert wird.

