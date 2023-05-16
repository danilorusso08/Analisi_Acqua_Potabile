# Analisi_Acqua_Potabile
Progetto finale start2impact

In questo progetto, l'obbiettivo sarà quello di costruire un modello predittivo per determinare la potabilità dell'acqua in base alle sue caratteristiche chimiche.<br><br>
Nell'analisi dei dati, è risultato uno sbilanciamento della classe target, per cui è stato adottato lo *stratified sampling* per mantenere la distribuzione dei dati, e una bassa correlazione tra le features e la classe target.<br>
Sono stati testati diversi modelli di classificazione per l'individuazione del migliore utilizzando $2$ approcci, nel primo caso abbiamo utilizzato tutte le features a disposizione (Modello1), mentre nel secondo caso abbiamo utilizzato le $4$ migliori features individuate tramite il chi quadro test (Modello2), dopo aver ottimizzato gli iperparametri dei modelli tramite *GridSearchCV*, il *GradientBoostingClassifier* che utilizza quattro feature è emerso come il migliore.
