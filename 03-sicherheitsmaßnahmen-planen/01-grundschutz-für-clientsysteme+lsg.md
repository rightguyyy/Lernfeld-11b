---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Grundschutz für Clientsysteme planen
---

## Aufgabe 1

Ein Kunde möchte den Schutz seiner Endgeräte überarbeiten.

a)  Für einen sinnvollen Schutz des Endgeräts ist die Zugriffsregelung
    auf die Geräte von hoher Bedeutung. Recherchieren Sie drei Methoden,
    den Zugriff auf ein Gerät zu regeln.

    ::: {.solution}
    - Benutzeranmeldung
    - Sperren des Gerätes nach einer bestimmten Zeitdauer der
      Inaktivität
    - Sichern der Hardware (z. B. Laptop) gegen Diebstahl durch
      Kabelschloss
    - Gesichtserkennung
    - Fingerabdruckscanner
    - Karten oder Sticks
    :::

<!-- -->

b)  Die Daten eines Endsystems müssen gesichert werden. Dazu werden
    regelmäßige Backups erstellt. Entscheiden Sie, welche Art von Daten
    eines Benutzerendsystems mittels Backup gesichert werden sollen.

    ::: {.solution}
    - Daten, die vom Benutzer bearbeitet und/oder erstellt werden (z. B.
      Office-Dokumente, Notizen, Bilder, Dateien zu Projekt, Quellcode)

    - Daten des Betriebssystems oder von Anwendungen brauchen nur dann
      gesichert werden, wenn diese individuell erstellt werden, mit
      einem hohen Aufwand bei der Wiederherstellung verbunden wären und
      nicht zentral verwaltet werden.

    - E-Mails und Kontakte

    - Benutzerprofil

    - privaten Schlüssel (SSH), Keyring
    :::

<!-- -->

c)  Bei mobilen Endgeräten ist eine Verschlüsselung der eingebauten
    Datenträger sinnvoll. Bei Verlust z. B. durch Diebstahl eines
    Gerätes führt so auch ein physischer Zugriff auf die Speichermedien
    nicht zu unberechtigtem Lesen der Daten.

    Diskutieren Sie innerhalb der Gruppe, ob die Verschlüsselung von
    Datenträgern auch bei stationären Geräten sinnvoll ist. Sammeln Sie
    Pro- und Kontra-Argumente.

    ::: {.solution}
    - Diebstahl von stationären Geräten

    - Beim Austausch der Datenträger oder des gesamten Gerätes ist das
      Löschen bzw. Unbrauchbarmachen der gespeicherten Daten einfacher,
      da nur bestimmte Bereiche auf dem Datenträger gelöscht bzw.
      überschrieben werden müssen, um ihn unbrauchbar zu machen.

    - 
    :::

<!-- -->

d)  Zur Erhöhung der Güte des Passworts sollen bestimmte Passwortregeln
    bezüglich Länge und Passwortraum verwendet werden.

    Füllen Sie die nachfolgende Tabelle aus. Geben Sie jeweils die
    Anzahl der möglichen verschiedenen Passwörter an und berechnen Sie,
    wie lange es dauert, das Passwort durchschnittlich zu ermitteln,
    wenn Sie 1 000 000 000 Passwörter pro Sekunde ausprobieren können.

    ::: {text="xs"}
    | Passwortlänge | Passwortzeichen | Anzahl Passwörter | benötigte Zeit für das »Knacken« |
    |----|----|----|----|
    | 8 | Zahlen | 100.000.000 | \< 1s |
    | 12 | Zahlen | 1.000.000.000.000 | 500 s--8,3 min (durchschnittlich wird nur die Hälfte der Zeit benötigt) |
    | 8 | Zahlen und Buchstaben; groß, klein; 62 Zeichen |  |  |
    | 12 | Zahlen und Buchstaben; groß, klein; 62 Zeichen |  |  |
    | 8 | Zahlen und Buchstaben; groß, klein, Sonderzeichen; 94 Zeichen |  |  |
    | 12 | Zahlen und Buchstaben; groß, klein, Sonderzeichen; 94 Zeichen |  |  |
    | 16 | Zahlen und Buchstaben; groß, klein, Sonderzeichen; 94 Zeichen |  |  |
    :::

    :::: {.solution}
    ::: {text="xs"}
    | Passwortlänge | Passwortzeichen | Anzahl Passwörter | benötigte Zeit für das »Knacken« |
    |----|----|----|----|
    | 8 | Zahlen | 100.000.000 | \< 1s |
    | 12 | Zahlen | 1.000.000.000.000 | 500 s--8,3 min (durchschnittlich wird nur die Hälfte der Zeit benötigt) |
    | 8 | Zahlen und Buchstaben; groß, klein; 62 Zeichen | ca. 218 Billionen | ca. 30 Stunden |
    | 12 | Zahlen und Buchstaben; groß, klein; 62 Zeichen | ca. $3,2 \cdot 10^{21}$ | ca. 51152 Jahre |
    | 8 | Zahlen und Buchstaben; groß, klein, Sonderzeichen; 94 Zeichen | ca. 6 Billiarden | ca. 35.28 Tage |
    | 12 | Zahlen und Buchstaben; groß, klein, Sonderzeichen; 94 Zeichen | ca. $475,9 \cdot 10^{21}$ | ca. 7,55 Millionen Jahre |
    | 16 | Zahlen und Buchstaben; groß, klein, Sonderzeichen; 94 Zeichen | ca. $37 \cdot 10^{30}$ | ca. 589 Billionen Jahre |
    :::
    ::::

<!-- -->

e)  Ein Auszubildender aus dem ersten Ausbildungsjahr bittet Sie um eine
    Erklarung zur Funktionsweise eines Virenscanners.

    Erstellen Sie einen Programmablaufplan, der die Funktionsweise eines
    Virenscanners abbildet Beginnen Sie mit dem Ereignis »Datei wird vom
    Scanner eingelesen«.

    ::: {.solution}
        Datei wird vom Scanner eingelesen

                 |
                 V

        Laden von Updates der Signaturdatenbank

                 |
                 V

        Datei auf Bitmuster (Signatur) absuchen
        und mit Signaturdatenbank abgleichen
                 
                 |
                 V
                 
            /- Datei enthält Signatur -\
         ja |                          | nein
            V                          V
            
        Datei löschen
        oder in Quarantäne-
        verzeichnis verschieben
    :::

## Aufgabe 2

Beschreiben Sie, was unter der Trennung von Betriebssystem- und
Datenadministration verstanden wird.

::: {.solution}
#### Serveradministratior

- kann Dateien anlegen, manipulieren und löschen
- kann Programme auf dem Server installieren
- kann Benutzer anlegen

#### DB-Administratior

- administriert die Datenbankanwendung
- kann neue DBs anlegen
- kann Tabellen anlegen, manipulieren und löschen
- kann DB-Benutzer anlegen
- hat *keinen* Zugriff auf die Rechte des Server-Administrators
:::

## Aufgabe 3

a)  Geben Sie mindestens drei Aspekte an, die beim
    Aktualisierungsmanagement zu beachten sind.

    ::: {.solution}
    - Bezugsquellen (online) prüfen: Zertifikate, SHA2-Prüfsummen der
      Software, PPA-Quellen (Personal Package Archive bei Ubuntu)
      überprüfen usw.

    - Regressionstest durchführen: Vor dem produktiven Einsatz Tests
      einplanen, um den Betrieb nicht zu stören

    - Informationsmanagement sicherstellen: Aktive Verfolgung von
      Nachrichten zu Sicherheitslücken der eingesetzten Software (z. B.
      Newsletter von Sicherheitsforen)

    - Hardware-Anforderungen prüfen (vor dem produktiven Einsatz)

    - Änderungen im Umgang: Benutzer-Schulungsbedarf prüfen, Mitarbeiter
      informieren
    :::

<!-- -->

b)  Nennen Sie Möglichkeiten, um Windows-Clients aktuell zu halten.

    ::: {.solution}
    - Paketmanager (Chocolately for Business)  
    - Microsoft Store
      - Microsoft Store for Business
      - Microsoft Store for Education
    - Windows Server Update Service (WSUS)
    - Deployment-Software wie Deskcenter, Empirum, Microsoft Endpoint
      Configuration Mananger (MECM)
    :::
