# Infos zur Corona Warn App

*Work in progress - Seite befindet sich im Aufbau*

Diese Seite will einige der gängigen Fragen zur Corona Warn App (CWA) beantworten, die immer wieder gestellt werden.

## Wieso? Wie?

### Was soll die CWA bringen?
In einer Pandemie ist die möglichst rasche Zurückverfolgung der Kontakte einer infizierten Person (IP) von entscheidender
Bedeutung, denn jede Kontaktperson einer IP kann von dieser bereits angesteckt worden sein ohne es zu
wissen. Bislang wird versucht, die Kontaktpersonen durch Befragung der IP herauszufinden - das ist umständlich,
fehleranfällig und zeitaufwändig. Mit der CWA soll das vereinfacht werden. Die Idee: Eine App kann - sollte
sich heraustellen, dass ihr Benutzer infiziert ist - alle Kontaktpersonen des Benutzers warnen.

### Wie funktioniert die CWA?

Die CWA nutzt die Bluetooth-Funktion eines Smartphones und sendet - wenn der Benutzer dem zugestimmt hat -
regelmässig kurze Funksignale (Beacons). Ausserdem registriert sie die Funksignale von anderen App-Benutzern
und merkt sich diese.

## Fragen und Antworten

### Wird meine (GPS-)Position gespeichert?
**Nein**. Die CWA verwendt nur Bluetooth. Positionsdaten (wo bedinde mich) werden von der CWA weder verwendet
noch gespeichert.

### Warum Google und Apple?
Zunächst: Google und Apple stellen nur die Grundfunktionen für das Senden und Empfangen der Bluetooth-Signale
zur Verfügung und haben diese seit kurzem (Mai 2020) in ihre Betriebssysteme Android bzw. iOS integriert.
Ohne diese Grundfunktionen wäre die Entwicklung einer sinnvoll funktionierenden CWA nicht möglich (z.B. könnte
eine App auf iOS sonst nur senden und empfangen während sie im Vordergrund läuft - mit entsprechend hohem
Energieverbrauch und mangelnder Sicherheit).

Die CWA wird übrigens **nicht** von Google oder Apple entwickelt sondern von Entwicklerteams in den jeweiligen
Ländern (in Deutschland sind dies SAP und die Telekom).

### Wird mein Akku schneller leer wenn ich die CWA verwende?
**Nein**. Die CWA verwendet den BTLE Standard (Bluetooth Low Energy), der nur wenig Energie für das Senden
und nur minimal Energie für das Empfangen benötigt.

