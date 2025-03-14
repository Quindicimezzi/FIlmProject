﻿# FIlm Project

### Spiegazione del README:

- **Titolo e Descrizione**: panoramica generale del progetto.
- **Fasi dell'analisi**: ogni fase importante dell'analisi dei dati è descritta separatamente, compresi gli obiettivi e le operazioni eseguite.
- **Tecnologie utilizzate**: viene specificato che strumenti e librerie sono stati usati (Python, Pandas, Matplotlib, Plotly, etc.).
- **Come eseguire il codice**: guida per l'utente su come clonare il repository, installare le dipendenze e eseguire il codice.
- **Licenza e contatti**: informazioni sulla licenza e su come mettersi in contatto.



# Analisi dei Dati dei Film

Questo progetto si concentra sull'analisi dei dati relativi ai film, esplorando vari aspetti come la valutazione IMDB, i guadagni al botteghino (Gross) e il coinvolgimento dei registi. L'analisi è stata condotta su un dataset contenente informazioni sui film, tra cui registi, attori, rating IMDB, e guadagni. Sono stati applicati filtri, raggruppamenti e visualizzazioni per ottenere informazioni interessanti sui trend e sui migliori registi.

## Descrizione dell'analisi

L'analisi è suddivisa in diverse fasi:

### 1. **Preparazione dei Dati**
   - **Filtraggio dei film con 'Runtime' inferiore a 130 minuti.**
   - **Pulizia dei dati**: i valori NaN nel rating IMDB sono stati sostituiti con `0` e le virgole nei valori di rating sono state sostituite con punti per facilitare la conversione in numeri decimali.
   - **Calcolo della somma e della media dei guadagni (`Gross`)** per ciascun regista nel set di dati filtrato.
   - **Calcolo della media del rating IMDB** per ciascun regista.

### 2. **Classifica dei Registi**
   - Viene calcolata la **media del rating IMDB per ogni regista**, ordinata in ordine decrescente, per ottenere i registi con i migliori rating medi.
   - Il ciclo `for` è stato utilizzato per stampare in modo automatizzato i registi con le migliori medie di rating.

### 3. **Unione dei Dati**
   - È stato eseguito un **merge** tra la classifica dei registi per media rating e quella per guadagni medi (`Gross`), al fine di ottenere un confronto tra i registi più apprezzati dal pubblico e quelli che hanno ottenuto i migliori guadagni.
   - I dati sono stati uniti utilizzando un **inner join**, mostrando solo i registi che si trovano in entrambe le classifiche.

### 4. **Analisi e Pivot**
   - **Pivot Table** sono state utilizzate per eseguire un'analisi comparativa dei guadagni e dei rating IMDB per ciascun regista.
   - Sono stati creati più pivot, tra cui:
     - Un pivot che calcola la media del rating IMDB e la somma dei guadagni (`Gross`).
     - Un pivot che visualizza solo la somma dei guadagni medi per ogni regista, ordinati in modo decrescente.

### 5. **Filtraggio per Attori e Registi**
   - È stato applicato un filtro per cercare i film in cui **Morgan Freeman** appare in uno qualsiasi dei ruoli principali (Star1, Star2, Star3).
   - I risultati sono stati concatenati per includere Morgan Freeman in qualsiasi ruolo, mostrando i film in cui ha partecipato.

### 6. **Visualizzazioni**
   - **Grafico a torta** per visualizzare i guadagni dei primi sei registi nel dataset.
   - **Grafico a barre interattivo** che mostra gli **incassi totali per ciascun film**.
   - Un altro **grafico a barre interattivo** visualizza il **rating medio per regista** per i registi con un rating IMDB superiore a 8.5.
   - Infine, un **grafico a barre** che mostra gli **incassi totali per regista**, con un filtro che consente all'utente di selezionare un valore minimo di 
     guadagni (`Gross`).

## Tecnologie Utilizzate

- **Python**: Linguaggio di programmazione utilizzato per l'analisi dei dati.
- **Pandas**: Utilizzato per la manipolazione e l'analisi dei dati.
- **Matplotlib & Plotly**: Utilizzati per creare visualizzazioni interattive e grafici.
- **Jupyter Notebook**: Ambiente interattivo per eseguire il codice e presentare i risultati in modo visivo.

