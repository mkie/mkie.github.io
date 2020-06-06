# Infos zur Corona Warn App

*Work in progress - Seite befindet sich im Aufbau*

Diese Seite soll einige der gängigen Fragen zur Corona Warn App (CWA) beantworten, die immer wieder gestellt werden.

Ich bemühe mich, den Sachverhalt so einfach wie möglich darzustellen. An der einen oder anderen Stelle kann es daher
sein, dass meine Darstellung nicht 100%ig korrekt ist. Wer alles noch genauer wissen möchte, dem empfehle ich die am
Ende verlinkten weiteren Informationen.

## Wieso? Wie?

### Was soll die CWA bringen?
In einer Pandemie ist die möglichst rasche Zurückverfolgung der Kontakte einer infizierten Person (IP) von entscheidender
Bedeutung, denn jede Kontaktperson einer IP kann von dieser bereits angesteckt worden sein ohne es zu
wissen. Bislang wird versucht, die Kontaktpersonen durch Befragung der IP herauszufinden - das ist umständlich,
fehleranfällig und zeitaufwändig. Mit der CWA soll das vereinfacht werden. Die Idee: Eine App kann - sollte
sich herausstellen, dass ihr Benutzer infiziert ist - alle Kontaktpersonen des Benutzers warnen.

### Wie funktioniert die CWA?
Wenn der Benutzer dem zugestimmt hat nutzt die CWA die Bluetooth-Funktion eines Smartphones und sendet regelmässig
kurze Funksignale (Broadcast Beacons / BB). Ausserdem registriert sie die BBs von anderen App-Benutzern und merkt
sich gesendete und empfangene BBs für einen Zeitraum von 14 Tagen. Die BBs werden dabei zufällig generiert
und in regelmässigen Abständen gewechselt. **Sie enthalten keine Informationen über die Identität oder den
Aufenthaltsort des App-Benutzers und lassen auch keine Rückschlüsse auf den Benutzer zu!**

Sollte nun ein Benutzer der CWA (z.B. weil er Krankheitssymptome hat) positiv getestet werden, also infiziert
sein, können die von seiner CWA *gesendeten* BBs auf einen Server hochgeladen werden. Dort liegen dann für einen
bestimmten Zeitraum die gesendeten BBs aller als infiziert getesteten Personen, die die CWA verwenden.
**Auch diese BBs enthalten keine Informationen darüber, wer sich wo wie lange mit wem aufgehalten hat!**

Die CWAs aller Benutzer vergleichen nun die auf dem Server liegenden gesendeten BBs mit den von ihnen empfangenen. Wenn
eine Übereinstimmung festgestellt wird, heisst das, dass ein Kontakt mit einer infizierten Person stattgefunden hat.
Die CWA informiert ihren Benutzer darüber (dabei kann sie eine Risikobewertung vornehmen).
Sinnvollerweise sollte er sich dann testen lassen und sich ggf. in Quarantäne begeben.
Dadurch kann verhindert werden, dass weitere Personen infiziert werden. **Die CWA schützt also nicht
den Benutzer selbst sondern alle seine zukünftigen Kontakte!**

## Fragen und Antworten

### Warum Google und Apple?
Zunächst: Google und Apple stellen nur die Grundfunktionen für das Senden und Empfangen der Bluetooth-Signale
zur Verfügung und haben diese seit kurzem (Mai 2020) in ihre Betriebssysteme Android bzw. iOS integriert.
Ohne diese Grundfunktionen wäre die Entwicklung einer sinnvoll funktionierenden CWA nicht möglich (z.B. könnte
eine App auf iOS sonst nur senden und empfangen während sie im Vordergrund läuft - mit entsprechend hohem
Energieverbrauch und mangelnder Sicherheit).

Die CWA wird übrigens **nicht** von Google oder Apple entwickelt sondern von Entwicklerteams in den jeweiligen
Ländern (in Deutschland sind dies SAP und die Telekom).

### Wird meine (GPS-)Position gespeichert?
**Nein**. Die CWA verwendt nur Bluetooth. Positionsdaten ("Wo befinde ich mich?") werden von der CWA weder verwendet
noch gespeichert.

### Wird mein Akku schneller leer wenn ich die CWA verwende?
**Nein**. Die CWA verwendet den BTLE Standard (Bluetooth Low Energy), der nur wenig Energie für das Senden
und nur minimal Energie für das Empfangen benötigt.

### Ist meine Privatsphäre in Gefahr?
**Nein**. Wie oben beschrieben: Weder auf dem Smartphones noch auf dem Server werden Daten gespeichert, die
eine Zuordnung zu Benutzern zulassen. Weil der Abgleich der BBs lokal auf den Smartphones der Benutzer stattfindet,
hat niemand eine Information darüber, wer wann mit wem Kontakt hatte. Das ist übrigens der Vorteil dieser
**dezentralen Lösung** gegenüber einer zentralen Lösung, bei der der Abgleich von einer zentralen Stelle
durchgeführt wird.

### Wird es zu Fehlalarmen kommen?
**Ja, ziemlich sicher**. Bluetooth ist leider nur bedingt geeignet, um Abstände zu messen, da dies von vielen
Faktoren abhängt (Signalstärke, Richtwirkung der Antennen in den Smartphones etc.). Ausserdem wird natürlich nicht
erkannt, ob sich zwischen zwei Smartphones eine Barriere (Wand, Scheibe) befindet. Die CWA kann deshalb nur eine
*Warnung* erzeugen. Ob tatsächlich eine Infektion stattgefunden hat, kann nur ein Test klären. Dennoch hoffen
Experten, dass Infektionen durch den Einsatz der CWA früher erkannt werden können. Wie gut das dann tatsächlich
funktioniert, wird sich zeigen.


## Mehr Informationen
Hier gibt's noch mehr Informationen zur CWA:
- [Exposure Notifications: Using technology to help public health authorities fight COVID‑19 (en)](https://www.google.com/covid19/exposurenotifications/)
- [Overview of COVID-19 Contact Tracing (en) bei Google](https://blog.google/documents/66/Overview_of_COVID-19_Contact_Tracing_Using_BLE_1.pdf)
- [Comic "Leben und Freiheit schützen - COVID-19 und Big Brother ein Schnippchen schlagen" vom DP3T-Projekt](https://github.com/DP-3T/documents/blob/master/public_engagement/cartoon/de/comic-de.pdf)
- []()


