---
title: Design Entscheidung
nav_order: 3
---

{: .label }
[Jane Dane]

{: .no_toc }
# Design Entscheidung

<details open markdown="block">
{: .text-delta }
<summary>Table of contents</summary>
+ ToC
{: toc }
</details>

# Meeting 15.11.2024

Beim heutigen Treffen auf Discord haben wir zuerst die Dokumentationsarchitektur besprochen, wie wir diese aufbauen sollen. Da dies unser erstes Projekt dieser Art ist, haben wir uns dafür entschieden, die Architektur des Dozenten Prof. Dr. Eck von [https://github.com/hwrberlin/fswd-app/tree/main](https://github.com/hwrberlin/fswd-app/tree/main) zu übernehmen. Diese wurde auch am 15.11.2024 in unser Repository [https://github.com/studSH/PetMatch](https://github.com/studSH/PetMatch) übernommen. 

## Design Decision 

### Zusammenarbeit 

**Meta**  
- **Status:** laufend  
- **Aktualisierung:** 15.11.2024  

### Problemstellung  
Da es sich hierbei um unser erstes Projekt dieser Art handelt, haben wir uns die Frage gestellt, wie wir effizient zusammenarbeiten können, ohne große Lücken in der Codeerstellung durch das gleichzeitige Arbeiten entstehen. Ein weiteres Problem ist die Aufteilung der zu verrichtenden Arbeiten, sodass die einzelnen Parteien des Projektes auch unabhängig voneinander arbeiten können, ohne dass es zu einem Arbeitsstau kommt. 

### Entscheidung  
Wir haben uns für GitHub entschieden. Dies wurde uns in der Vorlesung vorgestellt, und wir sehen es als ein optimales Werkzeug, um die oben genannten Probleme zu bewältigen. Um einen Arbeitsstau zu verhindern, haben wir uns für folgende Option entschieden:  

Wir teilen uns die Arbeit in **User-Screen-Ansichten** auf, mit der Option, dass wir uns gegenseitig helfen bei Komplikationen oder bei einem nicht vorhersehbaren Mehraufwand:  
- **Erster Screen:** Patryk  
- **Hauptseite:** Simone/Patryk (wir vermuten hier einen großen Aufwand)  
- **Anmeldung:** Patryk  
- **Beiträge verfassen:** Simone  
- **Registrieren:** Patryk  
- **Profil Haustiere:** Simone  

Es wird wie folgt gearbeitet:  
1. **Entwurf erstellen** – Dieser wird der anderen Partei vorgestellt, und es werden Änderungen besprochen.  
2. **Änderung umsetzen** – Die Änderung wird umgesetzt und nochmals vorgestellt.  
3. **Wiederholen** – Diese Schritte werden so lange wiederholt, bis beide Parteien zufrieden sind.  

### Betrachtete Optionen  
Wir haben keine weiteren Optionen der Zusammenarbeit betrachtet. Für uns ist es sehr plausibel, die vorgestellte Art der Zusammenarbeit zu nutzen, da wir uns damit schon beschäftigt haben und es soweit eingerichtet haben, dass es funktioniert. Es wäre ein unnötiger Mehraufwand, sich jetzt noch über andere Optionen zu informieren, da GitHub auch eine Anforderung vom Dozenten ist.  

Bei der Aufgabenaufteilung war unsere erste Idee, diese auf rein **Frontend** und **Backend** zu verteilen. Beim heutigen Meeting ist uns jedoch aufgefallen, dass der Backend-Anteil viel größer und komplexer ist als der vom Frontend. Deswegen haben wir einstimmig entschieden, diese Idee zu verwerfen und die oben genannte Option in **Entscheidung** weiterzuverfolgen. Diese kann sich im Laufe des Projektes noch ändern.  

<details open markdown="block">
{: .text-delta }
<summary>Table of contents</summary>
+ ToC
{: toc }
</details>



## Vergleich der Geoapify Geocoding API und Google Geocoding API

| Merkmal                 | Geoapify Geocoding API                                 | Google Geocoding API                              | Bewertung für unser Projekt               |
|-------------------------|--------------------------------------------------------|---------------------------------------------------|-------------------------------------------|
| **Kosten**              | Kostenlose Nutzung bis 3.000 Anfragen pro Tag; günstige Tarife für Mehrbedarf. | Monatliches Gratis-Guthaben von 200 USD, für bis zu 40.000 Anfragen; Konto mit Abrechnung nötig. | Geoapify ist kostengünstig und ohne Abrechnung ideal für unser kleines Projekt |
| **Einrichtung**         | API-Schlüssel ohne Abrechnungsanforderungen.           | API-Schlüssel nur mit aktivierter Abrechnung.     | Geoapify hat eine einfache Einrichtung ohne Abrechnungszwang |
| **Datenumfang**         | Basisdaten: Koordinaten, Adressstruktur. Zusätzliche Funktionen gegen Gebühr. | Sehr detaillierte Adressdaten und Geodaten.       | Für unsere Zwecke sind die Geoapify-Basisdaten ausreichend |
| **Zusätzliche Funktionen** | Länderspezifische Infos, Zeitzonen (kostenlos nutzbar) | Zusätzliche Standortinformationen (z. B. `location_type`). | Geoapify bietet einige nützliche Funktionen, Google ist detaillierter |
| **Datenschutz**         | Nutzt OpenStreetMap-Daten, speichert keine Nutzerdaten dauerhaft. | Erfordert Google Cloud-Account und speichert Daten auf Google-Servern. | Geoapify bietet besseren Datenschutz ohne externe Speicherung |
| **Support und Dokumentation** | Solide Dokumentation, hauptsächlich in Englisch. | Umfangreiche Dokumentation in Deutsch und Englisch. | Google hat umfassendere Doku, Geoapify reicht aber für ein kleines Projekt |
| **Einsatzbeispiele**    | Ideal für Prototypen, kleine bis mittlere Anwendungen. | Bewährt für umfangreiche kommerzielle Anwendungen mit hohen Anforderungen. | Geoapify ist ideal für Prototypen und kleine Projekte wie unseres |

## Entscheidungshilfe und Begründung

### Wir haben uns für die **Geoapify Geocoding API** entschieden:
**Begründung**: Die Wahl der Geoapify API liegt in ihrer Einfachheit und Kosteneffizienz, die sich besonders für ein kleines, moderates Projekt wie ein Uni-Projekt anbietet. Geoapify bietet einen unkomplizierten Zugriff ohne Anforderungen an die Abrechnung und eine solide kostenlose Nutzung für bis zu 3.000 Anfragen pro Tag, was für eine solche Anwendung völlig ausreicht. Zudem erfordert Geoapify keine Speicherung sensibler Nutzerdaten auf externen Servern, was den Datenschutz verbessert.

Diese API bietet ausreichende Funktionalität für die Umwandlung von Adressen in Geokoordinaten und ist schnell und einfach integrierbar. Daher eignet sich die Geoapify API für einen ersten Prototyp, bei dem eine moderate Nutzung und einfache Handhabung im Vordergrund stehen.

**Quellen**:
- Geoapify Geocoding API: [https://www.geoapify.com/geocoding-api/](https://www.geoapify.com/geocoding-api/)
- Google Geocoding API: [https://developers.google.com/maps/documentation/geocoding/](https://developers.google.com/maps/documentation/geocoding/)
Zugriff 13.11.2024