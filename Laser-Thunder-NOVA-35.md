![DRAFT](https://img.shields.io/badge/Status-ENTWURF-red.svg)

**Todo**

- Lasern
	- Allgemein
		- Bedienelemente
	- Start des Laserprogramms
	- Paramerter prüfen/anpassen
		- Geschwindigkeit, Power, Zuluft, ...

---------------------------------------------

# Laser Thunder NOVA 35

## :warning: Sicherheitshinweise

:no_entry_sign: Arbeiten am Laser dürfen nur nach vorheriger Einweisung ausgeführt werden!

- Während der Laser läuft, immer dabei stehen bleiben
- CO² Feuerlöscher steht für den Brandfall neben der Maschine
- Notaus-Knopf befindet sich rechts oben auf der Maschine
- Bei einigen Materialien können bei der Verarbeitung giftige oder Dämpfe entstehen

## Inhaltsverzeichnis

- [Sicherheitshinweise](#warning-sicherheitshinweise)
- [Allgemein](#allgemein)
	- [Technische Daten](#technische-daten)
- [Material](#material)
- [Daten aufbereiten](#daten-aufbereiten)
	- [Mapping](#mapping)
	- [Toleranzen](#toleranzen)
- [Laser](#laser)
	- [Ein-/ausschalten](#ein-ausschalten)
	- [Daten an Laser senden](#daten-an-laser-senden)
	- [Material einlegen und fokusieren](#material-einlegen-und-fokusieren)
	- [Startposition festlegen](#startposition-festlegen)

	- [Manuelles Schneiden](#manuelles-schneiden)
- [Sonstiges](#sonstiges)
	- [Schmauchspuren (vermeiden)](#schmauchspuren)
- [FAQ](#faq)
- [Links zu weiterführender Dokumentation](#links-zu-weiterführender-dokumentation)

## Allgemein

### Technische Daten

| Arbeitsfläche        |  900 x 600 mm |                    |
| Tischgröße           | 1000 x 730 mm |                    |
| Z-Höhe               |        230 mm | max. Materialdicke |
| max. Materialgewicht |         40 kg |                    |

## Material

:skul: Nicht jedes Material kann und darf mit dem Laser bearbeitet werden. Diverse Kunststoffe entwickeln unter Hitze giftie Gase und/oder Säuren.

:warning: Zur eigenen Sicherheit und der anderen Benutzer im FabLab sollte nur **Acrylglas (Plexiglas, PMMA)** verwendet werden. Zu vermeiden ist auch "Bastelglas" aus dem Baumarkt.

Ansonsten lässt sich (fast) jedes organische Material mehr oder minder problemlos bis zu einer Dicke von ungefähr 8 mm verarbeiten.

Für Holz (z.B. Sperrholz Birke) gilt, dass **B-Qualität** vollkommen ausreichend ist. Beim Kauf sollte man auf **Laserqualität** achten, da hier keine ungewollten Einschlüsse, wie z.B. Kleber bei "Löchern" zwischen den einzelnen Materialschichten, vorhanden sind.

Weitere nützliche Informationen zu Materialien sind unter anderem auf den [Wiki-Seiten des FabLab Nürnberg][MöglicheMaterialien] zu finden.

## Daten aufbereiten

Für die Erstellung der zu lasernden Daten kann jedes beliebige Programm verwendet werden welches Vektoren z.B. als SVG exportieren kann.
Die Mehrzahl von uns verwendet [InkScape][InkScape], da es eine Integration mit dem Laserprogramm [VisiCut][VisiCut] gibt.

Auch das Lasern von Bild-/Bitmapdaten ist möglich, z.B. wenn graviert werden soll.

Aufbereitete Daten mit zugewiesenem [Mapping](#mapping) können mit [VisiCut][VisiCut] direkt [an den Laser gesendet](#daten-an-laser-senden) werden.

### Mapping

Alle definierten Profile werden in der Reihenfolge abgearbeitet, wie diese im Mapping in [VisiCut][VisiCut] definiert wurden. Sinnvollerweise beginnt man mit dem gravieren und markieren, zum Schluss schneidet man. 

Geschnitten wird nach dem Prinzip "Inside-Out", also immer von innen nach außen.

Für die unterschiedlichen Bearbeitungsmöglichkeiten durch den Laser wird folgendes Mapping (Profil zu Farbe) vorgeschlagen.

| Profil       | VisiCut    | Farbe    | Typ            | Hinweise                                               |
|--------------|------------|----------|----------------|--------------------------------------------------------|
| 3D gravieren | engrave 3d | andere   | Fläche, Bitmap |                                                        |
| gravieren    | engrave    | schwarz  | Fläche, Bitmap | Auflösung um die 200 dpi ist meist ausreichend         |
| markieren    | mark       | grün     | Linie          | Linien oder Konturen werden nur oberflächlich markiert |
| ignorieren   | ignore     | blau     | -              |                                                        |
| schneiden    | cut        | rot      | Linie          | Material-Parameter zum (Durch)Schneiden setzen         |

### Toleranzen

Sollen Teile passgenau gefertigt werden, ist die Breite des Laserstrahls mit ~0,2 mm bereits bei der Datenerstellung zu berücksichtigen.

## Laser

### Ein-/ausschalten

#### Einschalten

1. Kompressor für Laser-Zuluft einschalten (Dreierblock Sicherungen im Sicherungsschrank neben der Theke)
2. Abluft im Nebenraum einschalten (Wippschalter an der Steckdose)
	- Motorgeräusche sind zu hören (evtl. dauert es kurz)
3. Laser einschalten (rechts unten), Hauptschalter und die beiden Wippschalter müssen auf 1 stehen
4. Roten Reset-Knopf drücken (oberhalb des Displays) - Signallampe wird grün, interner Rechner wird gestartet
5. Dateien können übertragen werden

#### Ausschalten

Das Ausschalten erfolgt in umgekehrter Reihenfolge zum [Einschalten](#einschalten).


### Daten an Laser senden

Daten sollten nur an den Laser gesendet werden, wenn man an der Maschine steht. Möglicherweise bedient gerade ein anderer den Laser und bekommt nicht mit, dass "fremde" Daten übermittelt wurden...

Mit [VisiCut][VisiCut] sendet man die Daten an den Laser. Wichtig vor der Übermittlung ist, auf das Mapping sowie das zu lasernde Material (inkl. Stärke) zu achten, damit am Laser die richtige Geschwindigkeit sowie die korrekten Energie (Power) Werte eingestellt werden.

An den Laser gesendete Daten sammeln sich im Speicher und werden nicht automatisch gelöscht. Maximal 100 Dateien kann der Speicher beinhalten und muss dann bereinigt werden, um neue Daten anzunehmen.

### Material einlegen und fokusieren

#### Material einlegen

Wenn ein Material eingelegt wird, muss darauf geachtet werden, dass die Laseroptik weit genug über dem Material steht, damit kein Schäden beim Verfahren oder Einlegen entstehen (siehe [Material fokusieren](#material-fokusieren)).

#### Material fokusieren

Um einen Crash der Laseroptik zu vermeiden, muss das Material korrekt fokusiert sein. Ein positiver Nebeneffekt ist eine saubere Schnittkante, da der Brennpunkt durch die Fokusierung auf die Oberfläche des Materials gesetzt wird.

Dazu fürht man folgende Schritte aus:

1. Darauf achten, dass **genügend zwischen Laseroptik und Material** ist, ggf. den Tisch nach unten fahren
2. Material flach auf den Tisch legen
3. `Z/U` drücken, das öffnet das Menü
4. `Auto focus` auswählen und `Enter` drücken
5. Tisch fährt automatisch hoch/runter

Zwar kann in VisiCut ebenfalls ein Wert für den Fokus eingegeben werden, jedoch sind das nur Korrekturwerte. Sie beziehen sich auf die fokusierte Optik an der Maschine und stellen relative Änderungen dar. Der Wert sollte immer auf 0 mm stehen!

### Startposition festlegen

Nachdem das Material fokusiert wurde, muss die Startposition des Lasers gesetzt werden. Dazu fährt man den Laser (roter Punkt) an den gewünschten Punkt auf dem Material.

Der Startpunkt ist immer die linke obere Ecke. Auch in VisiCut muss der Nullpunkt (Position) auf die linke obere Ecke gesetzt sein - evtl. Daten noch mal übertagen!

So setzt man den Startpunkt:

1. Startposition ist, wie in VisiCut eingestellt, immer die linke obere Ecke
2. Positionierung durch...
	1. manuelles verschieben des Materials
	2. verfahren des Laseroptik mit den Cursortasten
3. Button `Start Position` drücken
4. `Box` drücken, um die äußeren Konturen der Daten visuell abzufahren
5. (optional) Neupositionierung: Zurück zu Punkt 2.

Punkt 4. dient zur Kontrolle, ob die Startposition passt und die zu lasernden Daten auch vollständig auf das Material passen





	### Programm starten/stoppen
		Sind die Daten am Laser angekommen und alle Vorbereitungen getroffen, sollte vor dem Start des Programms noch einmal kontrolliert werden, dass rechts oben im Display auch der eigene Dateiname steht.

	### Unterbrechung, Fortsetzen
	### Änderung der Werte (Geschwindigkeit, Energie, Zuluft, ...)

	### Bedienelemente 





### Manuelles Schneiden

Große Materialstücke können auch manuell mit dem Laser getrennt werden. Dazu platziert man das Material im Laser und richtet es ein (fokusieren).

Wichtig beim manuellen Schneiden ist, dass die Zuluft von Hand eingeschaltet werden muss.

1. Deckel schließen
2. Reset-Knopf drücken
3. An Startposition fahren
4. Bei Bedarf die Werte für Geschwindigkeit und Power anpassen
5. Zuluft einschalten - Knopf links am Laser für 5 Sek. drücken
6. _Laser_ Button an Display drücken und halten
7. Laserstrahl mit Cursortasten am Display entsprechend verfahren

## Sonstiges

### Schmauchspuren

Schmauchspuren auf der Unterseite eines Werkstücks entstehen, wenn der Laser auf die Wabenstruktur des Tisches auftrifft.

#### Schmauchspuren vermeiden

Um Schmauchspuren zu vermeiden oder zu vermindern, gibt es unter anderem folgende Möglichkeiten:

- Werkstück erhöht lagern, so dass kein direkter Kontakt zur Wabenstruktur vorhanden ist. Auf sicheren Halt des Werkstücks achten!
- Papier unter zu schneidendes Werkstück legen, ca. 80% der Schmauchspuren bleiben am Papier anhaften und nicht am Werkstück
- Abdeckfolie bzw. Abdeckpapier aufbringen - z.B. hier: [Abdeckfolie, Papier-weiß](https://www.cameo-laser.de/shop/index.php?route=product/product&path=60&product_id=95)

##### Weitere Informationen

Weitere Informationen über optimiertes CO2-Laserschneiden finden sich im Artikel [Perfekte Schnittkanten mit pfiffiger Absaugung](https://www.maschinenmarkt.vogel.de/perfekte-schnittkanten-mit-pfiffiger-absaugung-a-509280/)

> **Je schneller die Absaugung, desto geringer die Nacharbeit**
> 
> Technische Einrichtungen zur Absaugung von Rauchgasen sind bei modernen Lasersystemen der Standard. 
> Dass die Art und Weise der Absaugung allerdings Einfluss auf die Schnittkanten hat, ist nicht jedem gleich klar.
> Je nach Werkstoff entsteht beim Schneiden Schmauch, der zu unerwünschten Verfärbungen 
> respektive Ablagerungen an der Schnittkante führt. Um aufwendige Nacharbeiten zu vermeiden, 
> muss dieser Schmauch schon bei der Entstehung evakuiert werden – je schneller, desto besser. 
> Die Absaugung muss also direkt am Schnittspalt erfolgen. Gute Absaugtechniken saugen die Gase nicht ausschließlich 
> nach unten weg, sondern gleichzeitig nach oben, und das möglichst gleichmäßig und parallel zum Laserstrahl.

## FAQ

Nachfolgend die häufigsten Fragen und Antworten im Umgang mit dem Thunder Laser NOVA 35.

**Wieso startet der Laser nicht, wenn ich auf "Start-Pause" drücke?**  
Wahrscheinlich leuchtet die Lampe noch rot. Deckel schließen und auf den Reset-Knopf drücken. Bitte auch die Anzeige auf dem Display beachten, evtl. muss hier noch ein Dialog bestätigt werden.

**Wieso leuchtet die rote Lampe?**  
Vermutlich ist oder war der Deckel geöffnet und der Reset-Knopf wurde (noch) nicht gedrückt. Auch der NOT-AUS Knopf könnte gedrückt sein.

**Wie kann ich von Hand verfahren/positionieren?**  
Deckel schließen, Reset-Knopf drücken und mit den Cursor-Tasten von Hand an die gewünschte Position fahren.

**Wie setze ich die Startposition für meine Datei?**  
An die gewünschte Startposition fahren und auf den Button "Startposition" klicken. Bitte vor dem Lasern nicht vergessen den Fokus zu setzen.

**Wie schalte ich die Zuluft von Hand ein?**  
Auf der linken Seite des Lasers den Knopf für 5 Sekunden drücken und dann loslassen.

**Wie groß ist die _Schnittbreite_ des Laserstrahls?**  
Die Schnittbreite beträgt **~0,2 mm**.

**Bis zu welcher Materialdick kann der Laser schneiden?**  
Die maximal mögliche Materialstärke zum Schneiden beträgt ca. **8 mm**.

## Links zu weiterführender Dokumentation

- Website des Herstellers: [Thunder Laser NOVA 35](http://www.thunderlaser.com/products/nova-laser-cutter.html)
- FabLab Nürnberg
	- [NOVA 35 Dokumentation](https://wiki.fablab-nuernberg.de/w/Nova_35)
	- [Mögliche Materialien][MöglicheMaterialien]
- [VisiCut][VisiCut] - Programm zum aufbereiten von Laserjobs
- Anleitung für [RDworks](https://raw.githubusercontent.com/jnweiger/ruida-laser/master/doc/laser-nova35-rdworks.md) (LaserCutter Software des Herstellers - [zum Download](http://www.thunderlaser.com/laser-download))





[MöglicheMaterialien]: https://wiki.fablab-nuernberg.de/w/ZING_4030#M.C3.B6gliche_Materialien
[InkScape]: https://inkscape.org/de
[VisiCut]: https://github.com/fablabnbg/VisiCut
