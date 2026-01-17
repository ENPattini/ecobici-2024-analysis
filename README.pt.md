# Mobilidade Urbana em Buenos Aires: Análise com R e Tableau (Ecobici 2024)

Este projeto analisa mais de 3.2 milhões de viagens do sistema público de bicicletas Ecobici em Buenos Aires em 2024 para descobrir padrões de uso, picos de demanda, estações populares e oportunidades para melhorar a mobilidade urbana sustentável.


## Principais Descobertas

- Forte foco em commuting: pico vespertino (16–18 hs, até 308k viagens/hora) e pico matutino secundário (7–10 AM).  
- Média em dias úteis ~10.724 viagens/dia vs ~4.081 nos fins de semana (razão ~2.6:1).  
- Estações de origem top (Constitución 35k, Pacífico 34k) e heatmaps espaciais mostram demanda concentrada em áreas centrais (Microcentro, Palermo, Recoleta).  
- Origens matutinas se agrupam em zonas residenciais/centrais, destinos vespertinos se dispersam, confirmando commuting bidirecional.  
- Duração dos viagens: mediana ~16.1 min, média ~21.7 min — maioria abaixo de 30 min.  
- Distribuição por gênero: Masculino ~60.8%, Feminino ~31.6%.  
- Picos sazonais na primavera tardia/início de verão (outubro 335k), mínimo no inverno (julho 215k).  
- Fluxos netos extremos (ex. Juan Manuel De Blanes +3.056, Cerrito -2.064) destacam necessidades de rebalanceamento.


## Dashboard Interativo

Explore o dataset completo de forma interativa no Tableau Public:  
[Visualizar o Dashboard Ecobici 2024](https://public.tableau.com/views/Ecobici2024-InteractiveUrbanBike-SharingInsights/Ecobici2024-UrbanBike-SharingInsights?:language=es-ES&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## Relatório HTML Completo

**Relatório HTML Completo** (com heatmaps interativos):  
[Abrir o Relatório Online](https://www.emilionahuelpattini.com/projects/ecobici-2024/urban-mobility-analysis.html) (Versão interativa com zoom, pan e tooltips. Sem necessidade de download.)  

**Alternativa (download offline)**: Baixe o ZIP do repositório e abra `outputs/urban-mobility-analysis.html` (requer a pasta `outputs/urban-mobility-analysis_files/`).

**Relatório PDF Completo** (versão imprimível):  

[Baixar Relatório PDF](https://www.emilionahuelpattini.com/projects/ecobici-2024/urban-mobility-analysis.pdf)  
(Relatório completo com todos os visuais e insights — versão estática, ~12 páginas)


## Habilidades Demonstradas

- Limpeza e preparação de dados (R, tidyverse, lubridate)  
- Análise Exploratória de Dados (temporal, espacial, demográfica)  
- Visualização: ggplot2, leaflet (heatmaps interativos), Tableau  
- Insights e recomendações acionáveis para o negócio  
- Reprodutibilidade e documentação


## Fonte de Dados

Portal oficial de dados abertos de Buenos Aires (público e gratuito): 

- Dados brutos: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas (baixar "ecobici_recorridos_realizados_2024.csv")  
- Dados processados: O CSV limpo (trips_clean_2024.csv) não está incluído devido aos limites de tamanho do GitHub (>100 MB). Você pode recriá-lo executando o relatório R Markdown (urban-mobility-analysis.Rmd) ou pedir para mim.


## Como Reproduzir

1. Clone este repositório.
2. **Baixe os dados brutos** (não incluídos por tamanho):  
   Da fonte oficial: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas  
   Baixe "ecobici_recorridos_realizados_2024.csv" e coloque em `data/raw/`.
3. Abra `urban-mobility-analysis.Rmd` no RStudio.  
4. Instale os pacotes necessários (uma vez só):  
   ```r
   install.packages(c("tidyverse", "lubridate", "scales", "leaflet", "leaflet.extras", "here"))
   ```
5. Knit para gerar o relatório (HTML/PDF).
6. Tableau: Importe data/processed/trips_clean_2024.csv para recriar ou explorar os visuais interativos (heatmaps, peak hours, etc.).
