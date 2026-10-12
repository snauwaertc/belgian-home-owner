---
name: lijst-nakijken
description: Loop alle links in de README van de repo belgian-home-owner na (bestaat de pagina nog, wanneer is een project laatst gewijzigd, welke licentie heeft het) en werk de lijst bij. Gebruik deze skill voor een onderhoudsronde of voor je een nieuwe regel toevoegt.
---

# De lijst nakijken

Uitgevoerd op 2026-10-12.

## Wanneer

- Bij een onderhoudsronde van de lijst in `README.md`.
- Voor je een regel toevoegt die iemand voorstelt.

Niet gebruiken om te beoordelen of een project goed is. Deze skill kijkt alleen na wat te meten valt.

## Nodig

- De GitHub-opdrachtregel `gh`, aangemeld (lezen volstaat).
- `curl`.

## Stappen

1. Lees `README.md` en maak een lijst van alle links.

2. Voor elke link naar een repo op GitHub, vraag de gegevens op:

   ```bash
   gh api "repos/EIGENAAR/NAAM" --jq '[.full_name, .pushed_at[0:10], (.license.spdx_id // "geen"), (if .archived then "gearchiveerd" else "actief" end), (.description // "geen beschrijving")] | join(" | ")'
   ```

   - `Not Found` betekent dat het adres niet bestaat.
   - Geeft `full_name` een andere eigenaar of naam terug dan in de link, dan is de repo verhuisd: neem het nieuwe adres over.
   - `NOASSERTION` als licentie betekent dat GitHub ze niet herkent. Lees dan het licentiebestand in de repo.

3. Voor elke andere link, vraag de statuscode en de titel van de pagina op:

   ```bash
   curl -s -o /dev/null -L -A 'Mozilla/5.0' -w '%{http_code}\n' --max-time 25 "ADRES"
   curl -s -L -A 'Mozilla/5.0' --max-time 25 "ADRES" | grep -o -i '<title>[^<]*</title>' | head -1
   ```

   Een code `200` volstaat niet: sommige sites, waaronder vlaanderen.be, geven ook voor een pagina die niet bestaat
   `200` terug. Klopt de titel niet met wat de regel beschrijft, dan is de link dood.

4. Werk `README.md` bij:

   - Zet **Laatste wijziging** en **Soort en licentie** op wat je mat.
   - Zet de datum bij "Laatst nagekeken" bovenaan op vandaag, alleen als je alle links hebt nagekeken.
   - Verplaats een regel waarvan de link dood is naar de tabel "Geweigerd of verwijderd" in `CONTRIBUTING.md`, met de
     reden en de datum.
   - Een gearchiveerd project blijft staan, met "gearchiveerd" in de kolom **Laatste wijziging**.

5. Controleer de inhoudstafel: elke kop in de lijst heeft een regel, en elke regel wijst naar een kop die bestaat.

## Wat je niet doet

- Een beschrijving verzinnen. Baseer ze op wat het project zelf zegt te doen.
- Een oordeel toevoegen over de kwaliteit van een project.
- Een prijs van een gesloten product wijzigen zonder de pagina te openen waar ze staat.
- Een regel toevoegen waarvan je de link niet hebt kunnen openen.

## Afsluiten

Meld hoeveel links je nakeek, welke regels veranderd zijn, welke weg zijn, en welke je niet kon controleren en waarom.
