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

Sinnvoll bei zustandsbehafteten Webanwendungen (z. B. Login/Shop), bei denen Sessiondaten lokal auf dem Backend gespeichert werden. Der Hash sorgt dafür, dass ein Client immer beim selben Server landet (Session-Stickiness), sodass Login/Warenkorb nicht verloren gehen.

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

Mitarbeiter am Standort Zentrale: Remote-Access-VPN (z. B. IPsec/IKEv2) zur Firewall der Zentrale.  
Mitarbeiter am Standort zweite Niederlassung: Remote-Access-VPN zur Firewall der zweiten Niederlassung.  
Mobilfunk: Zwei getrennte VPN-Profile (je ein Tunnel zu beiden Standorten).

<!-- -->

c)  Für VPN-Verbindungen mittels IPsec kann der Tunnel- oder
    Transport-Modus genutzt werden. Erläutern Sie die Nachteile des
    Transport-Modus gegenüber dem Tunnel-Modus.

Der ursprüngliche IP-Header bleibt sichtbar (keine Tarnung interner Netze). Nur Host-zu-Host geeignet und unpraktisch für Standortkopplungen. Häufig schlechtere NAT-Kompatibilität.

<!-- -->

d)  Die folgenden Hex-Dumps enthalten jeweils den Beginn des AH- und
    ESP-Headers eines entschlüsselten IPsec-Paketes.

Next Header: 50 (ESP)  
SPI: 0x000002bc

SPI: 0x000002bd  
Sequence Number: 0x0000002b

<!-- -->

e)  Die Mitarbeitenden im Homeoffice haben zum Teil Schwierigkeiten beim
    Aufbau der IPsec-Verbindung mit einem IPsec-Client zur Zentrale.
    Alle anderen Internet-Verbindungen funktionieren.

Ältere NAT-Router verändern IP-Header. AH schützt den Header, wodurch Authentifizierung fehlschlägt. ESP (IP-Protokoll 50) kann von NAT nicht korrekt umgesetzt werden. Lösung: NAT-Traversal (UDP 4500).

## Aufgabe 3

Beschreiben Sie, welcher Konflikt bei der verschlüsselten Speicherung
von Daten in einem Cloud-Speicher und dem Teilen dieser Daten mit
anderen Nutzern besteht.

Zum Teilen müssen weitere Nutzer Zugriff auf den Schlüssel erhalten. Dadurch wird Schlüsselmanagement komplex und die Vertraulichkeit sinkt.

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

Verschlüsselung  
Zugriffsbeschränkungen/Berechtigungskonzepte

<!-- -->

b)  Nennen Sie zwei TOM, mit denen das Schutzziel Integrität erhöht
    wird.

Digitale Signaturen/Hash-Prüfsummen  
Vier-Augen-Prinzip

<!-- -->

c)  Nennen Sie zwei TOM, mit denen das Schutzziel Verfügbarkeit erhöht
    wird.

Backups  
Redundanz (z. B. Cluster/RAID)