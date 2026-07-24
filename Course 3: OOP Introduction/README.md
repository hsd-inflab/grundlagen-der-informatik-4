## Course 3: OOP Introduction
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the network drive (Dieser PC -> Netzwerkadressen)!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______

***Vorbereitung***

Befassen Sie sich mit den vier Säulen der Objektorientierung. Sie müssen diese in diesem Versuch identifizieren und erklären können, wie diese funktionieren und warum diese eingesetzt werden.


*Note: (Currently German only)*

### Overview: "Einstieg in die Objektorientierung"
Im Rahmen dieses Versuchs sollen mehrere Klassen erstellt werden und darüber die vier Säulen der Objektorientierung anhand von praktischen Beispielen kennen gelernt werden.

Sämtlicher Code ist vor Ort zu programmieren. Eine inhaltliche Vorbereitung und vorherige Planung ist jedoch zwingend erforderlich um das Praktikum erfolgreich zu absolvieren.

Laden Sie das **Java Projekt** `dicegameTemplate` unter folgendem Link herunter: https://github.com/hsd-inflab/dicegameTemplate

Ziel des Praktikums ist das Implementieren neuer Würfelklassen für das Würfelspiel. 
Bereits vorhanden sind:
1. Die Main Klasse
2. Das Package **types** mit der abstrakten Oberklasse `Dice.java`, von der die zu erstellenden Würfelklassen abgeleitet werden sollen
3. Das Package **framework** mit den Klassen `Shaker.java`, welche den Würfelbecher repräsentiert, sowie `DiceFactory.java` und `DiceResult.java`, welche die Erstellung der Würfelobjekte und deren Ergebnisse behandeln.
4. Das Package **ui**, welches die Darstellung der Würfel ermöglicht.

Bevor Sie während des Praktikums mit der Implementierung starten: Besprechen Sie mit einem Betreuer eine geeignete Vererbungsstrategie und halten diese schriftlich fest. 
Die bereits vorhandenen Klassen dürfen (und müssen!) nicht verändert werden.

Die konkreten Würfelklassen müssen im Package **types** abgelegt werden, damit diese vom Framework gefunden werden können. Sobald Sie einen Würfel implementiert haben, erscheint dieser automatisch in der JavaFX-Ansicht. Diese starten Sie, indem Sie die Main Methode ausführen.
   
Es sollen die folgenden vier Würfel von `Dice.java` abgeleitet werden:
1. `RegularDice.java`
   - normaler, sechsseitiger Würfel
2. `MultisidedDice.java`
   - mehrseitiger Würfel zwischen 4 und 20 Seiten
   - Seitenzahl kann nur bei Erstellung des Objekts festgelegt und danach nicht mehr geändert werden 
3. `LoadedDice.java`
   - gezinkter Würfel mit sechs Seiten
   - kann auf alle Seiten fallen, aber mit 50% Wahrscheinlichkeit auf die größte Zahl
4. `ChaosDice.java`
   - Würfel zwischen 4 und 20 Seiten
   - wechselt **nach** jedem Wurf die Seitenanzahl
5. `CustomDice.java`
   - Ein Würfel mit einem Verhalten Ihrer Wahl. Seien Sie kreativ.

![dice](https://upload.wikimedia.org/wikipedia/commons/c/c8/Wuerfel5.jpg?uselang=de)

Quelle: https://de.wikipedia.org/wiki/Spielwürfel
 

![instant](../images/instantiating.png)




