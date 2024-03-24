# Note da lezioni di Gregoratti

## Variabili Aleatorie 1

Il codominio di X si dice "insieme degli stati", in quanto contiene l'insieme di valori che può assumere X. In altri termini, se alla fine di un esperimento, noi abbiamo accesso al solo valore di X e non alla conoscenza degli esiti dell'esperimento, gli "stati" sono tutte le immagini che potremo visualizzare. 

Lavorando con X, e cioè studiando una quantità (actually, uno "stato") calcolata dall'esito, diventa immediato porsi domande non sugli esiti, quando invece sugli stati. In altri termini, la domanda "tipo" diventa da "dopo il lancio di 2 dadi, è uscito l'esito (3,4)" a "dopo il lancio di due dadi, la somma degli esiti è 7". Gli eventi del secondo genere si rappresentano naturalmente con le controimmagini, per esempio
$$
\{ X = x_0 \} \qquad \text{oppure} \qquad \{ X \in A_0 \}.
$$
Quindi, avendo accesso ai soli stati e non agli esiti, uno si pone domande (== cerca di fare previsioni) sugli stati, per cui è naturale lavorare con le controimmagini.

Il motivo per cui non chiediamo tutte le controimmagini è che bastano quelle corrispondenti a domande, a predicati effettivi. In altri termini, bastano le controimmagini di una sigma-algebra che descriva tutti i sottoinsimei di interesse tra gli stati.

Se la sigma algebra dello spazio di partenza è quella delle parti, in automatico generated sigma è un subset della sigma, e quindi ogni funzione è misurabile. Questo è specialmente vero nel caso in cui siamo in un setting discreto, in cui tutte le funzioni sono misurabili. Questo si traduce, nel caso di una var aleatoria su partizione, in una condizione ns di misurabilità: serve che X sia costante su ogni insieme di partizione. Questo estende l'idea di partizione.

Un probabilista non fornisce un Omega, ed X, e poi verifica che è misurabile, che è un approccio da analista.
L'idea è che il probabilista fissa Omega, e la sua sigma algebra, e poi assume per ipotesi che X sia una variabile aleatoria (utilità del lemma di bassetti: sappiamo che esiste X con quella distribuzione!!). Questo approccio, al contrario, è fecondo: infatti, possiamo a questo punto definire una funzione Y come trasformata di X, e per X r.v., Y (se la trasformata è abbastanza regolare, that is è misurabile) è r.v. Questo permette di tradurre l'intero workflow sullo spazio d'arrivo, rather than on lo spazio di partenza.
Fare previsioni su X è equivalente a fare previsioni su Y, e permette di dimenticarsi di lo spazio di probabilità che c'è sotto.
=> il lemma è lo strumento per poter iniziare un esercizio con "sia data X con legge ...", visto che per l'esempio cardinale  almeno 1 such situazione (banale) esiste.

Distribuzione di X == Legge di X == Probabilità di B generata attraverso X.

Per indicare la distribzione di una variabile aleatoria, usiamo la notazione

X \tilde P_X

Nota: dalle info statistiche, possiamo verificare SOLO se la distribuzione P_X è adeguata a descrivere l'esperimento, e non abbiamo info su tutti gli oggeti che la generano (spazio di partenza e X). Quindi lo sforzo modellistico si concentra sulla distribuzione, e l'associazione dallo sp di prob non è unica: quindi, fare i conti con la legge astre dal modello di probabilità, e permette di ottenere risultati validi indipendenti dalla struttura probabilistica sottostante. 

distribuzione == applied
legge == matematico

Poichè P_X uno si ritrova un sacco di roba! Per esempio, che è caratterizzata dalla CDF: la funzione di ripartizione di X. Quest'oggetto determina DA SOLO se la legge di X è discreta, ass continua or what.

L'immagine di una r.v. ha un suo interesse (per esempio fornisce condizioni sufficienti "facili" sul supporto), ma ciò che conta davvero è il supporto, che può essere strettamente più piccolo e ci indica cosa può essere osservato (deciso da prob. e funzione X.).

Perchè il lemma di bassetti solitamente non va bene (i.e. perchè non prendiamo sempre la situazione della legge cardinale per modellizzare la situazione di legge di X data?). La risposta è che qualsiasi altra variabile aleatoria definita sullo spazio della legge cardinale è funzione di omega, e cioè di X. Quindi, Y = h(X) è trasformata di X e ne è *sempre* una funzione deterministica. Quindi questa legge, facile, ci obbliga a cambiare tutto lo spazio per ogni domanda, invece di poterlo riutilizzare defindovi sopra più r.v.

## Variabili Aleatorie 2

### Identità di r.v.

3 tipologie.
1. Funzionale: X=Y. Questo implica che il dominio sia lo stesso, e anche la legge. Corrisponde, modellisticamente, a registrare i risultati di un esperimento, e poi calcolarvi sopra 2 volte la stessa funzione. Lancio due dadi, e mi annoto 2 volte la somma.
2. Di distribuzione: P_X=P_Y. Le due variabili aleatorie possono provenire da spazi diversi, differire per P sullo spazio di probabilità, o per funzione X [Y], e l'unica relazione è che hanno stessa distribuzione. Modellisticamente, lancio 2 dadi, e se X è il primo risultato ed Y il secondo, X ed Y hanno la stessa distribuzione.
3. Quasi certa: Per X, Y sullo stesso spazio di probabilità, esiste un insieme A quasi certo (P(A)=1) nella sigma-algebra tale che lì X=Y. Questa definizione astratta nel caso di E = R diventa che P(X=Y)=1. Questa affermazione è molto meno forte della prima, ma comunque importante. 

Una nota sull'ultimo: fondamentalmente, dice che **ovunque rilevabile** X ed Y sono indistinguibili (that is, a livello modellistico). Quindi, X ed Y possono avere anche legge diversa, a patto che l'insieme su cui lo fanno abbia probabilità 0. Questo è rilevante quando, ad esempio, la probabilità è concentrata solo in una porzione di spazi. Per esempio, l'esponenziale negativa, che ha la prob. concentrata in R+, è tale che se X=Y su R+ e sono del tutto diverse su R- in realtà sono uguali quasi certamente! Un esempio poco interessante, ma sempre curioso, è quello di Q. Poichè l'insieme Q ha probabilità nulla, se X ed Y differiscono solo ivi allora sono q.c. uguali.

L'insieme di r.v. uguali ad X q.c. è indicato con [X]: si tratta di una relazione d'equivalenza. L'utilità di studiare le r.v. in questa maniera è che essendo modellisticamente indistinguibili, vogliamo che le proprietà rilevabili diano lo stesso risultato.

Prop (Relazione tra identità)
X = Y => X = Y qc => P_X = P_Y
Dim: interessante solo l'ultima identità. Si usa il fatto che la traccia della legge sull'insieme A=(X=Y) descrive completamente P_X e P_Y, anche nel caso non discreto.

Il fatto che X=Y qc => P_X = P_Y ha un'implicazione interessante: 
per la definzione, per conoscere la legge di X serve sapere X(\cdot) per ogni \omega\in\Omega, mentre grazie a questa osservazione basta conoscere X su tutti gli elementi di un sottoinsieme di probabilità 1. 
Addirittura, è irrilevante se X esiste o meno: basta che esista su A, e che esista un'estensione consistente e misurabile ad Omega. 

Concretamente, un'applicazione è che per trovare la legge di W = X / Y sarà sufficiente che Y != 0  con probabilità 1 (quindi, se Y è continua va beneeee). Un'altro esempio è quello della r.v. "prima uscita di testa". Potrebbe non uscire mai, ma per noi è irrilevante, visto che Z è (ben) definita per un insieme di prob. 1 (la prob. che escano solo croci è 0). Per aggiustare questo, si può dare una definizione ad hoc per quel caso.

Possiamo estendere l'idea di q.c. agli insiemi (e cioè alle proprietà). Una proprietà per un insieme vale quasi certamente se su un set di probabilità 1 vale. Per esempio, per P=exp(\lambda), X(\omega)=\omega, avremo che X>0 q.c.

## (Integrale rispetto ad una probabilità) 
## Valore Atteso e Varianza
