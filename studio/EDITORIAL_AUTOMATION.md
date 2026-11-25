# Automazione editoriale IU
Impostazione concordata il 2026-11-25: progetto individuale sostenibile, non orientato alla monetizzazione immediata. Automatizzare il lavoro meccanico, non il giudizio umano.
## Flusso
1. Raccolta periodica via API e RSS, scraper solo se consentiti e necessari. Conservare URL, data, provenienza, tipo di fonte e limiti di accesso.
2. Java normalizza, deduplica, filtra date, domini e pertinenza prima di spendere token.
3. AI economica valuta pertinenza, qualità apparente delle evidenze, sintesi, contraddizioni e affermazioni da verificare. Scarta o inoltra con motivazione; archivia gli scarti recuperabili. Nessuna certificazione automatica di verità.
4. Dashboard privata, utilizzabile da telefono: revisione delle fonti, approvazione o rifiuto umano.
5. Argomenti approvati nel backlog editoriale (non pubblicati); selezione successiva, anche circa cinque candidati per formato.
6. Su richiesta genera articolo, carosello, post statico, scaletta video, storyboard e istruzioni grafiche a partire dalla stessa ricerca.
7. Revisione finale di fatti, citazioni, grafica, licenze e testo; solo dopo approvazione programmare o pubblicare.
8. Sito pubblico come archivio autorevole dei contenuti pubblicati; social come distribuzione e newsletter come riepilogo.
## Fonti candidate
arXiv, OpenAlex, Crossref, PubMed, Hacker News, GitHub, NASA, CERN, OpenAI Research, Google DeepMind. Verificare API, RSS, licenze, limiti e costi prima dell'integrazione. Preprint distinti da studi peer reviewed; comunicati aziendali e social sono piste, non prove indipendenti. Avviare con 3–5 fonti.
## AI
Spring AI è integrazione con provider, non modello. Tre livelli: filtri deterministici, modello economico per screening, modello più capace solo per approfondimenti selezionati. Risposta strutturata JSON: titolo, categoria, rilevanza, qualità apparente evidenze, tipo fonte, sintesi, limiti, claimsToVerify, sources, suggestedFormats, status. Punteggi non probabilità di verità. URL e citazioni verificabili, non inventati; contenuti esterni trattati come dati non fidati, non istruzioni.
## Moduli candidati
Source Manager, Research Engine, AI Gateway (provider, token, budget, fallback), Editorial Manager, Content Generator, Media Engine, Publishing Manager, Newsletter Manager. Monolite modulare iniziale, non microservizi.
## MVP
Raccogliere da 3–5 fonti, deduplicare, analizzare con AI, mostrare motivazioni e fonti, approvare/scartare, salvare backlog. Testare errori provider, duplicati, risposte invalide, limiti di spesa e blocco pubblicazione senza approvazione. Poi bozze articolo e carosello; sito, video e newsletter dopo. Nessun codice implementato.
## Frequenza
Ricerca quotidiana proposta; pubblicazione sostenibile ogni tre giorni circa oppure settimanale, senza obbligo quotidiano. Partenza suggerita: un articolo e carosello a settimana, video quando pipeline pronta. Newsletter settimanale proposta, solo contenuti pubblicati.
