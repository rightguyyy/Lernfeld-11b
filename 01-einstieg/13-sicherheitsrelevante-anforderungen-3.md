---
css: ../css/style.css
date: Schuljahr 2025/2026
lang: de-DE
subtitle: Lernfeld 11b -- Betrieb und Sicherheit vernetzter Systeme
  gewährleisten
title: Netzwerk -- Sicherheitsrelevante Anforderungen 3
---

## Aufgabe 1

Erläutern Sie folgende drei Befehle der Betriebssystem-Kommandozeile.

a) ping* 
Mit `ping` wird geprüft, ob ein Zielrechner im Netzwerk erreichbar ist.  
Es sendet ICMP-Echo-Anfragen und misst die Antwortzeit.  
So lassen sich Verbindungsprobleme oder Paketverluste erkennen.  

b) nslookup
Mit `nslookup` lassen sich DNS-Abfragen durchführen.  
Man kann prüfen, welche IP-Adresse zu einem Domainnamen gehört oder umgekehrt.  
Das hilft, DNS-Probleme zu aktivieren.

c) tracert / traceroute 
Mit `tracert` (Windows) bzw. `traceroute` (Linux/Unix) wird der Weg der Pakete zum Zielrechner angezeigt.  
Es listet die Router (Hops) auf, die die Daten durchlaufen.  
So lässt sich feststellen, wo es Verzögerungen oder Ausfälle im Netzwerkpfad gibt.  


## Aufgabe 2

Informieren Sie sich mithilfe des folgenden Schaubilds und des
englischen Informationstextes über SDN und Netzwerkvirtualisierung und
bearbeiten Sie folgende Teilaufgaben.

::: {.frame}
![](sdn.png)
:::

::: {.frame}
> Software-defined networking (SDN) describes a decoupling of the
> network control logic from the executing devices such as routers,
> bridges, gateways or switches that control information in the
> underlying network. To avoid network administrators having to use
> flexible hardware to support network services, virtualization replaces
> hardware with physical network connectivity.
>
> The aim of the SDN architecture is to provide fast and reliable access
> to business applications. In software-defined networks, a software
> application controller manages the network and its activities. With
> SDN, engineers and administrators can manage network services
> centrally and based on software, so they can react quickly to changing
> business requirements.
>
> Network virtualization is realized in three layers --- the application
> layer, the control layer and the infrastructure levels. Connectivity
> between the layers is enabled by northbound and southbound APIs.
>
> The application layer includes a set of applications and network
> functions to improve the applications. Virtualization helps here to
> enable more performance, simplify IT and increase security. Examples
> are application wide area networks (WAN), firewalls, load balancing,
> WAN Optimization Controllers (WOCs), Authentication and Application
> Delivery Controllers (ADCs). With software-defined virtualization of
> hardware components, less flexible and hardware-specific controllers
> can be replaced.
>
> The control layer manages policies and traffic flow across the
> network. It consists of the SDN Controller, which connects the
> application layer with the infrastructure layer. This layer handles
> the requests that are sent from the application layer via the
> southbound API to the actual network.
>
> The infrastructure is connected via the northbound API. It also
> communicates information back to the application layer extracted from
> the infrastructure to optimize functionality.
>
> The infrastructure layer contains the physical devices such as
> switches and routers. These network devices control important routing
> functions and data processing capabilities. They are responsible for
> providing critical information for network usage and topology to
> collect and send back to the control layer.
>
> The northbound API enables communications between the control and
> application layers.
>
> The southbound API enables communications between the control and
> infrastructure layers.
:::

a)  Geben Sie dem Schaubild eine Überschrift.

Architektur von Software-defined Networking (SDN) und Netzwerkvirtualisierung  

b)  Was ist der Grundansatz von SDN hinsichtlich der Geräte und der
    Netzwerksteuerung?

Die Steuerungslogik wird von den Geräten (Switches, Router, Gateways) entkoppelt und zentral durch Software gesteuert. Geräte übernehmen nur noch die Weiterleitung.

c)  Aus welchen Schichten besteht die Netzwerkvirtualisierung?

- Anwendungsschicht (Application Layer)  
- Steuerungsschicht (Control Layer)  
- Infrastrukturschicht (Infrastructure Layer)

d)  Welche Netzwerkfunktionen werden in der Anwendungsschicht
    bereitgestellt?

WAN, Firewalls, Load Balancing, WAN-Optimierung, Authentifizierung, Application Delivery Controller (ADC).  

e)  Was leistet die Steuerungsschicht?

Der SDN-Controller verwaltet Richtlinien und den Datenverkehr. Er verbindet Anwendungen mit der Infrastruktur und leitet Anfragen über die Southbound-API an die Geräte weiter.  

f)  In welcher Schicht sind die physischen Switches und Router
    angesiedelt?

Infrastrukturschicht (Infrastructure Layer). 

g)  Was ist der Unterschied zwischen der Northbound-API und der
    Southbound-API?

- Northbound-API: Kommunikation zwischen Control Layer und Application Layer.  
- Southbound-API: Kommunikation zwischen Control Layer und Infrastructure Layer.  