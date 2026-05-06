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

## Bidra til vedtektene

Vedtekter-siden har en innebygd revisjonsfunksjonalitet hvor besøkende kan foreslå endringer:

- **Foreslå endring**: Klikk på "✏️ Endre" ved hver paragraf
- **Foreslå fjerning**: Klikk på "🗑️ Fjern" ved hver paragraf
- **Foreslå ny paragraf**: Bruk "➕ Foreslå ny paragraf" knappen
- **Generell kommentar**: Bruk kommentarfeltet nederst på siden

Alle forslag opprettes som GitHub Issues med pre-filled templates.

### GitHub Labels for vedtektsendringer

For å organisere vedtektsforslag, opprett følgende labels i GitHub repository:

- `vedtektsendring` - For forslag til endringer i vedtekter
- `kommentar` - For generelle kommentarer
- `ny-paragraf` - For forslag til nye paragrafer

## E-postvarsler for endringer

Det er nå satt opp en GitHub Actions workflow som sender e-post til `jorgen.nordahl@ulrikenskiskole.no` når det opprettes eller oppdateres en pull request, eller når det push-es til `main`.

For å aktivere dette må du legge til følgende secrets i repository under `Settings > Secrets and variables > Actions`:

- `SMTP_HOST` - SMTP-server
- `SMTP_PORT` - SMTP-port (f.eks. 465 eller 587)
- `SMTP_USERNAME` - SMTP-brukernavn
- `SMTP_PASSWORD` - SMTP-passord
- `MAIL_FROM` - e-postadresse som skal være avsender

Workflown ligger i `.github/workflows/email-review-notification.yml`.

## Lisens

Dette prosjektet er åpent og fritt tilgjengelig for alle interesserte.