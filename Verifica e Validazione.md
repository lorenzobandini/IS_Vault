Il problema della verifica di correttezza è difficile e non esiste un algoritmo che lo risolva.
Nel 1937 Alan Turing dimostrò che alcuni problemi non possono essere risolti da un algoritmo e che tali problemi coinvolgono il [[Problema della Terminazione]].

Esistono programmi che è possibile dimostrare corretti in tempo finito ma ne esistono altri per cui ciò non è possibile.
Quindi non esiste alcun programma P che prende in input altri programmi e per ognuno di questi decide in tempo finito se è corretto o meno infatti non esiste un algoritmo che per ogni formula F in logica al primo ordine mi permetta di decidere in tempo finito se F è valida o meno ma esiste solo una formula che mi enumeri tutte le formule valide ma non è possibile in tempo finito arrivare a scrivere se F è valida o meno.

Il software ha alcune caratteristiche che rendono la validazione e verifica particolarmente difficile:
- Requisiti di qualità diversi
- Il software è sempre in evoluzione
- Distribuzione irregolare dei guasti
- Non linearità
- Nuovi approcci di sviluppo possono introdurre nuovi tipi di errori come deadlock o race conditions per software distribuito o problemi di polimorfismo o binding dinamico in software object-oriented

I progettisti nella fase di verifica devono scegliere e programmare la giusta combinazione di tecniche per raggiungere il livello richiesto di qualità entro i limiti di costo e progettare una soluzione specifica che si adatti al problema, ai requisiti e all'ambiente di sviluppo senza poter contare su "ricette fisse".

Le 5 Domande da usare come guida sono:
1. [[Quando iniziare verifica e convalida e quando sono complete]]
2. [[Quali tecniche applicare]]
3. [[Come possiamo valutare se un prodotto è pronto per essere rilasciato]]
4. [[Come possiamo controllare la qualità delle relase successive]]
5. [[Come può essere migliorato il processo di sviluppo]]

La differenza tra Convalida e Verifica è che nella convalida ci chiediamo se stiamo costruendo il sistema che serve all'utente mentre nella verifica ci chiediamo se stiamo costruendo un sistema che rispetta le specifiche.

![[Pasted image 20231122184717.png]]

Alcune terminologie IEEE che possiamo trovare in questa fase sono:
- Malfunzionamento: il sistema software a tempo di esecuzione non si comporta secondo le specifiche oppure c'è un malfunzionamento di natura dinamica visibile solo mediante esecuzione causato da un difetto
- Difetto: è un difetto del codice cioè della struttura statica del programma e viene corretto con debug. Può essere latente se causa un malfunzionamento.
- Errore: è la causa di un difetto ed è l'incomprensione umana nel tentativo di comprendere o risolvere un problema o nell'uso di strumenti

Il testing è una tecnica di verifica ed è come le altre sottoposta al problema dell'indecidibilità. Una prova formale di correttezza corrisponde all'esecuzione del sistema con tutti i possibili input mentre un testing esaustivo è eseguire e provare ogni possibile input del programma ma ciò richiederebbe tempo infinito se gli input sono infiniti.
Perciò il test di un programma può rilevare la presenza di difetti ma non dimostrarne l'assenza.

Per controllare gli errori utilizziamo delle tecniche di verifica che possono essere:
- [[Verifica Statica]]
- [[Verifica Dinamica]]