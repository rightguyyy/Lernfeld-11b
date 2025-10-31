---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Schadenspotenziale in vernetzen Systemen identifizieren
---

## Aufgabe 1

Sie arbelten bei der Schutzbedarfsanalyse eines neuen Kunden als
Unterstutzung mit. Es llegt ein Plan des Netzwerks vor.

![](images/network-1.png)

Beschreibung des Kunden: Der Kunde ist eine kleine Werbeagentur mit 5
Mitarbeitenden.

Die 5 Mitarbeitenden arbeiten an Windows-basierten PCs.

Alle Benutzerdaten, wie Projekt- und Kundendaten, werden auf einem
Windows-Dateiserver abgespeichert. Die Benutzer und deren Rechte werden
über ein Active Directory verwaltet.

Ein Auszug aus der Strukturanalyse liegt bereits vor.

![](images/strukturanalyse.png)

a)  Die Schutzbedarfsanalyse ist Teil des Sicherheitsprozesses. Ordnen
    Sie die Reihenfolge der Teilaspekte des Sicherheitsprozesses.

    - Organisation des Sicherheitéprozesses

    - Sicherheitsprozess initiiert

    - Erstellung einer Sicherheitskonzeption

    - Leitlinie zur Informationssicherheit

    - Sicherheitsprozess verbessern

    - Sicherheitskonzeption umgesetzt

    ::: {.solution}
    1.  Sicherheitsprozess initiiert

    2.  Leitlinie zur Informationssicherheit

    3.  Organisation des Sicherheitéprozesses

    4.  Erstellung einer Sicherheitskonzeption

    5.  Sicherheitskonzeption umgesetzt

    6.  Sicherheitsprozess verbessern

    (Vgl. Buch S. 173)
    :::

<!-- -->

b)  Erstellen Sie für den Dateiserver eine Schutzbedarfsanalyse.
    Bewerten Sie dazu den Schutzbedarf für die drei Schutzziele
    Vertraulichkeit, Integrität und Verfügbarkeit.

    **Beispiel:**

    Grundwert: Vertraulichkeit

    Schutzbedarf: sehr hoch

    Begründung: Auf dem Dateiserver liegen personenbezogene Daten, z. B.
    von Kunden. Diese dürfen nur von berechtigten Personen gelesen
    werden. Sonst kann es zu einem Missbrauch von personenbezogenen
    Daten kommen.

    ::: {.solution}
    Grundwert: Integrität

    Schutzbedarf: normal

    Begründung: Fehler werden durch z. B. Prüfsummen erkannt und können
    korrigiert werden

      

    Grundwert: Verfügbarkeit

    Schutzbedarf: hoch

    Begründung: Bei einem Ausfall des Dateiservers kann der Betrieb nur
    noch eingeschränkt weiterarbeiten, da auf die projekt- und
    kundenspezifischen Daten nicht oder nur noch eingeschränkt
    zugegriffen werden kann.

    (Vgl. S. 179--183)
    :::

## Aufgabe 2

Die Schutzbedarfsfeststellung für den Webserver liegt vor.

Grundwert: Vertraulichkeit

Schutzbedarf: sehr hoch

Begründung: Auf dem Webserver liegen neben firmeneigenen Daten auch
Daten von Kunden. Diese dürfen nur von berechtigen Personen gelesen
werden. Sonst kann es zu einem Missbrauch von personenbezogenen Daten
kommen.

  

Grundwert: Integrität

Schutzbedarf: sehr hoch

Begründung: Daten auf der Webseite repräsentieren das Unternehmen. Wenn
hier eine unbemerkte Veränderung möglich ist, kann das für das
Unternehmen einen großen Imageschaden bedeuten. Außerdem enthält der
Webserver u. U. personenbezogene Kundendaten. Diese dürfen nicht
unbemerkt verändert werden.

  

Grundwert: Verfügbarkeit

Schutzbedarf: hoch

Begründung: Der Webserver präsentiert die Agentur. Ein Ausfall des
Webservers kann bedeuten, dass die Agentur nicht mehr von Kunden (auch
Neukunden) im Internet erreicht werden kann. Außerdem steht auf dem
Webserver ein Intranetzugang für Kunden bereit. Ein Ausfall ist nur
kurzfristig annehmbar.

a)  Aufgrund des sehr hohen Schutzbedarfs ist eine gesonderte
    Risikoanalyse nötig. Nennen Sie zwei Sicherheitsrisiken, die den
    Betrieb des Webservers betreffen.

    ::: {.solution}
    1.  SQL-Injection: Bei diesem Angriff nutzt ein Angreifer
        Schwachstellen in Webanwendungen, um über Eingabefelder
        bösartigen SQL-Code in die Datenbank zu schleusen. Dadurch kann
        der Angreifer auf vertrauliche Daten zugreifen, diese
        manipulieren oder löschen. Besonders betroffen sind unsichere
        Formulare oder URL-Parameter, die direkt in SQL-Abfragen
        eingebunden werden.

    2.  Cross-Site Scripting (XSS): Dieser Angriff erfolgt, wenn eine
        Webanwendung unsichere Benutzereingaben in Webseiten integriert,
        ohne sie ausreichend zu überprüfen oder zu bereinigen. Ein
        Angreifer kann bösartigen Code (meist JavaScript) einschleusen,
        der dann von anderen Nutzern ausgeführt wird. Dies kann zu
        Datendiebstahl, Manipulation der Benutzeroberfläche oder der
        Kontrolle über Nutzerkonten führen.

    3.  Unbefungter Zugriff durch unsichere Passwörter

    4.  Schwachstellen in der Implementierung durch Unbefugten Zugang zu
        geschützten Daten erlaubt.
    :::

<!-- -->

b)  Sie identifizieren einen DDoS-Angriff als mögliches Risiko für den
    Webserver. Bewerten Sie die Eintrittshäufigkeit dieses Risikos.

    ::: {.solution}
    Kleinere oder weniger bekannte Websites sind seltener betroffen, da
    sie weniger sichtbar und für Angreifer weniger lukrativ sind.

    Eine Werbe-Agentur hostet keine sicherheitsrelevanten oder politisch
    umstrittene Inhalte, daher ist sie nicht einem höheren Risiko
    ausgesetzt.
    :::

<!-- -->

c)  Erläutern Sie eine Möglichkeit, einem DDoS-Angriff entgegenzuwirken.

    ::: {.solution}
    Webserver, die DDoS-Schutzdienste (z. B. Cloudflare, Imperva) oder
    Lastverteilungstechnologien nutzen, sind besser geschützt und
    reduzieren die Wahrscheinlichkeit eines erfolgreichen DDoS-Angriffs.
    :::

## Aufgabe 3

Diskutieren Sie in Gruppen mögliche Schadenspotenziale für die folgenden
Branchen:

- Apotheken

- Einzelhandel und

- ÖPNV

Benennen Sie mindestens zwei Szenarien für jede Branche im Bereich

::: {.solution}
- Apotheken

  - Bestellungen beim Großhandel können nicht aufgegeben werden →
    wirtschaftlicher Schaden und Imageschaden

  - E-Rezepte

  - Wenn die Kassensysteme betroffen sind, können keine Waren mehr
    verkauft werden → wirtschaftlicher Schaden

  - Wenn das Lagersystem betroffen sind, werden ggf. Waren nicht
    gefunden oder können nicht aus dem Lager entnommen werden und damit
    auch nicht verkauft werden. → wirtschaftlicher Schaden

- Einzelhandel

  - Wenn das Warenwirtschaftsystem betroffen ist, werden ggf. keine
    Waren vom Außenlager angeliefert oder bei Großhandel geliefert,
    d. h. irgendwann drohen leere Regale im Geschäft → wirtschaftlicher
    Schaden und ggf. auch Imageschaden

  - Wenn die Kassensysteme betroffen sind, können keine Waren mehr
    verkauft werden → wirtschaftlicher Schaden

  - wenn aus Systeme für die Kundenbindung (Treuepunkte usw.) Daten
    gestohlen werden, kann dies zu Bußgeldern und Imageschäden führen.

- ÖPNV

  - ggf. fallen Busse aus, Personen werden nicht transportiert. →
    wirtschaftlicher Schaden und Imageschaden
:::

## Aufgabe 4

Notieren Sie wesentliche Aspekte aus dem Abschnitt 3.2.1 im grünen Buch
(S. 183--184).

::: {.solution}
#### Allgemein

Verstöße gegen den Datenschutz können

- Bußgelder und/oder
- Freiheitsstrafen

nach sich ziehen.

#### Imageschaden

insbesondere bei - Banken - Steuerbüros - Unternehmen, die
Passwortmanager zur Verfügung stellen

→ Verstöße gegen den Datenschutz können sich auf die Akzeptanz durch die
Kunden auswirken.

Störung bei Betriebsablauf bei Ausfall kritischer Systeme kann sich auch
negativ auf das Image auswirken.

#### wirtschaftlicher Schaden

Unterbrechungen des Betriebsablaufs können direkt zur wirtschaftlichen
Schäden führen, aber auch zu Imageschäden.

→ Georedundanz (mind. 200km), Trennung der Backups vom Produktivsystem

#### Schaden durch Datenverlust

- Daten können nicht mehr für Geschäftsprozesse genutzt werden
- bei Datendiebstahl drohen je nach Verantworlichkeit auch Bußgelder
:::
