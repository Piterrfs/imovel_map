# imovel_map

Projeto do mapa `mapa_calor_valor_m2_leaflet.html` (Leaflet) para visualizar **R$/mÂ²** (ou outras mÃ©tricas do CSV) por **bairro** e por **logradouro** (OSM/Overpass).

## Como rodar local

No Windows (PowerShell), dentro desta pasta:

```powershell
python -m http.server 8010
```

Abra no navegador:

- `http://localhost:8010/mapa_calor_valor_m2_leaflet.html`

## Arquivos

- `mapa_calor_valor_m2_leaflet.html`: app (Leaflet) com camadas/controles.
- `itbi_valor_m2.csv`: dados base (inclui coluna `R$/mÂ²`).
- `rj_bairros_2022.geojson`: limites de bairros.

## ObservaÃ§Ãµes

- A camada "Logradouros (OSM)" baixa vias sob demanda (zoom â‰¥ 13) usando Overpass (sem API key).
