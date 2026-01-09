# imovel_map

Projeto do mapa `mapa_calor_valor_m2_leaflet.html` (Leaflet) para visualizar **R$/m²** (ou outras métricas do CSV) por **bairro** e por **logradouro** (OSM/Overpass).

## Filtros (uso e tipologias)

O mapa permite filtrar os dados do CSV por:

- **Uso do imóvel**: `RESIDENCIAL` e `NÃO RESIDENCIAL` (tratado como “Comercial” no filtro).
- **Tipologias**: lista carregada automaticamente a partir da coluna `principais_tipologias`.

Ao aplicar filtros, o mapa recalcula as médias e **atualiza cores e valores**.

## Como rodar local

No Windows (PowerShell), dentro desta pasta:

```powershell
python -m http.server 8010
```

Abra no navegador:

- `http://localhost:8010/mapa_calor_valor_m2_leaflet.html`

## Arquivos

- `mapa_calor_valor_m2_leaflet.html`: app (Leaflet) com camadas/controles.
- `ITBI_transacoes_logradouro_mes.csv`: base de transações com colunas como `uso`, `principais_tipologias`, `bairro`, `logradouro`, `R$/m²`, `média_valor_imóvel` etc.
- `itbi_valor_m2.csv`: base anterior (mantida por compatibilidade/histórico; inclui coluna `R$/m²`).
- `rj_bairros_2022.geojson`: limites de bairros.

## Observações

- A camada "Logradouros (OSM)" baixa vias sob demanda (zoom ≥ 13) usando Overpass (sem API key).
