# Cost Management — Dealer E2K

Calcolatore costi/produzione per dealer Euroelettronica 2000 con logica Multibrand
aggiornata mensilmente in base alla gara ufficiale.

**Live:** https://costmanagement-seven.vercel.app/

## Stato gara

Aggiornato a **Maggio 2026** secondo la gara ufficiale E2K.

## Funzionalità

- Selezione brand attivi: ACEA, SKY, FASTWEB (+HO opzionale), TISCALI, EFFICIENCY, RENT.
- Configurazione percentuali di produzione personalizzate per ogni brand virtuale
  (FW Sim / Fisso / Energia separate, Tiscali Sim / Fisso separate).
- Calcolo automatico della combinazione ottimale di contratti per coprire i costi
  + marginalità desiderata, rispettando i vincoli di brand Multibrand e i punti minimi.
- Output WhatsApp + esportazione **PDF professionale** con font Montserrat.
- Nota convergenze (+10€ → +40€) sempre evidenziata nel risultato.

## Deploy

Il file `cost aprile MODIFICA FASTWEB TELCO.html` è il sorgente unico.
Per il deploy su Vercel viene rinominato come `index.html`.

## Note implementative

- Tutto il calcolo è in JavaScript vanilla, nessuna dipendenza esterna a runtime.
- DP con pruning per la ricerca combinatoria multivariate.
- Bonus Protect FW (+15€/SIM) **non incluso** nei calcoli da Maggio 2026 — va
  aggiunto manualmente solo per le SIM con Protect effettivamente venduto.
