---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Zugriffsmöglichkeiten auf Systeme im LAN planen
---

## Aufgabe 1

a)  Geben Sie die Möglichkeiten an, mit denen die VLAN-Zugehörigkeit
    umgesetzt werden kann.

    ::: {.solution}
    - statisch über Portzuordnung an den Switches
    - Markierungen (Tags) an den Paketen
    - dynamisch (MAC-Adressen, IP-Adressen, TCP-Ports, UDP-Ports und
      höhere Potokolle)
    - Zuordnung nach Authentifizierung, z. B. mittels 802.1X
    :::

<!-- -->

b)  Im Netzwerk der Rigudo GmbH soll die Sicherheit für den Zugriff auf
    die unterschiedlichen Unternehmensbereiche erhöht werden. Es wird
    über Alternativen zur bisherigen VLAN-Konfiguration nachgedacht. Die
    einzelnen Rechner bzw. Benutzer sollen ggf. den VLANs zugewiesen
    werden. Erörtern Sie Möglichkeiten für diese Überlegung und
    unterbreiten Sie Vorschläge, welche Lösung man für die
    unterschiedlichen Abteilungen vorsehen sollte.

    Entwicklungsabteilung: überwiegend Notebooks, an flexiblen
    Arbeitsplätzen ca. 20 Geräte

    ::: {.solution}
    Entweder dynmaische Zuordnung über die MAC-Adresse oder höhere
    Protokolle oder -- vermutlich sicherer -- Zuordnung nach
    Authentifizierung
    :::

    Personalabteilung: feste Arbeitsplätze; ca. 10 Geräte

    ::: {.solution}
    Hier ist von der statischen Zuordnung über die Portzuordnung an den
    Switches (Transparent für die Benutzer) bis hin zu Zuordnung nach
    Authentifizierung alles möglich.
    :::

    Vertrieb: überwiegend Notebooks, an flexiblen Arbeitsplätzen auch
    Homeoffice bzw. Remote-Zugriff; ca. 40 Geräte

    ::: {.solution}
    Hier bietet sich eine Kombination von VPN mit Zuordnung nach
    Authentifizierung an.
    :::

<!-- -->

c)  Sie wurden wegen Ihrer Erfahrungen bei der Planung von VLANs
    beauftragt, für einen weiteren Kunden die Port-Konfiguration von
    drei Switches zu planen. Geben Sie für die Schnittstellen der
    angeschlossenen Rechner den jeweiligen VLAN-Modus an. Alle Rechner
    sind zunächst in der Standard-Konfiguration (untagged).

    Es sollen vier LANs mit den folgenden Zugehörigkeiten umgesetzt
    werden.

    - VLAN 10: A, B, D
    - VLAN 20: C, D
    - VLAN 30: B, E
    - VLAN 40: F, G

    ![](images/vlan.png){width="50%"}

    | Switch/Port | VLAN-Konfiguration |
    |-------------|--------------------|
    | s1/01       | 10; untagged       |
    | S1/05       |                    |
    | S1/08       |                    |
    | s1/15       |                    |
    | S2/01       |                    |
    | S2/02       |                    |
    | S2/03       |                    |
    | S2/09       |                    |
    | S3/01       |                    |
    | S3/07       |                    |
    | s3/11       |                    |

    | Rechner | VLAN-Modus     |
    |---------|----------------|
    | PC A    |                |
    | PC B    | 10, 30; tagged |
    | PC C    |                |
    | PC D    |                |
    | PC E    |                |
    | PC F    |                |
    | PC G    |                |

    ::: {.solution}
    | Switch/Port | VLAN-Konfiguration |
    |-------------|--------------------|
    | s1/01       | 10; untagged       |
    | S1/05       | 10, 30; tagged     |
    | S1/08       | 10, 20, 30; tagged |
    | s1/15       | 20; untagged       |
    | S2/01       | 10, 20, 30; tagged |
    | S2/02       | ~~40, untagged~~   |
    | S2/03       | 10, 20; tagged     |
    | S2/09       | 30; untagged       |
    | S3/01       | ~~40; untagged~~   |
    | S3/07       | 40; untagged       |
    | s3/11       | 40; untagged       |
    |             |                    |

    | Rechner | VLAN-Modus     |
    |---------|----------------|
    | PC A    | 10; untagged   |
    | PC B    | 10, 30; tagged |
    | PC C    | 20; untagged   |
    | PC D    | 10, 20; tagged |
    | PC E    | 30; untagged   |
    | PC F    | 40; untagged   |
    | PC G    | 40; untagged   |
    |         |                |
    :::

## Aufgabe 2

Die Rigudo GmbH möchte ihre Firewall-Infrastruktur neu organisieren. Ihr
Unternehmen soll bei der Planung und der Umsetzung unterstützen. Ihr
Abteilungsleiter bittet Sie, mit der Rigudo GmbH zusammenzuarbeiten.

a)  Bisher verwendet die Rigudo GmbH nur eine Firewall, um den aus- und
    eingehenden Verkehr zu filtern. Um die Vorgaben des BSI zu erfüllen
    soll eine DMZ (Demilitarisierte Zone) eingesetzt werden. Entscheiden
    Sie, welche der folgenden Systeme in der DMZ platziert werden
    müssen.

    1.  Webserver -- Enthält die Internetseite der Rigudo GmbH.
    2.  Webserver -- Stellt Kunden der Rigudo GmbH bestimmte Webdienste
        bereit.
    3.  Dateiserver -- Enthält die Benutzerprofile der Beschäftigten.
    4.  Dateiserver Enthält die Nutzdaten der Beschäftigten.
    5.  HTTP-Proxy-Server -- Vermittelt HTTP(S)-Daten weiter.
    6.  AD-Domain-Controller -- Organisiert den Verzeichnisdienst.
    7.  Druckerserver -- Stellt die Druckerwarteschlange bereit.
    8.  E-Mail-Server -- Sendet und empfängt E-Mails.
    9.  DHCP-Server -- Verteilt IP-Adressen.

    ::: {.solution}
    1.  Webserver -- Enthält die Internetseite der Rigudo GmbH.

    2.  Webserver -- Stellt Kunden der Rigudo GmbH bestimmte Webdienste
        bereit.

    3.  HTTP-Proxy-Server -- Vermittelt HTTP(S)-Daten weiter.

    4.  E-Mail-Server -- Sendet und empfängt E-Mails.
    :::

<!-- -->

b)  Die äußere Firewall der DMZ soll durch eine Paketfilter-Firewall
    umgesetzt werden. Der Paketfilter soll „Stateful Packet Inspection"
    (SPI) unterstützen.

    Erstellen Sie zunächst drei Regeln für die Firewall und eine Regel
    für die „Default Policy". DNS-Anfragen von intern sollen erlaubt
    werden, HTTPS-Anfragen von intern sollen ebenfalls erlaubt werden.
    E-Mails sollen versendet werden können. Es soll ein
    Allow-List-Prinzip angewendet werden. Vervollständigen Sie dafür die
    nachfolgende Tabelle.

    ![](images/dmz-firewall-extern.png){width="75%"}

    | Nr. | Ziel-IP-Adresse | Quell-IP-Adresse | Ziel-Port | Quell-Port | Aktion |
    |-----|-----------------|------------------|-----------|------------|--------|
    | 1   | any             | 172.17.0.150     | 53        | any        | ACCEPT |
    | 2   |                 |                  |           |            |        |
    | 3   |                 |                  |           |            |        |
    | 4   | any             | any              |           |            |        |

    ::: {.solution}
    | Nr. | Ziel-IP-Adresse | Quell-IP-Adresse | Ziel-Port      | Quell-Port | Aktion |
    |-----|-----------------|------------------|----------------|------------|--------|
    | 1   | any             | 172.17.0.150     | 53             | any        | ACCEPT |
    | 2   | any             | 172.15.0.150     | 443            | any        | ACCEPT |
    | 3   | any             | 172.17.0.100     | 25, (465, 587) | any        | ACCEPT |
    | 4   | any             | any              | any            | any        | DROP   |
    :::

<!-- -->

c)  Sie sollen eine Regel anlegen, die einer bestimmten IP-Adresse
    (192.168.0.15) verbietet, HTTPS-Verkehr zu versenden.

    Gegeben ist das folgende Regelwerk (sehr reduziert):

    | Nr. | Ziel-IP-Adresse | Quell-IP-Adresse | Ziel-Port | Quell-Port | Aktion |
    |-----|-----------------|------------------|-----------|------------|--------|
    | 1   |                 |                  |           |            |        |
    | 2   | any             | 192.168.0.0/24   | 443       | any        | ACCEPT |
    | 3   |                 |                  |           |            |        |
    | 4   | any             | any              | any       | any        | DROP   |
    | 5   |                 |                  |           |            |        |

    Geben Sie an, an welcher Stelle die Regel eingesetzt werden muss.

    ::: {.solution}
    | Nr. | Ziel-IP-Adresse | Quell-IP-Adresse | Ziel-Port | Quell-Port | Aktion |
    |-----|-----------------|------------------|-----------|------------|--------|
    | 1   | any             | 192.168.0.15     | 443       | any        | DROP   |
    | 2   | any             | 192.168.0.0/24   | 443       | any        | ACCEPT |
    | 3   |                 |                  |           |            |        |
    | 4   | any             | any              | any       | any        | DROP   |
    | 5   |                 |                  |           |            |        |
    :::

<!-- -->

d)  Zwischen der DMZ und dem internen Netzwerk soll eine Firewall vom
    Typ Application Layer Gateway (ALG) zum Einsatz kommen.

    Die Firewall soll HTTPS-Verkehr an bestimmte Webseiten unterbinden
    (URL-Filter).

    Recherchieren Sie, auf welches Feld des HTTPS-Headers die Firewall
    den HTTPS-Verkehr überprüfen muss.

    ::: {.solution}
    `Host`, falls gegeben, ansonsten das `:authority` Pseudo-Feld.
    :::

## Aufgabe 3

a)  Erklären Sie in eigenen Worten, wie ein Proxy verfährt, wenn eine
    lnhaltllche Aufbereitung der Daten durchgeführt wird.

    ::: {.solution}
    Bei der inhaltlichen Aufbereitung werden Datenpakete verändert.
    Beispiels weise können URL-Parameter hinzugefügt oder entfernt
    werden. Für den Client sind diese Änderungen nicht sichtbar.
    :::

<!-- -->

b)  Die Rigudo GmbH möchte für bestimmte Unternehmensbereiche den
    Zugriff auf inadäquate Inhalte einschränken. Unterbreiten Sie
    Vorschläge, wie dies umgesetzt werden kann.

    ::: {.solution}
    - Einsatz eines Application-Layer-Gateway, der als URL- und
      Content-Filter genutzt wird.
    - Einsatz eines Proxys zur Filterung des Datenverkehrs, in
      Verbindung mit eines Paketfilter, der die Nutzung des Proxys
      erzwingt.
    :::
