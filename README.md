

## Project Description
Questo progetto usa una rete neurale per imitare la guida di un veicolo nel simulatore di Udacity. E' un problema di regressione supervisionata tra i comandi del veicolo e le immagini dell'ambiente circostante.
Le immagini sono state scattate da tre camere poste a bordo del veicolo (di fronte, a sinistra e a destra).
La rete è basata sul [modello di NVIDIA](https://devblogs.nvidia.com/parallelforall/deep-learning-self-driving-cars/) che ha dimostrato delle buone performance in questo dominio applicativo.

La seguente guida si riferisce al SO Windows 10. Il procedimento potrebbe differire per altri ambienti.

Setup dell'ambiente:

1. Clonare la repository.
2. Scaricare e installare [Anaconda](https://www.anaconda.com/products/distribution).
3. Installare l'ambiente con le dependencies specificate nel file `env.yalm`.
4. Scaricare [Udacity Simulator](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/Term1-Sim/term1-simulator-windows.zip).
5. Creare la cartella `data` nella directory del file `model.py`.

Raccolta del dataset:

1. Avviare l'applicazione `beta_simulator.exe` scaricata al punto 4, scegliere le opzioni grafiche che si preferiscono e premere `Play!`.
2. Scegliere il percorso da cui si vuole ricavare il dataset e premere `Training mode`.
3. Premere il tasto `R`, selezionare la directory `data` creata in precedenza, e premere `select`.
4. Premere il tasto `R` e guidare il veicolo nel percorso con le freccette direzionali (consigliati 3-5 giri).
5. Premere il tasto `R` per catturare il dataset.

Training:
1. Aprire un `Anaconda Prompt` e digitare `activate env`.
2. Andare nella directory in cui è stata clonata la repository ed eseguire il comando `python model.py`. E' possibile aggiungere `-n` seguito da un valore per specificare il numero di epoch (default 30). Per consultare tutti i parametri che si possono modificare, consultare il file `model.py`.

Alla fine dell'apprendimento, nella directory principale sarà possibile trovare una copia del modello per ogni epoch eseguito.

Testing:
1. Avviare l'applicazione `beta_simulator.exe, scegliere le opzioni grafiche che si preferiscono e premere `Play!`.
2. Scegliere il percorso su cui testare il modello e premere `Autonomous mode`.
3. Aprire un `Anaconda Prompt` e digitare `activate env`.
4. Andare nella directory in cui si trova il modello da testare ed eseguire il comando `python drive.py model.h5` sostituendo `model.h5` con il nome del proprio file.

Nella repository sono già presenti due modelli già allenati.
`model-t1.h5` completa il primo percorso ed è stato allenato su 10 epoch.
`model-t2.h5` completa il secondo percorso ed è stato allenaro su 23 epoch.
