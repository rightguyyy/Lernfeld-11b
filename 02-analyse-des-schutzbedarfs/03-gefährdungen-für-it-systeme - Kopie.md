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

    |Personen                                | Begründung                                           |
    |                                        |                                                      |
    | Administratoren der Server             | Um Wartungsarbeiten am Server vornehmen zu können    |
    | Geschäftsleitung                       |  Entscheidungsbefugnis, Notfälle                     |
    | IT-Mitarbeiter für Bandsicherung       |  Backup und Wiederherstellung von Daten              |

<!-- -->

b)  Nachdem im ersten Schritt die Berechtigten festgelegt wurden, bittet
    Sie Ihr Vorgesetzter, im IT-Grundschutz-Kompendium weitere
    Anforderungen an den Serverraum nachzuschlagen. Lesen Sie dazu im
    IT-Grundschutz-Kompendium im Baustein „INF.2 Rechenzentrum sowie
    Serverraum". Notieren Sie die Anforderungen in Bezug auf die
    Zutrittskontrolle.

    Zutritt nur für autorisierte Personen
    Dokumentation von Zutritten (Protokoll)
    Physische Sicherung: abschließbare Türen, Videoüberwachung optional
    Notfallregelungen (z. B. Rettungswege, Panikschlösser)

<!-- -->

c)  Der Kunde wünscht eine Regelung der Zutrittskontrolle für den
    Serverraum. Sie sollen ein entsprechendes System auswählen. Nach
    einer Recherche entscheiden Sie sich für ein System mit RFID-Tokens.

    Formulieren Sie in Partnerarbeit Fragen, die bei der Einführung
    eines solchen Systems geklärt werden müssen.

    Wer erhält Token und wie wird die Vergabe dokumentiert?
    Was passiert bei Verlust oder Diebstahl eines Tokens?
    Wie lange gilt die Berechtigung?
    Werden Zutritte protokolliert und wie lange gespeichert?
    Gibt es Notfallzugänge oder Ausnahmen?

## Aufgabe 2

Bei einem Ihrer Kunden wurden Fensterscheiben beschädigt. Es kam zu
keinen weiteren Folgen, da die Alarmanlage sofort aktiviert wurde.
Trotzdem ist ein hoher Sachschaden entstanden. Es soll ein Videosystem
angeschafft werden. Die drei Kameras sollen eine Auflösung von 1024 x
768 mit einer Farbtmfe von 8 Bit besmzen Die Kameras sollen mit 30 fps
filmen. Die Daten werden nach einem Tag überschrieben.

a)  Ermitteln Sie die nötige Datenmenge in TiB (gerundet auf 2
    Nachkommastellen).

    Auflösung: 1024 × 768 × 8 Bit = 6.291.456 Bit ≈ 0,75 MB pro Frame
    30 fps → 0,75 MB × 30 × 60 × 60 × 24 ≈ 1,94 TB pro Kamera
    3 Kameras → 1,94 × 3 ≈ 5,82 TB pro Tag

b)  Die Kameras sollen gegen Vandalismus geschützt sein. Recherchieren
    Sie, was unter einem IK-Stoßfestigkeitsgrad verstanden wird, und
    entscheiden Sie sich begründet für eine Schutzart, die Sie gegen
    Vandalismus einsetzen möchten.

    IK = Schutz gegen mechanische Stöße (Vandalismus)
    Empfehlung: IK10 für maximale Stoßfestigkeit gegen Schläge und Würfe

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

Mindestentfernung von 200 km zwischen Rechenzentren

Reduziert Risiko, dass Naturkatastrophen (Hochwasser, Brand, Stromausfall) beide Standorte gleichzeitig treffen

Erhöht Verfügbarkeit und Ausfallsicherheit

Sicherstellung georedundanter Backups