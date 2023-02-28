# Enterprise µServices mit Spring Boot

## Tag 1 (Freitag)
-> Einführung Spring (initializr)
-> µServices:
--> Was ist zu beachten,
--> CAP: Consistency, Partion Tolerance, Availability
----> Nur zwei der drei Sachen können erfüllt.
----> Partition Tolerance: Bei µService gegeben.
----> Entscheidung zwischen Consistency und Availability.
--> Was ist ein µService?
----> Isoliertes System
----> Self-contained
----> Alle Layer ggf. enthalten
----> Aufruf über das Netzwerk: Typisch: http oder asynchron (JMS, Kafka)
--> Warum µService?
----> Modularisierung
-------> Bessere Wartbarkeit
-------> Bessere Skalierbarkeit
-------> Bessere Ressourcennutzung
-------> Parallele Entwicklung. Kleine Teams, alle Stakeholder
--> Warum keine µService, d.h. was sind die Nachteile, "Herausforderungen"
----> Technologie-Zoo
----> Abstimmung der einzelnen Services (Kommunikation)
----> Komplexität für den Betrieb

-> lesson03-Projekt: Build mit maven und dependencies
-> Projekt lokal testen

## Tag 2 (Montag)
-> Domain Driven Design (DDD)
----> Funktionalitäten in Bounded Contexts => Modell für verschiedene µServices
----> Was passiert bei gegenseitigen Abhängigkeiten
--------> Ist ein besserer Schnitt möglich? Manchmal lässt es sich nicht vermeiden ---> Ist es ggf. ein Bounded Context?
----> Falls getrennte bounded contexts: Schnittstellen
--------> Erstmal fachlich, danach technisch
--------> Supplier ./. Customer, OpenHost ./. Conformis (ACL: Anti corrupotion layer), shared kernel, sperate ways
--------> Ziel: Schnittstelle sollte möglichst einfach sein, d.h. keine umfangreiche Kenntnis der fachlich zur Nutzung erforderlich.
-> Ziel: Markoarchitektur
----> µService so zerlegen, dass use-cases (d.h. Anforderungen) typischerweise nur wenige µServices betreffen, sofern sie ähnlich sind.
----> Nicht ähnliche use-cases sind in verschiedenen µServices.
-> Context Map (UML)
----> Ein Weg: Statisches Domänenmodell
----> Alternativ: Business Processes
-> µServices API Patterns
---> Struktur für Schnittstellen in einer Systemlandschaft.
-> 12 factor App
---> Nicht-funktionale Anforderungen an µServices (Schwerpunkt: Betrieb)
