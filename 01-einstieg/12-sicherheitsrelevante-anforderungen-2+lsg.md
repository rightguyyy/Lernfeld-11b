---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Netzwerk -- Sicherheitsrelevante Anforderungen 2
---

## Aufgabe 1

Geben Sie eine Erklärung ab, warum Endpoint Security, Zero Trust
Security und Sicherheit in SDN eine höhere Sicherheit in Netzwerken
ermöglichen.

::: {.solution}

SDN
:   Sicherheit des Netzwerkes kann zentral gemanagt werden

Zero Trust Security
:   strenge Zugriffskontrolle auf der Basis von Layer-7-Richtlinien,
    keine Fremdgeräte im Netzwerk

Endpoint Security
:   Endpoint Security schützt Endgeräte vor Bedrohungen

Endpoint Security schützt Endgeräte vor Bedrohungen. Zero Trust Security
überprüft kontinuierlich jede Netzwerkkommunikation, ohne automatisches
Vertrauen zuzulassen. SDN ermöglicht die flexible Anpassung von
Sicherheitsrichtlinien und begrenzt Angriffe durch
Netzwerksegmentierung. Diese kombinierten Ansätze gewährleisten ein
effektives und anpassungsfähiges Sicherheitsnetzwerk.
:::

## Aufgabe 2

Ordnen Sie die Begriffe den Aussagen passend zu

(1) Angriffsvektor
(2) APT
(3) BSI
(4) DoS
(5) DSGVO
(6) Echtheit/Überprüfbarkeit
(7) Malware
(8) Man-in-the-Middle
(9) PDCA
(10) Ping Flooding
(11) PUA
(12) Ransomware
(13) S/MIME
(14) Single-Sign-on
(15) Spam
(16) Trojaner
(17) Verfügbarkeit
(18) Vertraulichkeit
(19) Whitelisting
(20) Würmer

#### Aussagen

a)  Bundesamt für Cybersicherheit (Kurzform)

b)  Gesetzliches Regelwerk zum Schutz persönlicher Daten

c)  Grundwert Availability im Deutschen

d)  Grundwert Confidentiality im Deutschen

e)  Grundwert Authenticity im Deutschen

f)  Deming-Zyklus

g)  Kombination aus Angriffsweg und Angriffstechnik

h)  Allgemeiner englischer Begriff für Schadsoftware

i)  Schadsoftware, die sich von selbst übertragen kann

j)  Schadsoftware, die Hintertüren im System öffnet

k)  Englische Kurzform für ungewünschte Anwendung

l)  Schadprogramme, die alles verschlüsseln und erpressen

m)  Angriff, der Server durch viele Anfragen überlastet

n)  Server sind durch diesen Angriff außer Betrieb, gestört

o)  Andauernder Cyberangriff auf das Netzwerk

p)  Serverangriffe durch Erreichbarkeitsüberprüfungen

q)  Angriffe durch Einmischung in Kommunikationen

r)  Vereinfachte Anmeldung im System

s)  Asymmetrisches Verschlüsselungsverfahren

t)  Zusammenstellung vertrauenswürdiger Quellen/Apps

::: {.solution}
a)  Bundesamt für Cybersicherheit (Kurzform) → (3) BSI

b)  Gesetzliches Regelwerk zum Schutz persönlicher Daten → (5) DSGVO

c)  Grundwert Availability im Deutschen → (17) Verfügbarkeit

d)  Grundwert Confidentiality im Deutschen → (18) Vertraulichkeit

e)  Grundwert Authenticity im Deutschen → (6) Echtheit/Überprüfbarkeit

f)  Deming-Zyklus → (9) PDCA Plan-Do-Check-Act-Modell

g)  Kombination aus Angriffsweg und Angriffstechnik → (1) Angriffsvektor

h)  Allgemeiner englischer Begriff für Schadsoftware → (7) Malware

i)  Schadsoftware, die sich von selbst übertragen kann → (20) Würmer

j)  Schadsoftware, die Hintertüren im System öffnet → (16) Trojaner

k)  Englische Kurzform für ungewünschte Anwendung → (11) PUA
    (Potentially Unwanted Application)

l)  Schadprogramme, die alles verschlüsseln und erpressen → (12)
    Ransomware

m)  Angriff, der Server durch viele Anfragen überlastet → (4) DoS
    (Denial of Service)

n)  Server sind durch diesen Angriff außer Betrieb, gestört → (15) DoS
    (Spam)

o)  Andauernder Cyberangriff auf das Netzwerk → (2) APT (Advanced
    Persistent Threat)

p)  Serverangriffe durch Erreichbarkeitsüberprüfungen → (10) Ping
    Flooding

q)  Angriffe durch Einmischung in Kommunikationen → (8)
    Man-in-the-Middle

r)  Vereinfachte Anmeldung im System → (14) Single-Sign-on

s)  Asymmetrisches Verschlüsselungsverfahren → (13) S/MIME

t)  Zusammenstellung vertrauenswürdiger Quellen/Apps → (19) Whitelisting
:::

## Aufgabe 3

Nennen Sie weitere fünf Gebote für Datensicherheit zu den bereits
aufgeführten.

Zugangskontrolle, Eingabekontrolle, Verfügbarkeitskontrolle,
Wirksamkeit, Trennbarkeit

::: {.solution}
Aus:
<https://www.marconomy.de/8-gebote-zur-datensicherheit-die-jeder-kennen-sollte-a-530186/>

- Zutrittskontrolle

  Alle Arten von IT-Systemen und Anlagen zur Datenverarbeitung müssen
  vor dem Zutritt Unbefugter geschützt sein. Herausforderung hierbei ist
  es, die entsprechenden Schutzbereiche im Unternehmen zu identifizieren
  und angemessene Barrieren zu errichten.

- Zugriffskontrolle

  Nur konkret berechtigte Personen dürfen Einblick in Daten erhalten und
  diese auch nur ihrer individuellen Berechtigung entsprechend nutzen.
  Ein schriftliches Berechtigungskonzept hilft dabei, den Überblick zu
  behalten, wer worauf Zugriff haben darf.

- Weitergabekontrolle

  Es müssen Vorschriften definiert werden, welche Daten an wen und unter
  welchen Voraussetzungen über welche zulässigen Übertragungswege
  weitergegeben werden dürfen.

- Auftragskontrolle

  Ob Software-Anbieter, Marketing- oder PR-Agentur: jeder externe
  Dienstleister, der personenbezogene Daten „im Auftrag" verarbeitet,
  muss verpflichtet, kontrolliert und regelmäßig überwacht werden. Der
  Grund: Auch die Verantwortung für ausgelagerte Aufgaben obliegt
  vollständig dem Auftraggeber.

Aus:
<https://www.staff.uni-mainz.de/pommeren/DSVorlesung/Grundprobleme/Gebote.html>

- Transportkontrolle

  Festlegung von Boten und Transportwegen, Quittung, Transportkoffer,
  Verschlüsselung.
:::

## Aufgabe 4

Nennen Sie je eine passende TOM zu den folgenden Geboten.

a)  Zugangskontrolle

    ::: {.solution}
    siehe Aufgabe 2

    Verwehrung des Zugangs zu Verarbeitungsanlagen, mit denen die
    Verarbeitung durchgeführt wird, für Unbefugte

    - Serverraum mit Zugangskontrolle (z. B. Transponder,
      Schlüsselkarte, biometrische Zugangskontrolle, Schlüssel, PIN),
    - abschließbare Netzwerkschränke
    :::

b)  Eingabekontrolle des Zugriffs

    ::: {.solution}
    Aus: \>https://datenschutzfachmann.eu/eingabekontrolle/\>

    wer hat wann was geändert

    Die Eingabekontrolle gehört zum Schutzziel der Integrität und ist
    auch Bestandteil der technischen und organisatorischen Maßnahmen. Im
    Art. 32 Abs. 1 lit. b DSGVO. Beim Schutzziel Integrität geht es um
    die Richtigkeit und Echtheit von personenbezogenen Daten. Beides
    stellen Sie über die kontrollierte Eingabe sicher.

    Änderungen an personenbezogenen Daten werden so nachvollziehbar.
    :::

c)  Verfügbarkeitskontrolle

    ::: {.solution}
    siehe Aufgabe 2

    Backups, Redundazen schaffen, um Verfügbarkeit zu erhöhen z. B.
    mithilfe von USV, RAID, zwei Netzteile Einrichtung von Überwachungs-
    und Alarmierungssystemen, um Ausfälle schnell zu erkennen und zu
    beheben. 3-2-1-Regel

    3 Kopien, 2 verschiedene Medien, 1 Kopie extern
    :::

d)  Wirksamkeitskontrolle

    ::: {.solution}
    Aus:
    <https://eac-sicherheit.de/umsetzung-und-wirksamkeitskontrolle/>

    Die Wirksamkeit der Maßnahmen muss regelmäßig überwacht und
    gegebenenfalls angepasst werden. Es empfiehlt sich die
    Wirksamkeitskontrolle mindestens einmal im Jahr durchzuführen. Dabei
    sollten die bereits umgesetzten Maßnahmen überprüft werden, um
    sicherzustellen, dass sie tatsächlich dazu beigetragen haben, das
    Unfallrisiko zu minimieren. Falls erforderlich, sollten weitere
    Maßnahmen ergriffen werden, um unfallfreie und sichere
    Arbeitssysteme zu gewährleisten. Die Wirksamkeitskontrolle muss auch
    dokumentiert werden, um bei Bedarf Nachweise über die erfolgten
    Überprüfungen und Maßnahmen vorlegen zu können. Dadurch können
    Unternehmen auch bei behördlichen Überprüfungen oder Audits
    nachweisen, dass sie ihrer Verpflichtung zur Gewährleistung von
    Arbeitssicherheit und Gesundheitsschutz nachkommen.
    :::

e)  Trennbarkeit/Trennungskontrolle

    ::: {.solution}
    Siehe Aufagbe 2

    Gewährleistung, dass zu unterschiedlichen Zwecken erhobene
    personenbezogene Daten getrennt verarbeitet werden können.
    Anwendungssoftware in Subdomänen aufteilen, die jeweils selbst für
    die Datenverarbeitung zuständig sind.
    :::

## Aufgabe 5

Erläutern Sie die folgenden sieben Begriffe

a)  Aktive Netzwerkkomponenten

    ::: {.solution}
    Aktive Netzwerkkomponenten sind alle Geräte, die aktiv Signale
    verarbeiten bzw. verstärken können (Netzwerkgeräte). Sie benötigen
    dazu eine Stromversorgung. Zu dieser Gruppe gehören Hubs und
    Switches, Router, Bridges, Firewalls und Session Border Controller.
    :::

<!-- -->

b)  DHCP

    ::: {.solution}
    Das Dynamic Host Configuration Protocol (DHCP) ist ein
    Netzwerkprotokoll, das die Zuweisung der Netzwerkkonfiguration an
    Clients durch einen Server ermöglicht.
    :::

<!-- -->

c)  DMZ

    ::: {.solution}
    Eine Demilitarisierte Zone (DMZ, auch Demilitarized Zone, Perimeter-
    oder Umkreisnetzwerk) bezeichnet ein Computernetz mit
    sicherheitstechnisch kontrollierten Zugriffsmöglichkeiten auf die
    daran angeschlossenen Server.
    :::

<!-- -->

d)  DNS

    ::: {.solution}
    Das Domain Name System, deutsch Domain-Namen-System ist ein
    hierarchisch unterteiltes Bezeichnungssystem in einem meist
    IP-basierten Netz zur Beantwortung von Anfragen zu Domain-Namen
    (Namensauflösung).
    :::

<!-- -->

e)  Firewall

    ::: {.solution}
    Eine Firewall ist ein Sicherungssystem, das ein Rechnernetz oder
    einen einzelnen Computer vor unerwünschten Netzwerkzugriffen
    schützt.
    :::

<!-- -->

f)  IPS

    ::: {.solution}
    Als Intrusion-Prevention-Systeme (kurz: IPS) werden
    Intrusion-Detection-Systeme (kurz: IDS) bezeichnet, die über die
    reine Generierung von Ereignissen (Events) hinaus Funktionen
    bereitstellen, die einen entdeckten Angriff abwehren können.
    :::

<!-- -->

g)  Proxy

    ::: {.solution}
    Ein Proxy ist eine Kommunikationsschnittstelle in einem Netzwerk aus
    Rechnern in Form eines Servers. Er arbeitet als Vermittler, der auf
    der einen Seite Anfragen entgegennimmt, um dann über seine eigene
    Adresse eine Verbindung zur anderen Seite herzustellen.

    Wird der Proxy als Netzwerkkomponente eingesetzt, bleibt einerseits
    die tatsächliche Adresse eines Kommunikationspartners dem jeweils
    anderen Kommunikationspartner verborgen, was eine gewisse Anonymität
    schafft. Als (mögliches) Verbindungsglied zwischen unterschiedlichen
    Netzwerken kann er andererseits eine Verbindung zwischen
    Kommunikationspartnern selbst dann realisieren, wenn deren Adressen
    zueinander inkompatibel sind und eine direkte Verbindung nicht
    möglich ist.
    :::
