---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Übungsaufgaben 2
---

## Aufgabe 1

![](images/vlan-2.png)

Für das gegebene Netzwerk sollen die folgenden VLANs eingerichtet
werden:

- 10: Apple Talk VLAN 1
- 20: Apple Talk VLAN 2
- 30: Red VLAN
- 40: Green VLAN

Der Server S2 soll sowohl auf »Red VLAN« als auch auf »Green VLAN«
zugreifen können.

Die Switche X und Y können auch die VLAN-Zugehörigkeit anhand von
Protokollen erkennen, so dass (zusätzlich) ein VLAN für Apple-Talk
ungetaggt bleiben kann.

Erstellen Sie eine geeignete VLAN konfiguration, d. h. die
VLAN-Zugehörigkeiten und tagged oder untagged.

| Switch/Port | VLAN-Konfiguration |
|-------------|--------------------|
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |
|             |                    |

| Rechner / Teilnetz | VLAN-Modus |
|--------------------|------------|
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |
|                    |            |

::: {.solution}
| Switch/Port | VLAN-Konfiguration                                           |
|-------------|--------------------------------------------------------------|
| X1          | 10 untagged ~~oder tagged~~; 20 tagged                       |
| X2          | 30 untagged ~~oder tagged~~; 40 tagged                       |
| X3          | 20 untagged ~~oder tagged~~; 30 untagged; 40 tagged          |
| X4          | 40 untagged                                                  |
| X5          | 30 untagged                                                  |
| X6          | 10 untagged                                                  |
| Y1          | 30 untagged ~~oder tagged~~; 40 tagged                       |
| Y2          | 40 untagged                                                  |
| Y3          | 20 untagged                                                  |
| Y4          | 40 untagged                                                  |
| Y5          | 30 untagged                                                  |
| Y6          | 20 untagged ~~oder tagged (wie X3)~~; 30 untagged; 40 tagged |
|             |                                                              |

| Rechner / Teilnetz | VLAN-Modus                                      |
|--------------------|-------------------------------------------------|
| Apple Talk Server  | 10 untagged ~~oder tagged (wie X1)~~; 20 tagged |
| S1                 | 30 untagged ~~oder tagged (wie X2)~~; 40 tagged |
| "Green VLAN" an X4 | 40 untagged                                     |
| "Red VLAN" an X5   | 30 untagged                                     |
| Apple Talk VLAN 1  | 10 untagged                                     |
| S2                 | 30 untagged ~~oder tagged (wie Y1)~~; 40 tagged |
| S3                 | 40 untagged                                     |
| Apple Talk VLAN 2  | 20 untagged                                     |
| "Green VLAN" an Y4 | 40 untagged                                     |
| "Red VLAN" an Y5   | 30 untagged                                     |
:::
