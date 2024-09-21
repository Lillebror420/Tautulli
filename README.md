
# Tautulli Webhook Integration

Denne samling af JSON-koder er designet til at oprette webhooks i Tautulli, der sender embeds til en platform som Discord, når der sker aktivitet på din Plex-server. Webhooks bruges til at give opdateringer om film- eller serieafspilning, såsom kvalitet, resterende tid, IMDb-rating, og mere.

### Funktionalitet
Disse webhooks sender detaljerede beskeder, der afhænger af, om indholdet er en film eller en episode af en tv-serie. Der er forskellige farver og felter afhængigt af indholdstypen.
## Farve skema

| Farve             | Hex                                                                |
| ----------------- | ------------------------------------------------------------------ |
| Film | ![#990000](https://via.placeholder.com/10/990000?text=+) #990000 |
| Serie/Episode | ![#FCBA03](https://via.placeholder.com/10/FCBA03?text=+) ##FCBA03 |

## Opsætning

#### Trin 1: Åbn Tautulli Log ind på din Tautulli-server.

#### Trin 2: Gå til Webhooks-indstillinger klik på Settings (Indstillinger) fra menuen. Naviger til Notification Agents.
#### Trin 3: Tilføj en ny webhook klik på Add a New Notification Agent. Vælg Webhook som agent-type.
#### Trin 4: Konfigurer Webhook webhook URL: 
Angiv URL’en til den platform, hvor beskederne skal sendes (f.eks. en Discord Webhook URL).
Payload:
I feltet til POST Payload, indsæt en af JSON-koderne fra denne samling. Vælg den, der passer til din ønskede beskedtype (f.eks. film eller episode).
Triggers:
Vælg de relevante triggers baseret på den aktivitet, du vil overvåge, f.eks.:
Playback Start (Afspilning startet)
Playback Pause (Afspilning pauseret)
Playback Stop (Afspilning stoppet)
#### Trin 5: Gem ændringerne Klik på Save for at gemme konfigurationen af din webhook.
#### Trin 6: Test din Webhook
Når webhook'en er opsat, kan du teste den ved at starte, pause eller stoppe afspilning på din Plex-server. Hvis alt er opsat korrekt, vil du modtage en besked i den platform, du har angivet (f.eks. Discord).

# Fejlfinding
Hvis webhooken ikke fungerer korrekt:

Tjek Tautulli-loggene for eventuelle fejlmeddelelser.
Sørg for, at webhook-URL’en er korrekt indtastet.
Verificér, at JSON-strukturen i payloaden er gyldig.
