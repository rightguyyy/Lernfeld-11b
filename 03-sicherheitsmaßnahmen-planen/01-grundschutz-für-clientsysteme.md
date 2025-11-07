---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Grundschutz für Clientsysteme planen
---
 
::: {.task}
## Aufgabe 1
 
Ein Kunde möchte den Schutz seiner Endgeräte überarbeiten.
 
a)  ::: {.subtask}
    Für einen sinnvollen Schutz des Endgeräts ist die Zugriffsregelung
    auf die Geräte von hoher Bedeutung. Recherchieren Sie drei Methoden,
    den Zugriff auf ein Gerät zu regeln.
    :::
 
 
A:
 
Passwort-/PIN-Schutz
Zwei-Faktor-Authentifizierung (z. B. Token, App)
Biometrische Anmeldung (Fingerabdruck, Gesichtserkennung)
 
<!-- -->
 
b)  ::: {.subtask}
    Die Daten eines Endsystems müssen gesichert werden. Dazu werden
    regelmäßige Backups erstellt. Entscheiden Sie, welche Art von Daten
    eines Benutzerendsystems mittels Backup gesichert werden sollen.
    :::
 
A:
 
Benutzerdateien (Dokumente, Bilder, Projekte)
System- und Programmeinstellungen
E-Mails und lokale Datenbanken
 
<!-- -->
 
c)  ::: {.subtask}
    Bei mobilen Endgeräten ist eine Verschlüsselung der eingebauten
    Datenträger sinnvoll. Bei Verlust z. B. durch Diebstahl eines
    Gerätes führt so auch ein physischer Zugriff auf die Speichermedien
    nicht zu unberechtigtem Lesen der Daten.
 
    Diskutieren Sie innerhalb der Gruppe, ob die Verschlüsselung von
    Datenträgern auch bei stationären Geräten sinnvoll ist. Sammeln Sie
    Pro- und Kontra-Argumente.
    :::
 
A:
 
| Pro                                              | Kontra                                    |
| ------------------------------------------------ | ----------------------------------------- |
| Schutz bei Diebstahl oder unbefugtem Zugriff     | Zusätzliche Systembelastung               |
| Datenschutzkonformität (z. B. DSGVO)             | Komplexere Wiederherstellung bei Defekten |
| Schutz sensibler Daten in Mehrbenutzerumgebungen | Administrativer Aufwand                   |
 
 
<!-- -->
 
d)  :::: {.subtask}
    Zur Erhöhung der Güte des Passworts sollen bestimmte Passwortregeln
    bezüglich Länge und Passwortraum verwendet werden.
 
    Füllen Sie die nachfolgende Tabelle aus. Geben Sie jeweils die
    Anzahl der möglichen verschiedenen Passwörter an und berechnen Sie,
    wie lange es dauert, das Passwort durchschnittlich zu ermitteln,
    wenn Sie 1 000 000 000 Passwörter pro Sekunde ausprobieren können.
 
    ::: {text="xs"}
 
A:
 
| Passwortlänge | Passwortzeichen | Anzahl Passwörter | benötigte Zeit für das »Knacken« |
| ------------- | --------------- | ----------------- | -------------------------------- |
| 8             | Zahlen          | 100 000 000       | < 1 s                            |
| 12            | Zahlen          | 1 000 000 000 000 | ca. 8 min                        |
| 8             | 62 Zeichen      | 2,18 × 10¹⁴       | ca. 30 h                         |
| 12            | 62 Zeichen      | 3,23 × 10²¹       | ca. 5,1 × 10⁴ Jahre              |
| 8             | 94 Zeichen      | 6,1 × 10¹⁵        | ca. 35 Tage                      |
| 12            | 94 Zeichen      | 4,7 × 10²³        | ca. 7,5 × 10⁶ Jahre              |
| 16            | 94 Zeichen      | 7,3 × 10³¹        | ca. 1,2 × 10¹⁵ Jahre             |
 
 
<!-- -->
 
e)  ::: {.subtask}
    Ein Auszubildender aus dem ersten Ausbildungsjahr bittet Sie um eine
    Erklarung zur Funktionsweise eines Virenscanners.
 
    Erstellen Sie einen Programmablaufplan, der die Funktionsweise eines
    Virenscanners abbildet Beginnen Sie mit dem Ereignis »Datei wird vom
    Scanner eingelesen«.
    :::
:::
 
::: {.task}
 
A:
 
Datei wird eingelesen
Signaturdatenbank laden
Vergleich der Dateiinhalte mit bekannten Signaturen
Falls Treffer → Datei isolieren / löschen / melden
Falls kein Treffer → Datei freigeben
Optional: Heuristische Analyse → Bewertung verdächtigen Verhaltens
Ergebnisprotokoll schreiben
 
## Aufgabe 2
 
Beschreiben Sie, was unter der Trennung von Betriebssystem- und
Datenadministration verstanden wird.
:::
 
::: {.task}
 
A:
 
Betriebssystemadministration: Installation, Updates, Benutzerverwaltung
 
Datenadministration: Zugriff auf Unternehmensdaten, Datenpflege
→ Ziel: Sicherheit, Nachvollziehbarkeit, geringeres Fehlerrisiko
 
## Aufgabe 3
 
a)  ::: {.subtask}
    Geben Sie mindestens drei Aspekte an, die beim
    Aktualisierungsmanagement zu beachten sind.
    :::
 
A:
 
Updates regelmäßig und zeitnah einspielen
Kompatibilität vor Rollout prüfen
Updates dokumentieren und testen
 
<!-- -->
 
b)  ::: {.subtask}
    Nennen Sie Möglichkeiten, um Windows-Clients aktuell zu halten.
    :::
:::
 
A:
 
Windows Update / WSUS
Microsoft Intune oder SCCM
Gruppenrichtlinien mit zentraler Update-Steuerung
Manuelle oder automatische Update-Funktion