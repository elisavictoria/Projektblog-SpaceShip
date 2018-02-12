# Projektblog-SpaceShip

SpaceShipGame: http://snap.berkeley.edu/snapsource/snap.html#present:Username=elisavictoria&ProjectName=SpaceShip

[Idee](#eins)

[Script Erklärung](#zwei)

[1. Spaceship](#zwei.eins)

[2. Laser](#zwei.zwei)

[3. Winner](#zwei.drei)

[4. Game over](#zwei.vier)

[5. Aliens](#zwei.fünf)

[6. Explosion](#zwei.sechs)

[Spielanleitung](#drei)

[Fazit](#vier)


# Idee<a name="eins"></a>

Aufgrund unterschiedlicher Recherche im Internet sind wir schließlich auf das klassische Spiel SpaceShip aus den 70ern gestoßen. Wir hatten schon am Anfang des Jahres den Wunsch geäußert ein eigenes Spiel zu programmieren. Der angebotene Onlinekurs The Beauty and Joy of Computing lehrte uns Grundlagen des Programms Snap. Allerdings brauchten wir für die einzelnen Aufgaben aufgrund von Verständnisschwierigkeiten etwas länger, sodass wir keine Lust mehr hatten nach den vorgegebenen Anleitungen zu arbeiten. Weil wir in dieser Einheit sowieso ein eigenes Projekt abgeben müssen, fingen wir an das Spiel selbst zu gestalten. Da wir durch den Kurs die Grundkenntnisse von Snap erlernt hatten, trauten wir uns die Aufgabe vom Schwierigkeitsgrad her zu. 

# Script Erklärung<a name="zwei"></a>

1. Spaceship<a name="zwei.eins"></a>

Zuerst programmierten wir das Spaceship. Es sollte sich beim Drücken der Pfeiltasten auf einer horizontalen x-Achse nach rechts oder links bewegen.
Dazu fügten wir den "change-x-by" Block ein. Damit das Raumschiff nicht aus dem Bild fliegt, sobald man zu lange auf die Pfeiltasten gedrückt hat, fügten wir "if on edge bounce"- Blöcke ein.
Auf dem script kann man neben den Befehlen für das Raumschiff auch ein Script für einen Timer erkennen. Unsere Idee war es, das Spiel durch zwei Einheiten einzugrenzen und so zwei Spielausgänge zu schaffen: man kann entweder gewinnen oder verlieren. Der Spieler muss die Aliens in einem von uns eingestellten Zeitraum abgeschossen haben, sonst verliert er. Außerdem zählt ein Score die getöteten Aliens, sodass man den Überblick halten kann. Das Einfügen eines Scores erleichtert zusätzlich das spätere Programmieren des Einfügens vom Winner Logo. Wir wollten uns die Möglichkeit lassen im Nachhinein noch eine Spielerliste in das Spiel zu integrieren. Eine Spielerliste zu programmieren lernten wir in einer zuvor absolvierten Lektion von Snap.

![6](https://user-images.githubusercontent.com/31760549/35722997-eb4b5976-07f8-11e8-8e65-7d524d0e720e.png)

2. Laser<a name="zwei.zwei"></a>

Den Laser zu programmieren, war ein wenig umfangreicher, als das Spaceship bewegen zu lassen. Er soll sich beim Klicken der grünen Fahne, aslo beim Starten des Spiels, hinter dem Spaceship verstecken. Deswegen fügten wir einen "go to Spaceship"- Block ein und geben ihm mit dem Block "hide" den Befehl sich am Anfang des Spiels hinter dem Raumschiff zu verstecken. Mit dem Drücken der Leertaste erscheint der Laser, der sich darauf hin in die Richtung (0) also nach oben bewegt. Mit dem "repeat until touching edge" grenzen wir die Bewegung ein, sodass der Laser nicht mehr zu sehen ist, sobald er einen Rand berührt.

![7](https://user-images.githubusercontent.com/31760549/35723047-1ab1f9ea-07f9-11e8-8d30-1b2cc6e23589.png)

3. Winner<a name="zwei.drei"></a>

Das "Winner"- Logo sollte erscheinen sobald, der Spieler die Bedingung erfüllt hat, alle Aliens in 10 Sekunden getötet zu haben. Davor soll es nicht zu sehen sein, das heißt beim Starten des Spiels muss es sich zunächst verstecken. 
Das Logo erscheint aufgrund des "If-Blocks", wenn der Spieler den Score 6 erreicht. Es könnte ja durchaus sein, dass der Spieler es in einer kürzeren Zeit schafft alle Aliens zu Töten. Wir können den Spielausgang also nicht im Zusammenhang mit dem Ablaufen des Timers programmieren.

![8](https://user-images.githubusercontent.com/31760549/35723144-7f7f6f6a-07f9-11e8-8c35-8551f5b362fe.png)

4. Game over<a name="zwei.vier"></a>

Sobald der Spieler die bedingungen nicht erfüllen konnte, sollte das "Game over" Logo erscheinen. Dazu haben wir es so programmiert, dass es auftaucht sobald der Timer abgelaufen ist und sich quasi "zeigt". Dann soll alles gestoppt werden und das Spiel muss erneut gestartet werden. 

<img width="1440" alt="bildschirmfoto 2018-02-11 um 17 56 08" src="https://user-images.githubusercontent.com/31760498/36075922-93a0c940-0f55-11e8-836c-58efa41a50fc.png">


5. Aliens<a name="zwei.fünf"></a>

Die Aliens sollten sich bewegen, damit man sie mit dem Laser abschießen kann. Das ist auch das Ziel des Spiles. Dazu haben wir die Aliens so programmiert, dass sie sich auf einer bestimmten y Koordinate waagerecht in unterschiedlichen Geschwindigkeiten hin und herbewegen. Leider drehen sich die Aliens immer um 180° wenn sie von der Wand abprallen, allerdings konnten wir nicht die Ursache dafür finden und deshalb drehen sie sich immernoch.

![9](https://user-images.githubusercontent.com/31760549/35723142-7f6788f0-07f9-11e8-8d38-842d0f8526b7.png)

6. Explosion<a name="zwei.sechs"></a>

Sobald ein Alien von dem Laser getroffen wurde, soll er wie eine Bombe explodieren und nach einer Sekunde komplett verschwinden. Deshalb haben wir die Aliens so programmiert, dass sie ihr Kostüm wechseln wenn sie abgeschossen wurden. 


# Spielanleitung<a name="drei"></a>

Das Spiel ist sehr einfach zu spielen. Mit der Space Taste schießt das Spaceship Laser Kugeln ab. Um das Schiff zu bewegen, können die rechte und die linke Pfeiltaste benutzt werden. Damit ist es möglich in der vorgegebenen Zeit alle Aliens abzuschießen. 


# Fazit<a name="vier"></a>

Grundsätzlich hat das Programmieren des Spieles Spass gemacht, weil man bei jedem Zwischenschritt das "Neuprogrammierte" gleich ausprobieren konnte. Nachdem wir das Grundspiel programmiert hatten, haben wir angefangen kleine Verbesserungen einzufügen indem wir einen Timer eingerichtet haben. Außerdem haben wir das "Winner und Game over - Logo" eingefügt. Eigentlich wollten wir auch noch zwei Barrikaden für das Spaceship programmieren, weil wir uns gedacht haben, dass die Aliens zurückschießen sollen. Dann wäre das Spaceship hinter diesen Barrikaden sicher vor den Laserangriffen der Aliens gewesen, weil wenn die Laser der Aliens das Spacship berührt hätten, das Spiel nach drei verlorenen Leben vorbei gewesen wäre. Doch leider haben wir es zeitlich nicht geschafft unsere Ideen in die Realität umzusetzten. Wir würden auf jeden Fall weiter an dem Spiel arbeiten können und es noch weiter ausbauen. 
