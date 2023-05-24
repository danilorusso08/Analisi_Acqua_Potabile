# Analisi Acqua Potabile

In questo progetto, l'obiettivo è quello di costruire un modello che determini la potabilità dell'acqua in base alle sue caratteristiche chimiche.<br><br>

## Obiettivi
- Analizzare e visualizzare le features del dataset.
- Individuare eventuali correlazioni tra le features e la classe target.
- Creare un modello *Dummy* randomico per stabilire un livello base di prestazioni.
- Creare il milgiore modello di classificazione utilizzando tutte le features a disposizione (Modello1).
- Creare il milgiore modello di classificazione utilizzando le migliori quattro features del dataset (Modello2).

## Analisi
Il dataset è composto da $9$ features più la classe target, nello specifico:
- ph: Indica il ph dell'acqua (0-14).
- Hardness: Capacità dell'acqua di precipitare in sapone mg/L.
- Solids: Solidi totali disciolti in ppm.
- Chloramines: Quantità di Clorammine in ppm.
- Sulfate: Quantità di Solfati disciolti in mg/L.
- Conductivity: Conducibilità elettrica dell'acqua in μS/cm.
- Organic_carbon: Quantità di carbonio organico in ppm.
- Trihalomethanes: Quantità di Trialometani in μg/L.
- Turbidity: Misura delle proprietà di diffusione della luce dell'acqua in NTU.
- Potability: Indica se l'acqua è sicura per il consumo umano.

<p align="center">
<img src="images/Distribuzione2.png" width="1000" height="845"/>
</p>

Nello specifico nella visualizzazione delle distribuzioni è evidente lo sbilanciamento della **classe target**:

<p align="left">
<img src="images/target.png" width="450" height="340"/>
</p>

Questo sbilanciamento della classe target, potrebbe compromettere il modello nel caso in cui si eseguisse un campionamento casuale (random sampling), per ovviare a questo problema viene utilizzato come campionamento lo **startified sampling** che tiene conto della distribuzione delle etichette di classe.


In aggiunta, è possibile notare come il dataset contenga diversi **outliers**, che tramite l'algoritmo di *IsolationForest*, possiamo stimare intorno al $10$% dei dati totali del dataset. 
<p align="left">
<img src="images/outliers.png" width="1000" height="500"/>
</p>

## Correlazioni
Utilizzando la matrice di correlazione possiamo ottenere la relazione tra le variabili del dataset, con valori che possono variare tra $-1$ e $1$, con il valore $0$ che indica assenza di correlazione.
<p align="left">
<img src="images/matrice.png" width="858" height="612"/>
</p>
