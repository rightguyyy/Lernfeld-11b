---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Zugriffsmöglichkeiten auf vernetzte Systeme am Internet-Anschluss
  planen II
---

## Aufgabe 1

Die Verfügbarkeit eines Webservices soll erhöht werden. Als Load
Balancing-Verfahren möchten Sie ein schlüsselbasiertes Verfahren
einsetzen. Bei diesem Verfahren wird aus verschiedenen Faktoren, z. B.
aus den Ziel- und Quelladressen sowie Ziel- und Quellports, ein
Hash-Wert gebildet. Pakete mit demselben Hash-Wert werden vom selben
Server bearbeitet.

Beschreiben Sie ein Beispiel, bei dem eine solche Verfahrensweise für
das Load Balancing sinnvoll ist.

Sinnvoll ist dies bei Webanwendungen mit Login oder Sessions, bei denen Sitzungsdaten lokal auf dem Server gespeichert werden. Durch den Hash landen alle Anfragen eines Clients immer beim gleichen Backend-Server (Session-Stickiness). Dadurch bleiben Logins oder Warenkörbe erhalten.

## Aufgabe 2

Für die Anbindung der Mitarbeitenden im Homeoffice Soll ein VPN zum
Einsatz kommen. Dieses muss zunächst geplant werden.

a)  Es sollten nur sichere Verfahren zum Einsatz kommen. Geben Sie für
    die folgenden Verfahren an, ob diese sicher bzw. unsicher sind.
    Geben Sie weiterhin an, ob es sich um ein kryptografisches Hash-
    oder ein Verschlüsselungsverfahren handelt.

    | Verfahren | sicher: ja/nein | Art: kryptographischer Hash/Verschlüsselung |
    |-----------|-----------------|---------------------------------------------|
    | Blowfish  | ja              | Verschlüsselung                             |
    | 3DES      | nein            | Verschlüsselung                             |
    | SHA-2     | ja              | kryptographischer Hash                      |
    | AES       | ja              | Verschlüsselung                             |
    | DES       | nein            | Verschlüsselung                             |

<!-- -->

b)  Im gegebenen Netzwerkplan sollen die neuen VPN-Verbindungen ergänzt
    werden. Ergänzen Sie die Homeoffice-Anschlüsse gemäß den folgenden
    Anforderungen.

    - Mitarbeiter am Standort Zentrale
    - Mitarbeiter am Standort zweite Niederlassung
    - Mitarbeiter per Mobilfunk (Kundengesprache vor Ort) getrennt an
      be1den Standorten

    ::: {.center}
    ![](images/vpn.png){width="75%"}
    :::

Mitarbeiter Zentrale: Remote-Access-IPsec-Tunnel zur Firewall der Zentrale.  
Mitarbeiter zweite Niederlassung: Remote-Access-IPsec-Tunnel zur Firewall der zweiten Niederlassung.  
Mobilfunk: Zwei getrennte VPN-Profile, je ein Tunnel zu beiden Standorten.

<!-- -->

c)  Für VPN-Verbindungen mittels IPsec kann der Tunnel- oder
    Transport-Modus genutzt werden. Erläutern Sie die Nachteile des
    Transport-Modus gegenüber dem Tunnel-Modus.

Der ursprüngliche IP-Header bleibt sichtbar, interne Adressen werden nicht verborgen. Der Modus ist hauptsächlich für Host-zu-Host geeignet und weniger flexibel für Standortkopplungen. Außerdem treten häufiger Probleme mit NAT auf.

<!-- -->

d)  Die folgenden Hex-Dumps enthalten jeweils den Beginn des AH- und
    ESP-Headers eines entschlüsselten IPsec-Paketes. Der Wert „0x32"
    entspricht dabei dem Feld „Next Header". Am Beginn der Zeilen ist,
    wie im Wireshark üblich, die relative Position (ebenfalls in Hex)
    angegeben.

    #### AH-Header

        Bytes Hex-Werte
        0000  32 04 00 00 00 00 02 bc 00 00 00 2b ec d0 29 65
        0010  3b a1 ff 88 01 76 7a bc

    | Next-Header (in Dezimal) | Protokoll |
    |--------------------------|-----------|
    | 1                        | ICMP      |
    | 4                        | IPv4      |
    | 17                       | UDP       |
    | 32                       | MERIT-INP |
    | 50                       | ESP       |
    | 51                       | AH        |
    | 58                       | IPv6-ICMP |
    |                          |           |

    Geben Sie das geschachtelte Protokoll (Next Header) und den
    verwendeten SPI des AH-Headers an.

Next Header: 50 (ESP)  
SPI: 0x000002bc

    #### ESP-Header

        Bytes Hex-Werte
        0000  00 00 02 bd 00 00 00 2b al 61 dc c5 fb 1d fO 14
        0010  66 fa 20 91 fe 77 5d 1c b5 0f bc 5f 3b 26 46 59
        0020  22 d6 d3 f5 c9 63 92 de b5 0d 66 8e 88 3a 5d 5c
        0030  3d d7 32 32 e0 04 97 e0 a3 b6 81 ef 23 8d 3b 92
        0040  2e 40 f4 dO 27 be 74 d8 5a d9 25 b7 71 al 4d d4
        0050  f3 0b 28 8a 99 Ob 6a bb

    Geben Sie den verwendeten SPI und die „Sequence Number" des
    ESP-Headers an.

SPI: 0x000002bd  
Sequence Number: 0x0000002b

<!-- -->

e)  Die Mitarbeitenden im Homeoffice haben zum Teil Schwierigkeiten beim
    Aufbau der IPsec-Verbindung mit einem IPsec-Client zur Zentrale.

Problem: NAT verändert IP-Adressen. AH schützt jedoch den IP-Header, wodurch die Authentifizierung fehlschlägt. Außerdem kann NAT ESP-Pakete (IP-Protokoll 50) oft nicht korrekt zuordnen. Ohne NAT-Traversal schlagen Verbindungen fehl. Lösung: NAT-T (UDP 4500) oder IPsec-Passthrough.

## Aufgabe 3

Beschreiben Sie, welcher Konflikt bei der verschlüsselten Speicherung
von Daten in einem Cloud-Speicher und dem Teilen dieser Daten mit
anderen Nutzern besteht.

Für hohe Vertraulichkeit sollen nur berechtigte Personen den Schlüssel besitzen. Beim Teilen müssen jedoch weitere Nutzer Zugriff auf den Schlüssel erhalten. Das erschwert das Schlüsselmanagement und kann die Sicherheit verringern.

## Aufgabe 4

Ordnen Sie die entsprechenden Schutzziele der folgenden TOM zu.

a) Vertraulichkeit  
b) Verfügbarkeit  
c) Vertraulichkeit  
d) Integrität  
e) Verfügbarkeit  
f) Integrität

## Aufgabe 5

a)  Nennen Sie zwei technische und organisatorische Maßnahmen (TOM), mit
    denen das Schutzziel Vertraulichkeit erhöht wird.

Verschlüsselung der Daten  
Berechtigungskonzept/Zugriffsbeschränkung

<!-- -->

b)  Nennen Sie zwei TOM, mit denen das Schutzziel Integrität erhöht
    wird.

Digitale Signaturen oder Hash-Prüfsummen  
Vier-Augen-Prinzip bei Änderungen

<!-- -->

c)  Nennen Sie zwei TOM, mit denen das Schutzziel Verfügbarkeit erhöht
    wird.

Backups  
Redundante Systeme oder Cluster
