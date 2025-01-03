# algoritmi-ex1

Questo progetto implementa una libreria generica per l'ordinamento di array in memoria, utilizzando gli algoritmi Merge Sort e Quick Sort. La libreria viene poi utilizzata per ordinare un file CSV contenente 20 milioni di record in base a tre campi (field1, field2, field3). 
Abbiamo usato un file di test con 1 milione di record generati casualmente per misurare i tempi di esecuzione. Ogni record conteneva:
Un id univoco (intero).
Una stringa casuale in field1 (simulata con parole della Divina Commedia).
Un intero casuale in field2.
Un numero in virgola mobile casuale in field3.
MergeSort è stato più prevedibile nei tempi grazie alla sua complessità O(n log n) garantita. Tuttavia, la gestione della memoria (allocazioni per i sub-array) lo ha reso leggermente più lento per dataset di grandi dimensioni.
QuickSort, pur essendo teoricamente più veloce in media, ha mostrato variazioni nei tempi in base al dataset (sensibilità al pivot). Abbiamo però osservato che, con un pivot scelto in modo casuale, il tempo è stato costante.
Campo Ordinato: I tempi di esecuzione variano leggermente in base al campo utilizzato. Questo era prevedibile perché:
Field1 (stringhe) richiede confronti più costosi.
Field2 (interi) è il più veloce da ordinare.
Field3 (floating-point) ha performance intermedie.
