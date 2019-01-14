![DRAFT](https://img.shields.io/badge/Status-ENTWURF-red.svg)

**Todo**

- Vorbereitung der Dateien
	- Farben für Laserprofile
	- Parameter
	- Daten an Laser senden
- Lasern
	- Allgemein
		- Bedienelemente
		- Dateien löschen
	- Material fokusieren
	- Startposition
	- Box abfahren
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

- [Sicherheitshinweise](#sicherheitshinweise)
- [Material](#material)
- [Vorbereitung](#vorbereitung)
	- Daten aufbereiten
		- Profile berücksichtigen (Schneiden, Gravieren, ...)
		- Reihenfolge der Profile in VisiCut
	- Materialwahl
		- Werte für Schneiden, Gravieren, Markieren, ...
	- Toleranzen beim Schneiden
- [Laser ein-/ausschalten](#laser-ein-ausschalten)
	- [Einschalten](#einschalten)
	- [Ausschalten](#ausschalten)
- [Laser starten und verwenden](#laser-starten-und-verwenden)
	- Bedienelemente 
	- Daten an Laser senden
		- Löschen von Daten
	- Material einlegen
		- Fokusieren (Höhe des Materials)
	- Startposition festlegen/Positionierung des Lasers
	- Programm starten/stoppen
	- Unterbrechung, Fortsetzen
	- Änderung der Werte (Geschwindigkeit, Energie, Zuluft, ...)
- [Sonstiges](#sonstiges)
	- [Manuelles Schneiden](#manuelles-schneiden)
	- [Schmauchspuren](#schmauchspuren)
- [FAQ](#faq)
- [Links zu weiterführender Dokumentation](#links-zu-weiterführender-dokumentation)

## Material

:skul: Nicht jedes Material kann und darf mit dem Laser bearbeitet werden. Diverse Kunststoffe entwickeln unter Hitze giftie Gase und/oder Säuren.

:warning: Zur eigenen Sicherheit und der anderen Benutzer im FabLab sollte nur **Acrylglas (Plexiglas, PMMA)** verwendet werden. Zu vermeiden ist auch "Bastelglas" aus dem Baumarkt.

Ansonsten lässt sich (fast) jedes organische Material mehr oder minder problemlos bis zu einer Dicke von ungefähr 8 mm verarbeiten.

Für Holz (z.B. Sperrholz Birke) gilt, dass **B-Qualität** vollkommen ausreichend ist. Beim Kauf sollte man auf **Laserqualität** achten, da hier keine ungewollten Einschlüsse, wie z.B. Kleber bei "Löchern" zwischen den einzelnen Materialschichten, vorhanden sind.

Weitere nützliche Informationen zu Materialien sind unter anderem auf den [Wiki-Seiten des FabLab Nürnberg][MöglicheMaterialien] zu finden.

## Vorbereitung
	### Daten aufbereiten
		#### Profile berücksichtigen (Schneiden, Gravieren, ...)
		#### Reihenfolge der Profile in VisiCut
	### Materialwahl
		#### Werte für Schneiden, Gravieren, Markieren, ...
	### Toleranzen beim Schneiden

## Laser ein-/ausschalten

### Einschalten

1. Kompressor für Laser-Zuluft einschalten (Dreierblock Sicherungen im Sicherungsschrank neben der Theke)
2. Abluft im Nebenraum einschalten (Wippschalter an der Steckdose)
	- Motorgeräusche sind zu hören (evtl. dauert es kurz)
3. Laser einschalten (rechts unten), Hauptschalter und die beiden Wippschalter müssen auf 1 stehen
4. Roten Reset-Knopf drücken (oberhalb des Displays) - Signallampe wird grün
5. Dateien können übertragen werden

### Ausschalten

Das Ausschalten erfolgt in umgekehrter Reihenfolge zum [Einschalten](#einschalten).

## Laser starten und verwenden
	### Bedienelemente 
	### Daten an Laser senden
		#### Löschen von Daten
	### Material einlegen
		#### Fokusieren (Höhe des Materials)
	### Startposition festlegen/Positionierung des Lasers
	### Programm starten/stoppen
	### Unterbrechung, Fortsetzen
	### Änderung der Werte (Geschwindigkeit, Energie, Zuluft, ...)

## Sonstiges

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



-----------------------------------------------



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
Die Schnittbreite beträgt **~ 0,2 mm**.

**Bis zu welcher Materialdick kann der Laser schneiden?**  
Die maximal mögliche Materialstärke zum Schneiden beträgt ca. **8 mm**.

## Links zu weiterführender Dokumentation

- Website des Herstellers: [Thunder Laser NOVA 35](http://www.thunderlaser.com/products/nova-laser-cutter.html)
- FabLab Nürnberg
	- [NOVA 35 Dokumentation](https://wiki.fablab-nuernberg.de/w/Nova_35)
	- [Mögliche Materialien][MöglicheMaterialien]
- [VisiCut](https://github.com/fablabnbg/VisiCut) - Programm zum aufbereiten von Laserjobs
- Anleitung für [RDworks](https://raw.githubusercontent.com/jnweiger/ruida-laser/master/doc/laser-nova35-rdworks.md) (LaserCutter Software des Herstellers - [zum Download](http://www.thunderlaser.com/laser-download))




[MöglicheMaterialien]: https://wiki.fablab-nuernberg.de/w/ZING_4030#M.C3.B6gliche_Materialien
