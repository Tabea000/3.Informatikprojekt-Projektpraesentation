# <a name="Inhaltsverzeichnis"></a> Projektpräsentation von Tabea und Juliane



# <a name="Inhaltsverzeichnis"></a> Projektpräsentation von Juliane und Tabea

## Informatikprojekt 3: 3D-Illusionen

In unserem dritten Informatikprojekt dieses äußerst kurzen Halbjahres widmeten wir uns der dritten Dimension. Hier haben wir anhand verschiedener Methoden eine Illusion von 3D-Formen (z.B ein Turm, ein Herz oder eine Pyramide) erschaffen. Da die erste Methode, wie im <a href="https://github.com/Tabea000/3.Informatikprojekt-Stundenblog/blob/master/README.md">Stundenblog</a>
beschrieben, nicht funtionierte, präsentieren wir hier beide Versionen von 3D-Effekt, die ein wunderbares Ergebnis aufzeigen:

[Erstes Projekt: Horizont](#1)

[Zweites Projekt: "Stamping"](#2)

## <a name="1"></a>Erstes Projekt: Horizont


## <a name="2"></a>Zweites Projekt: "Stamping"

Die zweite Methode, einen 3D-Effekt zu erzielen ist das "layering and stamping", gefunden auf der Seite <a href="https://en.scratch-wiki.info/wiki/How_to_Make_a_Three-Dimensional_Project"> . 
Hierbei verändert man öfters die Position des Sprites und macht bei jeder neuen Position eine Kopie des Sprites, praktisch wie ein Stempel. 
Der Sprite an sich ist eine flache 2D-Form, durch mehrere seiner Art übereinander gestempelt wir dieser zu einem scheinbaren 3D-Körper.

BILD: GESTEMPELTER SPRITE

Um diesen Effekt zu erzielen brauch man zunächst die Bausteine "change y by()", um die Position des Sprites auf der y-Achse zu ändern, und den neuen Baustein "stamp". Dieser ist bei Snap unter "pen" zu finden und ist zuständig für das Stempeln. Setzt man diese Bausteine nun mehrmals abwechselnd hintereinander, so heißt dies, dass der Sprite eine Kopie von sich macht, nach oben wandert, eine neue Kopie von sich macht usw..

Der Block benötigt für die Fertigstellung nun noch einige grundlegende Bausteine, die lediglich zur Funktion des Blockes beitragen: "When flag clicked" zum Starten des Blocks, "clear" für die Beseitigung vorheriger Malereien,"go to x:0 y:0", um den Sprite zentral auszurichten und den "forever"-Baustein.

BILD: BLOCK 1
So sieht der Block zusammengebaut aus.

In diesem Block kann man die Zahl im "change y by()"-Baustein variieren. 
Die vorgegebene Zahl ist zwei, ändert man diese, ändert man auch den Abstand der Stempel zueinander, sodass unterschiedliche Bilder zustandekommen.

BILDER: Y-KLEINER WERT, Y-GROßER WERT --ANGEBEN

Zu dieser Methode gehört noch ein zweiter Block, der aus "when flag clicked", "forever" und "point towards (mouse-pointer)" besteht.

BILD: BLOCK ZWEI

Dies veranlasst den Sprite, sich immer nach der Maus auszurichten. Somit kann man den Sprite drehen und den 3D-Effekt von allen Seiten begutachten. Diese mögliche 360°-Drehung verstärkt die Illusion, da man den Körper bewegen kann und nicht 2-Dimensional auf dem Bildschirm betrachtet.

BILD: SPRITE VON UNTERSCHIEDLICHEN SEITEN

Neben der ursprünglichen Pfeilform des Sprites auf Snap, kann man auch andere gemeometrische Figuren im 3D-Effekt ausprobieren. Dazu geht man bei "costumes" auf das Pinselsymbol, wodurch man zu dem Paint Editor gelangt. Hier kann man anhand verschiedener Funktionen eine eigene Form kreieren und schließlich durch die "layering and stamping"-Methode eine 3D-Illusion annehmen lassen.

BILD: PAINT EDITOR

BILDER: VERSCHIEDENE FORMEN









