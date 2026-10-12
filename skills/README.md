# Skills

> **English summary.** Agent skills: step-by-step procedures an AI agent can follow.

Een skill is een werkwijze in tekst die een AI-agent stap voor stap kan volgen: in welke volgorde, met welke
gereedschappen, wanneer controleren, wat niet doen zonder te vragen.

## Gebruiken

Een skill is een map met een bestand `SKILL.md`. Kopieer de map naar de plaats waar je agent zijn skills zoekt. Bij
Claude Code is dat `.claude/skills/` in je project, of `~/.claude/skills/` voor al je projecten.

## Beschikbaar

| Skill | Wat ze doet | Waarvoor je ze gebruikt |
|---|---|---|
| [lijst-nakijken](lijst-nakijken/SKILL.md) | Opent elke link in de lijst, haalt voor elke repo de licentie en de laatste wijziging op, en werkt de lijst bij | De lijst in deze repo actueel houden |

## Een skill toevoegen

Een skill hoort hier als ze:

1. zegt wanneer ze van toepassing is, en wanneer niet;
2. de gereedschappen noemt die ze nodig heeft;
3. de agent laat controleren na elke stap die iets wijzigt;
4. zegt wat de agent niet mag doen zonder te vragen;
5. door iemand is uitgevoerd, met de datum erbij.
