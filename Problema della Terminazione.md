> "Esiste un algoritmo che presi in ingresso un qualsiasi altro programma e un input stabilisca se il programma su tale input termina o no?"

Si assuma che esista un programma C che prende in input un programma (a) e un input per a (d).
```C
boolean C(a,d) {return halts(a(d))}
```
Dato che un programma è a sua volta una sequenza di caratteri, si può invocare `C(a,a)`.
Si può quindi definire `K(a)` come segue:

```C
boolean K(a){
	if C(a,a) while (true){skip};
	else return false;
}
```
Il programma K con input K termina?
Il programma K con input K termina, (restituendo il valore false) se e solo se `C(K,K)` è falso, ma `C(K,K)` è falso solo se `halts(K(K))` è falso, vale a dire se il programma K con input K non termina.
`K(K)` termina se e solo se `K(K)` non termina e questa è una contraddizione.
Perciò non può esistere un programma C che prende in input un programma e un input e dica se termina o no.