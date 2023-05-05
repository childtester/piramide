# piramide
## esercizio piramide
### Quando si avvia un progetto come la costruzione di una piramide, è meglio pensarci due volte.
Questo programma calcola l'altezza massima di una piramide (in piani) dato un certo numero di cubi di pietra.
Ipotizzando che:

- i piani della piramide siano quadrati
- la piramide da costruire sia compatta, cioè non ci siano cavità al suo interno. 
- ogni piano è quadrato, con una lunghezza laterale inferiore di due rispetto a quella sottostante.
- il primo piano è sempre di un mattone

Esempi:

- il primo piano ha un mattone, il secondo 9 mattoni, il terzo 25 e così via
- con 1 mattone la piramide è alta 1 piano
- con 84 mattoni la piramide è alta 4 piani

Va bene se hai blocchi rimanenti, purché tu costruisca una piramide completa.

## Per il calcolo dei piani:

```
public static int Piani( int mattoni )
       {
            int q = 1;
            int i;
            int risultato = 0;
            if(mattoni<=0){
                return 0;
            }

            for (i = 0; risultato < mattoni;i++){
                risultato=q*q;
                q += 2;
                mattoni -= risultato;
            
            }
            if(mattoni<0){
                return i-1;
            }
            
            return i;
        }
```
## Per il conteggio dei mattoni rimanenti:
```
        public static int Rimanenti( int mattoni )
        {
            int q = 1;
            int i;
            int risultato = 0;
            if(mattoni<=0){
                return 0;
            }

            for (i = 0; risultato < mattoni;i++){
                risultato=q*q;
                q += 2;
                mattoni -= risultato;

            }
            
            return mattoni;
        }
```
## Controllo del numero dei mattoni:
```
            if(mattoni<=0){
                return 0;
            }
