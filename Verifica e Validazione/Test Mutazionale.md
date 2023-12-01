Metodo di test strutturale volto a valutare/migliorare l'adeguatezza della suite di test e a stimare il numero di difetti nei sistemi sotto test.

La precondizione è aver esercitato un programma $P$ su una batteria di test $T$, e aver verificato $P$ corretto rispetto a $T$.
Si vuole fare una verifica più profonda sulla correttezza di $P$ introducendo dei difetti piccoli dette mutazioni su $P$ e chiamiamo il programma modificato $P'$.
Si eseguono su $P'$ gli stessi test di $T$.
Il test dovrebbe manifestare dei malfunzionamenti:
- Se il test non rileva questi difetti, allora significa che la batteria di test non era abbastanza buona
- Se li rileva, abbiamo una maggior fiducia sulla batteria di test

Si dice che $T$ uccide il mutante $P_j$ se rileva un malfunzionamento.

L'efficacia di un test è uguale a $\frac{\text{Mutanti Uccisi}}{\text{Numero Mutanti}}$

Un mutante sopravvive a una test suite se per tutti i test case della suite non si distingue l'esito del test se eseguito sul programma originale o su quello mutante.

Un mutante è invalido se non è sintatticamente corretto, cioè se non passa la compilazione, è valido altrimenti.
Un mutante è utile se è valido e se non è facile distinguerlo dal programma originale.
Un mutante è inutile se è ucciso da quasi tutti i casi di test.