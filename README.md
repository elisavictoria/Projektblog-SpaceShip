# Projektblog-SpaceShip
Datei: http://snap.berkeley.edu/snapsource/snap.html#present:Username=elisavictoria&ProjectName=SpaceShip
# Idee

Aufgrund unterschiedlicher Recherche im Internet sind wir schließlich auf das klassische Spiel SpaceShip aus den 70ern gestoßen. Wir hatten schon am Anfang des Jahres den Wunsch geäußert ein eigenes Spiel zu programmieren. Der angebotene Onlinekurs The Beauty and Joy of Computing lehrte uns Grundlagen des Programms Snap. Allerdings brauchten wir für die einzelnen Aufgaben aufgrund von Verständnisschwierigkeiten etwas länger, sodass wir keine Lust mehr hatten nach den vorgegebenen Anleitungen zu arbeiten. Weil wir in dieser Einheit sowieso ein eigenes Projekt abgeben müssen, fingen wir an das Spiel selbst zu gestalten. Da wir durch den Kurs die Grundkenntnisse von Snap erlernt hatten, trauten wir uns die Aufgabe vom Schwierigkeitsgrad her zu. 

# Script Erklärung

1. Spaceship

Zuerst programmierten wir das Spaceship. Es sollte sich beim Drücken der Pfeiltasten auf einer horizontalen x-Achse nach rechts oder links bewegen.
Dazu fügten wir den "change-x-by" Block ein. Damit das Raumschiff nicht aus dem Bild fliegt, sobald man zu lange auf die Pfeiltasten gedrückt hat, fügten wir "if on edge bounce"- Blöcke ein.
Auf dem script kann man neben den Befehlen für das Raumschiff auch ein Script für einen Timer erkennen. Unsere Idee war es, das Spiel durch zwei Einheiten einzugrenzen und so zwei Spielausgänge zu schaffen: man kann entweder gewinnen oder verlieren. Der Spieler muss die Aliens in einem von uns eingestellten Zeitraum abgeschossen haben, sonst verliert er. Außerdem zählt ein Score die getöteten Aliens, sodass man den Überblick halten kann. Das Einfügen eines Scores erleichtert zusätzlich das spätere Programmieren des Einfügens vom Winner Logo. Wir wollten uns die Möglichkeit lassen im Nachhinein noch eine Spielerliste in das Spiel zu integrieren. Eine Spielerliste zu programmieren lernten wir in einer zuvor absolvierten Lektion von Snap.

![6](https://user-images.githubusercontent.com/31760549/35722997-eb4b5976-07f8-11e8-8e65-7d524d0e720e.png)

2. Laser

Den Laser zu programmieren, war ein wenig umfangreicher, als das Spaceship bewegen zu lassen. Er soll sich beim Klicken der grünen Fahne, aslo beim Starten des Spiels, hinter dem Spaceship verstecken. Deswegen fügten wir einen "go to Spaceship"- Block ein und geben ihm mit dem Block "hide" den Befehl sich am Anfang des Spiels hinter dem Raumschiff zu verstecken. Mit dem Drücken der Leertaste erscheint der Laser, der sich darauf hin in die Richtung (0) also nach oben bewegt. Mit dem "repeat until touching edge" grenzen wir die Bewegung ein, sodass der Laser nicht mehr zu sehen ist, sobald er einen Rand berührt.

![7](https://user-images.githubusercontent.com/31760549/35723047-1ab1f9ea-07f9-11e8-8d30-1b2cc6e23589.png)

3. Winner 

Das "Winner"- Logo sollte erscheinen sobald, der Spieler die Bedingung erfüllt hat, alle Aliens in 10 min getötet zu haben. Davor soll es nicht zu sehen sein, das heißt beim Starten des Spiels muss es sich zunächst verstecken. 
Das Logo erscheint aufgrund des "If-Blocks", wenn der Spieler den Score 6 erreicht. Es könnte ja durchaus sein, dass der Spieler es in einer kürzeren Zeit schafft alle Aliens zu Töten. Wir können den Spielausgang also nicht im Zusammenhang mit dem Ablaufen des Timers programmieren.

![8](https://user-images.githubusercontent.com/31760549/35723144-7f7f6f6a-07f9-11e8-8c35-8551f5b362fe.png)

![9](https://user-images.githubusercontent.com/31760549/35723142-7f6788f0-07f9-11e8-8d38-842d0f8526b7.png)




