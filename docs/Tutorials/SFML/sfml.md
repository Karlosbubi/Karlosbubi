# SFML

## Die Library(s)

SFML ist eine Sammlung Libraries, die für die 2D spiele entwicklung gemacht wurden.
Die wichtigsten Komponenten sind der Wrapper für Fenster management sowie das Grafik rendering. Außerdem stehen Audio und Netzwerk APIs zu verfügung.

## Installation

[Offizielle Anleitung](https://www.sfml-dev.org/tutorials/2.5/start-vc.php)

### Linux

```bash
# Ubuntu, Mint, Pop!, etc.
sudo add-apt-repository ppa:sonkun/sfml-development 
sudo apt-get update
sudo apt install libsfml-dev

# Fedora, RHEL
sudo dnf install SFML-devel

# Arch, Manjaro, etc.
sudo pacman -S sfml
```

### Windows (Visual Studio)

![Image Missing](assets/1Capture.PNG)

![Image Missing](assets/2Capture.PNG)

![Image Missing](assets/3Capture.PNG)

![Image Missing](assets/4Capture.PNG)

![Image Missing](assets/5Capture.PNG)

![Image Missing](assets/6Capture.PNG)

![Image Missing](assets/7Capture.PNG)

![Image Missing](assets/8Capture.PNG)

![Image Missing](assets/9Capture.PNG)

![Image Missing](assets/10Capture.PNG)

![Image Missing](assets/11Capture.PNG)

![Image Missing](assets/12Capture.PNG)

![Image Missing](assets/Capture16.PNG)

![Image Missing](assets/13Capture.PNG)

![Image Missing](assets/16Capture.PNG)

![Image Missing](assets/14Capture.PNG)

![Image Missing](assets/15Capture.PNG)

![Image Missing](assets/17Capture.PNG)

### Installation Testen

Testen mit dem Offiziellen Beispielcode :

```c++
#include <SFML/Graphics.hpp>

int main()
{
    sf::RenderWindow window(sf::VideoMode(200, 200), "SFML works!");
    sf::CircleShape shape(100.f);
    shape.setFillColor(sf::Color::Green);

    while (window.isOpen())
    {
        sf::Event event;
        while (window.pollEvent(event))
        {
            if (event.type == sf::Event::Closed)
                window.close();
        }

        window.clear();
        window.draw(shape);
        window.display();
    }

    return 0;
}
```

Erwartetes Ergebinss :
![Image Missing](assets/18Capture.PNG)

---
Mitautor : [Philipp Golla](https://github.com/PhilippGolla)
