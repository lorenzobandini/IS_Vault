Il Single Responsibility Principle fu introdotto da Tom DeMarco nel suo libro Structured Analysis and Systems Specification, 1979.

Una classe, un modulo o un metodo dovrebbe avere solo un motivo per cambiare. La responsabilità è identificata come un motivo per cambiare.

Questo principio afferma che se abbiamo 2 motivi per cambiare una classe, dobbiamo dividere la classe in due classi così che se in futuro abbiamo bisogno di fare un cambiamento, lo facciamo nella classe che realizza la funzionalità. Se dovessimo fare un cambiamento in una classe che ha più responsabilità, le modifiche potrebbero influenzare altre funzionalità della classe e a cascata tutti i moduli che le usano.

Robert Martin ha reinterpretato il concetto e definito la responsabilità come “un motivo per cambiare”.

E’ un altro modo per dire che una classe deve essere funzionalmente coesa

Un eccezione alla regola si ha quando non si può cambiare una delle due responsabilità dell'applicazione senza cambiare contestualmente anche l'altra. Allora separarle introdurrebbe solamente una complessità non necessaria.