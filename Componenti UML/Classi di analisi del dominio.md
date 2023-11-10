Corrispondono a concetti concreti del dominio che servono per evitare di introdurre classi di progettazione.

Hanno come caratteristiche di:
- astrarre uno specifico elemento del dominio
- avere un numero ridotto di responsabilità
- evitano di definire classi "onnipotenti"
- evitano funzioni travestite da classi
- evitano gerarchie di eredità profonde (>=3)

Operazioni e attributi solo quando veramente utili
- Le classi di analisi dovrebbero contenere attributi e operazioni ad "alto livello"
- Limitare la specifica di tipi, valori, etc...
- Non inventare mai niente rispetto a quanto scritto nel documento

Per individuarle non esistono metodi automatici ma possiamo usare alcune tecniche note:
- Approccio **Data Driven**: tipico della fase di analisi, si identificano tutti i dati del sistema e si dividono in classi
- Approccio **Responsability Driven**: soprattutto durante la progettazione, si identificano le responsabilità e si dividono le classi


