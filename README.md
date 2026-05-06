# Ulriken Aktiv Fritid - Driftsmodell

Dette er nettsiden for Ulriken Aktiv Fritid, som presenterer foreningens driftsmodell, organisasjon og vedtekter.

## Lokal kjøring

For å kjøre siden lokalt:

```bash
# Start en lokal webserver
python3 -m http.server 8000

# Åpne http://localhost:8000 i nettleseren
```

## Publisering til GitHub Pages

Denne siden kan publiseres til GitHub Pages for å gjøre den tilgjengelig på internett.

### Automatisk publisering (anbefalt)

1. Gå til repository-innstillingene på GitHub
2. Under "Pages" i sidelinjen, velg "Deploy from a branch"
3. Velg "main" som kilde-branch
4. Klikk "Save"

Siden vil da være tilgjengelig på `https://[brukernavn].github.io/driftsmodell/`

### Manuell publisering

Hvis du vil publisere til en annen plattform:

1. Last ned alle filene fra dette repository
2. Last opp til din webhotell-leverandør
3. Sørg for at `index.html` er rotfilen

## Struktur

- `index.html` - Hovedsiden med faner for Om oss, Organisasjonskart, Driftsmodell
- `vedtekter.html` - Foreningens vedtekter
- Ingen eksterne avhengigheter - siden fungerer offline

## Bidra

For å bidra til utviklingen av siden:
1. Fork repository
2. Gjør endringer
3. Send pull request

## Lisens

Dette prosjektet er åpent og fritt tilgjengelig for alle interesserte.