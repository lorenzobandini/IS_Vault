Il design pattern Adapter è un pattern strutturale che consente a interfacce incompatibili di lavorare insieme. Questo pattern consente a classi con interfacce diverse di collaborare, fungendo da ponte tra di loro. L'Adapter traduce un'interfaccia in un'altra, consentendo a oggetti con interfacce incompatibili di comunicare in modo armonioso.

La delega viene utilizzata per vincolare un Adapter a un Adaptee. L'ereditarietà dell'interfaccia viene utilizzata per specificare l'interfaccia della classe Adapter. Target e Adaptee (generalmente chiamato sistema legacy) esistono prima dell'Adapter. Il Target può essere realizzato come un'interfaccia in Java.

Differenza tra Adaptee e Adapter:
- L'Adaptee è un termine utilizzato per indicare la classe o l'oggetto esistente, la cui interfaccia potrebbe non essere compatibile con ciò che il client richiede.
- L'Adapter, d'altra parte, è la classe che implementa l'interfaccia richiesta dal client e "adatta" l'interfaccia dell'Adaptee a quella del Target (l'interfaccia desiderata dal client). L'Adapter agisce come uno strato intermedio che consente la collaborazione tra il client e l'Adaptee

La struttura è

![[Pasted image 20231120110332.png]]

I partecipanti sono:
- Target: Definisce l'interfaccia specifica dell'applicazione che i client utilizzano.
- Client: Collabora con gli oggetti conformi all'interfaccia del target.
- Adaptee: Definisce un'interfaccia esistente che necessita di adattamento.
- Adapter: Adatta l'interfaccia dell'Adaptee all'interfaccia del target.

L'Adapter può svolgere il ruolo di una strategia concreta: se abbiamo diversi moduli che implementano la stessa funzionalità e abbiamo scritto adattatori per essi, otteniamo un insieme di adattatori che implementano la stessa interfaccia. Possiamo quindi sostituire gli oggetti adattatori durante l'esecuzione.

Il Façade è un altro [[GoF]] pattern che inoltra le richieste a molti Adaptee.