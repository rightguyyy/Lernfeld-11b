---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Benutzerrechte I
---

## Aufgabe 1

Beschreiben Sie, welches Schutzziel mit der Verwendung von Benutzername
und Passwort umgesetzt werden kann.

Vertraulichkeit.  
Durch Authentifizierung mit Benutzername und Passwort wird sichergestellt,
dass nur berechtigte Personen Zugriff auf ein System oder auf Daten erhalten.

## Aufgabe 2

Nennen Sie mindestens drei Einsatzbereiche von ACL.

- Dateisysteme (z. B. erweiterte Rechtevergabe unter Linux)
- Netzwerkgeräte (z. B. Router, Switches, Firewalls zur Paketfilterung)
- Anwendungen bzw. Betriebssysteme (Zugriffssteuerung auf Ressourcen)

## Aufgabe 3

Notieren Sie den Vorteil, der durch die Verwendung von Role Based Access
Control (RBAC) entsteht.

Rechte werden Rollen und nicht einzelnen Benutzern zugewiesen.
Dadurch wird die Verwaltung übersichtlicher, Änderungen sind einfacher
umsetzbar und Fehler bei der Rechtevergabe werden reduziert.

## Aufgabe 4

Recherchieren Sie das sogenannte Prinzip der geringsten Rechte.

Das Prinzip der geringsten Rechte (Least Privilege) besagt, dass Benutzer
und Prozesse nur die minimal notwendigen Rechte erhalten, die sie zur
Erfüllung ihrer Aufgaben benötigen. Dadurch wird das Sicherheitsrisiko
bei Fehlkonfigurationen oder Angriffen reduziert.

## Aufgabe 5

Erklären Sie den Unterschied zwischen einem Hard Link und einem Soft
Link in einem Linux-Dateisystem.

Ein Hard Link ist ein zusätzlicher Verzeichniseintrag, der direkt auf
dieselbe Inode wie die Originaldatei verweist. Wird die Originaldatei
gelöscht, bleibt der Hard Link bestehen.

Ein Soft Link (symbolischer Link) ist eine eigene Datei, die nur auf den
Pfad einer anderen Datei verweist. Wird die Zieldatei gelöscht, zeigt der
Soft Link ins Leere.

## Aufgabe 6

Für zwei Dateien in einem Linux-Dateisystem werden die folgenden Werte
für die Zugriffsrechte angegeben:

a)  Datei 1: 754  
b)  Datei 2: 740  

Geben Sie an, welche Aktionen der Benutzer, die Gruppe und andere
ausführen dürfen.

Datei 1 (754):

Benutzer: lesen, schreiben, ausführen  
Gruppe: lesen, ausführen  
Andere: lesen  

Datei 2 (740):

Benutzer: lesen, schreiben, ausführen  
Gruppe: lesen  
Andere: keine Rechte  

## Aufgabe 7

Beschreiben Sie die Problematik, die besteht, wenn unter Linux eine
ausführbare Datei dem Benutzer root gehört. Erläutern Sie die
entsprechenden Lösungsmöglichkeiten.

Wenn eine ausführbare Datei root gehört und mit erweiterten Rechten
ausgeführt wird, kann bei Sicherheitslücken oder Manipulationen
Schadcode mit Root-Rechten ausgeführt werden. Dadurch besteht die
Gefahr einer vollständigen Systemkompromittierung.

Lösungsmöglichkeiten:

- Prinzip der geringsten Rechte anwenden
- Sudo gezielt konfigurieren
- Dateirechte korrekt setzen
- Setuid-Bit nur wenn zwingend erforderlich verwenden
- Integrität der Dateien regelmäßig prüfen