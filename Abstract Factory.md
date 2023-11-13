Quando si parla di Abstract Factory, ci si riferisce a una situazione in cui i pattern di creazione degli oggetti si concentrano sulla delega dell'istruzione di creazione a un altro oggetto.

L'Abstract Factory fornisce un'interfaccia per creare famiglie di oggetti correlati o dipendenti senza specificare le classi concrete.

Rispetto al Factory Method, nell'Abstract Factory pattern, una classe delega la responsabilità dell'istanziazione degli oggetti a un altro oggetto tramite composizione, mentre il Factory Method utilizza l'ereditarietà e si affida a una sottoclasse per gestire l'istanziazione dell'oggetto desiderato.

In pratica, l'oggetto delegato nell'Abstract Factory utilizza spesso metodi di fabbrica per eseguire l'istanziazione, combinando entrambi i pattern.

La sua struttura è:

![[Pasted image 20231113164406.png]]

