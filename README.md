
# <a name="Inhaltsverzeichnis"></a> Projektpräsentation von Juliane und Tabea

## Informatikprojekt 3: 3D-Illusionen

Hier in der Projektpräsentation widmen wir uns dem Vorgehen im unserem Projekt schrittweise, welches Programm wir nutzen wie wir programmierten. Weitere Informationen zu unserem Halbjahresprojekt, wie Probleme, Fortschritte oder Unterichtsausfälle, sind in unserem <a href="https://github.com/Tabea000/3.Informatikprojekt-Stundenblog/blob/master/README.md">Stundenblog</a> genauestens dokumentiert. 

In unserem dritten Informatikprojekt dieses äußerst kurzen Halbjahres widmeten wir uns der dritten Dimension. Hier haben wir anhand verschiedener Methoden eine Illusion von 3D-Formen (z.B ein Turm, ein Herz oder eine Pyramide) erschaffen. Da die erste Methode, wie im <a href="https://github.com/Tabea000/3.Informatikprojekt-Stundenblog/blob/master/README.md">Stundenblog</a>
beschrieben, nicht funtionierte, präsentieren wir hier beide Versionen von 3D-Effekt, die ein wunderbares Ergebnis aufzeigen:

[Erstes Projekt: Tiefenwahrnehmung](#1)

[Zweites Projekt: "Stamping"](#2)

## <a name="1"></a>Erstes Projekt: Tiefenwahrnehmung

Bei dieser Methode eine 3D-Illusion zu erzeugen, arbeitet man in einem fiktiven Horizont mit der Tiefenwahrnehmung. Mithilfe der Pfeiltasten der Tastatur kann man den Sprite so vergrößern/ verkleinern, dass es so aussieht, als würde der Sprite auf einen zukommen/sich von einem entfernen. 

Normalerweise hat man in der 3D-Welt drei Achsen: die x-Achse, auf der sich etwas nach links oder rechts bewegt, die y-Achse, auf der sich etwasnach oben oder unten bewegt und die z-Achse. Diese macht das ganze 3-dimensional, das sich etwas auf dieser Achse nach vorne oder hinten bewegt. Da man auf Snap keine richtige z-Achse programmieren kann, schafft man sich die Illusion einer, indem man den Sprite in seiner Größe verändert. Bewegt sich in der realen Welt etwas in die Ferne, so erscheint es uns kleiner. Auf Snap wird der Sprite wirklich kleiner und schafft somit die Illusion einer z-Achse und folglich auch von einer dritten Dimension, obwohl es letztendlich bloß 2D ist.

Um diese Tiefenwahrnehmung erzeugen zu können, benötigt man einen Block:

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%209%20zugeschnitten.png)

Als ersten Schritt muss man drei Variablen erstellen: scroll x,scroll y, scroll z, welche repräsentativ für die Achsen in dem 3D-Raum sind. Dieses kann man auf Snap unter der Option "Variables"->"make a variable" machen. Man gibt den Namen ein, drückt auf ok und die Variable erscheint auf der linken Seite. Das macht man nun dreimal für alle Achsen. Danach setzt man die drei Variablen in "set() to()"-Bausteine. Dort trägt man die dem oberen Screenshot zu entnehmenden Werte ein. Dadurch dass man die Werte von x und y verändern kann, kann man auch die Position des Sprites verändern, genauso wie seine Größe durch den Wert von z. 

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%2010%20zugeschnitten.png)

Als zweiten Schritt baut man die "set(Variable) to()"-Bausteine unter einen "when flag clicked"-Baustein ein, damit man einen Start für den Block hat. Unter diese Variablen setzt man nun eine "forever"-Schleife, die später alle restliche Bausteine umschließt uns somit dafür sorgt, dass der 3D-Effekt anhält.

Nun baut man drei größere Bausteine zusammen, die hier beschrieben sind:

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%2011%20zugeschnitten.png)

Diese seztzen zum einen fest, um wieviel Prozent sich der Sprite zukünftig verändern soll, wenn die Größe/ die z-Achse verändert wird. Zum anderen werden hier Werte für die x- und y-Achsen festgelegt. 

Im vierten Schritt wir der Code für die Pfeiltasten verfasst, sodass man mit diesen den Sprite auf dem Bildschirm kontrollieren kann. Die Blöcke für die "up" und "down" sind gleich, sie unterscheiden sich lediglich in den Werten, die einmal positiv und einmal negativ sind. Dies gilt sowohl für die "left" und "right" Tasten.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%2012%20zugeschnitten.png)

Für den "up"-/"down"-Code benötigt man zunächst einen "if"-Baustein, indem man "key(jeweilige Taste) pressed?" einsetzt. Des weiteren gehören in den Baustein zwei "change() by()"-Bausteine. In den ersten setzt man die Variable "scroll z" und "size/45(-45)" ein, sodass der Sprite beim drücken der "up"-Taste größer wird. Der zweite wird mit "scroll x" und "x position/55(-55)"beschrieben, damit sich der Sprite gemäß der Illusion von 3D auf der x-Achse bewegt.

Damit sich der Sprite auch ohne Größenveränderung auf der x-Achse bewegen kann, baut man die gleichen Blöcke für die "left"- und "right"-Pfeiltasten. Diese sind wie die vorherigen durch einen "if"-, einen "key() pressed?"- und einen "change() by ()"-Baustein aufgebaut. In letzterem wird noch die Variable "scroll x" für die x-Achse und "size/55(-55)" eingesetzt:

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%2013%20zugeschnitten.png)

Somit kann man nun den Sprite auf einer horizontalen Ebene, der x-Achse, und scheinbar in Richtung Horizont und zurück bewegen.
Da sich ein Objekt oder eine Person irgendwann aus der möglichen Sichtweite entfernt, wenn es sich von einem wegbewegt, wurde ein "if()else()"-Baustein eingebaut, der diesen Fall aufnimmt. In diesem wird beschrieben, dass wenn der Sprite kleiner oder größer als der dafür festgelegte Wert ist, versteckt er sich sozusagen. Dies geschieht durch den Baustein "hide". Ist dies nicht der Fall (else), so ist der Sprite zu sehen ( "show"-Baustein"). In diesem Teil wurde auch ein "größer als" eingebaut, damit der Spielraum der 3D-Aktivitäten eingeschränkt ist.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%2014%20zugeschnitten.png)

Mit diesem letzten Teil ist der Block für die 3D-Illusion anhand von Tiefenwahrnehmung fertig. Nun kann man den Sprite mit den Pfeiltasten auf der fiktiven z-Achse (scroll z) bewegen lassen und ihn im Horizont verschwinden lassen.

[→Inhaltsverzeichnis](#Inhaltsverzeichnis)


## <a name="2"></a>Zweites Projekt: "Stamping"

Die zweite Methode einen 3D-Effekt zu erzielen ist das "layering and stamping", die wir ebenfalls auf der Seite <a href="https://en.scratch-wiki.info/wiki/How_to_Make_a_Three-Dimensional_Project">How to make a Three-Dimensional Project</a> gefunden haben. 
Hierbei verändert man mehrfach die Position des Sprites und macht bei jeder neuen Position eine Kopie des Sprites, praktisch wie ein Stempel. 
Der Sprite an sich ist eine flache 2D-Form, durch mehrere seiner Art übereinander gestempelt, wird dieser jedoch zu einem scheinbaren 3D-Körper.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%201%20zugeschnitten.png)

Um diesen Effekt zu erzielen, braucht man zunächst den bekannten Baustein "change y by()", um die Position des Sprites auf der y-Achse zu ändern, und den neuen Baustein "stamp". Dieser ist bei Snap unter "pen" zu finden und ist zuständig für das Stempeln. Setzt man diese Bausteine nun mehrmals abwechselnd hintereinander, so heißt dies, dass der Sprite eine Kopie von sich macht, nach oben wandert, eine neue Kopie von sich macht usw..

Der Block benötigt für die Fertigstellung nun noch einige grundlegende Bausteine, die lediglich zur Funktion des Blockes beitragen: "When flag clicked" zum Starten des Blocks, "clear" für die Beseitigung vorheriger Malereien,"go to x:0 y:0", um den Sprite zentral auszurichten und den "forever"-Baustein.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%202%20zugeschnitten.png)

So sieht der Block zusammengebaut aus:

In diesem Block kann man die Zahl im "change y by()"-Baustein variieren. 
Die vorgegebene Zahl ist zwei, ändert man diese, beeinflusst dies auch den Abstand der Stempel zueinander, sodass unterschiedliche Bilder zustandekommen.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%203%20zugeschnitten.png)

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%204%20zugeschnitten.png)

Zu dieser Methode gehört noch ein zweiter Block, der aus "when flag clicked", "forever" und "point towards (mouse-pointer)" besteht.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%202.2%20zugeschnitten.png)

Dies veranlasst den Sprite, sich immer nach der Maus auszurichten. Somit kann man den Sprite drehen und den 3D-Effekt von allen Seiten begutachten. Diese mögliche 360°-Drehung verstärkt die Illusion, da man den Körper bewegen kann und nicht 2-dimensional auf dem Bildschirm betrachtet. Hier sind unterschiedliche Perspektiven dargestellt:

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%205%20zugeschnitten.png)

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%206%20zugeschnitten.png)

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%207%20zugeschnitten.png)


Neben der ursprünglichen Pfeilform des Sprites auf Snap kann man auch andere gemeometrische Figuren im 3D-Effekt ausprobieren. Dazu geht man bei "costumes" auf das Pinselsymbol, wodurch man zu dem Paint Editor gelangt. Hier kann man mithilfe verschiedener Funktionen eine eigene Form kreieren und diese schließlich durch die "layering and stamping"-Methode eine 3D-Illusion annehmen lassen.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/Bild%208%20zugeschnitten.png)

Dies ist der Paint Editor

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/23.3..png)
Ein Haus in 3D anhand der "stamping"-Methode.
Nach einer gewissen Anzahl an gestapelten Rechtecken (Hauswände) wurde die Größe weiter verkleinert, sodass sich eine spitz zulaufendes Dach bildet.

![bsp applab](https://raw.githubusercontent.com/Tabea000/3.Informatikprojekt-Stundenblog/master/Bildverzeichnis/16.3..png)
Zwei Herzen (kopfüber) in 3D

Man kann beide 3D-Methoden miteinander kombinieren, sodass man sowohl einen scheinbaren mehrfach dimensionalen Körper vorliegen hat, als auch eine Tiefenwahrnehmung, ,mit der sich der Körper bewegt.

[→Inhaltsverzeichnis](#Inhaltsverzeichnis)








