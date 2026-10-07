## Course 3: Four Pillars of OOP & Interfaces
______

**ATTENTION:** When working with HSD lab computers, save ALL your work on the network drive (Dieser PC -> Netzwerkadressen)!!!

Any data stored on `C:\` will only be saved to the local computer and can be deleted or manipulated by any other user. 
______

***Vorbereitung***

Machen Sie sich mit der Codebase vertraut und bearbeiten Sie Schritt 1.

*Note: (Currently German only)*

# Praktikum: Parkhaus-Simulator

## Worum geht es?

In diesem Projekt steuert ein kleiner Simulator ein Parkhaus mit 100 Stellplätzen.
Fahrzeuge (PKW, LKW, Motorrad) fahren ein und aus; an der **Einfahrt** wird
entschieden, ob ein Fahrzeug ein gültiges Ticket bekommt oder abgewiesen wird,
an der **Ausfahrt** wird anhand des Tickets die zu zahlende Gebühr (ein
`Receipt`) berechnet.

Das Projekt können Sie unter [parking-garage-template](https://github.com/hsd-inflab/parking-garage-template) herunterladen.

Das Verhalten von Ein- und Ausfahrt steckt hinter zwei Interfaces:

- `parking.gate.iface.Entrance`
- `parking.gate.iface.Exit`

Aktuell existieren im Package `parking.gate.impl` **zwei Klassen**:
`EntranceGate` und `ExitGate`. Sie implementieren jeweils ein Interface und stellen das Standardverhalten
bereit (jedes Fahrzeug bekommt ein Ticket, es wird ein fester Betrag berechnet).
Ihre Aufgabe ist es, dieses Standardverhalten durch **vier neue Regeln** zu
ersetzen bzw. zu erweitern.


Ergänzen Sie ausschließlich neue Klassen (und die Interfaces) – die
übrige Infrastruktur (GUI, Simulator, Modelle) ist fertig und sollen, mit Ausnahme von `Lot` und der beiden Gate-Implementierungen, nicht verändert werden.

Damit Ihre Klassen in der GUI auswählbar werden, tragen Sie sie in die Listen
`availableEntrances()` bzw. `availableExits()` in der Klasse `Lot` ein.

## Die umzusetzenden Regeln

| Nr. | Regel |
|-----|-------|
| 1 | Ist das Parkhaus **voll**, werden einfahrende Fahrzeuge **abgewiesen**. |
| 2 | Wie 1, zusätzlich: Ab **80 % Auslastung** wird **LKWs** (`SEMI`) die Zufahrt verweigert. |
| 3 | Statt des Standardpreises kostet das Parken **2 € je angefangene Stunde**. Wer **innerhalb von 15 Minuten** wieder ausfährt, zahlt **nichts** (Kulanz für Kurzparker). |
| 4 | Wie 3, zusätzlich ein pauschaler Zuschlag nach Fahrzeugtyp: **LKWs** (`SEMI`) zahlen **+5 €**, **Motorräder** erhalten **−1 €** Rabatt, **PKW** unverändert. Eine kostenfreie Ausfahrt nach Regel 3 bleibt kostenfrei (der Zuschlag gilt nur für zahlungspflichtige Aufenthalte), und der Parkpreis darf nie **negativ** werden (mindestens 0 €). |

---

## Aufgaben

Die beiden Interfaces `Entrance` und `Exit` deklarieren im Auslieferungszustand
je **eine parameterlose Methode**. Das reicht nicht aus, um die vier Regeln
umzusetzen.

**Schritt 1 – Analyse (zuerst, bevor Sie Code schreiben).** Füllen Sie für jede
Regel die folgende Tabelle aus: *Welche Information* brauchen Sie, um die Regel
entscheiden bzw. berechnen zu können, und *woher* bekommen Sie diese Information
(welche Klasse bzw. welcher Getter liefert sie)?

| Nr. | Nötige Information | Bereitsteller (Klasse / Getter) |
|-----|--------------------|---------------------------------|
| 1   |                    |                                 |
| 2   |                    |                                 |
| 3   |                    |                                 |
| 4   |                    |                                 |

Relevante Daten sind in den folgenden Klassen verfügbar:

- `Lot` - Das Parkhaus
- `Vehicle` - Das Fahrzeug
- `Ticket` – Ticket inkl. Einfahrtszeitpunkt
- `SimClock` – Zeitgeber der Simulation einschließlich aktueller Sim-Uhrzeit

**Schritt 2 – Signatur festlegen.** Aus den beiden Spalten „Nötige Information"
ergibt sich, welche Parameter die Interface-Methoden `processIncoming(...)` und
`processOutgoing(...)` bekommen müssen. Das Interface muss **alle** Parameter enthalten!
Legen Sie darauf aufbauend die endgültige Signatur beider Interface-Methoden fest.

**Schritt 3 – Aufrufstellen anpassen.** Alle Aufrufe der Interface-Methoden liegen 
in der Klasse `Lot`. Passen Sie die beiden
Aufrufe in `Lot.enter(...)` und `Lot.exit(...)` so an, dass sie die neuen
Argumente übergeben. Mehr müssen Sie an der vorhandenen Infrastruktur **nicht**
ändern.

**Schritt 4 – Regeln implementieren.** Legen Sie im Package `parking.gate.impl`
neue Klassen an, die `Entrance` bzw. `Exit` implementieren und die Regeln
umsetzen. 

Für Abweisungen bzw. gültige Tickets stehen `Ticket.denyEntry(...)` und `Ticket.issue(...)` bereit; die Ausfahrt liefert ein `Receipt`.

**Abschließende Fragen:**

Zeigen Sie **Abstraktion**, **Kapselung**, **Vererbung** und **Polymorphie** jeweils an einer konkreten Stelle Ihres Codes bzw. des vorhandenen Projekts und erläutern Sie kurz,
warum es sich dort um die jeweilige Säule handelt.

Was ist ein Interface, und warum werden `Entrance` und `Exit`
hier als Interfaces eingesetzt? 

Hätte man statt der Interfaces auch **reguläre
   Vererbung** (eine gemeinsame Oberklasse) einsetzen können? 

---
