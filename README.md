# Weather MCP Server

[![smithery badge](https://smithery.ai/badge/@HugoGuedesipvc/ao-generativeai-cp3)](https://smithery.ai/server/@HugoGuedesipvc/ao-generativeai-cp3)

Servidor MCP para previsão meteorológica, riscos e avisos em Portugal, usando dados do IPMA.

## Tecnologias Utilizadas

- **Python 3.11+**
- **httpx** (HTTP client assíncrono)
- **uv** (Python package and project manager)
- **FastMCP** (framework MCP)
- **IPMA Open Data API** (dados meteorológicos oficiais)

## Endpoints MCP Disponíveis

Cada função decorada com `@mcp.tool()` é um endpoint MCP:

- **get_forecast(city: str)**  
  Previsão meteorológica para 5 dias para uma cidade portuguesa.  
  _Exemplo de uso:_ `get_forecast("Lisboa")`

- **weather_warnings()**  
  Avisos meteorológicos ativos para Portugal (até 3 dias).

- **get_sea_forecast(day: int = 0)**  
  Previsão do estado do mar para zonas costeiras portuguesas.  
  _Parâmetro:_ `day` (0=hoje, 1=amanhã, 2=depois de amanhã)

- **get_earthquakes(area: int = 7)**  
  Informação sobre sismos recentes.  
  _Parâmetro:_ `area` (3=Açores, 7=Continente+Madeira)

- **get_fire_risk_forecast(day: int = 1)**  
  Previsão de risco de incêndio para Portugal.  
  _Parâmetro:_ `day` (1=hoje, 2=amanhã)

- **uv_forecast()**  
  Previsão do índice ultravioleta (UV) para os próximos 3 dias.
