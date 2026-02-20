---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Benutzerrechte II
---

## Aufgabe 1

Geben Sie, wo unter Linux die Benutzer-Passwörter gespeichert werden.

## Aufgabe 2

Beschreiben Sie die beiden gängigen Systeme für Netzwerkfreigaben unter
Linux und deren Vor- und Nachteile.

## Aufgabe 3

Beschreiben Sie, wie mithilfe von Benutzerkonten allgemein der Zugriff
auf Ressourcen von Computersystemen geregelt wird.

## Aufgabe 4

a)  Beschreiben Sie, wie mithilfe von Access Control Lists (ACL)
    Zugriffsrechte auf Ressourcen erteilt werden.

<!-- -->

b)  Nennen Sie drei Einsatzbereiche für die Verwendung einer ACL.

<!-- -->

c)  Die Rigudo GmbH nutzt zwei Netzwerkfreigaben. Eine für alle
    Mitarbeitenden und eine für eine besondere Gruppe von
    Mitarbeitenden, die an der Entwicklung der Videokonferenzsoftware
    arbeiten. Die jeweiligen Gruppen sollen Lese- und
    Schreibberechtigungen auf die entsprechenden Freigaben erhalten.
    Nutzen Sie exemplarisch für die Mitarbeitenden die drei Benutzer
    User1, User2 und User3, wobei User3 auch in der Entwicklung arbeiten
    soll.

    Beschreiben Sie, wie Sie mithilfe einer ACL die Zugriffsrechte für
    die drei Benutzer auf die Freigaben regeln.

## Aufgabe 5

Beschreiben Sie den Unterschied zwischen Role Based Access Control
(RBAC) und ACL.

## Aufgabe 6

a)  Beschreiben Sie, in welchem Zusammenhang das Schema Account Global
    Domain Local Permission (AGDLP) im Zusammenhang mit Role Based
    Access Control (RBAC) steht.

<!-- -->

b)  Die Rigudo GmbH nutzt zwei Netzwerkfreigaben. Eine für alle
    Mitarbeitenden und eine für eine besondere Gruppe von
    Mitarbeitenden, die an der Entwicklung der Videokonferenzsoftware
    arbeiten. Die jeweiligen Gruppen sollen Lese- und
    Schreibberechtigungen auf die entsprechenden Freigaben erhalten.
    Nutzen Sie exemplarisch für die Mitarbeitenden die drei Benutzer
    User1, User2 und User3, wobei User3 auch in der Entwicklung arbeiten
    soll.

    Beschreiben Sie, wie Sie nach dem Schema Account Global Domain Local
    Permission (AGDLP) die Zugriffsrechte für die drei Benutzer auf die
    Freigaben regeln.

## Aufgabe 7

Sie wollen den Status verschiedener Dateien überprüfen. Sie nutzen die
Befehle „stat" und „Is -ail".

**Ausgabe von „stat":**

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

**Ausgabe von „ls -all":**

    2490370 -rw-rw-r-- 2 george 27 Jun 10 17:18 test2.md I
    2490371 lrwxrwxrwx 1 george 7 Jun 10 17:17 test3.md -> test.md
    2490370 -rw-rw-r-- 2 george 27 Jun 10 17:18 test.md

a)  Geben Sie die Hauptdatei, den symbolischen Link und den „Hard Link"
    an.

<!-- -->

b)  Geben Sie für die Datei „test.md" jeweils die Rechte in
    „umask"-Schreibweise und in dezimaler Schreibweise an.

<!-- -->

c)  Geben Sie jeweils den Ordner an, in dem bei einem Linux-System
    standardmäßig die beschriebenen Dateien abgelegt werden.

    | Beschreibung | Ordner |
    |----|----|
    | Konfigurationsdateien für systemweite Programme |  |
    | Benutzeranwendungen, die systemweit installiert wurden |  |
    | Administrative Anwendungen, die nicht direkt zum Betriebssystem gehören |  |
    | Dateien von normalen Benutzern |  |
