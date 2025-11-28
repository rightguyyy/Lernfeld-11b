---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Gefährdungen für IT-Systeme
---
 
## Aufgabe 1
 
Im Serverraum eines Kunden hat eine Reinigungskraft unbeabsichtigt die
Stromversorgung einer USV unterbrochen. Der Zwischenfall wurde durch die
Benachrichtigung einer Monitoring-Software sofort bemerkt und ein
Datenverlust konnte vermieden werden.
 
Dieses unbeabsichtigte Ereignis hat die Mitarbeitenden der IT-Abteilung
aber aufgeschreckt.
 
a)  Ihr Vorgesetzter bittet Sie, ein Konzept mit Zutrittsberechtigungen
    für den Serverraum des Kunden zu entwickeln.
 
    Er schlägt vor, dass Sie zunächst den Personenkreis eingrenzen der
    Zutritt zum Serverraum haben muss. Er bittet Sie, die Auswahl zu
    begründen. Verwenden Sie die nachfolgende Tabelle.
 
    | Personen                          | Begründung                                        |
    |-----------------------------------|---------------------------------------------------|
    | Administratoren der Server        | Um Wartungsarbeiten am Server vornehmen zu können |
    | Geschäftsleitung                  | Nur bei Audits oder Kontrollen, in Begleitung einer berechtigten Person.
    | IT-Mitarbeiter für Bandsicherung  | Zugriff zum Wechseln und Prüfen der Sicherungsmedien.
 
<!-- -->
 
b)  Nachdem im ersten Schritt die Berechtigten festgelegt wurden, bittet
    Sie Ihr Vorgesetzter, im IT-Grundschutz-Kompendium weitere
    Anforderungen an den Serverraum nachzuschlagen. Lesen Sie dazu im
    IT-Grundschutz-Kompendium im Baustein „INF.2 Rechenzentrum sowie
    Serverraum". Notieren Sie die Anforderungen in Bezug auf die
    Zutrittskontrolle.
 
A:
 
Zutritt nur für berechtigte Personen.
Zutritte müssen protokolliert werden.
Raum ist ständig verschlossen zu halten.
Besucher nur mit Begleitung.
Berechtigungen regelmäßig prüfen und anpassen.
 
 
<!-- -->
 
c)  Der Kunde wünscht eine Regelung der Zutrittskontrolle für den
    Serverraum. Sie sollen ein entsprechendes System auswählen. Nach
    einer Recherche entscheiden Sie sich für ein System mit RFID-Tokens.
 
    Formulieren Sie in Partnerarbeit Fragen, die bei der Einführung
    eines solchen Systems geklärt werden müssen.
 
A:
 
Wer erhält Zutritt?
Wie wird der Verlust eines Tokens gehandhabt?
Wie lange gelten Berechtigungen?
Werden Zutritte protokolliert?
Funktioniert das System bei Stromausfall?
 
 
## Aufgabe 2
 
Bei einem Ihrer Kunden wurden Fensterscheiben beschädigt. Es kam zu
keinen weiteren Folgen, da die Alarmanlage sofort aktiviert wurde.
Trotzdem ist ein hoher Sachschaden entstanden. Es soll ein Videosystem
angeschafft werden. Die drei Kameras sollen eine Auflösung von 1024 x
768 mit einer Farbtiefe von 8 Bit besitzen Die Kameras sollen mit 30 fps
filmen. Die Daten werden nach einem Tag überschrieben.
 
a)  Ermitteln Sie die nötige Datenmenge in TiB (gerundet auf 2
    Nachkommastellen).
 
A:
 
3 Kameras × 1024×768 px × 8 Bit × 30 fps × 86 400 s / 2^40 = 5,56 TiB pro Tag
 
 
<!-- -->
 
b)  Die Kameras sollen gegen Vandalismus geschützt sein. Recherchieren
    Sie, was unter einem IK-Stoßfestigkeitsgrad verstanden wird, und
    entscheiden Sie sich begründet für eine Schutzart, die Sie gegen
    Vandalismus einsetzen möchten.
 
A:
 
Gibt Widerstand gegen mechanische Schläge an (EN 62262).
IK10 = 20 J Schlagenergie → geeignet für vandalismussichere Kameras.
 
 
## Aufgabe 3
 
Ihr Kunde betreibt ein kleines Rechenzentrum. Dort werden größere Mengen
Daten verarbeitet. Im Zuge jüngster Hochwasserkatastrophen wurde
entschieden, zusätzliche Sicherheit zu gewährleisten.
 
Sie werden gebeten, bei der Wahl eines georedundanten Standorts zu
unterstützen. Als erste Informationsquelle dient Ihnen das Dokument des
BSI „Kriterien für die Standortwahl von Rechenzentren". Das Kapitel 4
gibt Hilfestellung zur Wahl eines Standorts für ein georedundantes
Rechenzentrum.
 
Recherchieren Sie in Partnerarbeit Gründe für die Mindestentfernung von
200 km zwischen den Rechenzentren.
 
 
A:
 
Gründe für Mindestentfernung von 200 km:
 
Schutz vor regionalen Katastrophen (z. B. Hochwasser, Stromausfall).
Getrennte Infrastruktur (Strom, Netz, Versorgung).
Erhöhte Ausfallsicherheit und Betriebskontinuität.
 