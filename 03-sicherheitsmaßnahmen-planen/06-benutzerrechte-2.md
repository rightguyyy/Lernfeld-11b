---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Benutzerrechte II
---

## Aufgabe 1

Unter Linux werden Benutzer-Passwörter in der Datei `/etc/shadow` gespeichert.  
Die Datei `/etc/passwd` enthält zwar Benutzerkonteninformationen, aber keine
Passwort-Hashes mehr. Die eigentlichen Passwort-Hashes liegen aus
Sicherheitsgründen in `/etc/shadow`, auf das nur der Benutzer `root`
Zugriff hat.

## Aufgabe 2

Die zwei gängigen Systeme für Netzwerkfreigaben unter Linux sind NFS
(Network File System) und Samba (SMB/CIFS).

NFS:

- Wird hauptsächlich in Linux- und Unix-Umgebungen verwendet.
- Vorteile:
  - Gute Integration in Linux-Systeme
  - Hohe Performance im lokalen Netzwerk
  - Einfache Konfiguration in reinen Linux-Umgebungen
- Nachteile:
  - Schlechte Unterstützung für Windows-Systeme
  - Sicherheitsmechanismen sind begrenzter

Samba (SMB/CIFS):

- Implementiert das Windows-Dateifreigabeprotokoll SMB unter Linux.
- Vorteile:
  - Kompatibel mit Windows-Netzwerken
  - Integration in Active Directory möglich
  - Gute Benutzer- und Rechteverwaltung
- Nachteile:
  - Komplexere Konfiguration
  - Etwas höherer Ressourcenverbrauch

## Aufgabe 3

Der Zugriff auf Ressourcen wird über Benutzerkonten und Gruppen
geregelt.

Jeder Benutzer meldet sich mit einem eigenen Benutzerkonto am System an.
Dieses Konto besitzt eine eindeutige Benutzer-ID (UID) und ist einer
oder mehreren Gruppen (GID) zugeordnet.

Dateien und Ordner besitzen ebenfalls einen Besitzer (User) und eine
Gruppe. Zusätzlich werden Zugriffsrechte vergeben:

- Lesen (r)
- Schreiben (w)
- Ausführen (x)

Diese Rechte können für drei Kategorien gesetzt werden:

- Besitzer (User)
- Gruppe
- Andere Benutzer

Dadurch kann festgelegt werden, welcher Benutzer oder welche Gruppe auf
bestimmte Dateien, Verzeichnisse oder Netzwerkfreigaben zugreifen darf.

## Aufgabe 4

a)  Access Control Lists (ACL) erweitern das klassische Linux-
    Rechtesystem. Neben Besitzer, Gruppe und anderen Benutzern können
    zusätzliche individuelle Rechte für einzelne Benutzer oder Gruppen
    vergeben werden.

    Mit ACL können beispielsweise mehreren Benutzern unterschiedliche
    Rechte auf dieselbe Datei oder denselben Ordner gegeben werden,
    ohne die Besitzstruktur ändern zu müssen.

    Die Verwaltung erfolgt über Befehle wie:

    - `setfacl` zum Setzen von Rechten
    - `getfacl` zum Anzeigen von ACL-Einträgen

    Beispiel:

    `setfacl -m u:user1:rw datei.txt`

    Dadurch erhält der Benutzer user1 Lese- und Schreibrechte auf
    die Datei.

<!-- -->

b)  Drei Einsatzbereiche für ACL:

- Detaillierte Rechtevergabe für einzelne Benutzer
- Zugriff auf gemeinsam genutzte Projektordner
- Rechteverwaltung in großen Netzwerken mit vielen Benutzern

<!-- -->

c)  Es existieren zwei Freigaben:

- Freigabe /share/mitarbeiter
- Freigabe /share/entwicklung

Benutzer:

- User1
- User2
- User3 (arbeitet zusätzlich in der Entwicklung)

Alle Benutzer erhalten Lese- und Schreibrechte auf
`/share/mitarbeiter`.

Beispiel:


setfacl -m u:User1:rw /share/mitarbeiter
setfacl -m u:User2:rw /share/mitarbeiter
setfacl -m u:User3:rw /share/mitarbeiter


Für die Entwicklungsfreigabe erhält nur User3 Zugriff:


setfacl -m u:User3:rw /share/entwicklung


Damit haben alle Mitarbeitenden Zugriff auf die allgemeine Freigabe,
während nur User3 auf die Entwicklungsfreigabe zugreifen kann.

## Aufgabe 5

Der Unterschied zwischen Role Based Access Control (RBAC) und
Access Control Lists (ACL) liegt in der Art der Rechtevergabe.

ACL:

- Rechte werden direkt einzelnen Benutzern oder Gruppen auf eine
  Ressource zugewiesen.
- Jede Ressource besitzt eine eigene Liste von Zugriffsrechten.

RBAC:

- Rechte werden zuerst Rollen zugewiesen.
- Benutzer werden anschließend diesen Rollen zugeordnet.

Vorteile von RBAC:

- Bessere Übersicht in großen Systemen
- Einfachere Verwaltung vieler Benutzer
- Rollen können zentral geändert werden

## Aufgabe 6

a)  Das Schema Account Global Domain Local Permission (AGDLP) ist ein
    Modell zur strukturierten Rechtevergabe in Windows-Domänen und
    basiert auf dem Prinzip von Role Based Access Control.

Die Struktur:

- Account (A): Benutzerkonto
- Global Group (G): Gruppe mit Benutzern
- Domain Local Group (DL): Gruppe mit Zugriff auf Ressourcen
- Permission (P): Berechtigungen auf Ressourcen

Benutzer werden zuerst globalen Gruppen zugeordnet. Diese Gruppen
werden anschließend in domainlokale Gruppen aufgenommen. Die
domainlokalen Gruppen erhalten dann die tatsächlichen Rechte auf eine
Ressource.

<!-- -->

b)  Beispiel für die Rigudo GmbH:

Benutzer:

- User1
- User2
- User3

Freigaben:

- Mitarbeiter-Freigabe
- Entwicklungs-Freigabe

1. Globale Gruppen erstellen

- GG_Mitarbeiter
- GG_Entwicklung

Zuordnung:

- User1 → GG_Mitarbeiter
- User2 → GG_Mitarbeiter
- User3 → GG_Mitarbeiter
- User3 → GG_Entwicklung

2. Domain Local Groups erstellen

- DL_Mitarbeiter_Freigabe
- DL_Entwicklung_Freigabe

3. Gruppen verschachteln

- GG_Mitarbeiter → DL_Mitarbeiter_Freigabe
- GG_Entwicklung → DL_Entwicklung_Freigabe

4. Berechtigungen vergeben

- DL_Mitarbeiter_Freigabe → Lese- und Schreibrechte auf Mitarbeiterfreigabe
- DL_Entwicklung_Freigabe → Lese- und Schreibrechte auf Entwicklungsfreigabe

Damit erhalten alle Mitarbeiter Zugriff auf die allgemeine Freigabe,
während nur Mitglieder der Entwicklungsgruppe Zugriff auf die
Entwicklungsfreigabe erhalten.

## Aufgabe 7

Sie wollen den Status verschiedener Dateien überprüfen. Sie nutzen die
Befehle „stat" und „Is -ail".

Ausgabe von „stat":

    Datei: test2.md

    Größe: 27 Blöcke: 8 EA Block: 4096 Normale Datei
    Gerät: 1030ah/66314d Inode: 2490370 Verknüpfungen: 2
    Zugriff: (0664/-rw-rw-r--) Uid: ( 1000/ george) Gid: ( 1000/ george)
    Zugriff: 2023-06-10 17:18:59.356190879 +0200 .
    Modifiziert: 2023-06-10 17:18:56.292193014 +0200/
    Geändert: 2023-06-10 17:18:56.304193006 +0200
    Geburt: 2023-06-10 17:17:07.932270495 +0200

    Datei: test3.md -> test.md

    Größe: 7 Blöcke: 0 EA Block: 4096 symbolische Verknüpfung
    Gerät: 1030ah/66314d Inode: 2490371 Verknüpfungen: 1
    Zugriff: (0777/l1rwxrwxrwx) Uid: ( 1000/ george) Gid: ( 1000/ george)
    Zugriff: 2023-06-10 17:17:52.652235945 +0200
    Modifiziert: 2023-06-10 17:17:49.004238323 +0200
    Geändert: 2023-06-10 17:17:49.004238323 +0200
    Geburt: 2023-06-10 17:17:49.004238323 +0200

    Datei: test.md

    Größe: 27 Blöcke: 8 EA Block: 4096 Normale Datei
    Gerät: 1030ah/66314d Inode: 2490370 Verknüpfungen: 2
    Zugriff: (0664/-rw-rw-r--) Uid: ( 1000/ george) Gid: ( 1000/ george)
    Zugriff: 2023-06-10 17:18:59.356190879 +0200
    Modifiziert: 2023-06-10 17:18:56.292193014 +0200
    Geändert: 2023-06-10 17:18:56.304193006 +0200
    Geburt: 2023-06-10 17:17:07.932270495 +0200

Ausgabe von „ls -all":

    2490370 -rw-rw-r-- 2 george 27 Jun 10 17:18 test2.md
    2490371 lrwxrwxrwx 1 george 7 Jun 10 17:17 test3.md -> test.md
    2490370 -rw-rw-r-- 2 george 27 Jun 10 17:18 test.md

a)  Geben Sie die Hauptdatei, den symbolischen Link und den „Hard Link"
    an.

Hauptdatei:  
test.md

Symbolischer Link:  
test3.md -> test.md

Hard Link:  
test2.md

<!-- -->

b)  Geben Sie für die Datei „test.md" jeweils die Rechte in
    „umask"-Schreibweise und in dezimaler Schreibweise an.

Rechte: -rw-rw-r--

umask-Schreibweise:  
0664

Dezimale Schreibweise:  
436

<!-- -->

c)  Geben Sie jeweils den Ordner an, in dem bei einem Linux-System
    standardmäßig die beschriebenen Dateien abgelegt werden.

| Beschreibung | Ordner |
|----|----|
| Konfigurationsdateien für systemweite Programme | /etc |
| Benutzeranwendungen, die systemweit installiert wurden | /usr/bin |
| Administrative Anwendungen, die nicht direkt zum Betriebssystem gehören | /usr/sbin |
| Dateien von normalen Benutzern | /home |