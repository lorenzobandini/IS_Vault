Il design pattern comportamentale State ha l'intento di dare la possibilità ad un oggetto di alterare il suo comportamento quando il suo stato interno cambia. L'oggetto sembrerà cambiare la sua classe.

Un esempio si ah nelle connessioni TCP nelle quali si risponde differentemente al client in base allo stato.

La struttura è:

![[Pasted image 20231113124901.png]]

E i partecipanti sono:
- State: Definisce un'interfaccia per incapsulare il comportamento associato a un particolare stato del contesto. Può anche essere una classe concreta con un'implementazione predefinita
- Context: Definisce un'interfaccia di interesse per i client. Mantiene un'istanza di ConcreateState che definisce lo stato corrente
- ConcreteState: Ogni sottoclasse implementa un comportamento associato ad uno stato del contesto

