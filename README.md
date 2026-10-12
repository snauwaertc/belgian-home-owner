# Belgian Home Owner

**NL** Een lijst van open projecten en officiële bronnen voor Belgische huiseigenaars, geordend per taak: wat doet
wat, en waarvoor gebruik je het. Elektriciteit en keuring (AREI), de digitale meter, het capaciteitstarief, domotica,
je woning modelleren en huishoudfinanciën.

**FR** Une liste de projets ouverts et de sources officielles pour les propriétaires belges, classée par tâche : qui
fait quoi, et pour quoi faire. Électricité et contrôle (RGIE), compteur numérique, tarif capacitaire, domotique,
modélisation de la maison et finances du ménage. Les descriptions sont en néerlandais.

**EN** A task-oriented list of open projects and official sources for Belgian home owners: what does what, and what
you use it for. Electrical inspection (AREI), the digital meter, the capacity tariff, home automation, modelling your
house and household finance. Descriptions are in Dutch.

Alles in deze lijst is door een bijdrager zelf gebruikt. Laatst nagekeken: **2026-10-12**. Elke link is op die datum geopend; van elk project op GitHub zijn de licentie en de
datum van de laatste wijziging toen opgevraagd. Ontbreekt er iets of klopt er iets niet: zie [bijdragen](CONTRIBUTING.md).

## Inhoud

- [Elektriciteit](#elektriciteit)
  - [Een eendraadschema en situatieplan tekenen](#een-eendraadschema-en-situatieplan-tekenen)
  - [De regels en de keuring](#de-regels-en-de-keuring)
- [Energie](#energie)
  - [De digitale meter uitlezen](#de-digitale-meter-uitlezen)
  - [Prijzen en tarieven volgen](#prijzen-en-tarieven-volgen)
  - [Verbruik sturen](#verbruik-sturen)
  - [De verwarming lokaal aansturen](#de-verwarming-lokaal-aansturen)
  - [Zonnepanelen doorrekenen](#zonnepanelen-doorrekenen)
- [Tuin](#tuin)
- [Weer en afval](#weer-en-afval)
- [Je woning modelleren](#je-woning-modelleren)
  - [Gegevens over je woning en perceel](#gegevens-over-je-woning-en-perceel)
  - [Opmeten](#opmeten)
  - [Een model bouwen en plannen maken](#een-model-bouwen-en-plannen-maken)
- [Huishoudfinanciën](#huishoudfinanciën)
- [Werken met een AI-agent](#werken-met-een-ai-agent)

## Elektriciteit

### Een eendraadschema en situatieplan tekenen

Bij een keuring van een huishoudelijke installatie horen een eendraadschema en een situatieplan.

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [eendraadschema](https://github.com/igoethal/eendraadschema) | Tekent een eendraadschema en een situatieschema in de browser, zonder installatie. Ook online op [eendraadschema.goethals-jacobs.be](https://eendraadschema.goethals-jacobs.be/). | Het schema van een woning tekenen en afdrukken | open, GPLv3 | 2025-09-18 |
| AREIplan | Fork van eendraadschema met een situatieplan dat je zelf tekent of op een plattegrond (pdf, DXF, DWG) legt, een bordplanner, lijsten, drie talen, een lokale app, en aansturing door een AI-agent | Het volledige dossier tekenen, ook door een agent | open, GPLv3 | nog niet gepubliceerd |

### De regels en de keuring

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort |
|---|---|---|---|
| [AREI, Boeken 1, 2 en 3](https://economie.fgov.be/nl/publicaties/algemeen-reglement-op-de) | De officiële tekst van het Algemeen Reglement op de elektrische installaties. Boek 1 gaat over laagspanning, dus ook over woningen. | Nalezen wat de regel zegt | FOD Economie |
| [Keuring van uw elektrische installatie](https://www.vlaanderen.be/keuring-van-uw-elektrische-installatie-arei) | Legt uit wanneer een installatie gekeurd moet worden en door wie | Weten of en wanneer je een keuring nodig hebt | Vlaamse overheid |

## Energie

### De digitale meter uitlezen

De digitale meter stuurt via zijn gebruikerspoort (P1) elke seconde je verbruik en vermogen uit. De poort moet eerst
opengezet worden.

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [Fluvius, poortbeheer](https://mijn.fluvius.be/poortbeheer) | De gebruikerspoort van je meter openen of sluiten. Uitleg: [maak je digitale meter slim](https://www.fluvius.be/nl/meters-en-meterstanden/maak-je-meter-slim). | De eerste stap voor je iets kan uitlezen | netbeheerder | n.v.t. |
| [ESPHome, component DSMR](https://esphome.io/components/sensor/dsmr.html) | Leest de P1-poort met een ESP-bordje en geeft de waarden door aan Home Assistant. Kent Belgische waarden, zoals het kwartiergemiddelde voor het piektarief en het gasverbruik. | Een eigen of gekochte P1-lezer laten werken met Home Assistant | open, zie [de repo](https://github.com/esphome/esphome) | 2026-10-12 |
| [zuidwijk/dsmr](https://github.com/zuidwijk/dsmr) | De configuratie van de SlimmeLezer, een kant-en-klare P1-lezer met wifi. De auteur verwijst voor onderhoud naar de component in ESPHome. | Een SlimmeLezer instellen | geen licentie | 2026-03-23 |

### Prijzen en tarieven volgen

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [Capaciteitstarief](https://www.vlaamsenutsregulator.be/nl/elektriciteit-en-aardgas/nettarieven/capaciteitstarief) | Legt uit hoe het capaciteitstarief berekend wordt: de hoogste kwartierpiek per maand, het gemiddelde over 12 maanden, het minimum van 2,5 kW | Begrijpen wat een verbruikspiek kost | Vlaamse Nutsregulator | n.v.t. |
| [V-test](https://vtest.vlaamsenutsregulator.be/) | Vergelijkt energiecontracten voor jouw verbruik | Een contract kiezen of nagaan of je huidige nog goed zit | Vlaamse Nutsregulator | n.v.t. |
| [hass-entso-e](https://github.com/JaccoR/hass-entso-e) | Integratie voor Home Assistant die de prijzen van de volgende dag ophaalt bij het ENTSO-E Transparency Platform | Dynamische prijzen in Home Assistant | open, Apache-2.0 | 2026-06-22 |
| [nordpool](https://github.com/custom-components/nordpool) | Integratie voor Home Assistant die energieprijzen van Nord Pool ophaalt | Dynamische prijzen in Home Assistant | geen licentie | 2025-12-29 |

### Verbruik sturen

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [Home Assistant](https://github.com/home-assistant/core) | Domoticaplatform dat lokaal draait en toestellen, meters en automatiseringen samenbrengt ([home-assistant.io](https://www.home-assistant.io/)) | De basis waarop de meeste projecten in deze lijst aansluiten | open, Apache-2.0 | 2026-10-12 |
| [EMHASS](https://github.com/davidusb-geek/emhass) | Rekent met lineair programmeren uit wanneer toestellen het best draaien, op basis van prijzen, zonneproductie en verbruik. Kan een capaciteitstarief meerekenen. | Verbruik verschuiven naar goedkope uren en pieken beperken | open, MIT | 2026-10-12 |

### De verwarming lokaal aansturen

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [ebusd](https://github.com/john30/ebusd) | Dienst die praat met verwarmingstoestellen over eBUS ([ebusd.eu](https://ebusd.eu/)) | Een ketel of warmtepomp met eBUS uitlezen en aansturen zonder de cloud van de fabrikant | open, GPL-3.0 | 2026-03-29 |
| [ebusd-configuration](https://github.com/john30/ebusd-configuration) | De beschrijvingen per toestel die ebusd nodig heeft; ebusd haalt ze standaard zelf op | ebusd laten werken met jouw toestel | open, GPL-3.0 | 2026-06-09 |
| [Versatile Thermostat](https://github.com/jmcollin78/versatile_thermostat) | Thermostaat voor Home Assistant met voorinstellingen, raam-, bewegings- en aanwezigheidsdetectie en begrenzing van het vermogen | Per kamer regelen vanuit Home Assistant | open, MIT | 2026-10-12 |

### Zonnepanelen doorrekenen

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [PVGIS](https://re.jrc.ec.europa.eu/pvg_tools/en/) | Schat de opbrengst van zonnepanelen voor een plaats, helling en oriëntatie | De opbrengst per dakvlak inschatten voor je een offerte vraagt | Europese Commissie, gratis | n.v.t. |
| [Open-Meteo](https://github.com/open-meteo/open-meteo) | Weerdienst met een archief van historisch weer ([documentatie](https://open-meteo.com/en/docs/historical-weather-api)) | Je verbruik naast temperatuur en zon leggen | open, AGPL-3.0; gratis voor niet-commercieel gebruik | 2026-10-12 |

## Tuin

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [Rain Bird-integratie](https://www.home-assistant.io/integrations/rainbird/) | Integratie in Home Assistant voor een Rain Bird-beregeningscomputer met wifi-module | De zones van de beregening bedienen en automatiseren vanuit Home Assistant | open, deel van Home Assistant | n.v.t. |

## Weer en afval

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [IRM KMI Weather Belgium](https://github.com/jdejaegh/irm-kmi-ha) | Weerintegratie voor Home Assistant met de gegevens van het Belgische KMI | Het weer en de verwachting van het KMI gebruiken in automatiseringen en op het dashboard | open, MIT | 2026-10-11 |
| [Waste Collection Schedule](https://github.com/mampfes/hacs_waste_collection_schedule) | Integratie voor Home Assistant die ophaalkalenders voor afval inleest; kent voor België onder meer de bron Recycle! | Weten welke afvalsoort wanneer buiten moet, met een herinnering | open, MIT | 2026-10-11 |

## Je woning modelleren

### Gegevens over je woning en perceel

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort |
|---|---|---|---|
| [GRB, Basiskaart Vlaanderen](https://overheid.vlaanderen.be/grb-grb-raadpleegdiensten) | De grootschalige kaart van Vlaanderen met gebouwen en percelen, op te vragen als webdienst | De omtrek en ligging van je woning | Digitaal Vlaanderen, gratis |
| [Digitaal Hoogtemodel Vlaanderen II](https://www.vlaanderen.be/digitaal-vlaanderen/onze-oplossingen/earth-observation-data-science-eodas/het-digitaal-hoogtemodel/digitaal-hoogtemodel-vlaanderen-ii) | Hoogtemodel uit LiDAR-opnames van 2013 tot 2015, als raster van 1 m, met en zonder gebouwen en begroeiing | Dakhoogtes, het terrein en de schaduw van bomen | Digitaal Vlaanderen, gratis |
| [EPC](https://www.vlaanderen.be/epc-voor-een-residentiele-eenheid) | Het energieprestatiecertificaat van een woning | De isolatiewaarden die een deskundige voor je woning noteerde | Vlaamse overheid |

### Opmeten

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [openPlan3D](https://github.com/laanlabs/openPlan3D) | Plattegrondeditor in 2D en 3D die in de browser draait ([app.openplan3d.com](https://app.openplan3d.com/)), met een iPhone-app die kamers scant met LiDAR en muren, deuren en ramen opbouwt terwijl je rondloopt | Een woning opmeten met je telefoon en de plattegrond bewerken en exporteren | open, MIT | 2026-09-17 |

### Een model bouwen en plannen maken

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [IfcOpenShell](https://github.com/IfcOpenShell/IfcOpenShell) | Bibliotheek om gebouwmodellen in het open formaat IFC te lezen en te schrijven. Bevat [Bonsai](https://bonsaibim.org/), een uitbreiding die van Blender een BIM-programma maakt. | Een model van je woning opbouwen dat ook een architect of aannemer kan openen | open, LGPL-3.0 | 2026-10-12 |
| [Blender](https://github.com/blender/blender) | 3D-programma voor modelleren en renderen ([blender.org](https://www.blender.org/)) | Het model bekijken en beelden maken | open, GPL | 2026-10-12 |
| [ezdxf](https://github.com/mozman/ezdxf) | Python-bibliotheek om DXF-bestanden te lezen en te schrijven | Plattegronden uit een model halen in een formaat dat tekenprogramma's openen | open, MIT | 2026-10-10 |

## Huishoudfinanciën

Europese banken moeten rekeninginformatie openstellen voor erkende dienstverleners (PSD2). Lezen en betalen zijn
aparte diensten.

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort |
|---|---|---|---|
| [Enable Banking](https://enablebanking.com/) | Geeft via een API toegang tot rekeninginformatie bij Europese banken. Geregistreerd als aanbieder van rekeninginformatie bij de Finse toezichthouder. [Bijzonderheden per Belgische bank](https://enablebanking.com/docs/markets/be/). | Je verrichtingen in je eigen hulpmiddelen krijgen, alleen lezen | dienst; geen prijs op de site |

## Werken met een AI-agent

| Naam | Wat het doet | Waarvoor je het gebruikt | Soort en licentie | Laatste wijziging |
|---|---|---|---|---|
| [homeassistant-ai/skills](https://github.com/homeassistant-ai/skills) | Skills die een agent leren hoe hij automatiseringen, helpers en dashboards voor Home Assistant goed opzet | Een agent laten meewerken aan je Home Assistant | open, MIT | 2026-10-11 |
| [Skills in deze repo](skills/README.md) | Werkwijzen die een agent stap voor stap kan volgen | Deze lijst onderhouden; meer volgt | open, MIT | 2026-10-12 |

## Bijdragen

Ken je een project of een officiële bron die hier hoort, of is een link dood? Lees [bijdragen](CONTRIBUTING.md).

## Disclaimer

Deze lijst beschrijft wat projecten en bronnen zelf zeggen te doen. Dat een bijdrager iets gebruikt heeft, is geen
garantie dat het bij jou werkt of veilig is. Werken aan een elektrische installatie is gevaarlijk en aan regels gebonden: laat het doen
door wie ervoor opgeleid is en laat de installatie keuren door een erkend organisme. Tarieven, prijzen en regels
veranderen; volg de officiële bron.

## Licentie

Tekst onder CC BY 4.0, code en skills onder MIT. Zie [LICENSE.md](LICENSE.md). Elk project in de lijst heeft zijn
eigen licentie.
