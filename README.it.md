# Mobilità Urbana a Buenos Aires: Analisi con R e Tableau (Ecobici 2024)

*Disponibile in: 🇬🇧 English → [README.md](README.md) | 🇪🇸 Español → [README.es.md](README.es.md) | 🇮🇹 Italiano (questo file)*

![R](https://img.shields.io/badge/R-4.3-blue?logo=r&logoColor=white)
![RMarkdown](https://img.shields.io/badge/RMarkdown-Reporting-2c3e50?logo=rmarkdown&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Questo progetto analizza oltre 3.2 milioni di viaggi del sistema di bike-sharing pubblico Ecobici di Buenos Aires nel 2024 per scoprire pattern di utilizzo, picchi di domanda, stazioni popolari e opportunità per migliorare la mobilità urbana sostenibile.


## Principali Risultati

- Forte focus sul commuting: picco serale (16–18, fino a 308k viaggi/ora) e picco mattutino secondario (7–10).  
- Media nei giorni feriali ~10.724 viaggi/giorno vs ~4.081 nei fine settimana (rapporto ~2.6:1).  
- Stazioni di origine top (Constitución 35k, Pacífico 34k) e heatmaps spaziali mostrano domanda concentrata in aree centrali (Microcentro, Palermo, Recoleta).  
- Origini mattutini si raggruppano in zone residenziali/centrali, destinazioni serali si disperdono, confermando commuting bidirezionale.  
- Durata dei viaggi: mediana ~16.1 min, media ~21.7 min — la maggior parte sotto 30 min.  
- Distribuzione per genere: Maschile ~60.8%, Femminile ~31.6%.  
- Picchi stagionali in tarda primavera/inizio estate (ottobre 335k), minimo in inverno (luglio 215k).  
- Flussi netti estremi (es. Juan Manuel De Blanes +3.056, Cerrito -2.064) evidenziano necessità di riequilibrio.


## Dashboard Interattivo

Esplora il dataset completo in modo interattivo su Tableau Public:  
[Visualizza il Dashboard Ecobici 2024](https://public.tableau.com/views/Ecobici2024-InteractiveUrbanBike-SharingInsights/Ecobici2024-UrbanBike-SharingInsights?:language=es-ES&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## Report HTML Completo

**Report HTML Completo** (con heatmaps interattivi):  
[Apri il Report Online](https://www.emilionahuelpattini.com/it/data/data-analysis/projects/ecobici-2024/urban-mobility-analysis.html) (Versione interattiva con zoom, pan e tooltip. Nessun download necessario.)  

**Alternativa (download offline)**: Scarica lo ZIP del repository e apri `outputs/urban-mobility-analysis.html` (richiede la cartella `outputs/urban-mobility-analysis_files/`).

**Report PDF Completo** (versione stampabile):

[Scarica Report PDF](https://www.emilionahuelpattini.com/it/data/data-analysis/projects/ecobici-2024/urban-mobility-analysis.pdf)  
(Report completo con tutti i visual e insights — versione statica, ~12 pagine)


## Competenze Dimostrate

- Pulizia e preparazione dati (R, tidyverse, lubridate)  
- Analisi Esplorativa dei Dati (temporale, spaziale, demografica)  
- Visualizzazione: ggplot2, leaflet (heatmaps interattivi), Tableau  
- Insights e raccomandazioni actionable per il business  
- Riproducibilità e documentazione


## Fonte dei Dati

Portale ufficiale dei dati aperti di Buenos Aires (pubblico e gratuito):  

- Dati grezzi: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas (scarica "ecobici_recorridos_realizados_2024.csv")  
- Dati elaborati: Il CSV pulito (trips_clean_2024.csv) non è incluso per limiti di dimensione di GitHub (>100 MB). Puoi ricrearlo eseguendo il report R Markdown (urban-mobility-analysis.Rmd) o richiedimelo.


## Come Riprodurre

1. Clona questo repository.
2. **Scarica i dati grezzi** (non inclusi per dimensione):  
   Dalla fonte ufficiale: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas  
   Scarica "ecobici_recorridos_realizados_2024.csv" e posizionalo in `data/raw/`.
3. Apri `urban-mobility-analysis.Rmd` in RStudio.
4. Installa i pacchetti necessari (una sola volta):  
   ```r
   install.packages(c("tidyverse", "lubridate", "scales", "leaflet", "leaflet.extras", "here"))
   ```
5. Knit per generare il report (HTML/PDF).
6. Tableau: Importa data/processed/trips_clean_2024.csv per ricreare o esplorare i visual interattivi (heatmaps, peak hours, ecc.).
