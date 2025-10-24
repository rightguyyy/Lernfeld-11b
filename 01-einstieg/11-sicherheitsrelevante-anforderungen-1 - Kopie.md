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

Endpoint Security bezeichnet Maßnahmen, die direkt an Endgeräten wie PCs, Laptops oder Smartphones ansetzen. Dadurch wird verhindert, dass infizierte oder manipulierte Geräte als Einstiegspunkt für Angriffe in das Netzwerk genutzt werden können.  
Zero Trust Security bedeutet, dass keinem Gerät, Benutzer oder Dienst automatisch vertraut wird. Jeder Zugriff muss kontinuierlich überprüft und freigegeben werden, was Missbrauch deutlich erschwert.  
Sicherheit in SDN (Software Defined Networking) nutzt eine zentrale Steuerungsebene. Damit lassen sich Sicherheitsrichtlinien flexibel anpassen und Angriffe schneller erkennen und blockieren.  
Zusammen ergibt sich ein höheres Schutzniveau, da sowohl Endgeräte als auch Netzwerkstrukturen konsequent abgesichert und überwacht werden.

## Aufgabe 2

Erstellen Sie zu den 14 Kontrollbereichen einen Katalog mit TOM im
Zusammenhang mit Unternehmensnetzwerken.

1. Zugangskontrolle

MFA, Chipkarten, Zutrittsprotokolle.

2. Datenträgerkontrolle

Verschlüsselung, sichere Löschung, Ausgabeprotokoll.

3. Speicherkontrolle

Rechteverwaltung, verschlüsselte Backups, Integritätsprüfung.

4. Benutzerkontrolle

Zentrales Identity Management, RBAC, Berechtigungsreviews.

5. Zugriffskontrolle

ACLs, VLANs, least privilege, zeitlich begrenzte Zugriffe.

6. Übertragungskontrolle

TLS/VPN, DLP, IDS/IPS.

7. Eingabekontrolle

Audit-Logs, Änderungsprotokolle, Versionierung.

8. Transportkontrolle

IPsec/TLS, Netzsegmentierung, Monitoring.

9. Wiederherstellbarkeit

Backups, Recovery-Tests, Offsite-Kopien.

10. Zuverlässigkeit

HA-Systeme, Monitoring, SLA-Checks.

11. Datenintegrität

Hashes, Signaturen, Change-Detection.

12. Auftragskontrolle

Verträge, technische Zugangsbeschränkungen, Audits.

13. Verfügbarkeitskontrolle

DDoS-Schutz, Redundanz, Lasttests.

14. Trennbarkeit

Mandantentrennung, getrennte Umgebungen, Zugriffsbeschränkung.
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

a) Antiviren-Scanner
b) Patches
c) HTTPS
d) VPN
e) PAP-Struktur
f) Perimeterbereich
g) DMZ
h) NGFW
i) Firewall
j) Paketfilter
k) IPS
l) IDS
m) Deep Packet Inspektion
n) Whitelist
