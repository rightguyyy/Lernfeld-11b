---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Netzwerk -- Sicherheitsrelevante Anforderungen 1
---

Grundlage: Seite 369--373

## Aufgabe 1

Erläutern Sie, warum im BSI-Grundschutzkompendium so viele
Grundschutzbausteine im Zusammenhang mit IT-Netzwerken erstellt wurden.

::: {.solution}
- hohe Relevanz für die IT-Sicherheit

- sehr viele unterschiedliche Anforderungen

- zahlreiche unterschiedliche Netzwerkkomponenten und Dienste
:::

## Aufgabe 2

Erstellen Sie zu den 14 Kontrollbereichen einen Katalog mit TOM im
Zusammenhang mit Unternehmensnetzwerken.

::: {.solution}
Siehe Seite 373

Siehe <https://www.gesetze-im-internet.de/bdsg_2018/__64.html>

1.  Zugangskontrolle

    Verwehrung des Zugangs zu Verarbeitungsanlagen, mit denen die
    Verarbeitung durchgeführt wird, für Unbefugte

    - Serverraum mit Zugangskontrolle (z. B. Transponder,
      Schlüsselkarte, biometrische Zugangskontrolle, Schlüssel, PIN),
    - abschließbare Netzwerkschränke
    - Festlegung von Zutrittsbrechtigungen

2.  Datenträgerkontrolle

    Verhinderung des unbefugten Lesens, Kopierens, Veränderns oder
    Löschens von Datenträgern

    - Verschlüsselung von Datenträgern
    - Festlegung von sicheren Aufbewahrungsorten
    - Schulungen zum sicheren Umgang

3.  Speicherkontrolle

    Verhinderung der unbefugten Eingabe von personenbezogenen Daten
    sowie der unbefugten Kenntnisnahme, Veränderung und Löschung von
    gespeicherten personenbezogenen Daten

    - Authentifikation und Autorisierung des Zugriffs auf Daten und
      entsprechende Anwendungen zur Verarbeitung dieser Daten.

    - Schulungen zum sicheren Umgang

4.  Benutzerkontrolle

    Verhinderung der Nutzung automatisierter Verarbeitungssysteme mit
    Hilfe von Einrichtungen zur Datenübertragung durch Unbefugte

    - Authentifikation und Autorisierung des Zugriffs, Vergabe von Rolen
      und Pflege der Zugänge.
    - MFA
    - individuelle Bentuzerkonten,
    - ggf. Rollensystem

5.  Zugriffskontrolle

    Gewährleistung, dass die zur Benutzung eines automatisierten
    Verarbeitungssystems Berechtigten ausschließlich zu den von ihrer
    Zugangsberechtigung umfassten personenbezogenen Daten Zugang haben.

    Implementierung von geeigneten Zugriffskontrollmechanismen mit
    Authentication, Autorisierung, z. B. mit Rollen oder ACLs,

    Richtlinen zur Benutzerverwaltung

6.  Übertragungskontrolle

    Gewährleistung, dass überprüft und festgestellt werden kann, an
    welche Stellen personenbezogene Daten mit Hilfe von Einrichtungen
    zur Datenübertragung übermittelt oder zur Verfügung gestellt wurden
    oder werden können.

    Protokollierung der Zugriffe zu personenbezogenen Daten.

7.  Eingabekontrolle

    Gewährleistung, dass nachträglich überprüft und festgestellt werden
    kann, welche personenbezogenen Daten zu welcher Zeit und von wem in
    automatisierte Verarbeitungssysteme eingegeben oder verändert worden
    sind.

    Protokollierung der Zugriffe zu personenbezogenen Daten.

8.  Transportkontrolle

    Gewährleistung, dass bei der Übermittlung personenbezogener Daten
    sowie beim Transport von Datenträgern die Vertraulichkeit und
    Integrität der Daten geschützt werden.

    Implementierung von Verschlüsselungstechnologien für die sichere
    Übertragung von Daten über das Netzwerk (bspw. VPN, HTTPS) bzw.
    Verschlüsselung von Datenträgern.

9.  Wiederherstellbarkeit

    Gewährleistung, dass eingesetzte Systeme im Störungsfall
    wiederhergestellt werden können.

    - Implementierung von regelmäßigen Backups, Einhaltung von
      Best-Practices, 3-2-1
    - Testen von Backup

10. Zuverlässigkeit

    Gewährleistung, dass alle Funktionen des Systems zur Verfügung
    stehen und auftretende Fehlfunktionen gemeldet werden.

    Implementierung von Redundanzen (USV, redundante Netzteile, RAID,
    rundandate Netzwerkkarten, Switches) und Failover-Mechanismen, um
    die Netzwerkzuverlässigkeit zu gewährleisten, Monitoring von Netzen
    und Diensten

11. Datenintegrität

    Gewährleistung, dass gespeicherte personenbezogene Daten nicht durch
    Fehlfunktionen des Systems beschädigt werden können.

    ECC-RAM, Verwendung von Hashfunktionen und digitalen Signaturen, um
    die Integrität von Daten zu gewährleisten.

12. Auftragskontrolle

    Gewährleistung, dass personenbezogene Daten, die im Auftrag
    verarbeitet werden, nur entsprechend den Weisungen des Auftraggebers
    verarbeitet werden können.

    Vertragliche Regelungen zur Einhaltung der Datenschutzrichtlininen
    und ggf. Vereinbarung von konkreten TOMs, der Auftragnehmer
    einhalten muss.

    Implementierung der Domainregeln in der Anwendungssoftware und /
    oder Datenbank.

13. Verfügbarkeitskontrolle

    Gewährleistung, dass personenbezogene Daten gegen Zerstörung oder
    Verlust geschützt sind.

    Backups, Redundazen schaffen, um Verfügbarkeit zu erhöhen z. B.
    mithilfe von USV, RAID, zwei Netzteile Einrichtung von Überwachungs-
    und Alarmierungssystemen, um Ausfälle schnell zu erkennen und zu
    beheben. 3-2-1-Regel

    Geo-Redundanz

14. Trennbarkeit

    Gewährleistung, dass zu unterschiedlichen Zwecken erhobene
    personenbezogene Daten getrennt verarbeitet werden können.

    Anwendungssoftware in Subdomänen aufteilen, die jeweils selbst für
    die Datenverarbeitung zuständig sind.
:::

## Aufgabe 3

Ordnen Sie folgende Begriffe korrekt zu:

- Antiviren-Scanner
- Deep Packet Inspektion
- DMZ
- Firewall
- Patches
- HTTPS
- IDS
- IPS
- NGFW
- PAP-Struktur
- Perimeterbereich
- Paketfilter
- VPN
- Whitelist

a)  Programme, die übertragene Dateien und Kommunikationsdaten auf
    Malware überprüfen.
b)  Der Softwareentwickler bietet ein Sicherheitsupdate an.
c)  Die Webseite läuft über einen Sicherheitsserver.
d)  Mit Clients erfolgt die Kommunikation über eine verschlüsselte
    Tunnelverbindung.
e)  Zum Schutz vor Angriffen auf das interne Netz werden zwei
    Paketfilter und ein Schicht-7-Gateway gefordert.
f)  Bereich ab der Grenze zum externen Netz
g)  Zwischensicherheitszone für Server, die nicht im internen Netz
    eingebunden sind
h)  Besonders effektive Schutzeinheit auf den OSI-Schichten 2--7
i)  Schutzeinheit auf den OSI-Schichten 2 und 3
j)  Software, die IP-Adressen und Ports filtert und nach Regeln
    entscheidet
k)  Malware-Erkennungstool, das Pakete nach Regeln und
    Kontrollfunktionen danach prüft, ob es diese blockieren kann.
l)  Sicherheitstool, das ein Netzwerk überwacht und Angriffe erkennt,
    aber nicht abwehrt
m)  Sicherheitsverfahren in Firewalls, um neben dem Header auch
    verschlüsselte Inhalte zu filtern
n)  Liste mit erwünschten Absendern

::: {.solution}
a)  Programme, die übertragene Dateien und Kommunikationsdaten auf
    Malware überprüfen. → Antiviren-Scanner
b)  Der Softwareentwickler bietet ein Sicherheitsupdate an. → Patches
c)  Die Webseite läuft über einen Sicherheitsserver. → HTTPS
d)  Mit Clients erfolgt die Kommunikation über eine verschlüsselte
    Tunnelverbindung. → VPN
e)  Zum Schutz vor Angriffen auf das interne Netz werden zwei
    Paketfilter und ein Schicht-7-Gateway gefordert. → PAP-Struktur
f)  Bereich ab der Grenze zum externen Netz → Perimeterbereich
g)  Zwischensicherheitszone für Server, die nicht im internen Netz
    eingebunden sind → DMZ
h)  Besonders effektive Schutzeinheit auf den OSI-Schichten 2--7 → NGFW
i)  Schutzeinheit auf den OSI-Schichten 2 und 3 → Paketfilter (
    Firewall)
j)  Software, die IP-Adressen und Ports filtert und nach Regeln
    entscheidet → Firewall (Paketfilter)
k)  Malware-Erkennungstool, das Pakete nach Regeln und
    Kontrollfunktionen danach prüft, ob es diese blockieren kann. → IPS
l)  Sicherheitstool, das ein Netzwerk überwacht und Angriffe erkennt,
    aber nicht abwehrt → IDS
m)  Sicherheitsverfahren in Firewalls, um neben dem Header auch
    verschlüsselte Inhalte zu filtern → Deep Packet Inspektion
n)  Liste mit erwünschten Absendern → Whitelisting (Allowlist)
:::
