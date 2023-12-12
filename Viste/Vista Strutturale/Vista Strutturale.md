Descrive la struttura del sistema come insieme di unità di realizzazione (Classi, packages...) e serve per:
- Analizzare le dipendenze tra packages
- Progettare testi di unità e di intergrazione
- Valutare la portabilità

Gli elementi o nodi del diagramma sono i **moduli**, unità software che realizzano un insieme coerente di responsabilità.
Le relazioni tra elementi sono: **"parte di"**, **"eredita da"**, **" dipende da"**, **"può usare"**

Servono per:
- Costruzione: la vista può fornire lo schema del codice e directory e file sorgente hanno una struttura corrispondente
- Analisi: tracciabilità dei requisiti e analisi d'impatto per valutare eventuali modifiche
- Comunicazione: se la vista è gerarchica, offre una presentazione top-down della suddivisione delle responsabilità nel sistema ai novizi
- Progettazione dei test di unità e di integrazione

Non sono utili invece per analisi dinamiche, fatte invece con [[Vista Comportamentale (C&C)]] e [[Vista Logistica]].

Nella vista strutturale in [[UML]] utilizziamo:
- Le classi sono rappresentate dando più specifica delle operazioni.

![[Pasted image 20231108175739.png]]

- I packages rappresentati come:

![[Pasted image 20231108175804.png]]

- Relazioni tra classi, tra packages e tra classi e packages

Le possibili viste sono:
- [[Vista Strutturale di Decomposizione]]
- [[Vista Strutturale d'Uso]]
- [[Vista Strutturale a Strati]]
- [[Vista Strutturale di Generalizzazione]]

