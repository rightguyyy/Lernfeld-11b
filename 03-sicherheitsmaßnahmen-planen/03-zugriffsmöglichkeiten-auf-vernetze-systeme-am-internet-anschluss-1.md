---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Zugriffsmöglichkeiten auf vernetzte Systeme am Internet-Anschluss
  planen I
---

## Aufgabe 1

Beschreiben Sie in eigenen Worten den Unterschied zwischen SNAT und DNAT

SNAT (Source NAT) verändert die Quelladresse (und ggf. den Quell-Port) eines Pakets. Es wird typischerweise für ausgehende Verbindungen verwendet, damit interne Geräte über eine öffentliche IP-Adresse ins Internet kommunizieren können.

DNAT (Destination NAT) verändert die Zieladresse (und ggf. den Ziel-Port). Es wird bei eingehenden Verbindungen verwendet, um externe Anfragen auf interne Server weiterzuleiten (Portweiterleitung).

## Aufgabe 2

Berechnen Sie den Schlüssel einer VPN-Verbindung, die mit dem
DH-Verfahren gesichert wird. Das System verwendet die Primzahl p=17
sowie die öffentlice Zufallszahl z=20 und die beiden Geheimzahlen
a=4 und b=5.

z mod p = 20 mod 17 = 3

A = 3^4 mod 17 = 81 mod 17 = 13  
B = 3^5 mod 17 = 243 mod 17 = 5  

K = 5^4 mod 17 = 625 mod 17 = 13  

Ergebnis: K = 13

## Aufgabe 3

Nennen Sie mindestens zwei Verfahren, die bei der Verteilung von Paketen
in einem Load Balancer eingesetzt werden. Erklären Sie die jeweiligen
Verfahren kurz.

Round Robin: Anfragen werden der Reihe nach gleichmäßig auf alle Server verteilt.  
Least Connections: Der Server mit den wenigsten aktiven Verbindungen bekommt die nächste Anfrage.  
IP-Hash: Die Quell-IP bestimmt per Hash immer denselben Server (Sitzung bleibt beim gleichen Backend).  
Weighted Round Robin: Leistungsstärkere Server erhalten mehr Anfragen durch höhere Gewichtung.

## Aufgabe 4

Unterscheiden Sie die Begriffe »Public Cloud« und »Private Cloud«.

Public Cloud: Infrastruktur eines externen Anbieters, von vielen Kunden gemeinsam genutzt, flexibel skalierbar, geringere Kontrolle über Hardware.  
Private Cloud: Infrastruktur nur für eine Organisation, mehr Kontrolle und Sicherheit, aber höhere Kosten und eigener Betriebsaufwand.

## Aufgabe 5

In der DMZ der Rigudo GmbH sollen private IP-Adressen zum Einsatz
kommen. Der gewählte IP-Adressbereich lautet 172.17.0.0/16.

Der Mailserver und der HTTPS-Proxy sollen mit dem öffentlichen Netzwerk
kommunizieren können. Sie werden gebeten, den NAT-Einsatz am Router bzw.
an der Firewall zu planen.

a)  Erläutern Sie die Besonderheiten der privaten IP-Adressen.

Private IP-Adressen sind nicht im Internet routbar und dürfen dort nicht direkt verwendet werden. Sie können in vielen Netzen gleichzeitig existieren. Für die Kommunikation ins Internet ist deshalb NAT erforderlich.

b)  Zur Verdeutlichung des NAT-Vorgangs sollen Sie diesen anhand einer
    Verbindung detailliert beschreiben.

    Der HTTPS-Proxy (172.17.0.150) baut eine Verbindung zum Webserver (1.2.3.4) auf.  
    Der Router ersetzt die interne Quelladresse durch seine öffentliche Adresse (SNAT/PAT) und speichert die Zuordnung in der NAT-Tabelle.

    | Teilstrecke | Ziel-IP-Adresse | Quell-IP-Adresse | Ziel-Port | Quell-Port |
    |-------------|-----------------|------------------|-----------|------------|
    | 1           | 1.2.3.4         | 172.17.0.150     | 443       | 53000      |
    | 2           | 1.2.3.4         | öffentliche WAN-IP des NAT-Routers | 443 | 53000 |
    | 3           | öffentliche WAN-IP des NAT-Routers | 1.2.3.4 | 53000 | 443 |
    | 4           | 172.17.0.150    | 1.2.3.4          | 53000     | 443        |

c)  Die internen Server sollen aus dem externen Netzwerk erreichbar sein.

    | Socket intern | Socket extern |
    |---------------|---------------|
    | 172.17.0.100:25 | öffentliche WAN-IP des NAT-Routers:25 |
