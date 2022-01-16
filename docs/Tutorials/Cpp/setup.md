# Hello World

Nun wollen wir erstmal die Teschnichen Voraussetzungen schaffen, im folgenden Kapitel werde ich dich durch eine Mengen vorarbeit leiten, und vergleichs weise Wenig erklären. Am Ende solltes du dein Erstes Programm ausgeführt haben.

## System

Für die Aktuelle version dieses Tutorial ist ein Unix ähnliches System von nöten, das heißt Linux, BSD oder MacOS. Solltest du bereits etwas mehr technisches Know-How besitzen und nur C++ neu erlernen kannst du unter Windows das WSL bzw. WSL2 verwenden.
Ich benutze Pop! OS und Fedora, zwei Linux Distributionen, damit du eine Referenz bezüglich des Aussehens hast, welches aber in den meisen fällen ähnlich genug sein sollte um die Funktionalität am eigenen System nach zu vollziehen.

## Format

Ein C++ programm ist effektiv eine sog. Rein-Textdatei, das heißt, dass sie Text aber nur Zeichen enthält ohne Metadaten und Verzierungen, wie Überschriften, Tabellen oder eingebette Bilder, denen du sonst, auch auf dieser Webseite, über den Wegläufst.
Wie bei anderen Dateien Teilen wir dem Computer den Datei-Typ über die Datei-Endung mit, den Buchstaben am Ende, hinter dem Punkt, sicherlich hast du Schon damit zu tun gehabt, etwa  `.odp`, `.fodp` oder `.pptx` für Präsentationen, `.mp3` oder `.opus` für Musik, `.png`, `.jpeg` oder `.svg` für Bilder, und so weiter und so fort.
Endungen für C++ programme gibt es tatsächlich auch mehrere, etwa `.cc`, `.cxx` oder `.cpp`. Letztere werden wir im weiteren verlauf verwenden.

## Code

Jetzt wollen wir unser Programm aber endlich haben, dafür suchst du dir einen schönen Ordner, am besten erstellst du einen neuen, leeren für den durchlauf dieses Tutorials. Hier speihern wir jetzt ein leere Datei mit einem passenden Namen und unserer C++ endung, ich Nehme `hello.cpp`.
Der Name selbst die endung ist für die funktion tatsächlich unerhblich, trotzdem rate ich dir dringend dazu im verlaufe des Tutorial nach meinem Beispiel zu richten, um Verwirrung zu vermeiden.
Das ganze sollte dann etwa so aussehen :
![hello.cpp](assets/Screenshot%20from%202021-12-22%2019-03-27.png)
Diese Datei, noch leer, öffnen wir jetzt in einem Text editor unserenr wahl, gleich siehst du Gedit.
NotePad++, Kate, Elementary Code, etc. sind gute alternativen, ich empehle den vor installierten. Eine Detailiertere Betrachtung userer Software folgt in einem Späteren Kapitel.
![Gedit hello.cpp](assets/Screenshot%20from%202021-12-22%2019-03-50.png)

In diese Datei kopieren wir nun Folgenden Code :

```C++
#include <iostream> // läd extra code, insbesondere 'cout'

using namespace std; // Bestimmt welche gruppe an extra code verwendent wird

int main(){ // die Haupt funktion, einstiegs punk des Programmes

    cout << "Hello World !" << endl; // Gibt die Zeile "Hello World !" aus
    
    return 0; // Beendet das Programm mit status Wert

} // Markiet das ende des Haup codes
```

Was genau das Bedeutet ist noch nicht so wichtig, ich habe jeweils hinter `//` einen kommentar verfasst, was in etwa passiert für den groben überblick und für den fall, dass dir einige begriffe bekannt vorkommen.
Probieren wir aber lieber aus.
Nun kommt die Shell/das Terminal ins Spiel.
Öffne das Terminal in dem Ordner mit der Datei, oder navigiere dich im Terminal dort hin.

![Open in Terminal](assets/Screenshot%20from%202021-12-22%2019-32-38.png)
`ls` listet die dateien im offenen Ordnenr auf.
![Im Terminal](assets/Screenshot%20from%202021-12-22%2019-34-50.png)

Um das Programm aus zu führen müssen wir es ersteinmal aus dem Source Code zu einem "echten" Programm machen, das nennt man `Kompilieren` und wird von einem Sogenannten `Kompiler` gemacht, dieser ist der haupt grund, wofür wir das terminal benötigen. Mein Kompiler der Wahl ist `gcc` und wird für C++ wie folgt verwendet.

```bash
g++ INPUT -o OUTPUT
```

oder in unserem Beispiel :

```bash
g++ hello.cpp -o hello
```

Durch diesen befehl wird ein ausfürhbares programm mit Namen `hello` erzeugt, dieses kann mit

```bash
./hello
```

im Terminal ausgeführt werden oder durch Doppelklick im Dateimanager.

![Hello World](assets/Screenshot%20from%202021-12-22%2019-46-20.png)
