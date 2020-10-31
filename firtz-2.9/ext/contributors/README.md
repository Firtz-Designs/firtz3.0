# contributors extension firtz

Diese Erweiterung bringt Teilnehmer und ihre Daten in den firtz.

Die Konfiguration ist ein wenig aufwändig, das liegt aber mehr an der Komplexität der Materie.

Das ganze geht wie folgt: 
1.) Extension installieren (in Ordner /ext verschieben oder hochladen). 
2.) Dort im Ordner "ext/contributors/data" für jeden Teilnehmer eine Datei anlegen; z.B.: eazy.cfg oder mccouman.cfg.

In der jeweiligen .cfg stehen dann die Daten der Nutzer:

```
type:             <- über den Typus kann festgelegt werden, ob es sich um die Teammitglieder handelt oder um einen Gast/Gästin
team

name:             <- Name der Person mit Vor- und / oder Nachnamen (Dieser wird öffentlich angezeigt!)
Nachname Vorname

description:      <- Kurze Beschreibung zur Person, z.B.: Beruf oder Hobbyist (Bitte unbedingt kurz halten!)
Podcaster

image:
https://domain.tld/benutzername_400x400.png

#: Netzwerke

mail:             <- Um Spam zu vermeiden solltest Du überlegen ob Du diese hier wirklich eingeben möchtest!
mail@domain.tld

mastodon:
https://bildung.social/@mccouman

twitter:
nvorname

github:
nvorname

url:
https://www.domain.tld
```

In jede Episode nun mittels **contributors:** eine Zeile mit allen Teilnehmern hinzufügen:

```
contributors:
eazy mccouman tina
```


Dieses Beispiel zeigt nun auch, was bisher möglich ist. Das template ist noch nicht schön, tut aber was es soll.
