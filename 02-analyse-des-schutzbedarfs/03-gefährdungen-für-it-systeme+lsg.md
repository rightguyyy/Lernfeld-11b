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

    | Personen | Begründung |
    |----|----|
    | Administratoren der Server | Um Wartungsarbeiten am Server vornehmen zu können |
    | Geschäftsleitung |  |
    | IT-Mitarbeiter für Bandsicherung |  |

    ::: {.solution}
    | Personen                                                                                        | Begründung |
    |----|----|
    | Administratoren der Server | Um Wartungsarbeiten am Server vornehmen zu können |
    | Geschäftsleitung | keine normale Zutrittsberechtigung notwendig, zur personellen Rudundanz muss die Geschäftsleitung weiteren Personen Zutrittsberechtigungen geben können |
    | IT-Mitarbeiter für Bandsicherung | Eingeschränkte Zutrittsberechtigung für diese Aufgabe, auch zur Wiederherstellung, z. B. durch räumliche Trennung oder ur für bestimmte Serverschränke |
    | Reinigungskräfte | Reinigung des Serverraumes, nur unter Begleitung |
    | Brandschutzbeauftragte | Sichtung des Serverraumes, nur unter Begleitung |
    | Feuerwehr über Brandschutzanlage | Im Brandfall muss diese auch den Serverraum betreten können |
    | Datenschutzbeauftragter | in der Regel ist kein eigenständiger Zugang notwendig, ggf. in besonderen Fällen bei besonderen Anlagen, |
    | für die keine alternativen Zugriffsöglichkeiten bestehen |  |
    :::

<!-- -->

b)  Nachdem im ersten Schritt die Berechtigten festgelegt wurden, bittet
    Sie Ihr Vorgesetzter, im IT-Grundschutz-Kompendium weitere
    Anforderungen an den Serverraum nachzuschlagen. Lesen Sie dazu im
    IT-Grundschutz-Kompendium im Baustein „INF.2 Rechenzentrum sowie
    Serverraum". Notieren Sie die Anforderungen in Bezug auf die
    Zutrittskontrolle.

    ::: {.solution}
    »Der Zutritt zum Rechenzentrum MUSS kontrolliert werden.
    Zutrittsrechte MÜSSEN gemäß der Vorgaben des Bausteins ORP.4
    Identitäts- und Berechtigungsmanagement vergeben werden. Für im
    Rechenzentrum tätige Personen MUSS sichergestellt werden, dass diese
    keinen Zutritt zu IT-Systemen außerhalb ihres Tätigkeitsbereiches
    erhalten.

    Alle Zutrittsmöglichkeiten zum Rechenzentrum MÜSSEN mit
    Zutrittskontrolleinrichtungen ausgestattet sein. Jeder Zutritt zum
    Rechenzentrum MUSS von der Zutrittskontrolle individuell erfasst
    werden. Im Falle eines Serverraums SOLLTE geprüft werden, ob eine
    Überwachung aller Zutrittsmöglichkeiten sinnvoll ist.

    Es MUSS regelmäßig kontrolliert werden, ob die Regelungen zum
    Einsatz einer Zutrittskontrolle eingehalten werden.

    Die Anforderungen der Institution an ein Zutrittskontrollsystem
    MÜSSEN in einem Konzept ausreichend detailliert dokumentiert
    werden.« (Seite 5--6)
    :::

<!-- -->

c)  Der Kunde wünscht eine Regelung der Zutrittskontrolle für den
    Serverraum. Sie sollen ein entsprechendes System auswählen. Nach
    einer Recherche entscheiden Sie sich für ein System mit RFID-Tokens.

    Formulieren Sie in Partnerarbeit Fragen, die bei der Einführung
    eines solchen Systems geklärt werden müssen.

    ::: {.solution}
    - Wer erhält ein Token?
    - Wie organisiert man den Ausgabeprozess?
    - Was passiert bei Verlust eines RFID-Tokens?
    - Wie werden Ausnahmen für Notfälle oder Vertretungen gehandhabt?
    - Wie wird das System bei technischen Ausfällen oder Notfällen
      gesichert oder was passiert?
    - Gibt es eine zusätzliche PIN-Eingabe für
      Zwei-Fakter-Authentifizierung?
    - Wie ist die Hardware-Auswahl?
    - Wie wird der Zutritt für externe Dienstleister geregelt?
    - Wie kann die Weitergabe eines persönlichen Tokens vermieden
      werden?
    - Welche Zugangstufen sollen es geben?
    - Zeitliche Begrenzung der Zugangsmöglichkeiten?
    - Wie sicher ist die eingesetzte Technologie?
    :::

## Aufgabe 2

Bei einem Ihrer Kunden wurden Fensterscheiben beschädigt. Es kam zu
keinen weiteren Folgen, da die Alarmanlage sofort aktiviert wurde.
Trotzdem ist ein hoher Sachschaden entstanden. Es soll ein Videosystem
angeschafft werden. Die drei Kameras sollen eine Auflösung von 1024 x
768 mit einer Farbtiefe von 8 Bit besitzen Die Kameras sollen mit 30 fps
filmen. Die Daten werden nach einem Tag überschrieben.

a)  Ermitteln Sie die nötige Datenmenge in TiB (gerundet auf 2
    Nachkommastellen).

    ::: {.solution}

    $$3 \cdot (1024 \cdot 768 \cdot 30 \cdot 3600 \cdot 24) / 2^{40} = 5,56 \text{TB}$$
    :::

<!-- -->

b)  Die Kameras sollen gegen Vandalismus geschützt sein. Recherchieren
    Sie, was unter einem IK-Stoßfestigkeitsgrad verstanden wird, und
    entscheiden Sie sich begründet für eine Schutzart, die Sie gegen
    Vandalismus einsetzen möchten.

    ::: {.solution}
    IK10 oder IK11/IK10+, dies entspricht einem Hammerschlag mit 400g
    bzw. 1000g.
    :::

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

::: {.solution}
»Grundsätzlich muss sich der Abstand einander Georedundanz gebender RZ
an dem in der Einleitung dieses Kapitels genannten Grundgedanken
orientieren. Da es aber, insbesondere durch den Blick in die
Vergangenheit, nicht möglich ist, zukünftige potenziell schädliche
Situationen und Ereignisse ausreichend genau vorherzusagen, sollten
einander Georedundanz gebende RZ einen Mindestabstand von ca. 200 km
zueinander haben. Dieser Wert orientiert sich an

- Erfahrungswerten aus der Vergangenheit zu den flächigen Ausdehnungen
  von Großschadensereignissen,
- dem Gedanken, dass die Wahrscheinlichkeit einer gleichzeitigen
  Beeinträchtigung mehrerer RZ einer Redundanzgruppe durch dasselbe
  Ereignis mit wachsendem Abstand der RZ zueinander sinkt,
- den in der Praxis erreichbaren Abstandsgrenzen, die sich aus der
  begrenzten Fläche der Bundesrepublik Deutschland ergeben.

Ist im Einzelfall ein deutlich geringerer Abstand unabweisbar, ist diese
Notwendigkeit schriftlich ausführlich darzulegen und einer Risikoanalyse
zu unterziehen. Keinesfalls sollen georedundante RZ weniger als 100 km
voneinander entfernt liegen.«
:::
