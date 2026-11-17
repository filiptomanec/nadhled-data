# Nadhled – data

Data, která čte web [Nadhled](https://www.nadhled-lokalit.cz) za běhu. Soubory leží v GitHub Releases, ne v gitu:

| Release (tag) | Obsah | Vyrábí |
| --- | --- | --- |
| `uzemni-plan` | stav územních plánů obcí (`obce.json`) a plochy obcí (`plochy__<kód>-<hash>.json`) | `scripts/uzemni_plany.py`, měsíčně |
| `osm` | výběr z OpenStreetMap: vybavenost, parky, trasy (`index.json`, `balik__*.bin`) | `scripts/osm.py`, týdně |

Lomítko v cestě souboru je v názvu nahrazené `__` (`plochy/123-ab.json` → `plochy__123-ab.json`).
Soubory s hashem v názvu se nemění, indexy (`obce.json`, `index.json`) se přepisují.

## Zdroje a licence

- **OpenStreetMap:** © přispěvatelé OpenStreetMap, data pod licencí [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/), výřez Česka od [Geofabriku](https://download.geofabrik.de/).
- **Územní plány:** Národní geoportál územního plánování (Ministerstvo pro místní rozvoj) a krajské portály, převedeno do WGS 84.

Repozitář plní automaticky GitHub Actions projektu Nadhled; ručně do něj nic nepřidávej.
