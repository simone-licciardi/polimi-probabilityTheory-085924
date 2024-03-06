### Quali sono le operazioni tra insiemi? Quali sono le loro proprietà di commutazione rispetto all'ordine?

Data una classe di insiemi $\{A_\alpha\}$, gli operatori insiemistici sono:
- $\bigcup A_\alpha$ (Unione)
- $\bigcap A_\alpha$ (Intersezione)
- $A^\mathsf{c}$ (Complementazione)

I primi due operatori rispettano la proprietà commutativa, associativa e distributiva. Proprio quest'ultima restituisce una regola per la gestione di applicazione successiva di unioni e intersezioni.

Per la complementazione, invece, valgono le Leggi di De Morgan: la complementazione commuta con unione e intersezione, a patto di invertire l'altro operatore. Formalmente,
$$
\left(\bigcup A_\alpha\right)^\mathsf{c} = \bigcap A_\alpha^\mathsf{c}, \\
\left(\bigcap A_\alpha\right)^\mathsf{c} = \bigcup A_\alpha^\mathsf{c}.
$$

### Come si dimostra un'inclusione insiemistica?

Per dimostrare un'inclusione insiemistica, diciamo
$$
A \subset B,
$$
si dimostra che se $x \in A$ allora $x \in B$.

### Come si dimostra un'identità insiemistica?

Per dimostrare un'identità insiemistica, diciamo
$$
A = B,
$$
si dimostrano due inclusioni:
1. $A \subset B$,
2. $B \subset A$.

**Operativamente**, nei casi più facili accade che si possa realizzare una catena di equivalenze per cui $x \in A$ se e solo se $x \in B$. In generale, si dimostra separatamente che se $x \in A$ allora $x \in B$ e il vice versa, e uno dei due versi è notevolmente più difficile.

### Come si dimostra la minimalità di un insieme?

Immaginiamo di cercare il minimo insieme che rispetti una certa proprietà. Dimostrare la minimalità insiemistica, vuole dire provare che ogni altro insieme che rispetta quella stessa proprietà contiene in nostro. ù

In altri termini, per dimostrarla serve conoscere (da un claim) il "candidato minimo" $A$, e a quel punto dimostrare che 
$$
A \subset B,
$$
per ogni insieme $B$ che rispetti la proprietà, o operativamente che se $x \in A$ allora $x \in B$.

### Definire i limiti successionali di *sequenze monotone* di insiemi. Conservano le proprietà topologiche dei termini della sequenza?

A fronte di molte maniere in cui si possono, distintamente, definire le sequenze monotone e i limiti, per i nostri fini è sufficiente una nozione più di base, che implicitamente consideri il risulato del limite come noto.

Diremo che la sequenza $\{A_k\}$
converge monotonamente dall'alto ad $A$, e lo indicheremo con $A_k \big\downarrow A$, se
1. $A_{n+1} \subset A_n$
2. $A = \bigcap A_k$

Una definizione analoga può essere data per la convergenza monotona dal basso, $A_k \big\uparrow A$.

Queste convergenze **non** conservano le proprietà topologiche poichè, per esempio, il limite di una sequenza di aperti può essere un chiuso.

### Definire i limiti di insiemi con la *classe limite*

Per definire i limiti insiemistici introduciamo le notazioni di $\lim\inf$ e $\lim \sup$ di sequenze di insiemi. Mentre è ovvio che il limite della sequenza sia ben definito se questi insiemi sono uguali, la definizione di questi insiemi varia.

Possono essere definiti 
- con la **convergenza puntuale** delle **funzioni indicatrice** associate agli elementi della sequenza
- usando le seguenti **definizioni insiemistiche**
$$
\lim\sup A_k = \{\omega \in A_k \text{ i.o.}\} = \bigcap_n\,\bigcup_{k>n} A_k \\
\lim\inf A_k = \{\omega \in A_k \text{ ult.}\} = \bigcup_n\,\bigcap_{k>n} A_k
$$
- usando la nozione di **minimalità** e **massimalità** di un insieme.

