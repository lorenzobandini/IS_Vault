Il design pattern comportamentale State ha l'intento di dare la possibilità ad un oggetto di alterare il suo comportamento quando il suo stato interno cambia. L'oggetto sembrerà cambiare la sua classe.

Un esempio si ah nelle connessioni TCP nelle quali si risponde differentemente al client in base allo stato.

La struttura è:

![[Pasted image 20231113124901.png]]

E i partecipanti sono:
- State: Definisce un'interfaccia per incapsulare il comportamento associato a un particolare stato del contesto. Può anche essere una classe concreta con un'implementazione predefinita
- Context: Definisce un'interfaccia di interesse per i client. Mantiene un'istanza di ConcreateState che definisce lo stato corrente
- ConcreteState: Ogni sottoclasse implementa un comportamento associato ad uno stato del contesto

Il passaggio da uno stato all'altro avviene tramite transizioni. Queste possono essere gestite all'interno del contesto o dagli oggetti stato stessi.

Il design pattern State potrebbe gestire queste transizioni di stato e i comportamenti associati a ciascuno stato, rendendo il codice più modulare e flessibile.

Usiamo lo State pattern nei seguenti casi:
- Il comportamento di un oggetto dipende dal suo stato e deve cambiare il suo comportamento a run-time in base a tale stato.
- Le operazioni hanno dichiarazioni condizionali complesse che dipendono dallo stato dell'oggetto

I passi per applicare questo pattern sono:
1. Identificare una classe esistente o crearne una nuova che funga da "macchina a stati" dal punto di vista del cliente. Questa classe è la classe"Context".
2. Creare una classe base State che replichi i metodi dell'interfaccia della macchina a stati. Ogni metodo richiede un parametro aggiuntivo: un'istanza della classe Context. La classe State specifica qualsiasi comportamento utile "predefinito".
3. Creare una classe derivata State per ogni stato del dominio. Queste classi derivate sovrascrivono solo i metodi che devono sovrascrivere.
4. La classe Context mantiene un oggetto State "corrente".
5. Tutte le richieste del client alla classe Context sono semplicemente delegato all'oggetto State corrente e viene passato il puntatore this dell'oggetto Context.
6. I metodi State modificano lo stato "corrente" dell'oggetto Context, come specificato.

State localizza il comportamento che dipende dallo stato e lo suddivide tra i diversi stati.
Tutti i comportamenti specifici di uno stato sono memorizzati in una classe.
L'alternativa è costituita da case statement giganti e perciò rimane la soluzione migliore produrre un gran numero di classi.
Le transizioni di stato sono esplicite e lo stato corrente è memorizzato in un'unica posizione. Gli oggetti State possono essere condivisi quando non hanno variabili di istanza.

La differenza con [[Strategy]] sta nell'intento poiché, pur essendo esempi di composizione con delega, un oggetto State incapsula un comportamento dipendente dallo stato mentre un oggetto Strategy incapsula un algoritmo.