---
sidebar_position: 2
sidebar_label: 2. Basisklasse Attack
---

# 2. Lösung: Basisklasse Attack

Diese Aufgabe bestand aus zwei Teilen. Schauen wir sie uns nacheinander an.

Zuerst sollten wir die Datei `Attack.cs` in einen neuen Ordner `Attacks` verschieben. Dabei müssen wir aber beachten, dass wir den Namespace der Datei anpassen müssen von `namespace ObjectOrientation;` zu `namespace ObjectOrientation.Attacks;`.<br/>
Daraus folgt ebenfalls, dass `Pokemon.cs`, `Pikachu.cs` und `Program.cs` diesen neuen Namespace über `using ObjectOrientation.Attacks;` importieren müssen, damit sie die Klasse `Attack` wieder verwenden können.

Danach erstellen wir (analog zu `Pikachu`) eine neue Klasse `Donnerblitz` in einer neuen Datei `Donnerblitz.cs` in dem eben erstellten Ordner `Attacks`. Die Klasse benötigt keine Parameter, denn der Namen und den Schaden der Attacke sind fest und können direkt an die Basisklasse übergeben werden.

```cs
namespace ObjectOrientation.Attacks;

public class Donnerblitz : Attack
{
    public Donnerblitz()
        : base("Donnerblitz", 30)
    {
    }
}
```