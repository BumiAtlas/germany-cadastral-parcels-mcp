# Germany Cadastral Parcels & Flurstück Lookup MCP (Baden-Württemberg, Berlin)

[Deutsch](#deutsch)

Connect your AI assistant (Claude, ChatGPT, Cursor) to [BumiAtlas](https://bumiatlas.com) for German land research through the Model Context Protocol (MCP).

This listing is a focused entry point for:

- ALKIS cadastral parcels (Flurstücke) from the states' open data: Baden-Württemberg (~9M, LGL) and Berlin (~400k, SenStadt)
- Parcel lookup by Gemeinde (or Berlin Bezirk) and Flurstück number (`Freudenberg 3491/3`), by Gemarkung or address within a Gemeinde, or by coordinates
- Gemarkung, Flur, Gemeinde, Kreis, Lagebezeichnung (address, Baden-Württemberg), tatsächliche Nutzung with areas, and registered area
- Satellite and street map images of a parcel and its neighbours, labelled by Flurstück number

Only Baden-Württemberg and Berlin are loaded so far. Neither state publishes owners.

## Connect

```
https://bumiatlas.com/mcp/germany
```

Add it as a custom connector in any MCP client and sign in with Google. Tools, examples and data notes: [bumiatlas.com/mcp-docs/germany](https://bumiatlas.com/mcp-docs/germany).

- **Claude:** Settings → Connectors → Add custom connector, paste the URL, then Connect.
- **ChatGPT:** Settings → Apps & Connectors → Advanced → Developer mode, then Create with the URL and OAuth authentication.

## Tools

| Tool | Description |
|---|---|
| `DE_parcel_search` | Find Flurstücke by Gemeinde and number, by Gemarkung or address within a Gemeinde, by ALKIS id, or by `latitude, longitude`; each result is the whole record, the boundary as GeoJSON on request |
| `DE_parcel_image` | Satellite or street map image of a parcel or point, with every parcel in view outlined and labelled with its Flurstück number |

## Example prompts

- *"Which parcel is at 49.75154, 9.32471? What is it used for?"*
- *"Look up Flurstück 3491/3 in Freudenberg and show it on satellite imagery."*
- *"Find the parcel at Hauptstraße 219 in Freudenberg."*
- *"Which parcels numbered 513 are there in Berlin-Mitte?"*

## Data source

Flurstücke © LGL Baden-Württemberg (dl-de/by-2-0) and Geoportal Berlin / ALKIS Berlin (dl-de/zero-2.0). A copy of public data for research, not a legal land record.

## Deutsch

Verbinden Sie Ihren KI-Assistenten (Claude, ChatGPT oder Cursor) über das Model Context Protocol (MCP) mit [BumiAtlas](https://bumiatlas.com), um Flurstücke in Deutschland zu recherchieren.

- ALKIS-Flurstücke aus Baden-Württemberg (~9 Mio.) und Berlin (~400.000)
- Suche nach Gemeinde und Flurstücksnummer (`Freudenberg 3491/3`), nach Gemarkung oder Adresse in einer Gemeinde, oder nach Koordinaten
- Tatsächliche Nutzung, Fläche sowie Satelliten- und Straßenkarten eines Flurstücks und seiner Nachbarn

Keine Eigentümerdaten: Beide Länder veröffentlichen keine.

**Verbinden:** Fügen Sie `https://bumiatlas.com/mcp/germany` in einem MCP-Client als Custom Connector hinzu und melden Sie sich mit Google an. Die Tool-Namen sind englisch, der Assistent kann aber auf Deutsch antworten.
