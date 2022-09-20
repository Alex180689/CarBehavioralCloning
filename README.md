

## Project Description

In this project, I use a neural network to clone car driving behavior.  It is a supervised regression problem between the car steering angles and the road images in front of a car.  

Those images were taken from three different camera angles (from the center, the left and the right of the car).  

The network is based on [The NVIDIA model](https://devblogs.nvidia.com/parallelforall/deep-learning-self-driving-cars/), which has been proven to work in this problem domain.

Questo progetto usa una rete neurale per imitare la guida di un veicolo nel simulatore di Udacity. E' un problema di regressione supervisionata tra i comandi del veicolo e le immagini dell'ambiente circostante.
Le immagini sono state scattate da tre camere poste a bordo del veicolo (di fronte, a sinistra e a destra).
La rete è basata sul [modello di NVIDIA](https://devblogs.nvidia.com/parallelforall/deep-learning-self-driving-cars/) che ha dimostrato delle buone performance in questo dominio applicativo.

La seguente guida si riferisce al SO Windows 10. Il procedimento potrebbe differire per altri ambienti.

Setup dell'ambiente:

1. Clonare la repository.
2. Scaricare e installare [Anaconda](https://www.anaconda.com/products/distribution).
3. Installare l'ambiente con le dependencies specificate nel file `env.yalm`.
4. Scaricare [Udacity Simulator] (https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/Term1-Sim/term1-simulator-windows.zip).
5. Creare la cartella `data` nella directory del file `model.py`.

Raccolta del dataset:

1. Avviare l'applicazione `beta_simulator.exe` scaricata al punto 4, scegliere le opzioni grafiche che si preferiscono e premere `Play!`.
2. Scegliere il percorso da cui si vuole ricavare il dataset e premere `Training mode`.
3. Premere il tasto `R`, selezionare la directory `data` creata in precedenza, e premere `select`.
4. Premere il tasto `R` e guidare il veicolo nel percorso con le freccette direzionali (consigliati 3-5 giri).
5. Premere il tasto `R` per catturare il dataset.

1. Aprire un 
