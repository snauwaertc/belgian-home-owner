# Bijdragen

Deze lijst is een uitnodiging. Heb je zelf een open project of een officiële bron gebruikt die een Belgische
huiseigenaar verder helpt, voeg ze toe.

**De hoofdregel: alleen wat je zelf getest hebt.** Een project komt in de lijst als iemand het in of voor zijn eigen
woning gebruikt heeft. Iets wat je alleen van naam kent, hoort bij de kandidaten onderaan.

## Wat hier thuishoort

- **Open projecten** (broncode publiek) die een taak in of rond de woning oplossen.
- **Officiële bronnen**: de overheid, de regulator, de netbeheerder.
- **Gesloten producten of diensten** alleen als je ze zelf gebruikt hebt, met de prijs erbij zoals die op hun eigen
  site staat.
- Bij voorkeur iets wat **specifiek Belgisch** is of in België anders werkt dan elders: het AREI, de digitale meter,
  het capaciteitstarief, de keuring, tariefkaarten.

## Wat hier niet thuishoort

- **Gegevens van een echte woning**: adres, plattegrond, foto's, keuringsverslag, EAN- of serienummers.
- **Meningen en ervaringen** in de lijst zelf. De lijst zegt wat iets doet en waarvoor, niet of het goed is.
- **Reclame.** Een beschrijving in de woorden van een verkoper wordt herschreven tot wat het product doet.
- **De tekst van het AREI** of van een andere beschermde bron. Verwijs ernaar.

## Hoe een regel eruitziet

Elke regel in een tabel heeft:

| Kolom | Wat erin staat |
|---|---|
| **Naam** | De naam, met een link naar de repo of de officiële pagina |
| **Wat het doet** | Eén of twee zinnen, feitelijk, bij voorkeur gebaseerd op de eigen beschrijving van het project |
| **Waarvoor je het gebruikt** | De taak van de huiseigenaar die ermee opgelost wordt |
| **Soort en licentie** | Open met de licentie, "geen licentie", of gesloten met de prijs |
| **Laatste wijziging** | Voor een repo: de datum van de laatste wijziging. Anders "n.v.t." |

Zet de regel onder de taak waar ze bij hoort. Past ze nergens, stel dan een nieuwe taak voor als kop.

"Geen licentie" betekent dat de auteur geen licentie koos. Je mag de code dan lezen en gebruiken zoals ze aangeboden
wordt, maar niet zomaar overnemen of verder verspreiden.

## Nakijken

Voor je een pull request maakt:

1. Heb je het zelf gebruikt? Zo niet, zet het bij de kandidaten.
2. Open de link. Bestaat de pagina, en is het de pagina die je bedoelt?
3. Voor een repo op GitHub: haal de licentie en de datum van de laatste wijziging op (zie de skill
   [lijst-nakijken](skills/lijst-nakijken/SKILL.md)).
4. Controleer dat je beschrijving zegt wat het project zelf zegt te doen.

## Kandidaten: wie heeft dit getest?

Deze open projecten lijken bruikbaar, maar niemand hier heeft ze gebruikt. Heb jij dat wel, verplaats de regel dan
naar de lijst.

| Project | Wat het zegt te doen | Onder welke taak |
|---|---|---|
| [belgian_digitalmeter_p1](https://github.com/jensdepuydt/belgian_digitalmeter_p1) | Python-script dat de uitvoer van de Belgische P1-poort ontleedt | De digitale meter uitlezen |
| [esp8266_p1meter_belgium](https://github.com/KurtKeunen/esp8266_p1meter_belgium) | Programma voor een ESP8266 dat de P1-gegevens van een Belgische meter naar een MQTT-broker stuurt | De digitale meter uitlezen |
| [homeassistant_be_electricity_prices](https://github.com/renaudallard/homeassistant_be_electricity_prices) | Integratie voor Home Assistant die de Belgische all-in prijs per kWh berekent uit de tariefkaarten van de leveranciers | Prijzen en tarieven volgen |
| [Smart Irrigation](https://github.com/altmenorg/HAsmartirrigation) | Integratie voor Home Assistant die berekent hoeveel water de tuin nodig heeft | Tuin |
| [Irrigation Unlimited](https://github.com/rgc99/irrigation_unlimited) | Beregeningssturing voor Home Assistant met zones en schema's | Tuin |

## Geweigerd of verwijderd

| Verwijzing | Waarom | Datum |
|---|---|---|
| `Raeymeister/BelgianSMR2Domoticz` | Het adres bestaat niet op GitHub (404). Ken je het juiste adres, open dan een issue. | 2026-10-12 |

## Licentie van je bijdrage

Met een bijdrage ga je akkoord dat je tekst onder CC BY 4.0 valt en je code en skills onder de MIT-licentie
(zie [LICENSE.md](LICENSE.md)).
