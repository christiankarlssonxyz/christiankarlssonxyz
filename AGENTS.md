# AGENTS.md

## Projekt

Projektet christiankarlsson.xyz består av ett WordPress-tema, fristående tillägg och mindre kommandoradsverktyg.

Läs README.md för projektets syfte och övergripande mål.

## Utvecklingsprinciper

- Mobil först (Mobile First).
- Mastodon först.
- Webbplatsen utvecklas för en administrerande användare.
- Följ Unix- och GNU-filosofin: gör en sak och gör den bra.
- Prioritera enkelhet, läsbarhet och underhållbarhet.
- Undvik onödiga beroenden och abstraktioner.
- Använd WordPress inbyggda funktioner där det är lämpligt.
- Utveckla endast funktionalitet som efterfrågas.

## Projektstruktur

- `theme/` – WordPress-temat och webbplatsens presentation.
- `plugins/` – Fristående WordPress-tillägg.
- `cli-tools/` – Små, självständiga kommandoradsverktyg.
- `docs/` – Teknisk dokumentation och utvecklingsbeslut.

Temat ska i första hand ansvara för presentation. Funktionalitet som är oberoende av temat ska placeras i tillägg.

## Kommandoradsverktyg

- Varje verktyg ska ha ett tydligt och avgränsat ansvarsområde.
- Verktygen ska kunna användas självständigt.
- Använd standard input, standard output och standard error där det är lämpligt.
- Verktygen ska kunna kombineras med andra kommandoradsverktyg.
- Använd tydliga felmeddelanden och korrekta exitkoder.
- Varje verktyg ska erbjuda `--help`.
- Bygg inte ett gemensamt TUI-gränssnitt.

## Git och versionshantering

Gitea är projektets primära utvecklingsmiljö. GitHub används för offentlig publicering och externa bidrag.

- `dev` är standardbranch på Gitea.
- `main` innehåller stabil och godkänd kod.
- `feature/*` används för nya funktioner.
- `fix/*` används för felrättningar.
- `hotfix/*` används för brådskande produktionsrättningar.

Utveckling sker i separata branches. Ändringar integreras genom Pull Requests.

Endast godkänd kod från `main` publiceras på GitHub.

## Säkerhet

- Lagra aldrig lösenord, API-nycklar eller åtkomsttoken i Git.
- Validera indata och hantera utdata på ett säkert sätt.
- Använd WordPress säkerhetsfunktioner.
- Ge inte komponenter större behörighet än de behöver.
- Granska innehållet före offentlig publicering.

## Instruktioner till AI-agenter

- Läs relevant dokumentation innan arbetet påbörjas.
- Kontrollera aktuell branch och Git-status.
- Förklara föreslagna ändringar innan implementation.
- Gör små och avgränsade ändringar.
- Ändra inte orelaterade filer.
- Skriv inte över användarens befintliga ändringar.
- Förklara koden så att användaren själv kan förstå och underhålla den.
- Välj lämplig tillgänglig modell för uppgiften.
- Använd subagenter endast när det tillför ett tydligt värde.
- Genomför relevanta tester.
- Skapa inte commits, pushar, merges, taggar eller releaser utan uttryckligt godkännande.
- Genomför aldrig produktionsändringar utan uttryckligt godkännande.

## Avslutning av uppdrag

Redovisa:

- Vad som har ändrats.
- Vilka filer som har ändrats.
- Vilka tester som har genomförts.
- Eventuella risker och kvarstående problem.
- Förslag på nästa steg.
