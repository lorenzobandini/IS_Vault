Un evento è un input o una condizione che può causare un cambiamento nello stato del sistema.
Un evento occorre istantaneamente.
Gli eventi che occorrono quando l’oggetto è in uno stato per cui non è prevista alcuna transizione etichettata con quell’evento vengono ignorati.

I tipi di evento sono:
- **Operazione o segnale** (op(a:T)): la transizione è abilitata quando l’oggetto (in quello stato) riceve una chiamata di metodo / un segnale con parametri (a) e tipo (T).
- **Evento di variazione** (when(exp)): la transizione è abilitata appena l’espressione diventa vera ed essa può indicare un tempo assoluto o una condizione.
- **Evento temporale** (after(time)): la transizione è abilitata dopo che l’oggetto è stato fermo "time" in quello stato

